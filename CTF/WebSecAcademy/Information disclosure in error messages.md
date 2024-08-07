***
# Information disclosure
### Lab:~# Information disclosure in error messages

In today's Web Security Academy lab, we are focusing on information disclosure. This lab highlights how verbose error messages can expose the use of a vulnerable version of a third-party framework. To complete the lab, you need to identify and submit the version number of this framework.

![pexels-markusspiske-113850](https://github.com/user-attachments/assets/9837bfe9-27e3-4eaa-9c42-1373beaf77f9)

***
### What is information disclosure?
**_Information disclosure, also known as information leakage, is when a website unintentionally reveals sensitive information to its users._**

### End Goals:~#
- Identify the version number of the framework.
- submit the version of the framework.

***
### Steps To Reproduce

![1](https://github.com/user-attachments/assets/1d2d9a77-20e0-422c-9fc1-d4f90ce1a9b3)

- The web application in question is an SHOPING site. First, we should test all the features and functionalities of the app. Additionally, open your proxy to begin collecting requests.
- When viewing each product, the web application assigns a unique numeric ID to each item.

![2](https://github.com/user-attachments/assets/79ca3dbc-6094-4fc0-ab16-72298cd4e2ba)

![3](https://github.com/user-attachments/assets/7ec4f1b0-274f-4f00-9878-b7eaf51c3c5f)

- Let's try changing the numeric ID to a number that doesn’t exist to see if it causes any errors. This will help us understand how the web app handles invalid IDs.
- I changed the value of the ID parameter to 1111, but the response status code returned a 404 Not Found error.

![4](https://github.com/user-attachments/assets/7b5ad5bd-8652-4122-8355-f277889ac585)

- Changing the value of ID parameter to `'` caused an error to be displayed. This error message, which the server should not disclose, revealed information about the framework version being used.

![5](https://github.com/user-attachments/assets/45fb837a-ccb0-493b-b274-c7c756d3d23a)

- This reveals that the lab is using Apache Struts 2 2.3.31.

![5](https://github.com/user-attachments/assets/2d795b52-c65e-49b3-9e5f-12d762ae670a)

- By submitting this information, we successfully completed the lab. That’s pretty cool!

![6](https://github.com/user-attachments/assets/858757d8-c4b3-4dba-8d13-df58cc274054)


That's all, friends. Thank you for reading up to this point. I would like to hear your feedback on anything not clear here. Here is my Twitter account @[T3chnocr4t](https://twitter.com/T3chnocr4t). Feel free to DM me if you have any issues with my write-up. Thanks!

[Go Back Home](https://t3chnocr4t.github.io/)



