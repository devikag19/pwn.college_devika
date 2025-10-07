# Processes and jobs 

# Listing processes
This challemge uses the list running processes using the `ps` command.

## My solve
**Flag** `pwn.college{E6OL2Wf9VEiNDrxQG-FSUzL7f7p.QX4MDO0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@processes~listing-processes:~$ ps -efww
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 04:54 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-init /run/dojo/bin/sleep 6h
root           7       1  0 04:54 ?        00:00:00 /run/dojo/bin/sleep 6h
root         132       1  0 04:54 ?        00:00:00 /challenge/3300-run-29273
root         135     132  0 04:54 ?        00:00:00 sleep 6h
hacker       137       0  0 04:54 pts/0    00:00:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/bin/bash /run/dojo/bin/ssh-entrypoint
hacker       143     137  0 04:54 pts/0    00:00:00 /run/dojo/bin/bash --login
hacker       156     143  0 04:57 pts/0    00:00:00 ps -efww
hacker@processes~listing-processes:~$ /challenge/3300-run-29273
Yahaha, you found me! Here is your flag:
pwn.college{E6OL2Wf9VEiNDrxQG-FSUzL7f7p.QX4MDO0wSNxEzNzEzW}
Now I will sleep for a while (so that you could find me with 'ps').
```

## What I learned
1. `ps` just lists the processes running in your terminal.
2. Standard Syntax: in this syntax, you can use `e` to list every process and `f` for a full format output, including arguments. These can be combined into a single argument `ef`.

BSD Syntax: we can use a to list processes for all users, `x` to list processes that aren't running in a terminal, and `u` for a user-readable output. These can be combined into a single argument `aux`.


# Killing processes 
This challenges uses the `kill` command to terminate processes.

## My solve
**Flag** `pwn.college{U8awaCxhp0t47PWtcldFNEVeHQD.QXyQDO0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@processes~killing-processes:~$ ps aux | grep /challenge/dont_run
hacker       136  0.0  0.0 231576  3520 ?        Ss   05:12   0:00 /challenge/dont_run
hacker       159  0.0  0.0 230696  2560 pts/0    S+   05:18   0:00 grep --color=auto /challenge/dont_run
hacker@processes~killing-processes:~$ kill 136
hacker@processes~killing-processes:~$ /challenge/run
Great job! Here is your payment:
pwn.college{U8awaCxhp0t47PWtcldFNEVeHQD.QXyQDO0wSNxEzNzEzW}
```

## What i learned 
1. we use the kill to terminate by passing the process identifier "PID from ps" as an argument.


# Interrupting processes 
This challenges uses the `ctrl-C`command to interupt the process.

## My solve
**Flag** `pwn.college{I_dsRdkr3cVGoF6uoakc-ruEgd-.QXzQDO0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@processes~interrupting-processes:~$ /challenge/run
I could give you the flag... but I won't, until this process exits. Remember,
you can force me to exit with Ctrl-C. Try it now!
^C
Good job! You have used Ctrl-C to interrupt this process! Here is your flag:
pwn.college{I_dsRdkr3cVGoF6uoakc-ruEgd-.QXzQDO0wSNxEzNzEzW}
```

## What i learned 
1. pressing the Crtl and C key together interrupts the running application.


# Killing misbehaving processes


# Suspending processes
THis challenge requires suspending processes instead of interupting them.

## My solve
**Flag** `pwn.college{Af0i3lYX738_Imp2mFYF0K37QLS.QX1QDO0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         138     129  0 05:51 pts/0    00:00:00 bash /challenge/run
root         140     138  0 05:51 pts/0    00:00:00 ps -f

I don't see a second me!

To pass this level, you need to suspend me and launch me again! You can
background me with Ctrl-Z or, if you're not ready to do that for whatever
reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         138     129  0 05:51 pts/0    00:00:00 bash /challenge/run
root         145     129  0 05:51 pts/0    00:00:00 bash /challenge/run
root         147     145  0 05:51 pts/0    00:00:00 ps -f

Yay, I found another version of me! Here is the flag:
pwn.college{Af0i3lYX738_Imp2mFYF0K37QLS.QX1QDO0wSNxEzNzEzW}
```

## What i learned
1. The  `crtr+Z` command can be used to suspend an application.


# Resuming processes
This challenges asks us to resume a suspended process.

