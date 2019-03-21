# Leviathan 0 -> 1
> SSH Info: ssh -p2223 leviathan0@leviathan.labs.overthewire.org  
> Password: leviathan0

## Level files
```console
leviathan0@leviathan:~$ ls -la
total 24
drwxr-xr-x  3 root       root       4096 Oct 29 21:17 .
drwxr-xr-x 10 root       root       4096 Oct 29 21:17 ..
drwxr-x---  2 leviathan1 leviathan0 4096 Oct 29 21:17 .backup
-rw-r--r--  1 root       root        220 May 15  2017 .bash_logout
-rw-r--r--  1 root       root       3526 May 15  2017 .bashrc
-rw-r--r--  1 root       root        675 May 15  2017 .profile
```

The only thing that seems interesting is the `.backup` directory so let's dig in.

```console
leviathan0@leviathan:~/.backup$ ls -la
total 140
drwxr-x--- 2 leviathan1 leviathan0   4096 Oct 29 21:17 .
drwxr-xr-x 3 root       root         4096 Oct 29 21:17 ..
-rw-r----- 1 leviathan1 leviathan0 133259 Oct 29 21:17 bookmarks.html
```

Let's check for password:

```console
leviathan0@leviathan:~/.backup$ grep password bookmarks.html 
<DT><A HREF="http://leviathan.labs.overthewire.org/passwordus.html | This will be fixed later, the password for leviathan1 is rioGegei8m" ADD_DATE="1155384634" LAST_CHARSET="ISO-8859-1" ID="rdf:#$2wIU71">password to leviathan1</A>
```

**Password:** rioGegei8m


[Next Level](../Leviathan%201%20--%202/README.md)
