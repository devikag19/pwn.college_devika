# Comprehending Commands
This module consists of 14 challenges.


# Cat:not the pet, but the command!
This challenge uses the `cat` command, which concatenates multiple files if provided multiple arguments. We used the command `cat flag` to capture the flag. On sumbitting the flag, challenge is completed.

## My solve
**Flag:** `pwn.college{4lvaQ3sjJW0tJSdy4SuzhBE3hnl.QXxcTN0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
Connected!
```

2. Now the shell is connected to dojo. Now on typing `cat flag` and clicking on Enter, I get the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@commands~cat-not-the-pet-but-the-command:~$ cat flag
pwn.college{4lvaQ3sjJW0tJSdy4SuzhBE3hnl.QXxcTN0wSNxEzNzEzW}
```


## What I learned
1. The `cat` command is most often used for reading out files. I learned how to use the cat command to read and display the contents of a file directly in the terminal. 

2. If no arguments are given at all, cat will read from the terminal input and output it.

## References  
-


# Catting absolute paths
The challenge asks to use the `cat` command and enter `cat /flag` to capture the flag. 
On sumbitting the flag, challenge is completed.


## My Solution
**Flag:** `pwn.college{csXT7GaNyZpKRbHA0u5A4SEOdrR.QX5ETO0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
Connected!
```

2. Now the shell is connected to dojo. Now on typing `cat /flag` and clicking on Enter, I get the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@commands~cat-not-the-pet-but-the-command:~$ cat /flag
pwn.college{csXT7GaNyZpKRbHA0u5A4SEOdrR.QX5ETO0wSNxEzNzEzW}
```

## What i learned 
1. `cat` can take arguements as absolute paths as well.

2. `/flag` is where the flag always lives in pwn.college, but unlike in this challenge, we cannot can't access that file directly.

## References
-


# More catting practice 
In this challenge we did not change the directory using `cd` and used the command `cat /lib/mysql/flag` to capture the flag.On sumbitting the flag, challenge is completed.

## My solution
**Flag:** `pwn.college{8BwIqEzjiqgx-gp6ekTBqVMYyqp.QXwITO0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
Connected!
```

2. Now the shell is connected to dojo. Now on typing `cat /lib/mysql/flag` and clicking on Enter, I get the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@commands~more-catting-practice:~$ cat /lib/mysql/flag
pwn.college{8BwIqEzjiqgx-gp6ekTBqVMYyqp.QXwITO0wSNxEzNzEzW}
```

## What i learned 
1. We can specify all sorts of paths as arguments to commands. I learned how to use the `cat` command by changing the directory without using the `cd` command.

## References
-


# Grepping for a needle in the haysack
In this challenge we used the command `grep pwn.college /challenge/data.txt` to capture the flag. On sumbitting the flag, challenge is completed.

## My solution
**Flag:** `pwn.college{0s-EzjRRl5RnsUKdgSJueMOIo7W.QX3EDO0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
Connected!
```

2. Now the shell is connected to dojo. Now on typing `grep pwn.college /challenge/data.txt` and clicking on Enter, I get the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt
pwn.college{0s-EzjRRl5RnsUKdgSJueMOIo7W.QX3EDO0wSNxEzNzEzW}
```

## What i learned
1. When the files that we are using with `cat` out are too big, we can use the grep command to search for the contents we need.

2.Using the grep command to search through files and directories and to quickly locate specific texts, such as  hidden flags.

## References
-


# Comparing files 
In this challenge we used the command ` diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt` to capture the flag. On sumbitting the flag, challenge is completed.

## My solution
**Flag:** `pwn.college{oNWimsY9U-HrwpSNuxzUxs06t_e.01MwMDOxwSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
Connected!
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@commands~comparing-files:~$ diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt
96a97
> pwn.college{oNWimsY9U-HrwpSNuxzUxs06t_e.01MwMDOxwSNxEzNzEzW}
```

## What i learned
1. In this challenge, I learned how to compare files to detect differences that can reveal hidden information, such as a flag. I practiced using the diff command to spot line-by-line changes between text files.

## References 
-


# Listing files
In this challenge we used the command `/challenge/18539-renamed-run-30194` to capture the flag. On sumbitting the flag, challenge is completed.

## My solution
**Flag:** `pwn.college{0SRKUhjeqYUN5InlbO-RGh5P4GV.QX4IDO0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
Connected!
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@commands~listing-files:~$ /challenge/18539-renamed-run-30194
Yahaha, you found me! Here is your flag:
pwn.college{0SRKUhjeqYUN5InlbO-RGh5P4GV.QX4IDO0wSNxEzNzEzW}
```

## What i learned
1. I learned how to list the content of the files using the `ls` command.

2. The `ls` command will list files in all the directories provided to it as arguments, and in the current directory if no arguments are provided. 

## References 
-


# Touching files
In this challenge we used the command `touch` to create new files and then run `/challenge/run` to capture the flag. On sumbitting the flag, challenge is completed.

## My solution
**Flag:** `pwn.college{MP4XVp3GHhflRyvbLGCn7ByiO4K.QXwMDO0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
Connected!
```

2. Now the shell is connected to dojo. Now on typing `touch` and clicking on Enter, I get the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@commands~touching-files:~$ touch /tmp/pwn
hacker@commands~touching-files:~$ touch /tmp/college
hacker@commands~touching-files:/tmp$ /challenge/run
Success! Here is your flag:
pwn.college{MP4XVp3GHhflRyvbLGCn7ByiO4K.QXwMDO0wSNxEzNzEzW}
```

## What i learned 
1. we can create a new blank file by touching it with the `touch` command.

## References 


# Removing files 
In this challenge we used the command `rm` to delete files and then run `/challenge/check` to capture the flag. On sumbitting the flag, challenge is completed.

## My solution
**Flag:** `pwn.college{YZTlW3NSY6kWWTpbkQqmTpKNkgJ.QX2kDM1wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
Connected!
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@commands~removing-files:~$ rm delete_me
hacker@commands~removing-files:~$ /challenge/check
Excellent removal. Here is your reward:
pwn.college{YZTlW3NSY6kWWTpbkQqmTpKNkgJ.QX2kDM1wSNxEzNzEzW}
```

## What i learned 
1. We can remove files with the `rm` command.

## References
-


# moving files
In this challenge we used the command `mv` to move files around and then run `/challenge/check` to capture the flag. On sumbitting the flag, challenge is completed.

## My solution
**Flag:** `pwn.college{4fpF4oeiKvfm-YrLmaGbPC59I6p.0VOxEzNxwSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
Connected!
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@commands~moving-files:~$ mv /flag /tmp/hack-the-planet
Correct! Performing 'mv /flag /tmp/hack-the-planet'.
hacker@commands~moving-files:~$ /challenge/check
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
pwn.college{4fpF4oeiKvfm-YrLmaGbPC59I6p.0VOxEzNxwSNxEzNzEzW}
```

## What i learned 
1. The files can be moved around using the `mv` command. We have to first name the file and then the source destination which is where the file needs to be moved to.

## References
-

# Hidden files
In this challenge we used the command `mv` to move files around and then run `/challenge/check` to capture the flag. On sumbitting the flag, challenge is completed.

## My solution
**Flag:** ``

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
Connected!
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash

```

## What i learned 


## References
-


# an epic filsystem quest 
In this challenge we used the command `mv` to move files around and then run `/challenge/check` to capture the flag. On sumbitting the flag, challenge is completed.

## My solution
**Flag:** ``

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
Connected!
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash

```

## Refernces

# Making directories
In this challenge we used the command `mkdir` to create new directories and then run `/challenge/check` to capture the flag. On sumbitting the flag, challenge is completed.

## My solution
**Flag:** `pwn.college{UIYfG9Q42LYBSb6Prn1Peyz-kFO.QXxMDO0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
Connected!
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@commands~making-directories:/tmp$ touch /tmp/pwn/college
hacker@commands~making-directories:/tmp$ ^C
hacker@commands~making-directories:/tmp$ /challenge/run
Success! Here is your flag:
pwn.college{UIYfG9Q42LYBSb6Prn1Peyz-kFO.QXxMDO0wSNxEzNzEzW}
```

## What i learned 
1. I learned hoe make directories using the `mkdir` command and adding files in it.

## Refernces
-