## My solve
**Flag** `pwn.college{cN5KZwyRNUn1kXO6Bz8dTRTwdXu.QX2QDO0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@processes~resuming-processes:~$ /challenge/run
Let's practice resuming processes! Suspend me with Ctrl-Z, then resume me with
the 'fg' command! Or just press Enter to quit me!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~resuming-processes:~$ fg
/challenge/run
I'm back! Here's your flag:
pwn.college{cN5KZwyRNUn1kXO6Bz8dTRTwdXu.QX2QDO0wSNxEzNzEzW}
Don't forget to press Enter to quit me!

Goodbye!
```

## What i learned 
the `fg` command is used to resume suspended processes.


# Backgrounding processes 
This challenge uses the `bg` command to resume processes in the background.

## My solve
**Flag** `pwn.college{oiko-PjXycL-NxRk8sDiY4mnctN.QX3QDO0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         155 T    bash /challenge/run
root         162 S+   bash /challenge/run
root         164 R+   ps -o user=UID,pid,stat,cmd

I found a second version of me, but it's suspended! Please resume it in the
background with the 'bg' command, then run me again.
hacker@processes~backgrounding-processes:~$ bg
[1]+ /challenge/run &
hacker@processes~backgrounding-processes:~$


Yay, I'm now running the background! Because of that, this text will probably
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times
to scroll this text out.

hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         155 S    bash /challenge/run
root         176 S    sleep 6h
root         177 S+   bash /challenge/run
root         179 R+   ps -o user=UID,pid,stat,cmd

Yay, I found another version of me running in the background! Here is the flag:
pwn.college{oiko-PjXycL-NxRk8sDiY4mnctN.QX3QDO0wSNxEzNzEzW}
```

## What i learned 
1. A `T` means that the process is suspended due to Ctrl-Z. The `S` in bash's STAT column means that bash is sleeping while waiting for input and the `R` in `ps`'s column means that it's actively running, and the `+` means that it's in the foreground.


## Foregrounding processes
This challenge uses the `fg` command more times

## My solve
**Flag** `pwn.college{omtmBaVXocHiYb-iEOhw9HhTPOT.QX4QDO0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@processes~foregrounding-processes:~$ /challenge/run
To pass this level, you need to suspend me, resume the suspended process in the
background, and *then* foreground it without re-suspending it! You can
background me with Ctrl-Z (and resume me in the background with 'bg') or, if
you're not ready to do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~foregrounding-processes:~$ bg
[1]+ /challenge/run &
hacker@processes~foregrounding-processes:~$


Yay, I'm now running the background! Because of that, this text will probably
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times
to scroll this text out. After that, resume me into the foreground with 'fg';
I'll wait.

hacker@processes~foregrounding-processes:~$ fg
/challenge/run
YES! Great job! I'm now running in the foreground. Hit Enter for your flag!

pwn.college{omtmBaVXocHiYb-iEOhw9HhTPOT.QX4QDO0wSNxEzNzEzW}
```

## What i learned 
1. We can foreground a backgrounded process with `fg` just like we foreground a suspended process.


# Starting Background processes
This challenge uses `&` to background processes.

## My solve
**Flag** `pwn.college{0q2siVkhptdglMzjtt7rGh4Ad28.QX5QDO0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@processes~starting-backgrounded-processes:~$ /challenge/run &
[1] 142
hacker@processes~starting-backgrounded-processes:~$


Yay, you started me in the background! Because of that, this text will probably
overlap weirdly with the shell prompt, but you're used to that by now...

Anyways! Here is your flag!
pwn.college{0q2siVkhptdglMzjtt7rGh4Ad28.QX5QDO0wSNxEzNzEzW}
```

## What i learned 
1. We can background processes without suspending them using the `&` command.


# Process exit codes 
This challenge makes us exit codes.

## My solve
**Flag** `pwn.college{Ur-DsxMbC6vYZ5cjfXNemiopuWN.QX5YDO1wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@processes~process-exit-codes:~$ /challenge/get-code
Exiting with an error code!
hacker@processes~process-exit-codes:~$ /challenge/submit-code $?
CORRECT! Here is your flag:
pwn.college{Ur-DsxMbC6vYZ5cjfXNemiopuWN.QX5YDO1wSNxEzNzEzW}
```

## What i learned 
1. Every shell command, including every program and builtin, exits with an exit code when it finishes running and terminates.