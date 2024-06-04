***
# Hackland
### Difficuity - Easy

👋 [Hackland](https://tryhackme.com/r/room/hackland)... Let's check this really quick guys. There are some really weird files on Hacksparo's desktop. Let's find out what is really hiding from us. This room is about learning about zip files and how to uncover secrets in a zip file. Let's get started.

![2024-06-04_00-57](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/f772cc30-670d-4d7a-ac4b-58a019181ea7)

***
### TASK 1# Note
- Note: Some browsers may flag these files as malicious because they are in ZIP format.
- it is not malicious...

##### Q1: Are you ready 
- Answer: No answer need

***
### Task 2# Werid Image
The first file is an weird image saying:

'W3lc0m3 to th3 H4ckl4nd. The king Hacksparo left his treasure somewhere. Please find it before pirates do. I believe in you, h4ckerm4n.'

##### Q1: please find that treasure
- Okay, let's find the treasure. First, let's start by downloading the file onto our machine.
- It is a zip file to unzip it use:

![1](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/6e2a5e19-1cf6-46f2-90dc-c8a5f6d0d37d)

- After the file is unzipped, we can see it is an image. We can use many tools here, but I love Stegseek. It is a command-line tool used for detecting hidden data, such as text or files, concealed within image files through steganography techniques. Let's check for hidden data in the image and specify a word list.

- Got the hidden message from the image, which is encoded in Base64. Let's decode it all (we can use many online tools to decode Base64 data), and we found the first flag. bang😂

![2](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/a4de5d7a-8281-4e1d-9422-2c2d6c19116d)

- Answer: hacksparo{golds_diamonds_money_buy_a_buggati_h4ckerman}

***
### Task 3# find the secret
I think the second file contains some secret. I'm curious to know that secret

##### Q1: what is Hacksparo's secret
- Downloading the second files
- Let's unzip the file; it has a 3 of files.

![3](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/2ef02078-ceaf-47ae-b4d9-f49f36da8045)

- Let's focus on the "private_key.asc" file first. We'll use a tool called "gpg2john" (which is used to extract hash data) so extract the hash data from the file and save it.

![4](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/c8eb11ac-de83-4c04-b921-951e2efacc29)

- Using john to crack the hash we get the password

![5](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/3d998aef-4c40-47a8-8c7f-1106dd2e556e)

- Now we can easily decrypt the GPG file found when we unzip the main file because without the password we can't decrypt it. Now that we know the password, let's decrypt it.

![6](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/da6cdedf-c30b-4387-92b5-0cb7d743f97d)

- That unveils Hacksparo's secret, but it is a Base64-encoded message. We also get a hash for the root password. Let's decode the message and crack the root password.
- Decoding the Base64 message gives us one part of the flag. Now let's crack the root password.

![7](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/a9eb83ea-980a-4a2f-8311-dae8a533a501)

- Save the hash and crack it with john

![8](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/2c790f6b-a253-437d-9e3a-2e06c5e220f8)

- 😂😂😂 Spongebob nah i love rick and morty.

- Answer: hacksparo{is_a_bigfun_of_spongebob}

***
### Task 3# FInd one piece
I know he is a big fan of One Piece, but the third file looks like a CTF. Play the CTF and find the One Piece.

##### Q: what is the one piece flag
- Download the file and let file one piece flag.
- Unzipping the zip file provides us with a password list and a Base64-encoded message.
- Decoding the Base64 message gives us another zip.
- save it with a file extension.zip

![9](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/0dd0a23b-f12e-4ee8-b79f-887a22f69215)

- To crack the zip file, I used a tool that I found on GitHub called [ZIP-Password-Cracker](https://github.com/Korozin/ZIP-Password-Cracker/tree/main) A simple Python script to crack ZIP Passwords. The script uses a mask attack which encompasses both bruteforce and dictionary attacks.

- Using the command e.g:
```
python3 PyZIP-Crack.py -zip Example2.zip -wordlist rockyou.txt
```

![ctf2](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/39b72a0e-2f07-47dd-b023-3304cd496b7d)

- Answer: Hacksparo{L0fiStr@wHatP1r@tes_OnTre@sureIsland_Crew2024}

And we are done, guys! We found everything that Hacksparo is hiding from us.

![icegif-535](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/563c5f9f-aba5-40d3-97d9-1f6e436bd174)

### ALL Flags:
- hacksparo{golds_diamonds_money_buy_a_buggati_h4ckerman}
- hacksparo{is_a_bigfun_of_spongebob}
- Hacksparo{L0fiStr@wHatP1r@tes_OnTre@sureIsland_Crew2024}

 That's all, friends. Thank you for reading up to this point. I would like to hear your feedback on anything not clear here. Here is my Twitter account @[T3chnocr4t](https://twitter.com/T3chnocr4t). Feel free to DM me if you have any issues with my write-up. Thanks!

[Go Back Home](https://t3chnocr4t.github.io/)














