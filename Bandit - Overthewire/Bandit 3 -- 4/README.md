
# Bandit 3 -> 4
> SSH Info: ssh -p2220 bandit3@bandit.labs.overthewire.org  
> Password: UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK

 ## Level Goal  
>The password for the next level is stored in a hidden file in the inhere directory.

We will use the [`cd`](https://en.wikipedia.org/wiki/Cd_(command)) in order to change the directory then get our flag.  
(Make sure u use the -la option when checking for files in order to see the hidden ones too)

```
bandit3@bandit:~$ ls -la
total 24
drwxr-xr-x  3 root root 4096 Oct 16 14:00 .
drwxr-xr-x 41 root root 4096 Oct 16 14:00 ..
-rw-r--r--  1 root root  220 May 15  2017 .bash_logout
-rw-r--r--  1 root root 3526 May 15  2017 .bashrc
drwxr-xr-x  2 root root 4096 Oct 16 14:00 inhere
-rw-r--r--  1 root root  675 May 15  2017 .profile
bandit3@bandit:~$ cd inhere
bandit3@bandit:~/inhere$ ls -la
total 12
drwxr-xr-x 2 root    root    4096 Oct 16 14:00 .
drwxr-xr-x 3 root    root    4096 Oct 16 14:00 ..
-rw-r----- 1 bandit4 bandit3   33 Oct 16 14:00 .hidden
bandit3@bandit:~/inhere$ cat .hidden
pIwrPrtPN36QITSp3EQaw936yaFoFgAB
bandit3@bandit:~/inhere$ 

```


**Password:** pIwrPrtPN36QITSp3EQaw936yaFoFgAB



[Next Level](../Bandit%204%20--%205/README.md)
