***
# Authentication
## Username enumeration via subtly different responses
***

Yo, people!😎 It's been a while. Here is another lab solution based on PortSwigger Labs. This lab is subtly vulnerable to username enumeration and password brute-force attacks. It has an account with a predictable username and password, which can be found in the following wordlists. Our task is to find the valid credentials and log in. Let's go, guys!


    Candidate usernames
    Candidate passwords


<p align="center">
  <img src="https://github.com/user-attachments/assets/e5afe668-554f-49f1-93ff-b80660446e56" alt="hacking" />
</p>

*** 
### Authentication
*Authentication vulnerability is a weakness in a system that allows attackers to bypass or break the process used to verify users' identities.*

### End Goals:
- Login valid credentials.

***
### Steps To Reproduce:

![1](https://github.com/user-attachments/assets/46e049da-8937-48e8-bad6-39ccec7cdb81)

- Check all the features and functionality of the application. Be sure to enable your proxy to capture and analyze the and then go to the login functionality pages.
- Enter any username and password you want, then send the request to the Intruder tab and modify some settings.
- In the Payloads make sure that the Simple list payload type is selected and the list of candidate usernames, then in the Settings side panel.Under Grep - Extract, click Add. in the response that appearwe show scroll down we will see `Invalid username or password.` Use the mouse to highlight the text content of the message. then click ok to start the attacks.

![2](https://github.com/user-attachments/assets/4c1d23c3-45a2-46b5-9717-025031b21f32)

![3](https://github.com/user-attachments/assets/b9a27553-c996-46af-99e8-013e116e9c2e)

- In the results, we can see one response that doesn't have a period in the error message. This indicates it's valid. Let’s notice the username.

![6](https://github.com/user-attachments/assets/d3377680-0090-4ca5-ab77-2e7ce9f319c7)

- We have a valid username, so now let's enumerate the passwords to get the full credentials.
- paste the list of passowrd in the payload configuration and start the attacks.

![7](https://github.com/user-attachments/assets/9a8d2eb7-6741-49c3-8eb3-2af22aa25a48)

- Only one response has a different code, 302, which means we have a valid password.

![8](https://github.com/user-attachments/assets/d73e7c6f-f808-4938-8b6c-15256c8f3a49)

- Logging in we sloved the labs.

![9](https://github.com/user-attachments/assets/15493951-211a-4986-9c1a-76acf50d15c9)

That's all, friends. Thank you for reading up to this point. I would like to hear your feedback on anything not clear here. Here is my Twitter account @[T3chnocr4t](https://twitter.com/T3chnocr4t). Feel free to DM me if you have any issues with my write-up. Thanks!

[Go Back Home](https://t3chnocr4t.github.io/)
