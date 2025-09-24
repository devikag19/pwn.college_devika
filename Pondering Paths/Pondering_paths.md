# Pondering Paths
The `Pondering Paths` module teaches basics of Linux filesystem paths.It introduces how the Linux filesystem is structured as a tree which contains root /, directories, files.


# The Root 
In this challenge we were required to enter `/pwn` into the command prompt and caputure the flag.On sumbitting the flag, the challenge was completed.

## My Solution
**Flag:** `pwn.college{AAJRm6Gvq9HmNBHQ43k7Bwv5knj.QX4cTO0wSNxEzNzEzW}`

1. I connected the dojo host using the SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
Connected!
```
2. After successfully connecting the shell, I entered `/pwn` into the command prompt and captured the flag which i then pasted onto pwn.college.
```bash
hacker@paths~the-root:~$ /pwn
BOOM!!!
Here is your flag:
pwn.college{AAJRm6Gvq9HmNBHQ43k7Bwv5knj.QX4cTO0wSNxEzNzEzW}
```
## What I learned
-The Linux filesystem is structured like a tree, starting from the root directory /.
-A file or program located directly under / can be run only by specifying its absolute path like /pwn.
-Simply typing pwn doesn't work, because the shell looks for executables in the directories listed in your path, and `/` is not included by default.

## References 
Youtube- (https://youtu.be/b67Jq6IZ3U8?list=PL-ymxv0nOtqqRAz1x90vxNbhmSkeYxHVC)


# Program and absolute paths
The challenge asks us to execute that program using its full absolute path.
We are required to type `/challenge/run` in the command prompt.On sumbitting the flag, the challenge was completed.

## My Solution 
**Flag** `pwn.college{cokQjBHA9_0TaUwQdQzwh0cHr-k.QX1QTN0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
 ```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
 Connected!
 ```
2. Now the shell is connected to dojo. Now on typing `/challenge/run` and clicking on Enter, I get the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.
```bash
hacker@paths~program-and-absolute-paths:~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{cokQjBHA9_0TaUwQdQzwh0cHr-k.QX1QTN0wSNxEzNzEzW}
 ```

## What I Learned
-Absolute paths always start from `/` and describe the exact location of a file in the filesystem.
-To run a program located in a directory like `/challenge/`, we must give its full path `/challenge/run`.
-This means we can execute any program on the system, from anywhere, as long as we know its absolute path.

## References 
Youtube- (https://youtu.be/b67Jq6IZ3U8?list=PL-ymxv0nOtqqRAz1x90vxNbhmSkeYxHVC)


# Position thy self
The  challenge asks you to change your current working directory to `cd` and then run the `/challenge/run` program from that location. On sumbitting the flag, the challenge was completed.

## My Solution 
**Flag** `pwn.college{UKosvB1pwop-W1pXSYoGOWxhbhQ.QX2QTN0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
 ```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
 Connected!
 ```
2. Now the shell is connected to dojo. Now on typing `/challenge/run` and clicking on Enter, I get the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.
```bash
hacker@paths~program-and-absolute-paths:~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{UKosvB1pwop-W1pXSYoGOWxhbhQ.QX2QTN0wSNxEzNzEzW}
```

## What i Learned 
1. Some programs expect to be run from a certain directory so they can find needed files or resources.The current working directory matters for writing commands.

2. i learned how to change the directory using the command `cd /desired/path` and used it to move to a different directory.

**Note**
If we need to check which directory we're currently in, we can type the command `pwd`.

## References
Youtube- (https://youtu.be/b67Jq6IZ3U8?list=PL-ymxv0nOtqqRAz1x90vxNbhmSkeYxHVC)


# Position Elsewhere 
The challenge asks to first check which directory in the filesystem we're currently working in. Then it requires to change the directory using `cd` and print the prompt `/challenge/run`.On sumbitting the flag, the challenge was completed.

## My solution
**Flag** `pwn.college{oAWAL0kmBqHfEKYZ5MRPs3NPCo7.QX3QTN0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
 ```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
 Connected!
 ```
2. Now the shell is connected to dojo. Now on typing `/challenge/run` and clicking on Enter, I get the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.
```bash
hacker@paths~position-elsewhere:/$ pwd
/
hacker@paths~position-elsewhere:/$ cd /usr/share/build-essential
hacker@paths~position-elsewhere:/usr/share/build-essential$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{oAWAL0kmBqHfEKYZ5MRPs3NPCo7.QX3QTN0wSNxEzNzEzW}
```

# What I learned
1. We can check the directory currently working on we can use the `pwd` command. 
2. I changed the directory to `/usr/share/build-essential`.
3. By solving this challenge, I gained practical experience in navigating and executing programs using absolute paths.

## References 
Youtube- (https://youtu.be/b67Jq6IZ3U8?list=PL-ymxv0nOtqqRAz1x90vxNbhmSkeYxHVC)


# Position yet elsewhere 
The challenge required me to change the directory using `cd` to `/usr/share/doc/fontconfig and print the prompt` and then run the command `/challenge/run`.On sumbitting the flag, the challenge was completed.

## My Solution 
**Flag** `pwn.college{Qq6J2_OdZ2HM1oWAOnfaHD3TxDC.QX4QTN0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
 ```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
 Connected!
 ```
2. Now the shell is connected to dojo. Now on typing `/challenge/run` and clicking on Enter, I get the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.
```bash
hacker@paths~position-yet-elsewhere:/usr/bin$ cd /usr/share/doc/fontconfig
hacker@paths~position-yet-elsewhere:/usr/share/doc/fontconfig$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{Qq6J2_OdZ2HM1oWAOnfaHD3TxDC.QX4QTN0wSNxEzNzEzW}
```

## What I learned 
1. We can check the directory currently working on we can use the `pwd` command. 
2. I changed the directory to `/usr/share/doc/fontconfig`.
3. By solving this challenge, I gained practical experience in navigating and executing programs using absolute paths.

## References
Youtube- (https://youtu.be/b67Jq6IZ3U8?list=PL-ymxv0nOtqqRAz1x90vxNbhmSkeYxHVC)


# Implicit relative paths, from /
In this challenge instead of running the program with its full absolute path (/challenge/run) we used a relative path from /. The directory was changed and then we run the command `challenge/run`. On sumbitting the flag, challenge was completed.

## My Solution
**Flag** `pwn.college{UXypLXCi9-Fo4u-P6frKh_7P9vR.QX5QTN0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
 ```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
 Connected!
 ```
2. Now the shell is connected to dojo. Now on typing `challenge/run` and clicking on Enter, I get the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.
```bash
hacker@paths~implicit-relative-paths-from-:/$ cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{UXypLXCi9-Fo4u-P6frKh_7P9vR.QX5QTN0wSNxEzNzEzW}
```

## What i learned 
1. A relative path is any path that does not start at root means it does not start with `/`.
The current working directory does matter for relative paths.
A relative path is interpreted relative to the current working directory (cwd). The cwd is the directory that the prompt is currently located at.
which means that how we specify a particular file, depends on where the terminal prompt is located.

2. The difference between Relative vs Absolute-
When your current working directory is the `/`, the relative path `challenge/run` points to the same file as the absolute path `/challenge/run`.

## References
Youtube- (https://youtu.be/b67Jq6IZ3U8?list=PL-ymxv0nOtqqRAz1x90vxNbhmSkeYxHVC)


# Emplicit relative paths, from /
This challenge asks to invoke the `./challenge/run` comamnd to retrieve the flag. On sumbitting the flag, the challenge was completed.

## My Solution
**Flag** `pwn.college{oNRqzvRbU-3i187JANo9ozJ1nOy.QXwUTN0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
 ```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
 Connected!
 ```
2. Now the shell is connected to dojo. Now on typing `./challenge/run` and clicking on Enter, I get the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.
```bash
hacker@paths~explicit-relative-paths-from-:~$ cd /
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{oNRqzvRbU-3i187JANo9ozJ1nOy.QXwUTN0wSNxEzNzEzW}
```

## What i Learned
1. `.` refers to the current directory. Writing `./challenge/run` makes it clear that the program is in the current directory.

2. `challenge/run` is implicit relative path the shell assumes it means to 'start here'.
`./challenge/run` is explicit relative path the shell is told exactly where to start.
 
3. It is important to specify `./` because many shells don't run programs in the current directory unless we specify otherwise.

## References
Youtube- (https://youtu.be/b67Jq6IZ3U8?list=PL-ymxv0nOtqqRAz1x90vxNbhmSkeYxHVC)


# Implicit Relative Path 
This challenge required us to print `./run` command in the prompt to collect the flag.On sumbitting the flag, challenge was completed.

## My solution
**Flag** `pwn.college{8SOWTeQJfxGd4izd17SOpeb1W3V.QXxUTN0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
 ```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
 Connected!
 ```
2. Now the shell is connected to dojo. Now on typing `./run` and clicking on Enter, I get the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.
```bash
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{8SOWTeQJfxGd4izd17SOpeb1W3V.QXxUTN0wSNxEzNzEzW}
```

## What i learned 
1. We don't always need `./` to run something in a subdirectory.
2. The implicit relative paths lets us run programs by just naming their path from the current directory, without needing to prefix `./`.

## References
Youtube- (https://youtu.be/b67Jq6IZ3U8?list=PL-ymxv0nOtqqRAz1x90vxNbhmSkeYxHVC)


# Home sweet home 
This challenge required us to write a copy of the flag to the file we specify as an argument on the commandline using `~/f` to capture the flag.On sumbitting the flag, challenge was completed.

## My solution
**Flag** `pwn.college{wAKt0hxSWJXPfUZkn2HOdZ-gN1b.QXzMDO0wSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
 ```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
 Connected!
 ```
2. Now the shell is connected to dojo. Now on typing `cat ~/f` and clicking on Enter, I get the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.
```bash
hacker@paths~home-sweet-home:~$ /challenge/run ~/f
Writing the file to /home/hacker/f!
... and reading it back to you:
pwn.college{wAKt0hxSWJXPfUZkn2HOdZ-gN1b.QXzMDO0wSNxEzNzEzW}
hacker@paths~home-sweet-home:~$ cat ~/f
pwn.college{wAKt0hxSWJXPfUZkn2HOdZ-gN1b.QXzMDO0wSNxEzNzEzW}
```

## What i learned 
1. Every user in Linux has a home directory .`~` is a shortcut that always expands to the home directory. When a shell is opened, it usually begins in the home directory by default.

2. The expansion of `~` is an absolute path, and only the leading `~` is expanded. 

## References
Youtube- (https://youtu.be/b67Jq6IZ3U8?list=PL-ymxv0nOtqqRAz1x90vxNbhmSkeYxHVC)


