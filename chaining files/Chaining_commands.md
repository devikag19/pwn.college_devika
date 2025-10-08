# Chaining commands 

# Chaining with semicolons 
This challenge uses `;` to chain commands. 

## My solve
**Flag** `pwn.college{Q0yuSTxUz6ZrrJzYIt13_xaa703.QX1UDO0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@chaining~chaining-with-semicolons:~$ /challenge/pwn ; /challenge/college ; cat /flag
cat: /flag: Permission denied
Yes! You chained /challenge/pwn and /challenge/college! Here is your flag:
pwn.college{Q0yuSTxUz6ZrrJzYIt13_xaa703.QX1UDO0wSNxEzNzEzW}
```

## What i learned 
The semicolon command is analogous, without the prompt and with entering both commands before anything is executed.


# Building on success 
This challenge uses the `&&` command. 

## My solve
**Flag** `pwn.college{Ygbd4zEew6ePN5AUfnZoWmbInaB.0lM0MDOxwSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@chaining~building-on-success:~$ /challenge/first-success && /challenge/second
Nice chaining! Flag: pwn.college{Ygbd4zEew6ePN5AUfnZoWmbInaB.0lM0MDOxwSNxEzNzEzW}
```

## What i learned 
The `&&` operator allows you to run a second command only if the first command succeeds. This is called the AND operator because both conditions must be true, the first command must succeed AND then the second command will run.


# Handling failure 
This challenge uses the `||` command. 

## My solve
**Flag** `pwn.college{gA4S4UzzCOf2IFbxGl32cj04aa8.01M0MDOxwSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@chaining~handling-failure:~$  /challenge/first-failure || /chall
enge/second
Nice chaining! Flag: pwn.college{gA4S4UzzCOf2IFbxGl32cj04aa8.01M0MDOxwSNxEzNzEzW}
```

## What i learned
The `||` operator allows us to run a second command only if the first command fails. This is called the OR operator because either the first command succeeds OR the second command will run.


# Your first shell script 
This challenge asks us to put commands in a file and execute the file.

## My solve
**Flag** `pwn.college{YA2SyCKBk5Zbwbg1AEE8T_WVucV.QXxcDO0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@chaining~your-first-shell-script:~$ echo -e '#!/bin/bash\n/challenge/pwn ; /challenge/college' > x.sh
hacker@chaining~your-first-shell-script:~$ chmod +x x.sh
hacker@chaining~your-first-shell-script:~$ bash x.sh
Great job, you've written your first shell script! Here is the flag:
pwn.college{YA2SyCKBk5Zbwbg1AEE8T_WVucV.QXxcDO0wSNxEzNzEzW}
```

## What i learned 
I learned how to write a shell script and executing it.


# Redirecting script output 
This challenge requires us to pipe the output by redirecting it. 

## My solve
**Flag** `pwn.college{03QgYuaAILsrNNBLvSGs6jrP3xi.QX4ETO0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@chaining~redirecting-script-output:~$ echo -e '#!/bin/bash\n/challenge/pwn ; /challenge/college' > x.sh
hacker@chaining~redirecting-script-output:~$ ./x.sh | /challenge/solve
Correct! Here is your flag:
pwn.college{03QgYuaAILsrNNBLvSGs6jrP3xi.QX4ETO0wSNxEzNzEzW}
```

## What i learned 
I learned how to pipe the output of a script into another program.


# Executable shell scripts 
This challenges requires us to not use the bash command to write scripts 

## My solve
**Flag** `pwn.college{UGcevnf_SthFlnVnr31YQhA7D98.QX0cjM1wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@chaining~executable-shell-scripts:~$ echo '#!/bin/bash' > solve.sh
echo '/challenge/solve' >> solve.sh
hacker@chaining~executable-shell-scripts:~$ ./solve.sh
Congratulations on your shell script execution! Your flag:
pwn.college{UGcevnf_SthFlnVnr31YQhA7D98.QX0cjM1wSNxEzNzEzW}
```

## what i learned 
i learned how to create a script without invoking the bash command. 


# Understanding Schebangs 
This challenge requires us to use the schbang command. 


## My solve
**Flag** `pwn.college{Mk3H0ss_nr_-7EAbmhgdMewtou3.0VOzMDOxwSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@chaining~understanding-shebangs:~$ echo -e '#!/bin/bash\necho "hack the planet"' > /home/hacker/solve.sh
hacker@chaining~understanding-shebangs:~$ /challenge/run
Testing your script...
Perfect! Your flag:
Flag: pwn.college{Mk3H0ss_nr_-7EAbmhgdMewtou3.0VOzMDOxwSNxEzNzEzW}
```

