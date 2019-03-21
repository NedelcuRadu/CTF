
# Bandit 9 -> 10
> SSH Info: ssh -p2220 bandit9@bandit.labs.overthewire.org  
> Password: UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR


 ## Level Goal  
>The password for the next level is stored in the file data.txt in one of the few human-readable strings, beginning with several ‘=’ characters.

We will use something simmilar to the last level, replacing [`cat`](https://en.wikipedia.org/wiki/Cat_(Unix)) with [`strings`](http://www.linfo.org/strings.html).


```
bandit9@bandit:~$ ls -la
total 40
drwxr-xr-x  2 root     root     4096 Oct 16 14:00 .
drwxr-xr-x 41 root     root     4096 Oct 16 14:00 ..
-rw-r--r--  1 root     root      220 May 15  2017 .bash_logout
-rw-r--r--  1 root     root     3526 May 15  2017 .bashrc
-rw-r-----  1 bandit10 bandit9 19379 Oct 16 14:00 data.txt
-rw-r--r--  1 root     root      675 May 15  2017 .profile
bandit9@bandit:~$ strings data.txt | grep =
2========== the
========== password
>t=	yP
rV~dHm=
========== isa
=FQ?P\U
=	F[
pb=x
J;m=
=)$=
========== truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk
iv8!=

```


**Password:** truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk


[Next Level](../Bandit%2010%20--%2011/README.md)
