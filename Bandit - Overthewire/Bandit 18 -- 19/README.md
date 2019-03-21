
# Bandit 18 -> 19
> SSH Info: ssh -p2220 bandit18@bandit.labs.overthewire.org  
> Password: kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd


 ## Level Goal  
>The password for the next level is stored in a file readme in the homedirectory. Unfortunately, someone has modified .bashrc to log you out when you log in with SSH.

When we try to connect we are indeed getting disconnected. However, by reading the [`ssh manpage`](https://linux.die.net/man/1/ssh) we find something interesting:

```
     -T      Disable pseudo-terminal allocation.

     -t      Force pseudo-terminal allocation.  This can be used to execute
             arbitrary screen-based programs on a remote machine, which can be
             very useful, e.g. when implementing menu services.  Multiple -t
             options force tty allocation, even if ssh has no local tty.

     -V      Display the version number and exit.

     -v      Verbose mode.  Causes ssh to print debugging messages about its
             progress.  This is helpful in debugging connection, authentica‐
             tion, and configuration problems.  Multiple -v options increase
             the verbosity.  The maximum is 3.

```
What we want is to use the -T flag:
```
ssh -p2220 -T bandit18@bandit.labs.overthewire.org
```
Looks like we managed to establish a connection, however our shell is pretty limited. Fortunately we do not have much to do:

```
cat readme
IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x
```

And we got our password.

**Password:** IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x


[Next Level](../Bandit%2019%20--%2020/README.md)
