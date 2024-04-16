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
It should be noted that when this challenge was created, the website related to that domain did not exist. Our job is to find as much information as you can about the website `RepublicofKoffee.com`. Let's get started and look for information that we can find from the website.

### Q1: Click To Complete
- Answer: No Answer Needed

***
## Task 2: Whois Registration
Just because nothing shows up when you visit `RepublicOfKoffee.com`, doesn't mean that someone doesn't own the domain. We can confirm the current registration status with a WHOIS lookup.
A 'WHOIS' lookup is the most basic form of domain reconnaissance available. There are multiple websites that will do it for you as well.

### Q1: What is the name of the company the domain was registered with?
- First, let's look up the domain name using the [WHOIS website](https://www.whois.com/).

**_The WHOIS tool is used to retrieve information about domain names, including registration details, the domain owner's contact information, registration and expiration dates, name server information, and more._**

![osint3](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/4411e053-4a05-4e51-9bdb-20ff22e623c6)

- Answer: Namecheap Inc

### Q2: What phone number is listed for the registration company? (do not include country code or special characters/spaces)
- We can gather a lot of information about the website by using the tools

![osint 5](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/8977f544-1e5c-4515-a193-8d334b887ac9)

- Answer: 9854014545

### Q3: What is the first nameserver listed for the site?

![osint 6](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/b43e7d7f-1c05-4f52-a7fb-cd1d62926783)

- Answer: ns1.brainydns.com

### Q4: What is listed for the name of the registrant?

![osint 7](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/c5a658db-8c45-43f7-8d85-acc579e33342)

- Answer: redacted for privacy

