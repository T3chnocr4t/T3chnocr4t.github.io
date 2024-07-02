***
# Access Control
## Lab #: User ID controlled by request parameter

Guys 👋, welcome back. Let's go through this lab real quick. This lab has a horizontal privilege escalation vulnerability on a user account page. Let's try to exploit the vulnerabilities.

To solve the lab, we need to obtain the API key for the user Carlos and submit it as the solution. Note: Am using caido you can follow along using burp also..

![access-control](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/233707e5-1d04-409f-b413-33766ae43a5b)

***
### End Goals:
- Obtain the API key for the user carlos
- You can log in to your own account using the following credentials: wiener:peter

***
### What Horizontal privilege escalation 🤔?
Horizontal privilege escalation occurs if a user is able to gain access to resources belonging to another user, instead of their own resources of that type. 

***
### Testing for vulnerabilities~:

![1](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/3c7a6207-54cd-4b86-a571-564fc5fef0e4)

- Let's log in to our account using the following credentials and test all features in the application. Turn on our proxy to collect requests. See how the web app handles requests, processes our requests, and identifies users.
- When log in, let's check our proxy. We can see that the web app identifies the user in the URL. The value of the id parameter contain our username.. Nice😂

![2](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/580ca22d-54bc-44b1-84ac-619768ee19ab)

- The hacker inside us. we should send the request to repeater/replay and modify the value of the 'id' parameter to 'carlos'.
- We got in (200 ok) and we can see user carlos API key

![3](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/5dce46f3-6b5c-48e5-8936-2305fc3dc459)

- Retrieve and submit the API key for carlos. we solve the lab easy right..

![4](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/3fb33e19-ea7e-4f5d-bb10-f80e770607fb)

![5](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/ae93ac63-0136-44bb-9de8-3c87e6d54e18)


That's all, friends. Thank you for reading up to this point. I would like to hear your feedback on anything not clear here. Here is my Twitter account @[T3chnocr4t](https://twitter.com/T3chnocr4t). Feel free to DM me if you have any issues with my write-up. Thanks!

[Go Back Home](https://t3chnocr4t.github.io/)
