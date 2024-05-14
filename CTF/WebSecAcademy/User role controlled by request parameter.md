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

![2024-05-12_03-45](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/1b610a6e-9633-45ce-9bd5-70cf298c5c29)

- Using Burp Suite, send the main page request to the Repeater tab to test for unprotected functionality to access the administrative functions. Browsing to the relevant admin URL, in this case, specifying `/admin` as the path, results in a 401 error, indicating "unauthorized."

![2](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/87971693-c6e7-4a7b-8621-4f1bde58dfbb)

- Let's log in to our own account using the following credentials: wiener:peter. We'll use the proxy tab and turn on the intercept to modify a request. Let's see 👀.

![2024-05-15_00-05](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/556ef814-caf8-4aa4-a975-0ad33c90811b)












