# Practicing piping 

# Redirecting Output 
This challenge required the use of `>` to redirect the output.

## My solve
**Flag** `pwn.college{Ar-n8GzsVNE191F4LYZ3hwbpqKL.QX0YTN0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your
flag:
pwn.college{Ar-n8GzsVNE191F4LYZ3hwbpqKL.QX0YTN0wSNxEzNzEzW}
```

## What I learned
1. I learnt the use of the `>` command to redirect the output to a particular file.


# Redirecting More output
In this challenge i had to redirect the output of the command `/challenge/run`.

## My solve
**Flag** `pwn.college{IbLDrjyl6T1WpeIu6L4N0GAS1XU.QX1YTN0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@piping~redirecting-more-output:~$ /challenge/run > myflag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-more-output:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{IbLDrjyl6T1WpeIu6L4N0GAS1XU.QX1YTN0wSNxEzNzEzW}
```

## What i learned 
1. I learned how to redirect the output to find the flag from the `my flag` file.


# Appending output 
This challenges uses the `>>` option to redirect files to genrerate the output.

## My solve
**Flag** `pwn.college{wCXq1Ksaa0V-cpd5KDzvlrIgjbv.QX3ATO0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@piping~appending-output:~$ /challenge/run >> /home/hacker/the-flag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /home/hacker/the-flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] Good luck!

[TEST] You should have redirected my stdout to a file called /home/hacker/the-flag. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
I will write the flag in two parts to the file /home/hacker/the-flag! I'll do
the first write directly to the file, and the second write, I'll do to stdout
(if it's pointing at the file). If you redirect the output in append mode, the
second write will append to (rather than overwrite) the first write, and you'll
get the whole flag!
hacker@piping~appending-output:~$ cat  /home/hacker/the-flag
 |
\|/ This is the first half:
 v
pwn.college{wCXq1Ksaa0V-cpd5KDzvlrIgjbv.QX3ATO0wSNxEzNzEzW}
                              ^
     that is the second half /|\
                              |

If you only see the second half above, you redirected in *truncate* mode (>)
rather than *append* mode (>>), and so the write of the second half to stdout
overwrote the initial write of the first half directly to the file. Try append
mode!
hacker@piping~appending-output:~$
```

## What i learned 
1. I learned the use of the append mode `>>` which redirects the output of the file to another file. 

**Note**
If you properly redirect in append-mode, the second half will be appended to the first, but if you redirect in truncation mode (>), the second half will overwrite the first and you won't get the flag.


# Redirecting errors 
The challenge required to redirect an error just like a file is redirected. 

## My solution 
**My flag** `pwn.college{ccRHAjHWD9Z-FlQI9GkF8rq9ceP.QX3YTN0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@piping~redirecting-errors:~$ /challenge/run > myflag 2> instructions
hacker@piping~redirecting-errors:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{ccRHAjHWD9Z-FlQI9GkF8rq9ceP.QX3YTN0wSNxEzNzEzW}
```

## What i learned 
1. Just like standard output, we can also redirect the error channel of commands.

2. When we redirect a process communication, we do it by FD number, though some FD numbers are implicit. For example, a > without a number implies 1>, which redirects FD 1 (Standard Output)



# Redirecting Input 
This challenge uses `<` to redirect input to programs.

## My solution 
**My flag** `pwn.college{o_eOLNBSAabUdYkiFKtEyUvUtYP.QXwcTN0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@piping~redirecting-input:~$ /challenge/run > PWN
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{o_eOLNBSAabUdYkiFKtEyUvUtYP.QXwcTN0wSNxEzNzEzW}
```

## What i learned 
1. Using the `<` command we can redirect input into the commands. 


# Grepping stored results 
This challenges conprises of redirecting the files and then using the  `grep` command to search for the resulting file.

## My solution 
**Flag** `pwn.college{YjCPrs3cMtFA2pkkE4KzZ5G-u3e.QX4EDO0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@piping~grepping-stored-results:~$ /challenge/run > /tmp/data.txt
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /tmp/data.txt
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to a file called /tmp/data.txt. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~grepping-stored-results:~$ grep "pwn.college" /tmp/data.txt
pwn.college{YjCPrs3cMtFA2pkkE4KzZ5G-u3e.QX4EDO0wSNxEzNzEzW}
```

## What i learned 
Using the `grep` command to search throught the resulting files once the output is redirected.


# Grepping live output 
This challenge uses the `|` operator. 

## My solution 
**Flag** `pwn.college{IDABGfC6hHu3BTDxt2V3TXmW4-n.QX5EDO0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@piping~grepping-live-output:~$ /challenge/run | grep flag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stdout : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/8b4vn1iyn6kqiisjvlmv67d1c0p3j6wj-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stdout!
[PASS] Success! You have satisfied all execution requirements.
[FLAG] Here is your flag:
camouflaged
camouflages
flagellating
flagstone
flagstaff's
flagstone's
persiflage
conflagration
flagging
flagellation's
flagged
flagons
flagrantly
flag
persiflage's
flagstaff
flagstones
flagellated
flagon
flagon's
flagship
camouflaging
unflagging
flagpole's
flagship's
flagella
conflagration's
flagstaffs
flags
flagpole
camouflage
flagellate
flag's
flagellation
flagellum
flagellum's
conflagrations
camouflage's
flagrant
flagships
flagpoles
flagellates
flagellums
hacker@piping~grepping-live-output:~$ /challenge/run | grep "pwn.college"
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stdout : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/8b4vn1iyn6kqiisjvlmv67d1c0p3j6wj-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stdout!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{IDABGfC6hHu3BTDxt2V3TXmW4-n.QX5EDO0wSNxEzNzEzW}
```

