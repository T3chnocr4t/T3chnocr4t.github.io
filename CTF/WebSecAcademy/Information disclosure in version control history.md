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
