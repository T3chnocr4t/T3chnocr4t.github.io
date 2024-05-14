***
# Access control
## Lab #2: Unprotected admin functionality With unpredictable URL

Hola 👋 welcome back. This is the Lab 2# [Unprotected Admin Functionality with Unpredictable URL](https://portswigger.net/web-security/learning-paths/server-side-vulnerabilities-apprentice/access-control-apprentice/access-control/lab-unprotected-admin-functionality-with-unpredictable-url) write-up of the Access Control labs on WebSec Academy. We are given the task to access the admin panel and delete the user Carlos. Let's get started!

![access-control](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/233707e5-1d04-409f-b413-33766ae43a5b)

### End Goal :#
- Locating and accessing the admin panel
- And using it to delete the user carlos.

### Testing For vulnerabilities:

![2024-05-14_16-16](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/7b5fa990-d69b-46e1-b338-45699044b86a)

- Using Burp Suite, send the main page request to the Repeater tab.

- From the lab’s main page, let’s first test for unprotected functionality within the URL and check the "robots.txt" file (a text file placed on a website that instructs web robots which pages or files they can or cannot access). However, we encountered an error: "not found".

- Next, let's check the source code of the main lab's page for any comments or JavaScript that were accidentally left behind during development or production that disclose the admin panel functionality.
- We found the path to the admin panel.

![2024-05-14_14-26](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/a5b36231-d719-4c6d-baba-e4602031498c)

- Navigating to the path gives us a 200 OK response. We accessed the admin pages and, checking the source code, found the URL to delete the user Carlos.

![2024-05-14_14-38](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/6276ba30-d730-47a9-960d-6647da45da47)

![2024-05-14_14-40](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/0f4d8117-21d5-430b-8d22-4c91a77004ec)


