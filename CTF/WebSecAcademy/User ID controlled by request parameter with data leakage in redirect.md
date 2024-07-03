***
# Access Control
## Lab:~# User ID controlled by request parameter with data leakage in redirect 

Guys 👋 welcome back! Here is another write-up on a web security academy lab. This lab contains an access control vulnerability where sensitive information is leaked in the body of a redirect response. Let's get started and exploit it.

![access-control](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/233707e5-1d04-409f-b413-33766ae43a5b)

***
### End Goals :~#
- Solve the lab, obtain the API key for the user carlos and submit it as the solution.
- You can log in to your own account using the following credentials: wiener:peter

*** 
### Testing For Vulnerabilities: 
- In some cases, an application detects when the user is not permitted to access the resource and returns a redirect to the login page.

![111](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/e1b8fd21-34de-4bfc-8f83-3cde1834b948)

- Log in using the supplied credentials to access your account page, and then let's send the request to reapter.
- Modify the value of the 'id' parameter to 'carlos' and send it. Carefully observe the response: it now redirects you to the homepage, but the body contains the API key belonging to Carlos.

![222](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/e30fdae7-3df6-42e3-a185-ea9767b46566)

- Copy the API key and submit. We solve the lab easily, right 😂

![333](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/ef1418b2-f6e0-443f-b57e-522be72196f2)

![444](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/32e6cc9e-1149-4521-bfc2-383e42964617)




That's all, friends. Thank you for reading up to this point. I would like to hear your feedback on anything not clear here. Here is my Twitter account @[T3chnocr4t](https://twitter.com/T3chnocr4t). Feel free to DM me if you have any issues with my write-up. Thanks!

[Go Back Home](https://t3chnocr4t.github.io/)
