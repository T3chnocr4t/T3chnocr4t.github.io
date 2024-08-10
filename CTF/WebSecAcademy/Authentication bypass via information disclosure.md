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

![1111](https://github.com/user-attachments/assets/670536df-bc76-4fea-9cb4-2e9db0678b4e)

- Logging in with the credentials provided
- Checking the proxy for collected requests. While checking the requests, we noticed that accessing the account details was done using a GET request.
- Changing the request to TRACE, which is used for diagnostic purposes. In the response, we saw a header called X-Custom-IP-Authorization that contain our ip address.

![2222](https://github.com/user-attachments/assets/b9fda507-50a9-4813-a2a7-c1339f9afe62)

- Looking what the header mean on google.

![3333](https://github.com/user-attachments/assets/8b892297-4ac0-4fc3-82bf-b7f4e5493c69)

- Knowing what the header means, we changed our request method and path to GET /admin, added the X-Custom-IP-Authorization header with our IP address as the value. We received a 401 status code in response.

![4444](https://github.com/user-attachments/assets/e681a7ca-a81d-410c-a333-41cbef50f86c)

- This means we need to change the value of the header so that the request appears to come from the localhost IP address.

![5555](https://github.com/user-attachments/assets/0391b492-5781-4500-9cb3-8693863c7e80)

- Bingo! We accessed the admin page, and by checking the response, we found the path to delete the user "carlos.

![6666](https://github.com/user-attachments/assets/1ecb5f80-5362-43de-864c-4c070088fa05)

- That’s it, hackerman—lab solved!

![7777](https://github.com/user-attachments/assets/ee98f778-bcec-4d20-a089-4793fa8ded45)


<p>That’s all, friends. Thank you for reading up to this point. I would like to hear your feedback on anything not clear here. Here is my Twitter account @<a href="https://twitter.com/T3chnocr4t">T3chnocr4t</a>. Feel free to DM me if you have any issues with my write-up. Thanks!</p>

<p><a href="https://t3chnocr4t.github.io/">Go Back Home</a></p>
