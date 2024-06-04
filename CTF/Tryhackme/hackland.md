***
# Hackland
### Difficuity - Easy

👋 [Hackland](https://tryhackme.com/r/room/hackland)... Let's check this really quick guys. There are some really weird files on Hacksparo's desktop. Let's find out what is really hiding from us. This room is about learning about zip files and how to uncover secrets in a zip file. Let's get started.

![2024-06-04_00-57](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/f772cc30-670d-4d7a-ac4b-58a019181ea7)

### TASK 1# Note
- Note: Some browsers may flag these files as malicious because they are in ZIP format.
- it is not malicious...

#### Q1: Are you ready 
- Answer: No answer need

### Task 2# Werid Image
The first file is an weird image saying:

'W3lc0m3 to th3 H4ckl4nd. The king Hacksparo left his treasure somewhere. Please find it before pirates do. I believe in you, h4ckerm4n.'

#### Q1: please find that treasure
- Okay, let's find the treasure. First, let's start by downloading the file onto our machine.
- It is a zip file to unzip it use:

![1](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/6e2a5e19-1cf6-46f2-90dc-c8a5f6d0d37d)

- After the file is unzipped, we can see it is an image. We can use many tools here, but I love Stegseek. It is a command-line tool used for detecting hidden data, such as text or files, concealed within image files through steganography techniques. Let's check for hidden data in the image and specify a word list.

- Got the hidden message from the image, which is encoded in Base64. Let's decode it all (we can use many online tools to decode Base64 data), and we found the first flag. bang😂

![2](https://github.com/T3chnocr4t/T3chnocr4t.github.io/assets/115868619/a4de5d7a-8281-4e1d-9422-2c2d6c19116d)

- Answer: hacksparo{golds_diamonds_money_buy_a_buggati_h4ckerman}






