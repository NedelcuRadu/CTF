# Bandit 0 -> 1
> SSH Info: ssh -p2220 bandit0@bandit.labs.overthewire.org  
> Password: bandit0

## Level Goal
>The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

We can check the list of files using [`ls`](https://en.wikipedia.org/wiki/Ls) command and then we will simply read the file using the [`cat`](https://en.wikipedia.org/wiki/Cat_(Unix)) command and then log into the next level.

```
bandit0@bandit:~$ ls -la
total 24
drwxr-xr-x  2 root    root    4096 Oct 16 14:00 .
drwxr-xr-x 41 root    root    4096 Oct 16 14:00 ..
-rw-r--r--  1 root    root     220 May 15  2017 .bash_logout
-rw-r--r--  1 root    root    3526 May 15  2017 .bashrc
-rw-r--r--  1 root    root     675 May 15  2017 .profile
-rw-r-----  1 bandit1 bandit0   33 Oct 16 14:00 readme
bandit0@bandit:~$ cat readme
boJ9jbbUNNfktd78OOpsqOltutMc3MY1
```


**Password:** boJ9jbbUNNfktd78OOpsqOltutMc3MY1


[Next Level](https://github.com/ShumaherK/Bandit-Writeups/blob/master/Bandit%201%20--%202/README.md)
