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





