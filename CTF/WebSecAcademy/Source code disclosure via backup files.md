***
# Information Disclosure
## Labs:~# Source code disclosure via backup files

Hey, In this lab, the source code is exposed through backup files located in a hidden directory. To complete the lab, you need to find and submit the database password, which is hard-coded within the leaked source code.


<p align="center">
  <img src="https://github.com/user-attachments/assets/cadb11d4-3671-45d4-b443-5f8c721baa7a" alt="hacking" />
</p>

***
### What is information disclosure?
**_Information disclosure, also known as information leakage, is when a website unintentionally reveals sensitive information to its users._**

### End Goals:~#
- Find and submit the database P455W0rd

### Steps To Reproduce:~#

![111](https://github.com/user-attachments/assets/eb9587da-f2fc-4cf2-992b-72952e2e7500)

- Check all the features and functionality of the application. Be sure to enable your proxy to capture and analyze the requests.
- Since we are looking for backup files, I searched through each request and response, but did not find any results.

![222](https://github.com/user-attachments/assets/41fdadfc-08b8-4440-9128-b148214f8e0a)

- While checking the robots.txt(The robots.txt file is used by websites to tell search engines and other web crawlers which parts of the site they should not visit or index. ) file of the web application, I discovered a path for the backup files.

![333](https://github.com/user-attachments/assets/4f204124-7ab0-4982-acd8-d0716e34a061)

- On the backup page, there is a file that we need to examine thoroughly to locate the database password.
- Checking it found the password.

![444](https://github.com/user-attachments/assets/bbaff491-d992-4af9-a581-afab9b97c795)

![555](https://github.com/user-attachments/assets/828afc0a-8bec-4633-bf42-8fa1dd734c11)

- We solve the lab. easy right?

![666](https://github.com/user-attachments/assets/ae0e21d3-d096-4bac-84af-476023e63a19)

That's all, friends. Thank you for reading up to this point. I would like to hear your feedback on anything not clear here. Here is my Twitter account @[T3chnocr4t](https://twitter.com/T3chnocr4t). Feel free to DM me if you have any issues with my write-up. Thanks!

[Go Back Home](https://t3chnocr4t.github.io/)
