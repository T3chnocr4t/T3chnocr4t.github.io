### ohSINT Tryhackme
Hola 👋here is my [ohSINT](https://tryhackme.com/room/ohsint) walkthrough on tryhackme which is real fun.

![oshint](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/7dbfcd89-8b93-49c4-b8c0-8c99eb54d9e9)

### What is OSINT 🤔?
OSINT, or Open Source Intelligence, is like being a detective on the internet. It involves gathering information from publicly available sources like social media, websites, news articles, and online databases to learn about people, organizations, or events.


So, lets begin. I started by downloading the given task, which was a window XP wallpaper 😆.
![WindowsXP](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/1dd44043-9fd9-456b-96e8-0d30a1270daf)

### Q1: What is this user's avatar of?

- So i started by checking what type of file it is.

![first](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/2bb12690-ea8d-4a0f-9e06-cd725943c08d)

- It did'nt give me much detailed, so i use ``Exiftool`` which is a command-line tool used for reading, writing, and editing metadata in various file types, including images, videos, audio files, and documents.
So i obtained a lot of details about the pictures, and we can see a copyright which is ``owoodfrint``."

![second2](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/603d072e-22d6-4565-a494-e12bb80e1fd3)

- "So I searched(recon) the name on Google, and I found a GitHub account and Twitter account..

![owood](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/ea741b68-59e9-43d2-beea-150da8f1a853)

- So I looked into the Twitter account and saw the answer to the first question: What is this user's avatar of

![profle (2)](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/ec090391-ee11-4d87-aa2b-9aec907d3822)
- Answer= Cat

### Q2: What city is this person in?
- "So I took a look at the GitHub account and found the location."

![owood github location](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/12f87ad2-ca14-4bb8-b2ad-9dccf752e880)
- Answer: London

### Q3: What is the SSID of the WAP he connected to?
- So I looked up its Twitter account and found the BSSID.
- Next, I used a website called `WiGLE`, which collects information about different wireless hotspots around the world.
- Then I used it to get the SSID name when I knew the BSSID. by zooming in alot 😟

![locat](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/20ecc84a-ec72-42d6-a3c7-715d8943d021)
Answer: UnileverWiFi

### Q4: What is his personal email address?
- Take a look at the Github account anfd found the email. 🕺

![owood github mail](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/6b581c29-0ba4-4b2f-8400-03379a86711f)

### Q5: What site did you find his email address on?
Answer: Github

### Q6: Where has he gone on holiday?
- yes 😆 "So I found its website on GitHub and took a look at it. Then I saw.. He went to new york to enjoy 😂

![owood web](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/fadd8f6a-cc1f-4517-ae63-a8551cf5aaf9)
Answer: New york

### Q7: What is the person's password?

- So I carefully viewed the page source of the website and found the victim's password.
![page syy](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/c37e9c7b-be7d-49b7-9685-74cf39e08e81)

