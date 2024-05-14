***
# Access Control
Hola 👋, welcome back. Here, I will be creating a write-up on [access control](https://portswigger.net/web-security/learning-paths/server-side-vulnerabilities-apprentice/access-control-apprentice/access-control/what-is-access-control) based on WebSec Academy, where I will go through how I solved the labs. Let's get started!

![access-control](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/233707e5-1d04-409f-b413-33766ae43a5b)

**_Access Control: refers to the mechanisms and policies put in place to regulate and manage access to resources within the application. This includes controlling which users can access certain pages, features, or data, and what actions they can perform once they are granted access.
In the context of web applications, access control is dependent on authentication and session management._**

***
### Lab #1: Unprotected admin functionality
This [lab](https://portswigger.net/web-security/learning-paths/server-side-vulnerabilities-apprentice/access-control-apprentice/access-control/lab-unprotected-admin-functionality) has an unprotected admin panel. Our task is to solve the lab by deleting the user "Carlos."
Accessing the lab....

![2024-05-12_03-45](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/7d962a8d-dcfd-497a-aede-23f600203f45)

- Using a proxy, I use Burp and send all the requests to the Repeater tab, specifying 'admin' in the web directory path, but couldn't find anything in the response header. I received a 404 (not found) error.

![2024-05-12_02-19](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/f236dfcf-729c-4dd5-964d-858a1fbec0c6)

- Accessing the "robots.txt"(s a text file placed on a website that instructs web robots which pages or files they can or cannot access.) file, I found the path to the admin pages.

![2024-05-12_02-20](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/b04143d7-a5b0-497c-afbd-284090f8c823)

- Navigating to the path `administrator-panel` gets us to the admin pages. By checking the response source code, we can see the URL to delete the user "Carlos".

![2024-05-12_02-22](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/445e396f-4752-4385-b339-5854c57dc96a)

![2024-05-12_02-23](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/bab2cd7a-f5e7-4af4-ac51-ad03243ef898)

- Specifying the path in the request to delete the user "Carlos," and we are done.

![2024-05-12_02-25](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/23865f25-024c-4f5b-a064-2467084c6a20)

![2024-05-12_02-26_1](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/4eea8002-81fc-43c0-9fb6-54554ab501f7)

That's all, friends. Thank you for reading up to this point. I would like to hear your feedback on anything not clear here. Here is my Twitter account @[T3chnocr4t](https://twitter.com/T3chnocr4t). Feel free to DM me if you have any issues with my write-up. Thanks!

[Go Back Home](https://t3chnocr4t.github.io/)










