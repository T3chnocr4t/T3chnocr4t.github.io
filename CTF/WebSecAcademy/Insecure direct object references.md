***
# Access Control
## Lab:~# Insecure direct object references
***

Hello, welcome back to another lab write-up. This [lab](https://portswigger.net/web-security/access-control/lab-insecure-direct-object-references) focuses on learning about IDOR (Insecure Direct Object Reference). The lab stores user chat logs directly on the server's file system and retrieves them using static URLs. Let's explore vulnerabilities and exploit them.

![prevent-IDOR-vulnerabilities](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/915ee66e-43d1-447c-9d06-097f19f04ddb)

***
### End Goals:~#
- Solve the lab by finding the password for the user carlos, and logging into their account.

### What is IDORs:~#
Insecure direct object references (IDORs) are a subcategory of access control vulnerabilities. IDORs occur if an application uses user-supplied input to access objects directly and an attacker can modify the input to obtain unauthorized access.

***
### Testing For Vulnerabilities:~#

