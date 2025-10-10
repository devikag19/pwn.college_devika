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
**Flag:** `pwn.college{YBwxcAtUKV0WKxUM_nKUmyiEmhP.0lN4IDOxwSNxEzNzEzW}`

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
The process of obtaining the flag involves finding an existing GNU Screen session.

## My solve 
**Flag:** `pwn.college{cugr2vetLIepnijMUUU9y0jFWMp.01N4IDOxwSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@terminal-multiplexing~finding-sessions:~$ screen -ls
There are screens on:
        176.pts-1.terminal-multiplexing~launching-screen  (Remote or dead)
        187.pts-1.terminal-multiplexing~launching-screen  (Remote or dead)
        154.pts-1.terminal-multiplexing~detaching-and-attaching    (Remote or dead)
        175.pts-1.terminal-multiplexing~detaching-and-attaching    (Remote or dead)
        144.session_532009095cf81f01    (Remote or dead)
        147.session_42b34cd29f0b75a5    (Remote or dead)
        150.session_aef8260f6dc0c463    (Remote or dead)
        188.pts-2.terminal-multiplexing~switching-windows (Remote or dead)
        199.pts-2.terminal-multiplexing~switching-windows (Remote or dead)
        136.challenge_session   (Remote or dead)
        135.challenge_session   (Remote or dead)
        144.session_0793b48ab468a1b3    (Remote or dead)
        146.session_b0ed8c0d04077e36    (Remote or dead)
        150.session_e2c327a7c53591e4    (Remote or dead)
        144.session_3aa12fc12bd461b3    (Remote or dead)
        147.session_104e3aba5c85d2e8    (Remote or dead)
        150.session_2523242995c7bd9e    (Remote or dead)
        115.-proc-self-fd-0.destruction~the-fork-bomb   (Remote or dead)
        144.session_ce202213d495874d    (Detached)
        147.session_a43d039c5622b447    (Detached)
        150.session_73c9df3b26c8da7c    (Detached)
21 Sockets in /home/hacker/.screen.
hacker@terminal-multiplexing~finding-sessions:~$ screen -r session_ce202213d495874d
[detached from 144.session_ce202213d495874d]
hacker@terminal-multiplexing~finding-sessions:~$ screen -r session_a43d039c5622b447
hacker@terminal-multiplexing~finding-sessions:~$  echo 'Congratulations! You found the right session!'
Congratulations! You found the right session!
hacker@terminal-multiplexing~finding-sessions:~$  echo pwn.college{cugr2vetLIepnijMUUU9y0jFWMp.01N4IDOxwSNxEzNzEzW}
pwn.college{cugr2vetLIepnijMUUU9y0jFWMp.01N4IDOxwSNxEzNzEzW}
```

## What i learned 
I learnt to list active screen sessions with `screen -ls` and to reattach to a specific session with screen -r <id>


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
