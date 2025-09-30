# Shell variables

# Printing variables

## My solve
**Flag:** `pwn.college{QCFS19SuolOF42R8MjdY-qLdXd5.QX3UTN0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@variables~printing-variables:~$ echo $FLAG
pwn.college{QCFS19SuolOF42R8MjdY-qLdXd5.QX3UTN0wSNxEzNzEzW}
```

## What I learned
using `echo` to print variables. 

# Setting variables
In this challenge we need to assign variables some values.

## My solve
**Flag:** `pwn.college{o9CXGpR4y40ExwVjL0HViBwTUxH.QX5UTN0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@variables~setting-variables:~$ echo $PWN
hacker@variables~setting-variables:~$ PWN=COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
hacker@variables~setting-variables:~$ echo $PWN
hacker@variables~setting-variables:~$ PWN=COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{o9CXGpR4y40ExwVjL0HViBwTUxH.QX5UTN0wSNxEzNzEzW}
```

## What i learned 
1. we can assign values to variables just like other languages. 

2. There are no spaces around the `=!`. If we put spaces the shell won't recognize a variable assignment and will, instead it will run the `VAR` command.

# Multi-word variables
This challenge uses quoting.

## My solve
**Flag:** `pwn.college{4kd9_HKZVel0_VMF3K4Vp6fYpZ1.QXwYTN0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@variables~multi-word-variables:~$ echo $PWN

hacker@variables~multi-word-variables:~$ PWN="COLLEGE YEAH"
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{4kd9_HKZVel0_VMF3K4Vp6fYpZ1.QXwYTN0wSNxEzNzEzW}
```

## What i learned 
1. how to set a variable's value to multiple terms.

2. Spaces have special significance in the shell, and there are places where we can't use them spuriously.

# Exploring variables 
The goal of the challenge is to read the value of a specific variable  and then pass that information to the challenge program.

## My solve
**Flag:** `pwn.college{UGRgjnqXacN1m_YmYFJJqQn8N30.QXyYTN0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@variables~exporting-variables:~$ echo $PWN
hacker@variables~exporting-variables:~$ COLLEGE=PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ /challenge/run PWN
CORRECT!
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great
job! Here is your flag:
pwn.college{UGRgjnqXacN1m_YmYFJJqQn8N30.QXyYTN0wSNxEzNzEzW}
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
```

## What i learned
By default variables that we set in a shell session are local to that shell process which means other commands would not inherit them.

# Printing exported variables 
This challenges requires the `env` variable. 

## My solution 
**Flag:** `pwn.college{wDCRDeOwvgG0CmJ_VAj1R2zHRLH.QX4UTN0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@variables~printing-exported-variables:~$ env
SHELL=/run/dojo/bin/bash
HOSTNAME=variables~printing-exported-variables
PWD=/home/hacker
MANPATH=/run/dojo/share/man:
DOJO_AUTH_TOKEN=192a9bf50cc19a53d91b8e5008b7a4e75e803db0fdc6807c8a86556e838cdead
HOME=/home/hacker
LANG=C.UTF-8
FLAG=pwn.college{wDCRDeOwvgG0CmJ_VAj1R2zHRLH.QX4UTN0wSNxEzNzEzW}
TERMINFO=/run/dojo/share/terminfo
TERM=xterm-256color
SHLVL=2
LC_CTYPE=C.UTF-8
SSL_CERT_FILE=/run/dojo/etc/ssl/certs/ca-bundle.crt
PATH=/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
DEBIAN_FRONTEND=noninteractive
_=/run/dojo/bin/env
```

## What i learned 
The `env` command prints out every exported variable set the your shell

# Storing command output 
This challenge uses the command substitution method.

## My solution 
**Flag:** `pwn.college{UkLjBdm0XoXz4RIaBL3sttRixjL.QX1cDN1wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@variables~storing-command-output:~$  PWN=$(/challenge/run)
Congratulations! You have read the flag into the PWN variable. Now print it out
and submit it!
hacker@variables~storing-command-output:~$ echo $PWN
pwn.college{UkLjBdm0XoXz4RIaBL3sttRixjL.QX1cDN1wSNxEzNzEzW}
```

## What i learned 
I learned storing the output of some command into a variable.


# Reading input 

## My solution 
**Flag:** `pwn.college{oMV_8hzH-Rk1ZTE1mLBdGcMA1QP.QX4cTN0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@variables~reading-input:~$ read PWN
COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{oMV_8hzH-Rk1ZTE1mLBdGcMA1QP.QX4cTN0wSNxEzNzEzW}
```

## what i learned 
the use of the read command by reading the input from the user.


# reading files 
this challenges uses the `read` command. 

## My solution 
**Flag:** `pwn.college{gJP2lM7qeVmwr0xFSKdAuV8O8bh.QXwIDO0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@variables~reading-files:~$ read PWN < /challenge/read_me
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{gJP2lM7qeVmwr0xFSKdAuV8O8bh.QXwIDO0wSNxEzNzEzW}
```

## What i learned 
The use of directly reading any imput from the file.