## What i learned 
We can cut out the middleman and avoid the need to store results to a file. We can do this by using the `|` (pipe) operator. Standard output from the command to the left of the pipe will be connected to (piped into) the standard input of the command to the right of the pipe.


## Grepping errors
In this challenge we grep through errors directly. 

## My solution
**Flag** `pwn.college{8SeG84t3ol1Ks9_G8XV3oSAv_fX.QX1ATO0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@piping~grepping-errors:~$ 2>& 1
hacker@piping~grepping-errors:~$ /challenge/run 2>& 1 | grep "pwn.c
ollege"
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stderr : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stderr to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/8b4vn1iyn6kqiisjvlmv67d1c0p3j6wj-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stderr!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{8SeG84t3ol1Ks9_G8XV3oSAv_fX.QX1ATO0wSNxEzNzEzW}
```

## What i learned 
1. I learnt how to the shell has a `>&` operator, which redirects a file descriptor to another file descriptor.

# Filtering with grep-v 
This challenge uses the `grep -v` command. 

## My solution 
**Flag** `pwn.college{MartNTEb80iTuUaRZ2Xqj7GUFEk.0FOxEzNxwSNxEzNzEzW}`
1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@piping~filtering-with-grep-v:~$ /challenge/run | grep -v "DECOY"
pwn.college{MartNTEb80iTuUaRZ2Xqj7GUFEk.0FOxEzNxwSNxEzNzEzW}
```

## What i learned 
1. While normal grep shows lines that match a pattern, `grep -v` shows lines that do NOT match a pattern.

# Dupliating piped data with tee
This challenge uses the `tee` command to duplicate data. 

## My solution 
**Flag** `pwn.college{U5-dfAh143EAtQAVcDhueIEmM4n.QXxITO0wSNxEzNzEzW}`
1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | tee secret | /challenge/college
Processing...
WARNING: you are overwriting file secret with tee's output...
The input to 'college' does not contain the correct secret code! This code
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ cat secret
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "U5-dfAh1"
hacker@piping~duplicating-piped-data-with-tee:~$  /challenge/pwn --secret U5-dfAh1 | /challenge/college
Processing...
Correct! Passing secret value to /challenge/college...
Great job! Here is your flag:
pwn.college{U5-dfAh143EAtQAVcDhueIEmM4n.QXxITO0wSNxEzNzEzW}
```

## What i learned 
learned that the tee command duplicates data flowing through your pipes to any number of files provided on the command line.


# Process substitution for input 
uses the `diff` command to diff two sets of command outputs.

## my solution 
**Flag** `pwn.college{gYwFfu5LG241kqRTOL3HAUvR8eL.0lNwMDOxwSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@piping~process-substitution-for-input:~$ diff <(/challenge/print_decoys) <(/challenge/print_decoys_and_flag)
98a99
> pwn.college{gYwFfu5LG241kqRTOL3HAUvR8eL.0lNwMDOxwSNxEzNzEzW}
```

## What i learned 
Process substitution <(...) gives diff file like views of each command's output so we can compare them and extract the lines present only in the version that contains the real flag.


# writing to multiple programs 
this challenge uses process substitution for writing to commands.

## my solution
**flag** `pwn.college{YbA9V-Y0d7BdPR0vGAkfAYDx907.QXwgDN1wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | tee >(/challenge/the) >(/challenge/planet)
This secret data must directly and simultaneously make it to /challenge/the and
/challenge/planet. Don't try to copy-paste it; it changes too fast.
23469231237248478
Congratulations, you have duplicated data into the input of two programs! Here
is your flag:
pwn.college{YbA9V-Y0d7BdPR0vGAkfAYDx907.QXwgDN1wSNxEzNzEzW}
```

## What i learned
Used output process substitution >(command) with tee to send /challenge/hack’s output simultaneously to both /challenge/the and /challenge/planet.

# split-piping stderr and stdout 
This challenge required us to redirect stdout to one program and stderr to another.

## My solution 
**Flag** `pwn.college{8n6uTxh03EJ4X7L6pTx03pq5Fot.QXxQDM2wSNxEzNzEzW}`

I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack > >( /challenge/planet ) 2> >( /challenge/the )
Congratulations, you have learned a redirection technique that even experts
struggle with! Here is your flag:
pwn.college{8n6uTxh03EJ4X7L6pTx03pq5Fot.QXxQDM2wSNxEzNzEzW}
```

## What i learned
Used output process substitution >(...) to hook the command’s stdout into /challenge/planet and its stderr (via 2>) into /challenge/the, keeping the streams separate.


# named pipes 
this challenge uses making our own named pipes calles `FIFOs`.

## My solution 
**Flag** `pwn.college{oalNRqhy_k1osuhKRkC0Dwtt_r6.01MzMDOxwSNxEzNzEzW}`

I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@piping~named-pipes:~$ cat < /tmp/flag_fifo &
[1] 152
hacker@piping~named-pipes:~$ /challenge/run > /tmp/flag_fifo
You're successfully redirecting /challenge/run to a FIFO at /tmp/flag_fifo!
Bash will now try to open the FIFO for writing, to pass it as the stdout of
/challenge/run. Recall that operations on FIFOs will *block* until both the
read side and the write side is open, so /challenge/run will not actually be
launched until you start reading from the FIFO!
You've correctly redirected /challenge/run's stdout to a FIFO at
/tmp/flag_fifo! Here is your flag:
pwn.college{oalNRqhy_k1osuhKRkC0Dwtt_r6.01MzMDOxwSNxEzNzEzW}
[1]+  Done                    cat < /tmp/flag_fifo
```

## what i learned 
I learned that FIFO's will block any operations on them until both the read side of the pipe and the write side of the pipe are ready.














