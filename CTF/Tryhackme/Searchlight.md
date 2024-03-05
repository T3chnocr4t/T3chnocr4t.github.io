***
# Searchlight IMINT
Difficulty = Easy
***
Hola👋 Welcome back. Here is a walkthrough on Searchlight IMINT based on TryHackMe. It covers learning the discipline of IMINT/GEOINT, which stands for Image Intelligence and Geospatial Intelligence.

![1](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/08f2137b-2295-4439-82b2-8efd00166638)

## What is IMINT and GEOINT 🤔 ?
- Image Intelligence (IMINT): Involves utilizing publicly available images, photographs, and visual media from open sources to gather intelligence.

- Geospatial Intelligence (GEOINT): Involves leveraging publicly available geospatial data, maps, satellite imagery, and other spatial information from open sources to gather intelligence.

Let get started

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

Let's start by downloading the given image.

![task3](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/71e4bda2-868a-4c6a-a0b0-b58a3a95d9ec)

### Q1: Which city is the tube station located in?
- By looking at the image carefully, we can identify the building; most of us know this is London 😂.
- But let's research the image to confirm if we are correct. By carefully looking at the image, we can see three words: `public subway, circus, and "underground.` Let's research it on Google.
- I then used Google maps at street level to make sure I had the exact same one:

![map](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/a3677233-8547-4c58-a962-2205a85e4757)

![map 2](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/36fd3096-8f05-4430-8606-67579b0c6ef4)

- I take a lok back in our search result then we can see many results about London
 
![1111111111111111111](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/dbf001b4-0422-46e3-9cfd-28d95e655709)

- Answer: London

### Q2: Which tube station do these stairs lead to?
- Taking a look at the Wikipedia page, we found our answer, which is `Piccadilly Circus`.

![55](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/543ff34e-dfbf-4708-b722-b888945ebd82)

- Answer: sl{Piccadilly Circus}

### Q3: Which year did this station open?

![55s](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/101930e0-e4bd-4d21-85d2-44e655f3b811)

- Answer: sl{1906}

### Q4: How many platforms are there in this station?
- Answer: 4

***
## Task 4: Keep At It!
- Downloads the given tasks
  
![task4](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/f603f7cc-e1e4-4122-91da-eb2121626d85)

### Q1: Which building is this photo taken in?
- By carefully looking at the image, we found `YVR Connect.` Let's make research about it and then we found...

![99](https://github.com/T3chnocr4t/T3chnocr4t/assets/115868619/ac3d29ac-18a0-4288-85b5-0d2b7742db90)

- Answer: sl{vancouver international airport}

### Q2: Which country is this building located in?
























