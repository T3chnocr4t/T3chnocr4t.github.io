***
# Authentication
### Lab#: 2FA simple bypass
***

Welcome 👋 back , friends! Here is my write-up on [2FA simple bypass](https://portswigger.net/web-security/learning-paths/server-side-vulnerabilities-apprentice/authentication-apprentice/authentication/multi-factor/lab-2fa-simple-bypass) based on Web Security Academy labs. The web app has a two-factor authentication functionality that can be bypassed. We have already obtained a valid username and password but do not have access to the user's 2FA verification code. Our task is to bypass the verification code for the 2FA. Let's get started, guys.

![giphyr,](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/04ba9281-a073-4bda-a980-020573be9162)

### End Goal #:
- Solve the lab and Access carlos account page.

***
### Testing for vulnerabilities
- Let's check the functionality of the web app. The app is a blog site.

![2fa1](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/6a25461a-0e83-486f-ad5c-ec9f21a0c5a3)

- We are given an account; let's log in to our account. We are sent a 2FA verification code to our email. Let's check our email to get the code.

![2fa3](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/d210e7eb-e944-4442-aee3-4e543da15341)

![2fa2](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/a098854f-2990-47a0-9827-892f7f4f95c0)

- By checking Burp, we can see that our username is the value of the ID parameter when we log in. Let's log out and log in as the user Carlos to access his account without his verification code.

![2fa5](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/8f251da6-d38b-440e-8b1b-e439cee89e12)

- Using the credentials for user Carlos, let's log in. Since we cannot access his email, let's send the request to the Repeater tab, modify the request, and navigate to `/my-account?id=carlos`. The lab is solved when the page loads.
- Or, after we log in, go back to the main web page and click the login functionality again, and it will automatically log in as the user Carlos.

![2fa6](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/19b17e60-a3cd-48c4-ba1b-f7592968c556)

That's all, friends. Thank you for reading up to this point. I would like to hear your feedback on anything not clear here. Here is my Twitter account @[T3chnocr4t](https://twitter.com/T3chnocr4t). Feel free to DM me if you have any issues with my write-up. Thanks!

[Go Back Home](https://t3chnocr4t.github.io/)





