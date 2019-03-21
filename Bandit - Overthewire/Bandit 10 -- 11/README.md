
# Bandit 10 -> 11
> SSH Info: ssh -p2220 bandit10@bandit.labs.overthewire.org  
> Password: truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk


 ## Level Goal  
>The password for the next level is stored in the file data.txt, which contains base64 encoded data

We will use a new command, [`base64`](https://linux.die.net/man/1/base64).


```
bandit10@bandit:~$ ls -la
total 24
drwxr-xr-x  2 root     root     4096 Oct 16 14:00 .
drwxr-xr-x 41 root     root     4096 Oct 16 14:00 ..
-rw-r--r--  1 root     root      220 May 15  2017 .bash_logout
-rw-r--r--  1 root     root     3526 May 15  2017 .bashrc
-rw-r-----  1 bandit11 bandit10   69 Oct 16 14:00 data.txt
-rw-r--r--  1 root     root      675 May 15  2017 .profile
bandit10@bandit:~$ base64 -d data.txt
The password is IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR
bandit10@bandit:~$ 


```


**Password:** IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR


[Next Level](https://github.com/ShumaherK/Bandit-Writeups/blob/master/Bandit%2011%20--%2012/README.md)
