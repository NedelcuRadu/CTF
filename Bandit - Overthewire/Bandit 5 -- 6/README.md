
# Bandit 5 -> 6
> SSH Info: ssh -p2220 bandit5@bandit.labs.overthewire.org  
> Password: koReBOKuIDDepwhWk7jZC0RTdopnAYKh


 ## Level Goal  
>The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:
-human-readable
-1033 bytes in size
-not executable

As before, we will [`cd`](https://en.wikipedia.org/wiki/Cd_(command)) into the hidden inhere directory and then search for the file with the specified proprieties using [`find`](https://en.wikipedia.org/wiki/Find_(Unix))
```
bandit5@bandit:~/inhere$ ls -la
total 88
drwxr-x--- 22 root bandit5 4096 Oct 16 14:00 .
drwxr-xr-x  3 root root    4096 Oct 16 14:00 ..
drwxr-x---  2 root bandit5 4096 Oct 16 14:00 maybehere00
drwxr-x---  2 root bandit5 4096 Oct 16 14:00 maybehere01
drwxr-x---  2 root bandit5 4096 Oct 16 14:00 maybehere02
drwxr-x---  2 root bandit5 4096 Oct 16 14:00 maybehere03
drwxr-x---  2 root bandit5 4096 Oct 16 14:00 maybehere04
drwxr-x---  2 root bandit5 4096 Oct 16 14:00 maybehere05
drwxr-x---  2 root bandit5 4096 Oct 16 14:00 maybehere06
drwxr-x---  2 root bandit5 4096 Oct 16 14:00 maybehere07
drwxr-x---  2 root bandit5 4096 Oct 16 14:00 maybehere08
drwxr-x---  2 root bandit5 4096 Oct 16 14:00 maybehere09
drwxr-x---  2 root bandit5 4096 Oct 16 14:00 maybehere10
drwxr-x---  2 root bandit5 4096 Oct 16 14:00 maybehere11
drwxr-x---  2 root bandit5 4096 Oct 16 14:00 maybehere12
drwxr-x---  2 root bandit5 4096 Oct 16 14:00 maybehere13
drwxr-x---  2 root bandit5 4096 Oct 16 14:00 maybehere14
drwxr-x---  2 root bandit5 4096 Oct 16 14:00 maybehere15
drwxr-x---  2 root bandit5 4096 Oct 16 14:00 maybehere16
drwxr-x---  2 root bandit5 4096 Oct 16 14:00 maybehere17
drwxr-x---  2 root bandit5 4096 Oct 16 14:00 maybehere18
drwxr-x---  2 root bandit5 4096 Oct 16 14:00 maybehere19
bandit5@bandit:~/inhere$ find -readable -size 1033c
./maybehere07/.file2
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
DXjZPULLxYr17uwoI01bNLQbtFemEgo7
                                       
```


**Password:** DXjZPULLxYr17uwoI01bNLQbtFemEgo7


[Next Level](https://github.com/ShumaherK/Bandit-Writeups/blob/master/Bandit%206%20--%207/README.md)
