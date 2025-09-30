# Digesting Documentation


# Learning from Documentation
This challenge wants us to pass the argument of `--giveflag` to `/challenge/challenge` to get the flag.

## My solution

**Flag** `pwn.college{AlBncV6v6X6Z6Cf9pFS8pheJ-vV.QX0ITO0wSNxEzNzEzW}`
1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
Connected!
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@man~learning-from-documentation:~$ /challenge/challenge --giveflag
Correct argument! Here is your flag:
pwn.college{AlBncV6v6X6Z6Cf9pFS8pheJ-vV.QX0ITO0wSNxEzNzEzW}
```
## What I learned 
1 Arguments have to be given properly to absolute paths.

## References 
-

# Learning Complex Usuage 

# Reading Manuals 
This challenge wants us to look for the int in the man page for the challenge command and then using that to get the flag.

## My solution

**Flag** `pwn.college{cr5QWu4tcrOjgdm8YQGNgRfg5If.QX0EDO0wSNxEzNzEzW}`
1. I conected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
Connected!
```
2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@man~reading-manuals:~$ man challenge
hacker@man~reading-manuals:~$ /challenge/challenge --fortune
Of course a platonic relationship is possible -- but only between
husband and wife.
hacker@man~reading-manuals:~$  /challenge/challenge --version
I'm exactly the version I need to be!
hacker@man~reading-manuals:~$  /challenge/challenge --crutcr 548
Correct usage! Your flag: pwn.college{cr5QWu4tcrOjgdm8YQGNgRfg5If.QX0EDO0wSNxEzNzEzW}
```

## What I learned 
- The man (manual) command is used to get more info on a particular command, its use and other specifications.
- The command has to be exexuted properly with the correct arguments to get the desired output which was the error that I faced earlier.


# Searching manuals 
This challenge wants us to look for the int in the man page for the challenge command and then using that to get the flag using the `/` command.

## My solution

**Flag** `pwn.college{cr5QWu4tcrOjgdm8YQGNgRfg5If.QX0EDO0wSNxEzNzEzW}`
1. I conected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
Connected!
```
2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$ /challenge/challenge --okp
Initializing...
Correct usage! Your flag: pwn.college{oAcQsVbJiOMBX7jwRJV0WSt42ix.QX1EDO0wSNxEzNzEzW}
```

## What i learned 
1. In the `man challenge` page using the `/` command i searched for flag. To find the word i used the `n` and `N` commands. 

## References
-

# Searching for Manuals 
This challenge wants us to first go to `man man` then find the directory where the flag is stored.

## My solution

**Flag** `pwn.college{UfYcaAQnPaqKRIxmc4iG-tMu_Kq.QX2EDO0wSNxEzNzEzW}`
1. I conected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
Connected!
```
2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@man~searching-for-manuals:~$ man man
hacker@man~searching-for-manuals:~$ man --regex challenge
hacker@man~searching-for-manuals:~$ /challenge/challenge --fortune
"In corporate life, I think there are three important areas which contracts
can't deal with, the area of conflict, the area of change and area of reaching
potential.  To me a covenant is a relationship that is based on such things
as shared ideals and shared value systems and shared ideas and shared
agreement as to the processes we are going to use for working together.  In
many cases they develop into real love relationships."
-- Max DePree, chairman and CEO of Herman Miller Inc., "Herman Miller's
   Secrets of Corporate Creativity", The Wall Street Journal, May 3, 1988
hacker@man~searching-for-manuals:~$ /challenge/challenge --version
I'm exactly the version I need to be!
hacker@man~searching-for-manuals:~$ /challenge/challenge --fcanaq 420
Correct usage! Your flag: pwn.college{UfYcaAQnPaqKRIxmc4iG-tMu_Kq.QX2EDO0wSNxEzNzEzW}
```

## What i learned 
1. In this challenge we used the `man man` command to search the man page database to find the hidden challenge man page. 

## References
-

# Helpful program
This challenge uses the command `--help` to read the program's documentation to get the flag.

## My solution

**Flag** `pwn.college{EvtvpDzkl2M51yTR6ySJAT-rzmI.QX3IDO0wSNxEzNzEzW}`
1. I conected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
Connected!
```
2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v]
                                            [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to
                        give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge --fortune
My opinions may have changed, but not the fact that I am right.
hacker@man~helpful-programs:~$ /challenge/challenge --version
I'm exactly the version I need to be!
hacker@man~helpful-programs:~$ /challenge/challenge --p
The secret value is: 251
hacker@man~helpful-programs:~$
hacker@man~helpful-programs:~$ /challenge/challenge --g 251
Correct usage! Your flag: pwn.college{EvtvpDzkl2M51yTR6ySJAT-rzmI.QX3IDO0wSNxEzNzEzW}
```

## What i learned 
1. In this challenge i learned the use to the program's documentation and complete a challenge to capture the flag.

## References
-

# Help for built-ins
This challenge uses the concept of `built-ins`.

## My solution

**Flag** `pwn.college{cdj6zVWKYAIexEqMVvw8kMU8rMI.QX0ETO0wSNxEzNzEzW}`
1. I conected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
Connected!
```
2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!

    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "cdj6zVWK".
    hacker@man~help-for-builtins:~$ challenge --fortune
The opposite of talking isn't listening.  The opposite of talking is waiting.
                -- Fran Lebowitz, "Social Studies"
hacker@man~help-for-builtins:~$ challenge --version
I'm exactly the version I need to be!
hacker@man~help-for-builtins:~$ challenge --secret cdj6zVWK
Correct! Here is your flag!
pwn.college{cdj6zVWKYAIexEqMVvw8kMU8rMI.QX0ETO0wSNxEzNzEzW}
```

## What i learned 
I learnt that built-ins, rather than being programs with man pages and help options, are built into the shell itself. Builtins are invoked just like commands, but the shell handles thm internally instead of launching other programs.



