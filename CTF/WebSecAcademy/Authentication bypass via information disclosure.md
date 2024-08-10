***
# Informaton Disclosure
## Lab:~#Authentication bypass via information disclosure

Welcome to my write-up for the PortSwigger Web Security Academy lab on [Authentication bypass via information disclosure](https://portswigger.net/web-security/information-disclosure/exploiting/lab-infoleak-authentication-bypass)! In this guide, I'll show you how I tackled the lab, including how I found security issues and created solutions.

This lab's administration interface has an authentication bypass vulnerability, but it is impractical to exploit without knowledge of a custom HTTP header used by the front-end.
To solve the lab, obtain the header name then use it to bypass the lab's authentication. Access the admin interface and delete the user carlos.

<p align="center">
  <img src="https://github.com/user-attachments/assets/9c928138-5ddb-41a1-b12c-24b51591f16a" alt="hacking" />
</p>

***
### What is information disclosure?
**_Information disclosure, also known as information leakage, is when a website unintentionally reveals sensitive information to its users._**

### End Goals:~#
- Obtain the header name then use it to bypass the lab's authenticatio.
- Access the admin interface and delete the user carlos.

***
### Steps To Reproduce:~#
