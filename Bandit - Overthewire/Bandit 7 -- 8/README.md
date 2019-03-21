
# Bandit 7 -> 8
> SSH Info: ssh -p2220 bandit7@bandit.labs.overthewire.org  
> Password: HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs


 ## Level Goal  
>The password for the next level is stored in the file data.txt next to the word millionth


We can try to [`cat`](https://en.wikipedia.org/wiki/Cat_(Unix)) the data.txt file, but searching for that specific word would take far too much time by hand. Instead, we use the [`grep`](https://en.wikipedia.org/wiki/Grep) command in order to get our flag.

```
bandit7@bandit:~$ ls -la
total 4108
drwxr-xr-x  2 root    root       4096 Oct 16 14:00 .
drwxr-xr-x 41 root    root       4096 Oct 16 14:00 ..
-rw-r--r--  1 root    root        220 May 15  2017 .bash_logout
-rw-r--r--  1 root    root       3526 May 15  2017 .bashrc
-rw-r-----  1 bandit8 bandit7 4184396 Oct 16 14:00 data.txt
-rw-r--r--  1 root    root        675 May 15  2017 .profile
bandit7@bandit:~$ grep millionth data.txt
millionth	cvX2JJa4CFALtqS87jk27qwqGhBM9plV

```


**Password:** cvX2JJa4CFALtqS87jk27qwqGhBM9plV


[Next Level](https://github.com/ShumaherK/Bandit-Writeups/blob/master/Bandit%208%20--%209/README.md)
