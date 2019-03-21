
# Bandit 13 -> 14
> SSH Info: ssh -p2220 bandit13@bandit.labs.overthewire.org  
> Password: 8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL



 ## Level Goal  
>The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Note: localhost is a hostname that refers to the machine you are working on





```
bandit13@bandit:~$ ls -la
total 24
drwxr-xr-x  2 root     root     4096 Oct 16 14:00 .
drwxr-xr-x 41 root     root     4096 Oct 16 14:00 ..
-rw-r--r--  1 root     root      220 May 15  2017 .bash_logout
-rw-r--r--  1 root     root     3526 May 15  2017 .bashrc
-rw-r--r--  1 root     root      675 May 15  2017 .profile
-rw-r-----  1 bandit14 bandit13 1679 Oct 16 14:00 sshkey.private
bandit13@bandit:~$ ssh -i sshkey.private bandit14@localhost


```


**Password:** 4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e



[Next Level](../Bandit%2014%20--%2015/README.md)
