***
# Path Traversal

Hola 👋 welcome back, guys! Here is my write-up on all the labs in Path Traversal on Web Sec Academy, curated in one place. I will go through how I solved each lab. Let's get started!

![directory-traversal](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/a11e326d-42e3-4cb3-b0c9-fd95511c1327)

### What is Path Traversal 🤔
**_Path traversal is also known as directory traversal. These vulnerabilities enable an attacker to read arbitrary files on the server that is running an application. This might include: Application code and data, Credentials for back-end systems, Sensitive operating system files._**

***
### Lab #1: 
- End Goal: This lab contains a path traversal vulnerability in the display of product images. To solve the lab, retrieve the contents of the /etc/passwd file.

![1](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/db83e70c-b13a-45fd-890d-4180de2d5d49)

- In Burp, check for any image product request and send it to the Repeater tab.

![3](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/1c08cb4b-9ab5-47a0-8ea0-5f35429a0609)

- This application implements no defenses against path traversal attacks. By modifying the request, we can retrieve the /etc/passwd file from the server's filesystem by stepping up one level in the directory structure. The three consecutive ../ sequences step up from /var/www/images/ to the filesystem root, and so the file that is actually read is /etc/passwd. We receive a 200 OK status code, indicating that the request was successful. We've successfully solved the first lab. Nice! Let's move on to the next one.

![4](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/433b1a0a-cd7b-4765-8ee4-c706f653dc66)

![5](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/9e21fe07-a760-4d1b-a08b-6bae7686741f)

***
### Lab #2: 













