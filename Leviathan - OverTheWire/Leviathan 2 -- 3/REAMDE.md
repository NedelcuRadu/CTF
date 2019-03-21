# Leviathan 2 -> 3
> SSH Info: ssh -p2223 leviathan2@leviathan.labs.overthewire.org
> Password: ougahZi8Ta

## Level files
```
leviathan2@leviathan:~$ ls -la
total 28
drwxr-xr-x  2 root       root       4096 Oct 29 21:17 .
drwxr-xr-x 10 root       root       4096 Oct 29 21:17 ..
-rw-r--r--  1 root       root        220 May 15  2017 .bash_logout
-rw-r--r--  1 root       root       3526 May 15  2017 .bashrc
-r-sr-x---  1 leviathan3 leviathan2 7436 Oct 29 21:17 printfile
-rw-r--r--  1 root       root        675 May 15  2017 .profile
```

Another setuid binary so let's run it.

```
leviathan2@leviathan:~$ ./printfile 
*** File Printer ***
Usage: ./printfile filename
```

**Password:** ougahZi8Ta


[Next Level](../Bandit%201%20--%202/README.md)
