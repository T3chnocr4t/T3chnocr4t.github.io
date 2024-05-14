***
# Access Control
## Lab #3: User Role Controlled By Request Parameter

Hola 👋 welcome back. This is the Lab 3# [User Role Controlled By Request Parameter](https://portswigger.net/web-security/learning-paths/server-side-vulnerabilities-apprentice/access-control-apprentice/access-control/lab-user-role-controlled-by-request-parameter) write-up of the Access Control labs on WebSec Academy. In this lab, we are access the admin panel and delete the user Carlos. Let's get started, friends!

![access-control](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/233707e5-1d04-409f-b413-33766ae43a5b)

***
### End Goal :#
- Locating and accessing the admin panel via forgeable cookies.
- And using it to delete the user carlos.

***
### Testing For Vulnerabilities: 

![2024-05-14_20-46](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/e9c41aa4-c6e0-48c1-9c75-6f1f79674f34)

- Using Burp Suite, send the main page request to the Repeater tab to test for unprotected functionality to access the administrative functions. Browsing to the relevant admin URL, in this case, specifying `/admin` as the path, results in a 401 error, indicating "unauthorized."

![2](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/87971693-c6e7-4a7b-8621-4f1bde58dfbb)

- Let's log in to our own account using the following credentials: wiener:peter. We'll use the proxy tab and turn on the intercept to modify a request. Let's see 👀.

![2024-05-15_00-05](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/556ef814-caf8-4aa4-a975-0ad33c90811b)

- We can see that we are using the POST method (sending data to the server). We can send the request to the Repeater tab and modify it more effectively there.
- Modify the request by changing the path to "/admin" and setting the cookie header value of "admin" to true. And use the cookie to acces the admin panel. Sending this request should take us to the admin panel. Bingo 😂

![33](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/7ac84be3-5336-4a30-88c6-d943af71c779)

- Checking the response source, we can identify the path to delete the user "Carlos." Upon following the redirection, we can proceed to delete the user "Carlos" and successfully complete the labs.

![7](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/525e2ff8-de99-4a24-9432-ebd26e909a3e)

[9](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/a6c16c12-3bda-471c-ac00-20a91b7cad5e)

And we complete our goal by accessing the admin panel and deleting the user "Carlos".

That's all, friends. Thank you for reading up to this point. I would like to hear your feedback on anything not clear here. Here is my Twitter account @[T3chnocr4t](https://twitter.com/T3chnocr4t). Feel free to DM me if you have any issues with my write-up. Thanks!

[Go Back Home](https://t3chnocr4t.github.io/)

























