
# Bandit 8 -> 9
> SSH Info: ssh -p2220 bandit8@bandit.labs.overthewire.org  
> Password: cvX2JJa4CFALtqS87jk27qwqGhBM9plV


 ## Level Goal  
>The password for the next level is stored in the file data.txt and is the only line of text that occurs only once


Again, we can try to simply [`cat`](https://en.wikipedia.org/wiki/Cat_(Unix)) the data.txt file, but it would be impossible to compare every line by hand. Instead, we will use a combination of a [`pipe`](http://www.linfo.org/pipes.html), the [`cat`](https://en.wikipedia.org/wiki/Cat_(Unix)) command, the [`uniq`](https://www.computerhope.com/unix/uuniq.htm) command and [`sort`](https://en.wikipedia.org/wiki/Sort_(Unix))
>Note: We need to use [`sort`](https://en.wikipedia.org/wiki/Sort_(Unix)) because [`uniq`](https://www.computerhope.com/unix/uuniq.htm) compares adjacent lines.

```
bandit8@bandit:~$ ls -la
total 56
drwxr-xr-x  2 root    root     4096 Oct 16 14:00 .
drwxr-xr-x 41 root    root     4096 Oct 16 14:00 ..
-rw-r--r--  1 root    root      220 May 15  2017 .bash_logout
-rw-r--r--  1 root    root     3526 May 15  2017 .bashrc
-rw-r-----  1 bandit9 bandit8 33033 Oct 16 14:00 data.txt
-rw-r--r--  1 root    root      675 May 15  2017 .profile
bandit8@bandit:~$ cat data.txt | sort | uniq -u
UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR
bandit8@bandit:~$ 

```


**Password:** UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR


[Next Level](../Bandit%209%20--%2010/README.md)
