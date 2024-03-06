***
# Searchlight IMINT
## Difficulty = Easy

***
Hola👋 Welcome back. Here is a walkthrough on [Searchlight IMINT](https://tryhackme.com/room/searchlightosint) based on TryHackMe. It covers learning the discipline of IMINT/GEOINT, which stands for Image Intelligence and Geospatial Intelligence.

![1](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/08f2137b-2295-4439-82b2-8efd00166638)

## What is IMINT and GEOINT 🤔 ?
- Image Intelligence (IMINT): Involves utilizing publicly available images, photographs, and visual media from open sources to gather intelligence.

- Geospatial Intelligence (GEOINT): Involves leveraging publicly available geospatial data, maps, satellite imagery, and other spatial information from open sources to gather intelligence.

Let get started 😆

***
## Task 1: Welcome to the Searchlight IMINT room! 
### This room introduce us to several topics within IMINT, among them: 
- Getting into the right mindset and how to be analytical 
- Visually extracting key data points from an image or video
- Applying different tools to assist you in geolocation and answering context questions

The flag format is: sl{flag} - this means that every answer needs to be submitted within the brackets, sl{your answer}. No capitalization is needed.

### Q1: Did you understand the flag format?
- Answer: sl{ready}

***
## Task 2: Your first challenge

![3](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/e1e15bcf-87ec-46e5-b425-bfc3789ad031)

Before we begin answering questions, I would like to bring up some important words mentioned in the room so we can have a better understanding of what we are doing.

### Let's introduce you to your first tool - your eyes! 
Before we can apply a tool or a methodology for finding the location of an image, we should use our eyes to scan the image for important information. Extracting key data points from the image will allow you to apply the right tool, craft a good Google search or identify which part of the world the image might have been taken in. 
### There are 5 elements of IMINT that you should consider when looking at an image, according to Geoint expert Benjamin Strick:
- Context
- Foreground
- Background
- Map markings
- Trial and error

A geolocation challenge like this lacks one important factor, which is the context or the source of the image. In real-world cases, you usually have a context in which the image was produced or shared, usually called context clues. Most of these challenges will not have context clues but you may find clues in the titles and descriptions, or if you're stuck you can use the hint function. 


### Here are some questions you should ask yourself while looking at the upcoming challenges:
- Are there any obvious data in the image that reveals the location, like a street name or storefront signs?
- Can you determine the country or region of the image by, for instance, which side of the road they drive on, language or architectural characteristics that may reveal a country or continent/region?  
- Do you recognize road sign styles, nature and environmental characteristics, or popular motor vehicle brands or vehicle types? 
- What is the quality of any visible infrastructure like? Is the road paved or do you see gravel roads? 
- Do you see any unique landmarks, buildings, bridges, statues or mountains that can help you geolocate the image?


Download the attached image and let begin

![task2](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/af6530e2-5b87-431c-a619-4186037c5828)

### Q1: What is the name of the street where this image was taken?
- Using our first tool, which is our eyes, we can see a welcome message on a billboard in the city: `Welcome to Carnaby Street.`
- Answer: sl{Carnaby Street}

***
## Task 3: Just Google it!

![2](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/8a3ede22-7c83-4bc4-8baa-b7487b3ee524)

We are introduced to our first tool, Google! If you see anything in the image that can be extracted into a keyword, phrase, a company name, telephone number, or any other question you may have as a result of scanning the image up and down: GOOGLE IT!

Let's start by downloading the given Task.

![task3](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/71e4bda2-868a-4c6a-a0b0-b58a3a95d9ec)

### Q1: Which city is the tube station located in?
- By looking at the image carefully, we can identify the building; most of us know this is London 😂.
- But let's research the image to confirm if we are correct. By carefully looking at the image, we can see three words: `public subway, circus, and "underground.` Let's research it on Google.
- I then used Google maps at street level to make sure I had the exact same one:

![map](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/a3677233-8547-4c58-a962-2205a85e4757)

![map 2](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/36fd3096-8f05-4430-8606-67579b0c6ef4)

- I take a lok back in our search result then we can see many results about London
 
![1111111111111111111](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/dbf001b4-0422-46e3-9cfd-28d95e655709)

- Answer: sl{London}

### Q2: Which tube station do these stairs lead to?
- Taking a look at the Wikipedia page, we found our answer, which is `Piccadilly Circus`.

![55](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/543ff34e-dfbf-4708-b722-b888945ebd82)

- Answer: sl{Piccadilly Circus}

### Q3: Which year did this station open?

![55s](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/101930e0-e4bd-4d21-85d2-44e655f3b811)

- Answer: sl{1906}

### Q4: How many platforms are there in this station?
- Answer: sl{4}

***
## Task 4: Keep At It!
- Downloads the given tasks
  
![task4](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/f603f7cc-e1e4-4122-91da-eb2121626d85)

### Q1: Which building is this photo taken in?
- By carefully looking at the image, we found `YVR Connect.` Let's make research about it and then we found...

![99](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/ac3d29ac-18a0-4288-85b5-0d2b7742db90)

- Answer: sl{vancouver international airport}

### Q2: Which country is this building located in?
- Answer: sl{canada}

### Q3: Which city is this building located in?
- Looking at the Wikipedia page.
- Answer: sl{richmond}

***
## Task 5: Coffee and a light lunch
- Download the given task

![task5](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/a39934a2-859c-4da1-a4a1-012b9c5cd276)

### Q1: Which city is this coffee shop located in?
- We are given a hint: Scotland
- By carefully looking at the image, we found "Edinburgh Woollen Mill." Let's also look it up on Google and found...

![14](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/bfaf51ba-4803-4703-84be-8e0cdcea9f19)

- looking it on google maps

![13](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/cb0ee937-484c-42f4-a25c-d3aeda524a58)

![123](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/e3e5d658-a5e8-4e5e-bb5a-621e6b2046de)

- Bingo 😂 we found the coffee shop

![142](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/5d4e3cdd-960c-4cd4-b98d-f4c7269d80b5)

- Answer: sl{blairgowrie}

### Q2: Which street is this coffee shop located in?
- So after I found the name of the coffee shop, I conducted research on it and was able to obtain the address and street.

![food 1](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/e7c2e6ac-ce8d-40bd-a1b8-c3f6b793783a)

- Answer: sl{allan street}

### Q3: What is their phone number?
- You can see the phone number in the above graphic
- Answer: sl{+447878 839128}

### Q4: What is their email address?
- By clicking on the site, we can find more information about them, and we can see that they have a website.

![Inkedfood_LI](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/b6e4b742-3ba2-4fdf-8239-5ac846792744)

- So the website led me to the official Facebook page, and there I found their email.

![food 4](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/4c994e82-0e5b-4a9e-9e9f-52570c9e61b3)

- Answer: sl{theweecoffeeshop@aol.com}

### Q5: What is the surname of the owners?
- By examining another website, I managed to discover the owner. Or researching who the owner is will definitely provide the answer.

![owner](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/99612af6-91f2-4d4a-8e3a-23df42964af4)

- Answer: sl{cochrane}

***
## Task 6:  Reverse your thinking

![0gFwCSO](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/69be921b-e074-4e92-b2d6-fe840c665a12)

- Reserve Thinking: This means that we are searching for the image itself online, and if the image has been indexed by search engines we may find the exact image or we can do a visual search or crop search to help us find similar images.
- "You can Perform a search by image. Choose between the image search engines Google, Bing, Yandex, TinEye and Baidu."
- Download the given task we have:

![task6](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/9ce38726-e706-4e91-90a8-cfdce714e5bc)

### Q1: Which restaurant was this picture taken at?
- By using Google Image Search, we found many items, and we also discovered the logo of the restaurant.

![tes](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/907678f9-6095-488c-95e8-c4d4cd07f711)

- I made a research on the name and was able to find many things, and I also took a look at the Wikipedia page. And i found the all about the company

![tes 3](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/61e79c6e-67dd-46d8-b0fa-80a295f6bcaa)

- Answer: sl{katz's deli}

### Q2: What is the name of the Bon Appétit editor that worked 24 hours at this restaurant?
- Researching, I found the answer.

![tes 4](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/0d37cc1c-343a-43af-a1fb-6abc5042e637)

- Answer: sl{andrew knowlton}

***
## Task 7: Locate this sculpture
![vDAqWCZ](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/b8b9b3ca-074d-457a-9c0b-0347dc674569)

Now that we have hand on practice of different tool and techniques , let use that knowledge to crack the below challenge questions by using the image provided:

![task7](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/f2f72b49-3adc-4120-a31f-b03315ecde25)

### Q1: What is the name of this statue?
- By using Google Image Search or other tools, I found a lot of sites about the sculpture.

![Inkedtek 7_LI](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/4843b078-4738-48ee-a17e-2d2890e8a318)

- Checking on that website only provided me with the location of the sculpture, but I didn't know its name.

![111](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/e61816d2-e68f-450b-8dfd-0558ddca999c)

- So what I did next is that I conducted an OSINT search on the motorcycle sculpture in Tjuvholmen, Oslo, and I found a site that provided me with the name. BINGO 😂

![222223](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/8bad7a11-ab77-485d-a088-45af2a9b4c59)

![222](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/f4d797fc-51d3-40b4-9756-ecf96ad38489)

- Answer: sl{rudolph the chrome nosed reindeer}

### Q2: Who took this image?
- Then, after I found the name of the sculpture, I conducted research on it as well. I found a site that provided me with the name of the individual who took the image.

![333](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/86bebaa6-5144-4d05-89f8-4b234ca4664c)

![444](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/8535e1cb-1392-473a-a969-bbb387faacde)

- Answer: sl{kjersti stensrud}

***
## Task 8:  ...and justice for all
- Continuing our reverse image search, let's try to figure out the answers to the challenge questions using the provided image.
  
![task8](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/3f835ed2-9f1e-4e07-88c5-cb9264309115)

### Q1: What is the name of the character that the statue depicts?
- By using Bing image search, I quickly obtained the name of the statue.

![Inked111_LI](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/d7c058ec-25d6-4f14-a3da-865563aaad39)

- Answer: sl{lady justice}

### Q2: where is this statue located?
- Using Bing image search, I needed to identify the name of the building. I continued cropping the image until I found the full name.

![222](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/a1d031ca-ae19-410b-b1d0-83aa9d5e6d30)

![333](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/4d06e09c-2d64-441d-8492-c1ceffc7144f)

- Then BINGO 😂 i found it

![4444](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/0b259daf-67c2-4b12-b1df-21ce04ee5c5b)

- Making a research on the name to locate it on Google Maps, then I found it location

![ttttt](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/c79eff04-21a1-41dd-ab69-619fe6e029f7)

- Answer: sl{alexandria, virginia}

### Q3: What is the name of the building opposite from this statue?
- Viewing around i found the opposite building 😆

![777](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/8b9a7ca6-d50d-4ea1-af3a-0f66a85f775c)

- Answer: sl{the westin alexandria old town}

***
## Task 9: The view from my hotel room

![vQJdwUh (1)](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/5ab64e16-f311-4387-ac9e-a19a1d19741f)

- Geolocating videos aren't much different from geolocating images. A video is just a string of images, usually played at 24 frames(or images) per second. In other words, a video will hold a whole lot more images that can be analyzed, reversed and scrutinized by you.
### Q1: What is the name of the hotel that my friend stayed in a few years ago? 
- I took a look at the downloaded video and found many interesting buildings.

1)
![1](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/51cfd20f-ed65-4a3f-a71b-7643e6369c2e)

2)
![2](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/d0affad4-d6f3-4398-8f9e-cea7da293a05)

3)
![vid 1](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/55e6bf02-d8ee-4025-acac-e20f5af4cdbb)

- 
Making research on the Riverside Point building using Google Image Search, I quickly found it is located in Singapore from the search results.

![vid 6](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/0db63eab-51bf-4415-af27-a06c251126e6)

- By using Google Maps to verify if I am correct.

![vid 10](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/02a5b916-d336-4e0f-a349-5de09650fe5c)

![vid 9](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/24c8d02f-f903-4b1f-8adb-9807d3bd8999)

- By viewing and examining the street map, I found the hotel where the video was taken. As you can recall from the videos, you can see the pool and the roads.
- It is amusing that Google Maps didn't show the name of the building. I had to conduct research on it again, and then I found the name.

![VID 12](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/691687ac-0555-4fca-94b8-48c544590a75)

- Answer: sl{novotel singapore clarke quay}
 
- And we are done! 👋 That's all, friends. Thank you for reading up to this point. I know it was a long read. I will try to make it shorter next time. I would like to hear your feedback on anything that was not clear here. Here is my Twitter account @[T3chnocr4t](https://twitter.com/T3chnocr4t). Feel free to DM me if you have any issues with my write-up. Thanks!


[Go Back Home](https://t3chnocr4t.github.io/)





























