***
# Information disclosure
## Lab:~# Information disclosure on debug page

***
Hello,

Here is the write-up for another information disclosure lab. Let's go through this quickly. This lab features a debug page that reveals sensitive information about the application. To complete the lab, you need to obtain and submit the SECRET_KEY environment variable.


<p align="center">
  <img src="https://github.com/user-attachments/assets/ef47b718-93cb-45be-885d-a627791e001e" alt="hacking" />
</p>


***
### What is information disclosure?
**_Information disclosure, also known as information leakage, is when a website unintentionally reveals sensitive information to its users._**

### End Goals:~#
- Complete the Labs
- You need to obtain and submit the SECRET_KEY environment variable.

### Steps To Reproduce:~#

![11](https://github.com/user-attachments/assets/ba6cb112-d529-4c81-8d21-8804e5a9585c)

- The web application is a shopping site. Start by exploring all its features, as there might not be any obvious issues at first. Then, check the source code for any comments left by the developers.

- It looks like the developer accidentally left a debug page accessible. This is a serious security mistake because the debug page might contain sensitive information that could be exploited

![22](https://github.com/user-attachments/assets/7b3e22a2-b835-4e12-b600-019031b4f1e6)

- Navigate to the page to investigate further.

![33](https://github.com/user-attachments/assets/72d32fcd-fc94-4202-9239-4fa14cfe9e94)

- To locate the SECRET_KEY, we need to search the debug page for the keyword secret. By examining the contents related to this term, we can find the SECRET_KEY value needed to complete the challenge.

![44](https://github.com/user-attachments/assets/d9e18562-ae45-4258-8b12-8a79cae7cdf0)

![66](https://github.com/user-attachments/assets/6f225b8e-883a-44a0-9385-b53fba4b9709)


- Submitting the Key complete solve Lab

![55](https://github.com/user-attachments/assets/12cb04c6-ddd9-46a6-90cb-c0176a86e2a6)


That's all, friends. Thank you for reading up to this point. I would like to hear your feedback on anything not clear here. Here is my Twitter account @[T3chnocr4t](https://twitter.com/T3chnocr4t). Feel free to DM me if you have any issues with my write-up. Thanks!

[Go Back Home](https://t3chnocr4t.github.io/)