## What i learned 
1. the schbang start with `#!`.
2. Linux treats the file as an interpreted program, and the contents of the rest of the line as the path to the interpreter. It then invokes the interpreter with the path to the program file as its only argument.


# Scripting with arguements 
This challenge makes us write scripts that can take arguments.

## My solve
**Flag** `pwn.college{Mk3H0ss_nr_-7EAbmhgdMewtou3.0VOzMDOxwSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@chaining~scripting-with-arguments:~$ echo -e '#!/bin/bash\necho "$2 $1"' > /home/hacker/solve.sh
hacker@chaining~scripting-with-arguments:~$ /challenge/run
Correct! Your script properly reversed the arguments.
Here's your flag:
pwn.college{QyV_rFZlXnSHvMLMfb6tInSoQfY.0VNzMDOxwSNxEzNzEzW}
```

## What i learned 
i learned how to input scripts with arguments using special variables.


# Scripting with conditionals 
This challenge made use of the `if` statement. 


## My solve
**Flag** `pwn.college{Mk3H0ss_nr_-7EAbmhgdMewtou3.0VOzMDOxwSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@chaining~scripting-with-conditionals:~$ echo '#!/bin/bash
if [ "$1" == "pwn" ]; then
    echo "college"
fi' > /home/hacker/solve.sh
hacker@chaining~scripting-with-conditionals:~$ /challenge/run
Correct! Your script properly handles all the conditions.
Here's your flag:
pwn.college{U4ogIOuHvHpdQs0j7NHi8WZvJLV.0lNzMDOxwSNxEzNzEzW}
```

## What i learned 
1. There must be spaces after if  after [, and before ]. If, then, and fi must all be on different lines or separated by semicolons; The terminator of the if statement is fi (if backwards).


# Scripting with defualt case 
this challenge uses the `if-else` statement.

## My solve
**Flag** `pwn.college{4qrfFOQ_OUisT3mRQhsG3oGs2Gf.01NzMDOxwSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@chaining~scripting-with-default-cases:~$ echo '#!/bin/bash
echo '#!/bin/bash
if [ "$1" == "hack" ]; then
    echo "the planet"
elif [ "$1" == "pwn" ]; then
    echo "college"
elif [ "$1" == "learn" ]; then
    echo "linux"
else
    echo "unknown"
fi' > /home/hacker/solve.sh
hacker@chaining~scripting-with-default-cases:~$ /challenge/run
Correct! Your script properly handles the if/else conditions.
Here's your flag:
pwn.college{4qrfFOQ_OUisT3mRQhsG3oGs2Gf.01NzMDOxwSNxEzNzEzW}
```

## What i learned 
1. else doesn't have a condition instead it catches everything that didn't match previously. 
2. It also doesn't have a then statement. the fi goes after the else block to denote the end of the statement.


# Scripting with multiple conditions 
this challenge uses the elif command. 

## My solve
**My flag** `pwn.college{8885FWJGnSzIGn9LWTNZUzo6Oo5.0FOzMDOxwSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@chaining~scripting-with-multiple-conditions:~$ echo '#!/bin/bash
if [ "$1" == "hack" ]; then
    echo "the planet"
elif [ "$1" == "pwn" ]; then
    echo "college"
elif [ "$1" == "learn" ]; then
    echo "linux"
else
    echo "unknown"
fi' > /home/hacker/solve.sh
hacker@chaining~scripting-with-multiple-conditions:~$ /challenge/run
Correct! Your script properly handles all the conditions with elif.
Here's your flag:
pwn.college{8885FWJGnSzIGn9LWTNZUzo6Oo5.0FOzMDOxwSNxEzNzEzW}
```

## What i learned 
This challenge makes the use of the elif stament and makes us practice it.


# Reading shell script 
this challenges requires us to read a script file. 

## My solve
**My flag** `pwn.college{kCuidU1bIEnp2yCZN4vDuRg1816.0lMwgDOxwSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
cat /challenge/run
#!/opt/pwn.college/bash

read GUESS
if [ "$GUESS" == "hack the PLANET" ]
then
        echo "CORRECT! Your flag:"
        cat /flag
else
        echo "Read the /challenge/run file to figure out the correct password!"
fi
hacker@chaining~reading-shell-scripts:~$ /challenge/run
hack the PLANET
CORRECT! Your flag:
pwn.college{kCuidU1bIEnp2yCZN4vDuRg1816.0lMwgDOxwSNxEzNzEzW}
```

## What i learned 
i learned how to read a shell script and decode a password which is encoded in a script file.
