***
# Access Control
## Lab:~# Insecure direct object references
***

Hello 😃, welcome back to another lab write-up. This [lab](https://portswigger.net/web-security/access-control/lab-insecure-direct-object-references) focuses on learning about IDOR (Insecure Direct Object Reference). The lab stores user chat logs directly on the server's file system and retrieves them using static URLs. Let's explore vulnerabilities and exploit them.

![prevent-IDOR-vulnerabilities](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/915ee66e-43d1-447c-9d06-097f19f04ddb)

***
### End Goals:~#
- Solve the lab by finding the password for the user carlos, and logging into their account.

### What is IDORs:~#
Insecure direct object references (IDORs) are a subcategory of access control vulnerabilities. IDORs occur if an application uses user-supplied input to access objects directly and an attacker can modify the input to obtain unauthorized access.

***
### Testing For Vulnerabilities:~#
- Let's log in to our account and check the live chat feature to send messages.

![idor1](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/a86f3e20-a183-4b1b-805f-580f90b2eb75)

- View the transcript and download our message. Notice the URL and observe that the transcripts are text files assigned a filename with a 'number'.

![idor 2](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/0cea37bc-41ed-4b04-8aec-5fb73c0796c4)

![idor 3](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/16780ef3-7586-4851-a908-f70c1f025a5d)

- The hacker 💻 inside us says we should test for IDOR. Let's change the number to 1 and we succeeded;(200 OK) now we can see Carlos's messages and password.

![idor 4](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/2208057e-103e-482e-8c95-d90ddcb88a2b)

- Login using the credentials to solve the lab.

![idor 5](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/b04f7f06-5086-4491-a7a3-b22630486fe2)

![giphy66](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/b4cb0aef-e2ed-4e78-92fb-022341501d95)


That's all, friends. Thank you for reading up to this point. I would like to hear your feedback on anything not clear here. Here is my Twitter account @[T3chnocr4t](https://twitter.com/T3chnocr4t). Feel free to DM me if you have any issues with my write-up. Thanks!

[Go Back Home](https://t3chnocr4t.github.io/)



