# Hello Hackers
This module incorporated the basics of the 'Command Line' and contained three challenges- 'Intro to Commands', 'Intro to Arguements' and 'Command History'

# Intro to commands
In this challenge we were required to invoke the hello command to get the flag. Once the flag is captured and the command terminates, the shell once again displays the prompt, ready for the next command.

## My Solution
**Flag:** 

Step 1- I linked my SSH key and connected it with- ssh hacker@dojo.pwn.college
```bash
HP@LAPTOP-IDCKVPOM MINGW64 ~ (master) ~ ssh -i ./key hacker@dojo.pwn.college
Connected!
```

Step 2- After clicking on enter, the flag was captured.
```bash
hacker@hello~intro-to-commands:~$ hello
Success! Here is your flag:
pwn.college{8inHv3nPIV7ujumQMHCoHhgaFfv.QX3YjM1wSNxEzNzEzW}
```

Step 3- Then i copied the flag and pasted it onto pwn.college.

## What I learned
1. I learned to get used to the linux interface.
- the `whoami` command, simply prints the username (hacker) to the terminal.
- When command is entered, the shell invokes it and performs the operation and prints the output.
- After pressing enter, shell prompt reappears for next command.

## References 
-The video tutorial available on pwn.college `The Command Line`
https://www.youtube.com/watch?list=PL-ymxv0nOtqqRAz1x90vxNbhmSkeYxHVC&v=g_85EVO3IC0


# Intro to Arguements
In this challenge, to get the flag, we had to run the `hello` command along with the word `hackers` so we had to print `hello hackers`.

## My solution
**Flag** `
Step 1- linked my SSH key and connected it with- ssh hacker@dojo.pwn.college
```bash
HP@LAPTOP-IDCKVPOM MINGW64 ~ (master) ~ ssh -i ./key hacker@dojo.pwn.college
Connected!
```
Step 2- Then i typed `hello hackers` into the command prompt and pressed enter to get the output,
```bash
hacker@hello~intro-to-commands:~$ hello
Success! Here is your flag:
pwn.college{8inHv3nPIV7ujumQMHCoHhgaFfv.QX3YjM1wSNxEzNzEzW}
```
Step 3- Then i copied the flag and pasted it onto pwn.college.

## What i learned 

1. When we run a command in a shell, we dont just run it by name, we pass arguments to it. 

2. The shell splits what you type into parts: the first word is the command, the subsequent words (separated by spaces) are arguments. 
pwn.college

3. Case-sensitivity matters, command names and arguments are handled exactly as written.

## References 
-(https://youtu.be/iwolPf6kN-k?si=Ys0nv4XRuFSdg_UY)-Introduction to Linux & Terminal Commands - Full Course for Beginners

# Command History 
This challenge will inject the flag into the history by pressing the up arrow button. The history contains the log of the already run commands, so similar commands can be inputted by scrolling through using the arrow keys.

# My Solution 
**Flag** `

1. Step 1- linked my SSH key and connected it with- ssh hacker@dojo.pwn.college
```bash
HP@LAPTOP-IDCKVPOM MINGW64 ~ (master) ~ ssh -i ./key hacker@dojo.pwn.college
Connected!
```
2. Now the shell is connected to dojo. Inside the shell, I pressed the up arrow key. The shell displayed the prevously saved command that contained the flag.
    ```bash
    hacker@hello~command-history:~$ the flag is 
    ```
3. I copied this flag and submitted it on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

##  What i learned
1. Efficiency
 One can reuse past commands via history. This helps avoid typos and speeds up workflow. The challenge lets you see directly how useful that is.
2. Navigating the interactive shell behavior
Using arrow keys to recall commands helps to learn the interactive shell features.It helps build muscle memory.

## References 
-(https://youtu.be/iwolPf6kN-k?si=Ys0nv4XRuFSdg_UY)-Introduction to Linux & Terminal Commands - Full Course for Beginners