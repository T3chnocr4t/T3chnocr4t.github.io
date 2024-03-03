# RootMe
### Difficulty = Easy
***
Hola 👋, Here is my write-up on [RootMe](https://tryhackme.com/room/rrootme) , based on the TryHackMe CTF. It covers learning reconnaissance, privilege escalation, and reverse shell techniques.

![root2qqq](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/40e7c2f9-c0d9-40ad-97f6-716070f68e10)

## Task 1: Deploy the machine
### Connect to TryHackMe network and deploy the machine
- So, I started by connecting to the TryHackMe network and deploying the machine.

***
## Task 2: Reconnaissance
### First, let's get information about the target.

### Q1: how many ports are open?
- So, I began by utilizing one of the best enumeration and scanning tools, which is `Nmap`. Nmap is a powerful network scanning tool used to discover hosts and services on a computer network.

- Running our nmap scan, give us this:

```powershell
# Nmap 7.94SVN scan initiated Sat Mar  2 16:09:04 2024 as: nmap -sC -sV -oN ./myfile.txt 10.10.88.68
Nmap scan report for 10.10.88.68
Host is up (0.20s latency).
Not shown: 998 closed tcp ports (conn-refused)
PORT   STATE SERVICE VERSION
22/tcp open  ssh     OpenSSH 7.6p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   2048 4a:b9:16:08:84:c2:54:48:ba:5c:fd:3f:22:5f:22:14 (RSA)
|   256 a9:a6:86:e8:ec:96:c3:f0:03:cd:16:d5:49:73:d0:82 (ECDSA)
|_  256 22:f6:b5:a6:54:d9:78:7c:26:03:5a:95:f3:f9:df:cd (ED25519)
80/tcp open  http    Apache httpd 2.4.29 ((Ubuntu))
|_http-title: HackIT - Home
| http-cookie-flags: 
|   /: 
|     PHPSESSID: 
|_      httponly flag not set
|_http-server-header: Apache/2.4.29 (Ubuntu)
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sat Mar  2 16:09:42 2024 -- 1 IP address (1 host up) scanned in 37.96 seconds
```




And we can see that we have 2 ports open from our Nmap scan.
- Answer: 2

### Q2: What version of Apache is running?
- From our `nmap` scan port 80 https is running of Apache httpd 2.4.29 ((Ubuntu))

![rootme1](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/9a67c10c-87ea-4108-a45e-58395b94693f)

- Answer: 2.4.29

### Q3: What service is running on port 22?
- Answer: SSH

### Q4: Find directories on the web server using the GoBuster tool.
- Answer: No Answer Needed

### Q5: What is the hidden directory?
- Using Gobuster, a command-line tool utilized for directory and file brute-forcing on web servers, we were able to uncover the hidden directory.

![rootme2](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/d0fb1a8e-c2be-43fc-a790-12d22ab03d1e)

- Answer: /Panel/
  
***
## Task 3: Getting a shell
### Find a form to upload and get a reverse shell, and find the flag.

- We have to Find a form for uploading files to obtain a reverse shell, and then locate the flag. In this scenario, access the IP address via a web browser. The hidden directory named "panel" will lead you to the upload form.

![rootme4](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/d6ed82a8-bbe4-4b18-adb0-f6baabbcceef)

- We can go here to find [PHP reverse shell scripts](https://github.com/pentestmonkey/php-reverse-shell/blob/master/php-reverse-shell.php). What we need to do is create a "shell.php" file that we can upload onto the vulnerable server used to establish a backdoor connection to a compromised server.
- So, we can create a file with nano, for example, "example.php". This will open the nano editor where you can copy-paste the payload from the Git repository. Afterwards, we need to change the "ip_addr" and port to the desired values for our communication. In this case, I use port 4444, but you can use any port convenient for you. Then, use the IP address of your TryHackMe (THM) VPN if you are connected using the VPN. Or using the attackbox.
scroll down you will see something similar.

![tes2](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/14c23347-747a-48c3-ab53-7fabf7b8c1d8)

- After completing the process, it's time to upload it to the /panel/ directory that we discovered earlier. However, what's this? It appears the server isn't accepting .php files. What should we do in this situation? We're aware that we have a .php file, and PHP files can be disguised with various extensions. A brief search on Google reveals alternative extensions such as: .php3, .php4, .php5, .php7, .phtml, .pht. Then, the .php5 extension finally works! Bingo! 😂

![rootme5](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/a5e4cf14-8d94-4c1d-ac14-d47d32c379e2)

- Now, we need to navigate to the uploads page at `ip_addr/uploads`, which was found earlier using Gobuster, to access hidden pages. It will look something like this. Then, we start our netcat listener in the terminal.

![new1](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/6a12837a-b81d-4654-94f5-fc53581a6c80)

- To start our Netcat, we have to open our terminal and enter the command: `nc -lvnp 4444` (replace "4444" with the port number specified in your PHP reverse shell file). In my case, I use port 4443.

![1](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/896acc83-8f9d-4706-8e6b-600776173c1b)

- Now, click on the PHP shell in the /upload/ directory and switch to the Netcat terminal window.

![Inkednew1_LI](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/11386d2c-63cb-4ae6-b171-f1ba7e39c39b)

- move to the terminal BINGO!! 😂 we are in:)

![new2](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/98d3dea5-f382-42da-8fe3-bc185d012c7f)

- ### Back to Q1:User.txt:
- How to find it 🤔? Use the find command. Type `find / -type f -name user.txt 2> /dev/null`.

* find: This command is used to search for files and directories within a specified directory hierarchy.
* /: Specifies the starting point of the search, which is the root directory.
* -type f: Indicates that we are searching for regular files.
* -name user.txt: Specifies the name of the file we are looking for, which is "user.txt".
* 2> /dev/null: Redirects any error messages (specifically stderr, represented by "2") to /dev/null, which essentially discards them.

- Then, we will obtain its path and can view it with the cat command to retrieve the flags.

![new4](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/7232c4cd-1edf-493f-9207-ab13f7dde4b7)

- Answer: THM{y0u_g0t_a_sh3ll}

## Task 4: Privilege escalation
### Now that we have a shell, let's escalate our privileges to root

### Q1: Search for files with SUID permission, which file is weird?
- We need to use the command "find / -user root -perm /4000". What does it mean? It's searching for a special kind of file that has a permission setting allowing it to be run as the root user. We have to carefully check the list of files it finds to see if any of them can be used to gain full control over the system as the root user.

![new5](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/15d307c1-2408-4166-9836-3a293cdd5c86)

- Answer: /usr/bin/python

### Q2: Find a form to escalate your privileges.
-Answer: No Answer Needed

### Q3: root.txt
- How to exploit it? Utilize [GTFOBins](https://gtfobins.github.io/gtfobins/python/#suid) and loook for Python GTFO.
 
![suid](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/3832864a-f121-47d8-ae65-15a718068e39)

- We need to run this `python -c 'import os; os.execl("/bin/sh", "sh", "-p")'`, copy it, and paste it into your terminal to see where we end up.
Then, type the command `whoami`.we are in 😂!
- To find the root.txt run this command in the terminal `find / -type f -name root.txt`

![new6](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/830787c5-ece2-4738-bc76-0d7692034364)

We got the flags.
- Answer: THM{pr1v1l3g3_3sc4l4t10n}

And we are done 👋! That's all, friends. Thank you for reading up to this point. I would like to hear your feedback on anything not clear here. Here is my Twitter account @[T3chnocr4t](https://twitter.com/T3chnocr4t). Feel free to DM me if you have any issues with my write-up. Thanks!


[Go Back Home](https://t3chnocr4t.github.io/)

![tenor](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/f8407250-3751-4845-afc9-b10aefdfa35e)








