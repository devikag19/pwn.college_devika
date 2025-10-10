# Pondering PATH 

# The PATH variable 
This challenge introduces the `PATH` variable.

## My solve 
**Flag:** `pwn.college{sH_PHSsEiHlWXvB9B_lOLjV6IHP.QX2cDM1wSNxEzNzEzW}`


1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@path~the-path-variable:~$ PATH=""
hacker@path~the-path-variable:~$ ls
bash: ls: No such file or directory
hacker@path~the-path-variable:~$ /challenge/run
Trying to remove /flag...
/challenge/run: line 4: rm: No such file or directory
The flag is still there! I might as well give it to you!
pwn.college{sH_PHSsEiHlWXvB9B_lOLjV6IHP.QX2cDM1wSNxEzNzEzW}
```

## What i learned
1. The `PATH` variable stores all directory paths.
2. a wrong command to `PATH` can erase all directory paths.  


# Setting PATH
this challenge requires us to add directories. 


## My solve 
**Flag:** `pwn.college{YF8CMKh1JkEa6aJ0rI_mTEDoIfy.QX1cjM1wSNxEzNzEzW}`


1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@path~setting-path:~$ PATH=/challenge/more_commands/
hacker@path~setting-path:~$ /challenge/run
Invoking 'win'....
Congratulations! You properly set the flag and 'win' has launched!
pwn.college{YF8CMKh1JkEa6aJ0rI_mTEDoIfy.QX1cjM1wSNxEzNzEzW}
```

## What i learned 
I learned how to add directories using the `PATH` function.


# Finding Paths 
This challenge uses the `which` command.

## My solve 
**Flag:** `pwn.college{kne84hy9Kt-tXP2j-S1Qyby0Krd.01NzEzNxwSNxEzNzEzW}`


1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@path~finding-commands:~$ which win
/challenge/paths/18470/win
hacker@path~finding-commands:~$ cat /challenge/paths/18470/win/flag
cat: /challenge/paths/18470/win/flag: Not a directory
hacker@path~finding-commands:~$ cat /challenge/paths/18470/flag
pwn.college{kne84hy9Kt-tXP2j-S1Qyby0Krd.01NzEzNxwSNxEzNzEzW}
```

## What i learned 
I learned how to find command locations using which command. 


# Adding Commands 
In this challenge we had to  make a shell script called `win`, add its location to the `PATH`then and use `/challenge/run` to find it.


## My solve 
**Flag:** `pwn.college{4siGkt5NXE5vs4SDdCg7BkQozDj.QX2cjM1wSNxEzNzEzW}`


1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@path~adding-commands:~$ mkdir /tmp/myscripts
hacker@path~adding-commands:~$ echo '#!/bin/bash' > /tmp/myscripts/win
hacker@path~adding-commands:~$ echo '/bin/cat /flag' >> /tmp/myscripts/win
hacker@path~adding-commands:~$ chmod +x /tmp/myscripts/win
hacker@path~adding-commands:~$ export PATH=/tmp/myscripts
hacker@path~adding-commands:~$ /challenge/run
Invoking 'win'....
pwn.college{4siGkt5NXE5vs4SDdCg7BkQozDj.QX2cjM1wSNxEzNzEzW}
```

## What i learned 
I learned how to create a custom command by writing a shell script, making it executable with chmod +x, and adding its location to the $PATH.


# Hijacking commands 

## My solve 
**Flag:** `pwn.college{UB-7hlB2gXSLHoaM2Tan0Pj0KY0.QX3cjM1wSNxEzNzEzW}`


1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@path~hijacking-commands:~$ mkdir /tmp/fake_bin
hacker@path~hijacking-commands:~$ echo '#!/bin/bash' > /tmp/fake_bin/rm
hacker@path~hijacking-commands:~$  echo 'echo " "' >> /tmp/fake_bin/rm
hacker@path~hijacking-commands:~$ chmod +x /tmp/fake_bin/rm
hacker@path~hijacking-commands:~$  export PATH=/tmp/fake_bin:$P
ATH
hacker@path~hijacking-commands:~$ /challenge/run
Trying to remove /flag...
Found 'rm' command at /tmp/fake_bin/rm. Executing!

hacker@path~hijacking-commands:~$  echo 'cat /flag' > /tmp/fake_bin/rm
hacker@path~hijacking-commands:~$ /challenge/run
Trying to remove /flag...
Found 'rm' command at /tmp/fake_bin/rm. Executing!
pwn.college{UB-7hlB2gXSLHoaM2Tan0Pj0KY0.QX3cjM1wSNxEzNzEzW}
```

## What i learned 
i learned how to find command locations using `which` command.
