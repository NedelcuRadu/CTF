
# Bandit 2 -> 3
> SSH Info: ssh -p2220 bandit2@bandit.labs.overthewire.org  
> Password: CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9

 ## Level Goal  
>The password for the next level is stored in a file called spaces in this filename located in the home directory

**Fastest option:**  
Once again, we will read the file using the cat command, but this time we will press `TAB` after the first word in order to autocomplete the file's name.

*Other options:*   
1.Replace whitespaces with `\`.  
2.Put the name of the file between `"`, as you would do with a string.

```
bandit2@bandit:~$ ls -la
total 24
drwxr-xr-x  2 root    root    4096 Oct 16 14:00 .
drwxr-xr-x 41 root    root    4096 Oct 16 14:00 ..
-rw-r--r--  1 root    root     220 May 15  2017 .bash_logout
-rw-r--r--  1 root    root    3526 May 15  2017 .bashrc
-rw-r--r--  1 root    root     675 May 15  2017 .profile
-rw-r-----  1 bandit3 bandit2   33 Oct 16 14:00 spaces in this filename
bandit2@bandit:~$ cat spaces\ in\ this\ filename 
UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK
```


**Password:** UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK



[Next Level](https://github.com/ShumaherK/Bandit-Writeups/blob/master/Bandit%203%20--%204/README.md)
