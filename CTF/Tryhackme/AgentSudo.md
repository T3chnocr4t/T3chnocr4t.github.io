# Agent Sudo
### Diffcuity: Easy

***
"Welcome back 👋! Here is my write-up on Agent Sudo, based on the TryHackMe CTF. In this challenge, we discovered a secret server hidden deep beneath the sea. Our task was to breach its defenses and uncover the truth within. Throughout the room, we learn into topics such as hash cracking, privilege escalation, and steganography, among others. Let's dive in 🕺.

![agentsudo](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/246974dc-6b89-4f2e-890c-3b778796d6ec)

***
## Task 1: Author note
### Deploy the machine

*** 
## Task 2: Enumerate
Enumerate the machine to gather all important information. Enumeration is the process of gathering information about a target system or network.

### Q1: How many open ports?
-  So, I began by utilizing one of the best enumeration and scanning tools, which is `Nmap`. Nmap is a powerful network scanning tool used to discover hosts and services on a computer network.
- Running our nmap scan, give us this:

```powershell
# Nmap 7.94SVN scan initiated Tue Apr 16 23:17:19 2024 as: nmap -sV -A -oN ./nmap_result.txt 10.10.58.229
Nmap scan report for 10.10.58.229
Host is up (0.20s latency).
Not shown: 997 closed tcp ports (conn-refused)
PORT   STATE SERVICE VERSION
21/tcp open  ftp     vsftpd 3.0.3
22/tcp open  ssh     OpenSSH 7.6p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey:
|   2048 ef:1f:5d:04:d4:77:95:06:60:72:ec:f0:58:f2:cc:07 (RSA)
|   256 5e:02:d1:9a:c4:e7:43:06:62:c1:9e:25:84:8a:e7:ea (ECDSA)
|_  256 2d:00:5c:b9:fd:a8:c8:d8:80:e3:92:4f:8b:4f:18:e2 (ED25519)
80/tcp open  http    Apache httpd 2.4.29 ((Ubuntu))
|_http-title: Annoucement
|_http-server-header: Apache/2.4.29 (Ubuntu)
Service Info: OSs: Unix, Linux; CPE: cpe:/o:linux:linux_kernel

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Tue Apr 16 23:17:59 2024 -- 1 IP address (1 host up) scanned in 39.93 seconds
```


- And we can see that we have 3 ports open from our Nmap scan.
- Answer: 3

### Q2: How you redirect yourself to a secret page?
- From the Nmap scan, we found port 80 open. checking the website, we observed...

![1](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/db42b883-0eb4-497f-9a13-bc543a0672df)

- At first, I didn't understand the message's intent. After reading it carefully, It was saying that we should a code name as the user-agent, i.e from the HTTP request header [ User-Agent in the HTTP request header identifies the client making the request, typically a web browser or other software application, to the server. ]

- Answer: user-agent

### Q3: What is the agent name?
- To access the site. So, I decided to use "R" first because of "Agent R"." 😂
- There are many ways to do this, either by using the User-Agent switcher extension from the web browser or by using a proxy to intercept the request and change the user agent. In this case, I used a Burp proxy.
- Using Burp:

![4](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/bc6aba5d-bc73-4e0f-b56b-6068db932640)

- Forwarding the request, display this in the browser

![3](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/bd43b7d1-5c34-418f-bb3a-fa95179738ca)

- Hmmm, there are 25 employees and another agent. So maybe we should change the user agent from A to Z. or, there was a hint from the question suggesting that we should use "C".

![6](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/6311939d-f1b4-474a-bfea-9dd709da8a46)

- Forwarding the request, display this in the browser

![5](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/5e423807-f16a-43c4-85be-1fb4abe4910c)

- Answer: chris

***
## Task 2: Hash cracking and brute-force
Time to brute way out.
### Q1: FTP password
- By using Hydra to get the FTP password, now that we know the username is Chris.

