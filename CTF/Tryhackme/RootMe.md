# RootMe
# Difficulty = Easy
***
Hola 👋, Here is my write-up on [RootMe](https://tryhackme.com/room/rrootme) , based on the TryHackMe CTF. It covers learning reconnaissance, privilege escalation, and reverse shell techniques.

![root2qqq](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/40e7c2f9-c0d9-40ad-97f6-716070f68e10)

## Task 1: Deploy the machine
- So, I started by connecting to the TryHackMe network and deploying the machine.

## Task 2: Reconnaissance
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

