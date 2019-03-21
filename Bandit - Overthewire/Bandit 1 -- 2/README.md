
# Bandit 1 -> 2
> SSH Info: ssh -p2220 bandit1@bandit.labs.overthewire.org  
> Password: boJ9jbbUNNfktd78OOpsqOltutMc3MY1

 ## Level Goal  
>The password for the next level is stored in a file called - located in the home directory


Again, we will read the file using the cat command. As you can see, nothing happens because `-` means standard input. 
In order to bypass this, we will put `./` (relative path) before the file name.

```
bandit1@bandit:~$ ls -la
total 24
-rw-r-----  1 bandit2 bandit1   33 Oct 16 14:00 -
drwxr-xr-x  2 root    root    4096 Oct 16 14:00 .
drwxr-xr-x 41 root    root    4096 Oct 16 14:00 ..
-rw-r--r--  1 root    root     220 May 15  2017 .bash_logout
-rw-r--r--  1 root    root    3526 May 15  2017 .bashrc
-rw-r--r--  1 root    root     675 May 15  2017 .profile
bandit1@bandit:~$ cat -
bandit1@bandit:~$ cat ./-
CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9
bandit1@bandit:~$ 

```

**Password:** CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9



[Next Level](https://github.com/ShumaherK/Bandit-Writeups/blob/master/Bandit%202%20--%203/README.md)
