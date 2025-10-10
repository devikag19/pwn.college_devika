# File gobbling 

# Matching with *
This challenge wants us to change the directory using the glob '*'.

## My solution
**Flag** `pwn.college{wxEymvnerKn7rtajD6Byxc8B3mW.QXxIDO0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
Connected!
This challenge resets your working directory to /home/hacker unless you change
directory properly...
This challenge resets your working directory to /home/hacker unless you change
directory properly...
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@globbing~matching-with-:~$ cd /c*
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{wxEymvnerKn7rtajD6Byxc8B3mW.QXxIDO0wSNxEzNzEzW}
```

## What I learned 
- This is invalid
'''
hacker@globbing~matching-with-:~$ cd /*l*
bash: cd: too many arguments
hacker@globbing~matching-with-:~$ cd /*e
bash: cd: too many arguments
'''
- To be able to use the glob '*', we have to use the command 'cd /c*'
- This is because, the error means the wildcard created a list of too many places to go and couldn't choose one.

## References
`

# Matching with ?
This challenge wants us to pass the argument of --giveflag to /challenge/challenge to get the flag.

## My solution
**Flag** `pwn.college{kGJocmDdvknmTqvR0AyFBLuR2bO.QXyIDO0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
Connected!
This challenge resets your working directory to /home/hacker unless you change
directory properly...
This challenge resets your working directory to /home/hacker unless you change
directory properly...
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{kGJocmDdvknmTqvR0AyFBLuR2bO.QXyIDO0wSNxEzNzEzW}
```

## What I learned 
- The glob '?' unlike '*' replaces just one character.


# Matching with []
This challenge wants us to search for file_b, file_a, file_s, and file_h using the glob '[]'.

## My solution
**Flag** `pwn.college{Q_GKPlKAttKBNpZDPAzInOGUTsq.QXzIDO0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@globbing~matching-with-:~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[absh]
You got it! Here is your flag!
pwn.college{Q_GKPlKAttKBNpZDPAzInOGUTsq.QXzIDO0wSNxEzNzEzW}
```

## What I learned 
- The glob '[]' is a wildcard for some subset of potential characters, specified within the brackets.

## References 
-


# Matching paths with []
This challenge wants us to search for file_b, file_a, file_s, and file_h using the entire paths with the glob '[]'.

## My solution
**Flag** `pwn.college{EwSTXkjV4PnHozPROougaU9HMA9.QX0IDO0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[absh]
You got it! Here is your flag!
pwn.college{EwSTXkjV4PnHozPROougaU9HMA9.QX0IDO0wSNxEzNzEzW}
```
## What I learned 
- The glob '[]' can take a single argument including the absolute paths of the file. 

## References 
-


# Multiple Globs
This challenge wants us to search for all the files that contain the letter p in their name.

## My solution
**Flag** `pwn.college{cy91mu9KTgH6MdvhUIKemtEhhun.0lM3kjNxwSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
Connected!
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@globbing~multiple-globs:~$ cd /challenge/files
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run *p*
You got it! Here is your flag!
pwn.college{cy91mu9KTgH6MdvhUIKemtEhhun.0lM3kjNxwSNxEzNzEzW}
```

## What I learned 
- we can use more than one globs in a single statement.


# Mixing Globs
This challenge wants us to use a 6 or less character glob that will match the files "challenging", "educational".

## My solution
**Flag** `pwn.college{cel6HqAoayiuRTAUY60X0Qjb3l4.QX1IDO0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
Connected!
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@globbing~mixing-globs:~$ cd /challenge/files
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cpe]*
You got it! Here is your flag!
pwn.college{cel6HqAoayiuRTAUY60X0Qjb3l4.QX1IDO0wSNxEzNzEzW}
```

## What I learned 
- To use multiple globs together.

## My mistakes
- Earlier I was trying to use the '*' inside the glob '[]'

```bash
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [i*n*]
Your expansion did not expand to the requested files (challenging, educational,
pwning). Instead, it expanded to:
[i*n*]
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [*i*n*]
Error: your argument is too long! It must be 6 characters or less.
- The argument '*i*n*' should've worked, but since we're told to use square brackets glob, it doesn't work.
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run *i*n*
Error: you did not use a square bracket glob...
```

## References 
-

# Exclusionary Globbing
This challenge wants us to list all files that don't start with p, w, or n using '!'.

## My solution
**Flag** `pwn.college{0dmy6e-pDjn59OqeoU3EOI7qj48.QX2IDO0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
Connected!
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{0dmy6e-pDjn59OqeoU3EOI7qj48.QX2IDO0wSNxEzNzEzW}
```

## What I learned 
- If the first character in the brackets is a ! or (in newer versions of bash) a ^, the glob inverts, and that bracket instance matches characters that aren't listed. 

## References 
-

# Tab Completion
This challenge wants us to use tab-completion to read the flag.

## My solution
**Flag** `pwn.college{UkRMrqkDZoHZ8M142AodJuNkLVi.0FN0EzNxwSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
Connected!
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@globbing~tab-completion:~$ cat /challenge/pwncollege?
pwn.college{UkRMrqkDZoHZ8M142AodJuNkLVi.0FN0EzNxwSNxEzNzEzW}
```

## What I learned 
- The tab button can be used to autofill the path of the file.


# Multiple options for tab completion 
This challenge requires us to use tab to complete commands for the suggested ones by the terminal.

## My solution
**Flag**  `pwn.college{4LxfmAfH10NHW_oea5B7waSVClb.0lN0EzNxwSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
Connected!
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/
cat: /challenge/files/: Is a directory
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-flag
pwn.college{4LxfmAfH10NHW_oea5B7waSVClb.0lN0EzNxwSNxEzNzEzW}
```

## What i learned 
The challenge taught me on how to use the tab to complete the commands to get through them easier.

# Tab Completion on Commands
This challenge wants us to use tab-completion to read the flag.

## My solution
**Flag** `pwn.college{g8OnfGT5hUXZIQcaNwuM1Qxe-40.0VN0EzNxwSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
Connected!
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@globbing~tab-completion-on-commands:~$ pwncollege-29513
Correct! Here is your flag:
pwn.college{g8OnfGT5hUXZIQcaNwuM1Qxe-40.0VN0EzNxwSNxEzNzEzW}
```
## What I learned 
- The tab button can also be used to complete commands




