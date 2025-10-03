# Data manupulation 

# Translating characters
This challenged used the `tr` command to translate a string

## My solve
**Flag:** `pwn.college{Ul0XhyMLDSg3DPskaGAQsqvTleM.01MxEzNxwSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@data~translating-characters:~$ /challenge/run | tr 'a-zA-Z' 'A-Za-z'
yOUR CASE-SWAPPED FLAG:
pwn.college{Ul0XhyMLDSg3DPskaGAQsqvTleM.01MxEzNxwSNxEzNzEzW}
```

## What I learned
1. `tr` translates the character provided in its first argument to the character provided in its second argument
2.  It translates characters it receives over standard input and prints them to standard output.


# Deleting Characters 
This challenges makes us delete particular parts of a command. 

## My solve
**Flag:** `pwn.college{Ul0XhyMLDSg3DPskaGAQsqvTleM.01MxEzNxwSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@data~deleting-characters:~$ /challenge/run
Your character-stuffed flag:
p^%w^%n^.^c^ol%l^eg^%e^{%Q%0%g^%J%p%B%5%fEScd^%P^%w^61^%W^%oiK^%i^%b^S^%O^%B^%j^%_^.^0%F%N%x%Ez^%N^%x%w%S^N%x^E^z^%Nz^%E%z%W%}^%^%
hacker@data~deleting-characters:~$ /challenge/run | tr -d '^%'
Your character-stuffed flag:
pwn.college{Q0gJpB5fEScdPw61WoiKibSOBj_.0FNxEzNxwSNxEzNzEzW}
```

## What i learned 
1. `tr` also  is used to delete characters. This is done via a `-d` flag and an argument of what characters to delete.


# Deleting newlines
Uses the  `\` character to delete new line chahracters.

## My solve
**Flag** `pwn.college{4O9c0JYgSK39JWM_m7ROwkhD4b1.0VNxEzNxwSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@data~deleting-newlines:~$ /challenge/run | tr -d '\n'
Your line-split flag: pwn.college{4O9c0JYgSK39JWM_m7ROwkhD4b1.0VN
```

## What i learned 
1.  To replace the `\` character, we need to escape it. `\\` will be treated as a backslash `\` by `tr`.


# Extracting the first few lines using head 
This challenge uses the `head` command to display the first few lines of its input.

## My solve
**Flag** `pwn.college{QMrCKyEI-SKF1wdFwAFRqMN6jwG.0lNxEzNxwSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@data~extracting-the-first-lines-with-head:~$ /challenge/pwn | head -n 7 | /challenge/college
Congratulations, you piped the right codes!
pwn.college{QMrCKyEI-SKF1wdFwAFRqMN6jwG.0lNxEzNxwSNxEzNzEzW}
```

## What i learned 
1. By default, linux shows the first 10 lines, but we can control this with the `-n` option.


# extracting spwcific sections of text 
This challenge uses the `cut` command to extract specifci columns of data.

##
## My solve
**Flag** `pwn.college{0AwnUjg7gOCzS-qx0eT42DxGmeR.01NxEzNxwSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run
21751 p
10275 w
17295 n
4517 .
10363 c
14618 o
2241 l
24399 l
29995 e
27640 g
868 e
20369 {
25288 0
18695 A
1072 w
31266 n
105 U
10347 j
17531 g
8263 7
7838 g
14323 O
28442 C
12715 z
22950 S
21805 -
3336 q
4964 x
2726 0
14074 e
30764 T
4811 4
27573 2
16763 D
6220 x
11181 G
28817 m
27158 e
32369 R
12716 .
8109 0
22380 1
30679 N
20654 x
21108 E
18103 z
17881 N
16580 x
12367 w
9298 S
17008 N
20424 x
22314 E
18272 z
5569 N
18034 z
8979 E
26771 z
7336 W
5573 }
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run | cut -d " " -f2 | tr -d '\n'
pwn.college{0AwnUjg7gOCzS-qx0eT42DxGmeR.01NxEzNxwSNxEzNzEzW}
```

## What i learned 
1.  -d argument specifies how columns are separated.
2.  The -f argument specifies which column to extract.


# Sorting data
This challenge uses the `sort` command to sort through the files.

## My solve
**Flag** `pwn.college{4q_-gm98mBig7n3BT8k0yKv3yM_.0FM0MDOxwSNxEzNzEzW}`

1. I connected the dojo host using SSH command.
```bash
root@LAPTOP-IDCKVPOM:~# ssh  -i ./key hacker@dojo.pwn.college
```

2. Now the shell is connected to dojo. Now, I got the flag that I can submit on [pwn.college](https://pwn.college/linux-luminarium/hello/) to complete the challenge.

```bash
hacker@data~sorting-data:~$ cat /challenge/flags.txt | sort | tail -n 1
pwn.college{4q_-gm98mBig7n3BT8k0yKv3yM_.0FM0MDOxwSNxEzNzEzW}
```

## What i learned 
By default, sort orders lines alphabetically. others ways to sort are-

-r: reverse order (Z to A)
-n: numeric sort (for numbers)
-u: unique lines only (remove duplicates)
-R: random order









