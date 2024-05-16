***
## Access Controls
## Lab #4: User ID controlled by request parameter, with unpredictable user IDs

Hola 👋 welcome back. This is the Lab 4# [User ID controlled by request parameter, with unpredictable user IDs](https://portswigger.net/web-security/learning-paths/server-side-vulnerabilities-apprentice/access-control-apprentice/access-control/lab-user-id-controlled-by-request-parameter-with-unpredictable-user-ids#) write-up of the Access Control labs on WebSec Academy. This lab revolves around a horizontal privilege escalation vulnerability. The web app identifies each user with GUIDs for their user account pages. We need to locate the GUID for user Carlos and submit his API key as the solution. Let's get started.

![access-control](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/233707e5-1d04-409f-b413-33766ae43a5b)

***
### End Goal :#
- Find the GUID for carlos, then submit his API key as the solution.

### Horizontal Privilege Escalation:
**_Occurs when a user is able to gain access to resources belonging to another user, instead of their own resourcesof that type._**

***
### Testing for vulnerabilities:

![2024-05-16_18-22](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/973d78cf-2005-4464-8f1f-338f4c00de18)

- The web application is a blog site where each user has posted blogs. Let's check for a blog that the user Carlos has posted. By clicking on Carlos and checking the URL, we can identify the value of the "id" parameter associated with the user Carlos. Let's copy it and save it for later use.

![2024-05-16_18-54](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/22c196c9-7089-4bba-9702-6895cab6d192)

- Next, let's log in to our own account using the following credentials: wiener:peter.
- So when I log in, we can see that I have an ID associated with my account.

![2024-05-16_19-13](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/bd97f90e-0423-4650-a740-2cd6f3d49a2c)

- In the Repeater tab, let's change the value of the Wiener ID to Carlos ID, which we copied earlier in the URLs, and send the request. Now, we're logged in as user Carlos.
 
![2024-05-16_19-20](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/f9b5d888-b136-4595-8100-ac210bdd2823)

-   and we can see his API key. Let's copy it and submit it. With that, we've completed our goal.

![2024-05-16_19-21](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/5cf4b7b7-9267-487e-9cd7-c51842cf8aba)

![2024-05-16_19-22](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/1f9d95b4-c91b-43a5-970e-2000c0c85967)


That's all, friends. Thank you for reading up to this point. I would like to hear your feedback on anything not clear here. Here is my Twitter account @[T3chnocr4t](https://twitter.com/T3chnocr4t). Feel free to DM me if you have any issues with my write-up. Thanks!

[Go Back Home](https://t3chnocr4t.github.io/)









