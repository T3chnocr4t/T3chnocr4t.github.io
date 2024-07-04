***
# Access Control
## Lab:~# Referer-based access control

Guys👋 let's go through this lab really quickly. Some websites base access controls on the Referer header submitted in the HTTP request. This lab controls access to certain admin functionality based on the Referer header. Let's solve the lab to exploit the flawed access controls and promote ourselves to become administrators.

![spider-man-spiderverse](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/bff8d90e-768b-47c0-b2c7-027d5156ad32)

***
### End Goals:~#
- Log in using the credentials wiener:peter and exploit the flawed access controls to promote yourself to become an administrator.

***
### Testing For Vulnerabilities:~#
- Let's familiarize ourselves with the admin panel by logging in using the credentials administrator and exploring all the functionalities available to administrators.

![refer 1](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/50248601-66f3-4588-b9ea-26550ab48e42)

- Using the admin panel, let's promote Carlos and send the HTTP request to Burp Repeater, then observe the Referer header.

![refer 2](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/1f35136b-1591-43e3-a047-f1d2a644702c)

- Open a private browser window or another browser, log in with normal user credentials, and copy its session cookie.
- In Burp Repeater, change the session from admin to the normal user, then promote yourself to admin by changing the value of the username parameter.

![refer 3](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/6f6119b5-a8a7-4fb6-9487-0ab120012f8b)

- We received a redirection and successfully solved the lab. Easy, right😂?

![refer 4](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/437e45a3-769d-4d1f-997d-a2509a691ed4)

That's all, friends. Thank you for reading up to this point. I would like to hear your feedback on anything not clear here. Here is my Twitter account @[T3chnocr4t](https://twitter.com/T3chnocr4t). Feel free to DM me if you have any issues with my write-up. Thanks!

[Go Back Home](https://t3chnocr4t.github.io/)
