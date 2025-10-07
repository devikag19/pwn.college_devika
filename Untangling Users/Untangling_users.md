# Untangling Users 

# Becoming root with su 
This challenge introduces the `root` command. 

## My solve
**Flag** `pwn.college{Uh-3En3ZAIwwGLpKi5FotA-WIR-.QX1UDN1wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@users~becoming-root-with-su:~$ su
Password:
root@users~becoming-root-with-su:/home/hacker# cat /flag
pwn.college{Uh-3En3ZAIwwGLpKi5FotA-WIR-.QX1UDN1wSNxEzNzEzW}
```

## What i learned 
1. There are two utilities that are used with root- su and sudo.
2. Before allowing the user to acess root Linux asks for root password.


# Other users with su 
This challenge explores more of the `su` command.

## My solve
**Flag** `pwn.college{obFLfml-hBk5UDH8XFwLN8tn7hS.QX2UDN1wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@users~other-users-with-su:~$ su zardus
Password:
zardus@users~other-users-with-su:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{obFLfml-hBk5UDH8XFwLN8tn7hS.QX2UDN1wSNxEzNzEzW}
```

## What i learned 
1. We can also give username as an arguement to `su` which switches to that user instead of root.


# Cracking Passwords
This challenge required us to crack the password through.

## My solve
**Flag** `pwn.college{U-b1YDUgmRCloHQFI0pkURLQrZB.QX3UDN1wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@users~cracking-passwords:~$ cat /challenge/shadow-leak
root:*:20182:0:99999:7:::
daemon:*:20182:0:99999:7:::
bin:*:20182:0:99999:7:::
sys:*:20182:0:99999:7:::
sync:*:20182:0:99999:7:::
games:*:20182:0:99999:7:::
man:*:20182:0:99999:7:::
lp:*:20182:0:99999:7:::
mail:*:20182:0:99999:7:::
news:*:20182:0:99999:7:::
uucp:*:20182:0:99999:7:::
proxy:*:20182:0:99999:7:::
www-data:*:20182:0:99999:7:::
backup:*:20182:0:99999:7:::
list:*:20182:0:99999:7:::
irc:*:20182:0:99999:7:::
gnats:*:20182:0:99999:7:::
nobody:*:20182:0:99999:7:::
_apt:*:20182:0:99999:7:::
systemd-timesync:*:20357:0:99999:7:::
systemd-network:*:20357:0:99999:7:::
systemd-resolve:*:20357:0:99999:7:::
mysql:!:20357:0:99999:7:::
messagebus:*:20357:0:99999:7:::
sshd:*:20357:0:99999:7:::
hacker::20357:0:99999:7:::
zardus:$6$XOVHCJ2ENpEIIvIV$Lezq0Uo9JmiOcIpaCHHHu7vEp/RRbQ/HMYypdhzbPM5HG7m2.Mcy/hMtRpoxC6du2xRGYSGrnqzlaBLNbnNkx/:20368:0:99999:7:::
hacker@users~cracking-passwords:~$ cat /challenge/shadow-leak > hash.txt
hacker@users~cracking-passwords:~$ cat hash.txt
root:*:20182:0:99999:7:::
daemon:*:20182:0:99999:7:::
bin:*:20182:0:99999:7:::
sys:*:20182:0:99999:7:::
sync:*:20182:0:99999:7:::
games:*:20182:0:99999:7:::
man:*:20182:0:99999:7:::
lp:*:20182:0:99999:7:::
mail:*:20182:0:99999:7:::
news:*:20182:0:99999:7:::
uucp:*:20182:0:99999:7:::
proxy:*:20182:0:99999:7:::
www-data:*:20182:0:99999:7:::
backup:*:20182:0:99999:7:::
list:*:20182:0:99999:7:::
irc:*:20182:0:99999:7:::
gnats:*:20182:0:99999:7:::
nobody:*:20182:0:99999:7:::
_apt:*:20182:0:99999:7:::
systemd-timesync:*:20357:0:99999:7:::
systemd-network:*:20357:0:99999:7:::
systemd-resolve:*:20357:0:99999:7:::
mysql:!:20357:0:99999:7:::
messagebus:*:20357:0:99999:7:::
sshd:*:20357:0:99999:7:::
hacker::20357:0:99999:7:::
zardus:$6$XOVHCJ2ENpEIIvIV$Lezq0Uo9JmiOcIpaCHHHu7vEp/RRbQ/HMYypdhzbPM5HG7m2.Mcy/hMtRpoxC6du2xRGYSGrnqzlaBLNbnNkx/:20368:0:99999:7:::
hacker@users~cracking-passwords:~$ echo '$6$XOVHCJ2ENpEIIvIV$Lezq0Uo9JmiOcIpaCHHHu7vEp/RRbQ/HMYypdhzbPM5HG7m2.Mcy/hMtRpoxC6du2xRGYSGrnqzlaBLNbnNkx/' > zardus_hash.txt
hacker@users~cracking-passwords:~$ echo '$6$XOVHCJ2ENpEIIvIV$Lezq0Uo9JmiOcIpaCHHHu7vEp/RRbQ/HMYypdhzbPM5HG7m2.Mcy/hMtRpoxC6du2xRGYSGrnqzlaBLNbnNkx/' > hash_local.txt
hacker@users~cracking-passwords:~$ john hash_local.txt
Loaded 1 password hash (crypt, generic crypt(3) [?/64])
Press 'q' or Ctrl-C to abort, almost any other key for status
aardvark         (?)
1g 0:00:00:10 100% 2/3 0.09881g/s 284.5p/s 284.5c/s 284.5C/s Johnson..buzz
Use the "--show" option to display all of the cracked passwords reliably
Session completed
hacker@users~cracking-passwords:~$ john --show hash_local.txt
?:aardvark

1 password hash cracked, 0 left
hacker@users~cracking-passwords:~$ su zardus
Password:
zardus@users~cracking-passwords:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{U-b1YDUgmRCloHQFI0pkURLQrZB.QX3UDN1wSNxEzNzEzW}.
```

## What i learned 
1. i learned how to input,save and then link an ec=xternal file to the Linux prompt.
2. How to crack a password using `su` command. 


# Using sudo
This challenge introduces the `sudo` command.

## My solve
**Flag** `pwn.college{kj76d_cHZaDvKPdVDNx8TYqnlMb.QX4UDN1wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@users~using-sudo:~$ sudo cat /flag
pwn.college{kj76d_cHZaDvKPdVDNx8TYqnlMb.QX4UDN1wSNxEzNzEzW}
```

## What i learned 
1. unlike the `su` command `sudo` checks policies to determine whether the user is authorized to run commands as root.