### Q5: What country is listed for the registrant?
- We got the name of the country, which is 'IS,' but that is a short code for a country. By using this [website](https://www.iban.com/country-codes), we can determine that the country is Iceland or by conducting research on the city Reykjavik, which is the capital of Iceland.

![osint 8](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/7c62876b-4faf-4609-9128-f7e5cca0c21c)

- Answer: Iceland

***
## Task 3: Ghosts of Websites Past 
Don't be discouraged if your initial searches on a website yield no results. That's where [Archive.org](https://archive.org/web/) and the Internet Wayback Machine come into play.

#### What is Internet Wayback Machine 🚙 ?

**_The Wayback Machine, is an online digital archive maintained by the Internet Archive. It stores snapshots of web pages taken at various points in time, allowing users to access historical versions of websites. This archive enables users to view how websites looked and what content they contained at different points in the past. It serves as a valuable resource for research, historical preservation, and accessing information that may have been removed or changed on the live web._**

- Looking at the historical information available for the site, you should be able to answer the following questions:

### Q1: What is the first name of the blog's author?
- I entered the domain name into the Wayback Machine and found the website. It was a blogging site. I opened one of the blogs and discovered the name of the author.

![osint 10](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/1db0e75b-c657-4628-9a00-d6951ba6c637)

![osint 12](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/4061514c-5dbb-440f-b3c6-a748c2015c79)

![osint 13](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/1320df23-8374-4642-9ec4-7eece3d654ba)

- Answer: Steve

### Q2: What city and country was the author writing from?
- By reading each and every blog, one consistent detail was the mention of the city name "Gwangju." Upon conducting research, it was found to be located in South Korea.

![osint 15](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/35467ea3-65c8-4a4b-b0ad-e762ad8d0baa)

- Answer: Gwangju, South Korea

### Q3: [Research] What is the name (in English) of the temple inside the National Park the author frequently visits?
- I got one blog where the author mentioned finding himself having a meeting in `Mudeungsan National Park` in Gwangju. By conducting research, I found the English name.

![osint 16](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/59b0e295-aef3-45dd-aebe-0bee2ac5c9cd)

- Answer: Jeungsimsa Temple

***
## Task 4: Digging into DNS 
So far we've gathered some good info about the content that was on our target website, even though it hasn't been live for several years.
But what about technical details? That's where [ViewDNS.info](https://viewdns.info) comes in. 

**_ViewDNS.info is a website offering tools and services related to DNS and domain information. It allows users to look up domain details, perform reverse IP lookups, check DNS propagation status, generate DNS reports, and conduct domain research. It's a valuable resource for gathering domain-related information and troubleshooting DNS issues._**
- Take a look at the search options available and we can answer the question below:

### Q1: What was RepublicOfKoffee.com's IP address as of October 2016?
- Use the IP History tool, which shows the historical IP addresses associated with a domain.

![osint 18](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/9aa39f9c-7f15-4a72-b08b-8595e0e58f78)

- Answer: 173.248.188.152

### Q2: Based on the other domains hosted on the same IP address, what kind of hosting service can we safely assume our target uses?

![osint 19](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/26ff94ba-f4c6-421a-a37a-48b0850bc84c)

- There are 82 domains hosted on the server.
- But we get that. By checking the hint question: What kind of hosting plan is usually used by websites on a tight budget that don't have a lot of visitors? The answer is  `shared` because Shared hosting is a type of web hosting service where multiple websites are hosted on a single physical server. Click [Here](https://www.quicksprout.com/types-of-web-hosting/) to learn more.

- Answer: Shared

***
## Task 5: Taking Off The Training Wheels 
- We are given a domain `heat.net` to use all the skills we have learned so far to answer the question 😂

### Q1: What is the second nameserver listed for the domain? 
- Using the WHOIS tool, we found the second name server.

![update](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/2a9f9231-eab7-4680-8e58-232b57ddf91c)

- Answer: NS2.HEAT.NET

### Q2: What IP address was the domain listed on as of December 2011?
- Hmm... that will be IP history, right? By using the ViewDNS.info tools

![update 1](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/e4fdbb66-1239-484e-94f9-d04ca8d90d11)

- Answer: 72.52.192.240

### Q3: Based on domains that share the same IP, what kind of hosting service is the domain owner using?
- Using the current IP, I utilized the Reverse IP Lookup tool and found that this was also likely SHARED.

- Answer: Shared

### Q4: On what date did was the site first captured by the internet archive? (MM/DD/YY format)
- Using the Wayback Machine, we can see that the domain was captured over 834 times between June 1, 1997, and March 15, 2024

![osint 22](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/1d15a773-de16-4d84-af2f-bc0719838e10)

- Answer: 06/01/97

### Q5: What is the first sentence of the first body paragraph from the final capture of 2001?
- July 6, 2001, is the last capture for 2001. Checking the snapshot, we have:

![osint 23 up](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/792e7e8d-64c8-421e-86ee-90e78fd8e766)

![osint 23](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/76696ec3-41d1-4cd9-96db-9d5c73d583d0)

- Answer: After years of great online gaming, it’s time to say good-bye.

### Q6: Using your search engine skills, what was the name of the company that was responsible for the original version of the site? 

![osint 24](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/87ce549e-a4ba-487f-a9d9-dfb01421dbb9)

- Answer: SegaSoft

### Q7: What does the first header on the site on the last capture of 2010 say?
- The last capture was on December 31, 2010.

![osint 25](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/1a8aded6-671f-44df-94e6-afa406f0da8a)

- Answer: Heat.net – Heating and Cooling

***
## Task 6: Taking A Peek Under The Hood Of A Website 
Often, clues about a website and its creator/owner may be unintentionally left behind in the source code of the website. Pretty much every web browser will have a method of doing this. By viewing the page source of a website, we could get more information about it.
These following questions refer to `heat.net/36/need-to-hire-a-commercial-heating-contractor/`

### Q1: How many internal links are in the text of the article?
- This task is quite simple. Just go through the text and count the links. You can tell if they're internal by hovering over them and seeing where they lead. If they take you to another page on heat.net, they're internal links.

- Answer: 5

### Q2: How many external links are in the text of the article?
- Answer: 1

### Q3: Website in the article's only external link ( that isn't an ad)
- the external link lead us to purchase.org

![osint 26](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/384f01a2-f485-4a8e-8382-78813283aa2d)

### Q4: Try to find the Google Analytics code linked to the site
- For this question, right-click anywhere on the page and select "View Page Source."
- Use Ctrl+F to search for 'UA-'.

![osint 27](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/54495452-4eff-4b94-b2bd-be590763f301)

- Answer: UA-251372-24

### Q5: Is the the Google Analytics code in use on another website? Yay or nay
- You can use [nerdydata](https://www.nerdydata.com/) to search for the Google Adsense ID.
- Here we can see that only one website is using it:

![one](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/a5b066da-3dc6-4b75-a1e6-deee274ffc7e)

- Answer: nay

### Q6: Does the link to this website have any obvious affiliate codes embedded with it? Yay or Nay
- No I searched for href and there was no any affiliate links
- Answer: nay

***
## Task 7: Final Exam: Connect the Dots 
### Q1:  Use the tools in Task 4 to confirm the link between the two sites. Try hard to figure it out without the hint.
- I used viewdns.info to compare the results of both the domains heat.net and purchase.org. One common finding was that the owner of both companies was Liquid Web, L.L.C.

![Annotation 2024-03-20 235530](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/d3ab4994-355c-4088-89a8-47e9cbfcd74f)

![2](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/0e59468a-cc14-4e28-acb1-ec51d3db77ff)

- Answer: Liquid Web, L.L.C

***
## Task 8: Debriefing 
- Answer: No Answer Needed

***
## Task 9: Wrap-up 
- Answer: No Answer Needed

And we are done 👋! That's all, friends. Thank you for reading up to this point. I would like to hear your feedback on anything not clear here. Here is my Twitter account @[T3chnocr4t](https://twitter.com/T3chnocr4t). Feel free to DM me if you have any issues with my write-up. Thanks!


[Go Back Home](https://t3chnocr4t.github.io/)




























