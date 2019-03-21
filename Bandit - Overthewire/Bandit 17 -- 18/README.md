
# Bandit 17 -> 18
> SSH Info: ssh -p2220 bandit17@bandit.labs.overthewire.org  
> Password: xLYVMN9WE5zQ5vHacb0sZEVqbrp7nBTn


 ## Level Goal  
>There are 2 files in the homedirectory: passwords.old and passwords.new. The password for the next level is in passwords.new and is the only line that has been changed between passwords.old and passwords.new  
**NOTE: if you have solved this level and see ‘Byebye!’ when trying to log into bandit18, this is related to the next level, bandit19.**

We use [`diff`](https://en.wikipedia.org/wiki/Diff) in order to compare the 2 files.

```
bandit17@bandit:~$ diff passwords.new passwords.old
42c42
< kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd
---
> hlbSBPAWJmL6WFDb06gpTx1pPButblOA
```
And we got our password.

**Password:** kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd


[Next Level](https://github.com/ShumaherK/Bandit-Writeups/blob/master/Bandit%2018%20--%2019/README.md)
