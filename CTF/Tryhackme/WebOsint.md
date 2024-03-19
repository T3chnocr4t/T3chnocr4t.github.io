***
# WebOsint
## Difficulty = Easy
***

Hola👋 Welcome back. Here is a walkthrough on [WebOsint](https://tryhackme.com/room/webosint) based on TryHackMe. It covers learning how to conduct basic open source intelligence research on a website.

![web](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/9af6f2d8-f7a2-47db-aa4b-3a201b3870bf)

## What is WebOsint all about 🤔 ?
**_WebOSINT stands for "Web Open Source Intelligence." It refers to the practice of gathering intelligence or information from publicly available online sources. This can include social media platforms, websites, forums, blogs, public databases, and any other online resources where information is openly accessible._**

***

## Task 1: When A Website Does Not Exist 
The first thing we do when we are given the name of a website/business to check out is fire up the ol' web browser, find the website, and check it out, right?
#### What if the website, or even the entire business, no longer exists?
That does NOT mean it's the end of the road. So let's begin.
This OSINT challenge starts off by focusing on a domain called ``RepublicofKoffee.com``.
It should be noted that when this challenge was created, the website related to that domain did not exist. Our job is to find as much information as you can about the website RepublicofKoffee.com. Let's get started and look for information that we can find from the website.

### Q1: Click To Complete
Answer: No Answer Needed
***

## Task 2: Whois Registration
Just because nothing shows up when you visit 'RepublicOfKoffee.com,' doesn't mean that someone doesn't own the domain. We can confirm the current registration status with a WHOIS lookup.
A 'WHOIS' lookup is the most basic form of domain reconnaissance available. There are multiple websites that will do it for you as well.

### Q1: What is the name of the company the domain was registered with?
- First, let's look up the domain name using the [WHOIS website](https://www.whois.com/). The WHOIS tool is used to retrieve information about domain names, including registration details, the domain owner's contact information, registration and expiration dates, name server information, and more.

![osint3](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/4411e053-4a05-4e51-9bdb-20ff22e623c6)

- Answer: Namecheap Inc

### Q2: What phone number is listed for the registration company? (do not include country code or special characters/spaces)
- We can gather a lot of information about the website by using OSINT tools

![osint 5](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/8977f544-1e5c-4515-a193-8d334b887ac9)

### Q3: What is the first nameserver listed for the site?

![osint 6](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/b43e7d7f-1c05-4f52-a7fb-cd1d62926783)

### Q4: What is listed for the name of the registrant?

![osint 7](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/c5a658db-8c45-43f7-8d85-acc579e33342)

### Q5: What country is listed for the registrant?
- We got the name of the country, which is 'IS,' but that is a short code for a country. By using this [website](https://www.iban.com/country-codes), we can determine that the country is Iceland or by conducting research on the city Reykjavik, which is the capital of Iceland.

![osint 8](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/7c62876b-4faf-4609-9128-f7e5cca0c21c)

- Answer: Iceland

## Task 3: Ghosts of Websites Past 
Don't be discouraged if your initial searches on a website yield no results. That's where Archive.org and the Internet Wayback Machine come into play.

#### What is Internet Wayback Machine 🚙 ?
The Wayback Machine, is an online digital archive maintained by the Internet Archive. It stores snapshots of web pages taken at various points in time, allowing users to access historical versions of websites. This archive enables users to view how websites looked and what content they contained at different points in the past. It serves as a valuable resource for research, historical preservation, and accessing information that may have been removed or changed on the live web.













