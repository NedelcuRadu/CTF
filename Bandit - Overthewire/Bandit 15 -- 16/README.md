
# Bandit 15 -> 16
> SSH Info: ssh -p2220 bandit15@bandit.labs.overthewire.org  
> Password: BfMYroe26WYalil77FoDi9qh59eK5xNr


 ## Level Goal  
>The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL encryption.

Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…

Pretty straightforward level, we use [`openssl`](https://www.openssl.org/docs/man1.0.2/apps/openssl.html) in order to complete our task.
(`-quiet` or `-ign_eof` MUST be before `-connect`)
```
bandit15@bandit:~$ openssl s_client -quiet -connect localhost:30001
depth=0 CN = localhost
verify error:num=18:self signed certificate
verify return:1
depth=0 CN = localhost
verify return:1
BfMYroe26WYalil77FoDi9qh59eK5xNr
Correct!
cluFn7wTiGryunymYOu4RcffSxQluehd

bandit15@bandit:~$ 

```


**Password:** cluFn7wTiGryunymYOu4RcffSxQluehd


[Next Level](https://github.com/ShumaherK/Bandit-Writeups/blob/master/Bandit%2016%20--%2017/README.md)