```
sudo hydra -L username.txt -P /usr/share/wordlists/rockyou.txt 10.10.58.229 ftp
```

![8](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/0595662d-c1a7-4209-8c1b-9c2421039859)

- Answer: crystal

### Q2: Zip file password
- I successfully login into ftp and found 3 file
- I use the get command to download all files to my local machine.

![9](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/2b62a1dd-a8c3-4116-a2cd-1191a103b299)

ls

![10](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/b5b74c37-0ee1-4301-a36c-6ff41ea647a3)

- Now we can read the txt file

![11](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/33bc65da-da66-400c-aff7-655268be7fa8)

- It points us to both a fake and a real picture. The fake picture conceals the login password for Agent J.

![2024-04-18_10-04](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/f6c0f837-1d17-4928-89f5-498e28efa9d4)

- There are many tools used to reveal information hidden in photos, so I chose to use binwalk.
- binwalk (Is used for analyzing and extracting data embedded in files, particularly firmware images and other binary files.)

![13](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/4c5382cc-5f42-452f-a1af-508c2eb3af43)

- So, in the case of cuite.png, binwalk extracted the information from there.
- We can use the zip2john tool to extract password hashes from encrypted ZIP files, making it suitable for John, a password-cracking tool
- `john hashes `

![15](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/e4a02d96-770f-4349-9f3c-f5b23685264a)

- Answer: alien

### Q3: steg password
-  `stegseek cute-alien.jpg /usr/share/wordlists/rockyou.txt`
-  For the second picture, there are many tools available, but I chose to use stegseek(is a tool used for steganography analysis, specifically for detecting hidden data within image files.)

![16](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/7c9ab25d-c795-46f3-adb3-f7b16ba0c645)

- Answer: Area51

### Q4: Who is the other agent (in full name)?
- Answer: james

### Q5: SSH password
- Answer: hackerrules

***
## Task 4: Capture the user flag
You know the drill.
### Q1: What is the user flag?
- log into james account using ssh

![17](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/79f3161a-1fbf-4187-878c-ad2c79d58f92)

- Answer: b03d975e8c92a7c04146cfa7a5a313c7

### Q2: What is the incident of the photo called?
- Exit the SSH session and copy the JPG file from the SSH service to your system using the following command:

![18](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/dad299c6-f097-48aa-abbf-372a2265fb5e)

- When performing a reverse image search( is a technique used to find information related to an image by using the image itself as the search query.), I prefer using Bing. From the results, most websites typically display three key points.

![Alien_autospy](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/687d6ea7-c6da-4a55-839b-34a53a0f8009)

![19](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/e415695f-0beb-4ff9-82e9-f4d2ddf806da)

- Answer: Roswell alien autopsy

## Task 5: Privilege escalation
Time to get real.
### Q1: CVE number for the escalation 
- Log back into the SSH account and use `sudo -l` to list user's privileges or check a specific command; use twice for longer format

![20](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/e6c23fb7-9144-4606-b1a3-7776c57b4f62)

- Searching it on [Expliot.db](https://www.exploit-db.com/)

![21](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/de28933f-63e3-48b1-a91e-be21b46204ee)

- Answer: CVE -2019-14287

### Q2: What is the root flag?
- using the expliot:

![22](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/fb0b79b9-84c1-413b-b804-1bb76bc8d0e8)

- Gain root access by executing the above command. Then navigate to the root directory and locate the root.txt file.

![final](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/660a6054-da2f-462e-b1ff-154c78de5093)

b53a02f55b57d4439e3341834d70c062

### Q3: (Bonus) Who is Agent R?
DesKel

And we are done 👋! That's all, friends. Thank you for reading up to this point. I would like to hear your feedback on anything not clear here. Here is my Twitter account @[T3chnocr4t](https://twitter.com/T3chnocr4t). Feel free to DM me if you have any issues with my write-up. Thanks!


[Go Back Home](https://t3chnocr4t.github.io/)



































