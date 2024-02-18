## Simple Nmap Scripts
***

Hola! :wave: Let's begin writing a simple Nmap script. Nmap is like a detective tool for computer networks. It helps you discover which devices are connected to a network, what services they're running, and how secure they are.

## Why Nmap🤔?

Nmap is used for network exploration and security auditing. It helps users discover devices on a network, identify open ports, and analyze network security.

![4289732-middle](https://github.com/T3chnocr4t/Linux/assets/115868619/7e6451c2-b47b-4ffd-ae5c-3076ffc2a7f5)

## Scripts

Let's proceed 🚀 to explain how the script works. This script is based on Nmap's TCP Connect Scan. I'll also be creating scripts for different types of scans in the future.

- First of all, I create a script by opening a text editor and naming the file with the extension ".sh" in this Nmap script. I also give it permission so that I can run it. Additionally, I was able to run it, but in this case, I'm not specifying any IP addresses or port numbers. Now, let me explain how the script works 😄.

![Screenshot_2024-01-30_05-55-55](https://github.com/T3chnocr4t/Linux/assets/115868619/042e971e-3461-4dfa-b220-3943fb99918c)

## Explanation of the Scripts:
***

![Screenshot_2024-01-30_05-48-18](https://github.com/T3chnocr4t/Linux/assets/115868619/a81fff38-d023-4712-ae6e-dd1eeb98ded3)

So, I started the script with the shebang 👉( #! /bin/bash) so that the interpreter will understand it is a Bash script. 
In the second and third lines, I specify a comment, i.e., #, which doesn't execute. The comment serves as a guide; it doesn't execute any commands. It's simply a way for anyone editing the script to understand how it works and make corrections if necessary.

## command use:

- The echo command displays text on the terminal,to printing a message. For instance, echo "Hello, world!" prints "Hello, world!" to the screen.
- The sleep command temporarily stops script execution for a set duration. For instance, sleep 5 pauses the script for 5 seconds before continuing to the next instruction.
- The read command is used to take input from the user while the script is running. It prompts the user to enter some text, which is then stored in a variable for the script to use.
- The Nmap command, in this case, is used specifically for conducting a TCP connect scan, focusing on a specific port and IP address. in the i use nmap -sT ip addr port
So in this : The command "nmap -sT" instructs Nmap to perform a TCP connect scan. In a TCP connect scan, Nmap attempts to establish a full TCP connection with the target ports to determine whether they are open, closed, or filtered by a firewall. This method is more reliable but also more detectable than other scan types.



Yeah, that's all. Feel free to ask questions or share feedback. Here is my [Twitter handle](https://twitter.com/T3chnocr4t).

[Go back home](https://T3chnocr4t.github.io)





