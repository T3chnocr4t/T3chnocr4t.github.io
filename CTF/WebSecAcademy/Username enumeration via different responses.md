***
# Authentication
### Lab#: Username enumeration via different responses

Hola 👋, welcome back! Here is my write-up on [Username Enumeration via Different Responses](https://portswigger.net/web-security/authentication/password-based/lab-username-enumeration-via-different-responses) on Web Security Academy, where I will go through how I approached it. This lab is vulnerable to username enumeration and password brute-force attacks. It has an account with a predictable username and password.

![password-reset-poisoning](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/3b0e1778-7aeb-47a4-9a3e-5177f6992582)

***
### End Goal :#
- To solve the lab, enumerate a valid username, brute-force this user's password
- Then access their account page.

### Username enumeration
**_Username enumeration is when an attacker is able to observe changes in the website's behavior in order to identify whether a given username is valid._**

***
### Testing for vulnerabilities
We are given a wordlists for the username and password:
[Candidate usernames](https://portswigger.net/web-security/authentication/auth-lab-usernames)
[Candidate passwords](https://portswigger.net/web-security/authentication/auth-lab-passwords)

- Accessing the lab, let's check for the features and functionality of the web app to know what type of vulnerabilities to look for. It is a blog site 😎

![1](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/69ac04d5-8bec-4a6f-9ffe-054cc1d102a9)

- Let's go to the login page and submit an invalid username and password and see if we get an 'invalid username' message.

![2](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/b3fd2771-27fa-4597-b9ad-f7d8c9e112ae)

- In Burp, go to Proxy > HTTP history tab and find the POST /login request. Send it to the Repeater tab so we can see it clearly there.

![3](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/79843416-420f-4713-bc31-7e551b408077)

- Highlight the value of the username parameter in the request and send it to Burp Intruder. Go to Burp Intruder in the Positions tab. We can see that the username parameter is automatically set as a payload position, indicated by two § symbols. And select the attack type to sniper.

![4](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/dcfa48b5-2543-4580-bd30-75f906872ebd)

- After that, go to the Payloads tab and make sure that the Simple list payload type is selected. Under Payload settings, paste the list of candidate usernames. and, click Start attack.

![5](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/1ecd1812-1058-4a27-abd6-3dd7ac1f0f82)

- 
