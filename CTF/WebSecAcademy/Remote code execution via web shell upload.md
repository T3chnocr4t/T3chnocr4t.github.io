***
# Files Upload Vulnerabilities
### Lab:# Remote code execution via web shell upload

Guys 👋, let's go through this really quick. This lab contains a vulnerable image upload function. It doesn't perform any validation on the files users upload before storing them on the server's filesystem.

Our task is to solve the lab by uploading a basic PHP web shell and using it to exfiltrate the contents of the file /home/carlos/secret. Submit this secret using the button provided in the lab banner. Let's get started.

![file-upload-vulnerabilities](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/3f8b05e5-8766-4750-9915-5f9eddd9d5a3)

### End Goals:
- Upload the basic php web shell
- And get the content of the file /home/carlos/secret.

***
### What is File Upload Vulnerabilities 🤔
**_File upload vulnerabilities is when a web sever allow the user to upload files to it filesytem without sufficiently valiating things like their name, type, content and size._**

### Enummeration/ Testing for Vulnerabilities

- First, to test a web app for vulnerabilities, we have to check each functionality of the web app. So, let's log in to our account and check how the web app works.

![1png](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/64d4e598-babd-4cb8-b902-bc3bfdd75a73)

- So, it has a functionality for uploading an avatar image. Let's try uploading our basic PHP web shell and check if the web application validates it.

![2](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/fea27cf2-e7ee-4056-91e1-c31ac89a98bd)

- On your machine, create a file called anyname.php—in my case, I used rick.php—containing a script for fetching the contents of Carlos's secret file. Add this script to the file:
```
<?php echo file_get_contents('/home/carlos/secret'); ?>
```
- Let's try uploading the malicious PHP file to the upload image function. If the web app doesn't validate it, and the script is successful, bingo! 😂

![4](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/399f8b00-0bde-4ad5-9541-bf9065fd309d)

- Let's send the request to the Repeater tab and modify it. In Burp Repeater, change the path of the request to point to your PHP file:
- And get Carlos's key. Submit it to complete the lab.

![5](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/6378c5d6-d287-4639-8e7c-eea0294957b1)

![giphyr,](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/8ca76684-b3b6-41c1-af87-4e440330d37f)

That's all, friends. Thank you for reading up to this point. I would like to hear your feedback on anything not clear here. Here is my Twitter account @[T3chnocr4t](https://twitter.com/T3chnocr4t). Feel free to DM me if you have any issues with my write-up. Thanks!

[Go Back Home](https://t3chnocr4t.github.io/)
