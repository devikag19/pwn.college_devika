# Terminal Multiplexing 

# Launching screen
This challenge makes us launch a scree.

## My solve 
**Flag:** `pwn.college{YBwxcAtUKV0WKxUM_nKUmyiEmhP.0lN4IDOxwSNxEzNzEzW}`


1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@terminal-multiplexing~launching-screen:~$ screen



[screen is terminating]
```

## What i learned 
i learned how to launch and exit a screen.


# Detaching and attaching 
This challenge requires us to detach a screen.

## My solve 
**Flag:** ``

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@terminal-multiplexing~detaching-and-attaching:~$ echo Yes! Flag is: pwn.college{YBwxcAtUKV0WKxUM_nKUmyiEmhP.0lN4IDOxwSNxEzNzEzW}
Yes! Flag is: pwn.college{YBwxcAtUKV0WKxUM_nKUmyiEmhP.0lN4IDOxwSNxEzNzEzW}
```

## What i learned 
i learned how to relaunch a screen, detach it.


# finding sessions 


# Switching windows 
This challenge makes us switch bewtween windows. 

## My solve 
**Flag:** ``

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
MSG
Excellent work! You found window 0!
Here is your flag: pwn.college{YXOYhGsNuZByIPwh9FxLJhD-q6T.0FO4IDOxwSNxEzNzEzW}
```

## What i learned 
1. Some commands wit `ctrl-A`
Ctrl-A c - Create a new window
Ctrl-A n - Next window
Ctrl-A p - Previous window
Ctrl-A 0 through Ctrl-A 9 - Jump directly to window 0-9
Ctrl-A " - bring up a selection menu of all of the windows

2. switching between windows.


# Detaching and attaching (tmux)
this challenge uses the `tmux` command.

## My solve 
**Flag:** `pwn.college{QNycJaAYOkXOH2rWLiLrvx6aZOA.0VO4IDOxwSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ tmux
[detached (from session 0)]
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ /challenge/run
Found detached tmux session: 0
Sending flag to your tmux session...

Flag sent! Now reattach to your tmux session with:
  tmux attach

You'll find the flag waiting for you there!
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ tmux attach
[detached (from session 0)]
```

## What i learned 
The `tmux` command does all the same things but with some different key bindings. tmux uses Ctrl-B as its command prefix.


# Switching windows (tmux)
This challenge made us switch windows with `tmux`.

## My solve 
**Flag:** `pwn.college{EhWBKIHkM0L2VCdzxQdiaLWO0sb.0FM5IDOxwSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
 Excellent work! You found window 0!
> Here is your flag: pwn.college{EhWBKIHkM0L2VCdzxQdiaLWO0sb.0FM5IDOxwSNxEzNzEzW}
```

## What i learned 
I learned that windows are swtiched in tmux by using the `crtl-b-0` command to shift to window 0.
