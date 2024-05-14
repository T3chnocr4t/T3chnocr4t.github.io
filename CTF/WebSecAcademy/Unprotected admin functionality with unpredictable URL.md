***
# Access control
## Lab #2: Unprotected admin functionality With unpredictable URL

Hola 👋 welcome back. This is the Lab 2# [Unprotected Admin Functionality with Unpredictable URL](https://portswigger.net/web-security/learning-paths/server-side-vulnerabilities-apprentice/access-control-apprentice/access-control/lab-unprotected-admin-functionality-with-unpredictable-url) write-up of the Access Control labs on WebSec Academy. We are given the task to access the admin panel and delete the user Carlos. Let's get started!

![access-control](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/233707e5-1d04-409f-b413-33766ae43a5b)

### End Goal :#
- Locating and accessing the admin panel
- And using it to delete the user carlos.

### Accessing the lab:

![2024-05-14_16-16](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/7b5fa990-d69b-46e1-b338-45699044b86a)

- From the lab’s main page, let’s first test for unprotected functionality within the URL and check the "robots.txt" file (a text file placed on a website that instructs web robots which pages or files they can or cannot access). However, we encountered an error: "not found".

- 
