***
# Infromation Disclosure
## Lab:~# Information disclosure in version control history

Welcome to my write-up for the PortSwigger Web Security Academy lab on [Information disclosure in version control history](https://portswigger.net/web-security/information-disclosure/exploiting/lab-infoleak-in-version-control-history) In this guide, I’ll show you how I tackled the lab, including how I found security issues and created solutions.
This lab discloses sensitive information via its version control history. To solve the lab, obtain the password for the administrator user then log in and delete the user carlos.

<p align="center">
  <img src="https://github.com/user-attachments/assets/87fa52fd-702d-4181-9efc-7356a04e0db6" alt="hacking" />
</p>

<h3 id="what-is-information-disclosure">What is information disclosure?</h3>
<p><strong><em>Information disclosure, also known as information leakage, is when a website unintentionally reveals sensitive information to its users.</em></strong></p>

<h3 id="end-goals">End Goals:~#</h3>
<ul>
  <li>Obtain the password of the admin.</li>
  <li>Login and delete the user carlos.</li>
</ul>

### Steps To Reproduce:~#

![11111](https://github.com/user-attachments/assets/7b9b331d-1f4c-41ea-8869-bd2649405b20)

- Open the lab and browse to /.git to reveal the lab's Git version control data. We need to find a way to download this data to our machine.

![22222](https://github.com/user-attachments/assets/8baae6df-773f-4504-9907-2772e64dcb10)

- Using the `wget` command (a utility for downloading files from the web), we can download all the data to our machine, making it easier to examine everything.

![33333](https://github.com/user-attachments/assets/ccdbc407-8437-4e39-99df-884574a906bd)

- On our Linux machine, when we download files, using `ls -a` shows hidden files and directories (those starting with `a` . like `.git`). We can navigate to these directories using cd and list all files and directories with ls.

![44444](https://github.com/user-attachments/assets/b041069c-5b62-437c-930a-634aaded44bc)

- I started checking all the files manually, hoping to find something useful. some file gave me a clue about where to look next.

![200](https://github.com/user-attachments/assets/03f0f3f5-cfa2-4dbf-bb98-ce0d81c028ad)


- There is a commit with the message "Remove admin password from config"
- Using the git diff command, we can show changes between commits or between a commit and the working tree. By typing git diff and pressing Tab, we can see available options and auto-completions.

![55555](https://github.com/user-attachments/assets/5610437a-13dc-41fa-a95d-81eceab315e8)

- Using git show show the password.

![66666](https://github.com/user-attachments/assets/1da1af2b-abec-436d-92b6-7d88679870d9)

- Bingo! We found the password and used the credentials to log into the admin panel. From there, we accessed all the functionalities and deleted the user "carlo" to complete the lab.

![77777](https://github.com/user-attachments/assets/9c69c93a-d6ee-4305-9f98-465f38c158b0)

![88888](https://github.com/user-attachments/assets/b540430c-ce63-4a74-b696-d7c422795e99)


<p>That’s all, friends. Thank you for reading up to this point. I would like to hear your feedback on anything not clear here. Here is my Twitter account @<a href="https://twitter.com/T3chnocr4t">T3chnocr4t</a>. Feel free to DM me if you have any issues with my write-up. Thanks!</p>

<p><a href="https://t3chnocr4t.github.io/">Go Back Home</a></p>
