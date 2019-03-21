
# Bandit 11 -> 12
> SSH Info: ssh -p2220 bandit11@bandit.labs.overthewire.org  
> Password: IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR


 ## Level Goal  
>The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

This type of encryption is called ROT13. In order to decrypt, we can use a regex expression or [`this`](https://www.rot13.com/) site.


```
bandit11@bandit:~$ ls -la
total 24
drwxr-xr-x  2 root     root     4096 Oct 16 14:00 .
drwxr-xr-x 41 root     root     4096 Oct 16 14:00 ..
-rw-r--r--  1 root     root      220 May 15  2017 .bash_logout
-rw-r--r--  1 root     root     3526 May 15  2017 .bashrc
-rw-r-----  1 bandit12 bandit11   49 Oct 16 14:00 data.txt
-rw-r--r--  1 root     root      675 May 15  2017 .profile
bandit11@bandit:~$ cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
The password is 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu
bandit11@bandit:~$ 


```


**Password:** 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu


[Next Level](../Bandit%2012%20--%2013/README.md)
