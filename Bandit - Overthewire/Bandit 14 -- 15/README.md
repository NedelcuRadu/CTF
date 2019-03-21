
# Bandit 14 -> 15
> SSH Info: ssh -p2220 bandit14@bandit.labs.overthewire.org  
> Password: 4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e


 ## Level Goal  
>The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.

Since we connected to this level, we do not have the password. However, we know that all passwords are stored at /etc/somegame_pass/ so we take a look there.
Then, we use [`nc`](https://en.wikipedia.org/wiki/Netcat) in order to complete our task.

```
bandit14@bandit:/$ cat ./etc/bandit_pass/bandit14
4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e
bandit14@bandit:/$ nc localhost 30000     -> Will read standard input
4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e
Correct!
BfMYroe26WYalil77FoDi9qh59eK5xNr

bandit14@bandit:/$ 

```


**Password:** BfMYroe26WYalil77FoDi9qh59eK5xNr


[Next Level](../Bandit%2015%20--%2016/README.md)
