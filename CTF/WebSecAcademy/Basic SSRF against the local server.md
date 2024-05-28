***
# SSRF
### Lab#: Basic SSRF against the local server

Guys 👋, let’s go through this really quick. This is an SSRF lab on PortSwigger Academy. This lab has a stock check feature that fetches data from an internal system. The task is to solve the lab by changing the stock check URL to access the admin interface at http://localhost/admin and delete the user Carlos. Let’s get started.

![server-side request forgery](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/533c6a2f-d600-44a3-87dc-e67322f803b6)

### End Goal:
- Access the admin panel and delete the user carlos.

### What is SSRF🤔
**_Server-side request forgery is a web security vulnerability that allows an attacker to cause the server-side application to make requests to an unintended location._**

***
### Testing for vulnerabilties
- Let's check the functionality of the web app.

![1](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/717f813d-b02a-4dce-a6ee-097692c6c597)

- There are many products listed in the web app. Let’s visit a product and click "Check Stock." In Burp, let’s check each request we make. Check the Proxy tab, and we can see our request. Let’s send it to the Repeater tab.

![3](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/ba8ec11c-bec8-4436-8448-4d2fadd01c3a)

- Let’s modify the value of the stockApi parameter to `http://localhost/admin or http://127.0.0.1/admin`. This will display the admin interface.

![4](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/75c2f2ac-1190-47c4-91d4-39fcb5a20b0a)

- Modifying the request gets us to the admin interface. Reading the HTML, we can see the URL to delete the target user, which is: `http://127.0.0.1/admin/delete?username=carlos`. Let’s submit this URL as the value in the stockApi parameter, and we solve the lab.

![5](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/94f0a460-0694-4519-a5e8-999977fb7e74)

![6](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/13186ee7-c383-4284-9a86-907db9014c06)

That's all, friends. Thank you for reading up to this point. I would like to hear your feedback on anything not clear here. Here is my Twitter account @[T3chnocr4t](https://twitter.com/T3chnocr4t). Feel free to DM me if you have any issues with my write-up. Thanks!

[Go Back Home](https://t3chnocr4t.github.io/)
