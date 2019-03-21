# Leviathan 1 -> 2
> SSH Info: ssh -p2223 leviathan1@leviathan.labs.overthewire.org  
> Password: rioGegei8m

## Level files
```console
leviathan1@leviathan:~$ ls -la
total 28
drwxr-xr-x  2 root       root       4096 Oct 29 21:17 .
drwxr-xr-x 10 root       root       4096 Oct 29 21:17 ..
-rw-r--r--  1 root       root        220 May 15  2017 .bash_logout
-rw-r--r--  1 root       root       3526 May 15  2017 .bashrc
-r-sr-x---  1 leviathan2 leviathan1 7452 Oct 29 21:17 check
-rw-r--r--  1 root       root        675 May 15  2017 .profile
```

There is a setuid binary so let's try to see how it works.

```console
leviathan1@leviathan:~$ ./check 
password: asd
Wrong password, Good Bye ...
```

We will have to find the password somehow so let's try [`ltrace`](http://man7.org/linux/man-pages/man1/ltrace.1.html).

```console
leviathan1@leviathan:~$ ltrace ./check 
__libc_start_main(0x804853b, 1, 0xffffd784, 0x8048610 <unfinished ...>
printf("password: ")                                                                      = 10
getchar(1, 0, 0x65766f6c, 0x646f6700password: asd
)                                                     = 97
getchar(1, 0, 0x65766f6c, 0x646f6700)                                                     = 115
getchar(1, 0, 0x65766f6c, 0x646f6700)                                                     = 100
strcmp("asd", "sex")                                                                      = -1
puts("Wrong password, Good Bye ..."Wrong password, Good Bye ...
)                                                      = 29
+++ exited (status 0) +++

```

When we enter the password sex we get a shell which can be used to get the password for next level:

```console
leviathan1@leviathan:~$ ./check 
password: sex
$ whoami
leviathan2
$ cat /etc/leviathan_pass/leviathan2
ougahZi8Ta
```

**Password:** ougahZi8Ta


[Next Level](../Leviathan%202%20--%203/README.md)
