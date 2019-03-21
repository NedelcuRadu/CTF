
# Bandit 19 -> 20
> SSH Info: ssh -p2220 bandit19@bandit.labs.overthewire.org  
> Password: IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x


 ## Level Goal  
>To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.

Let's check that setuid binary and find out how it works.

```
bandit19@bandit:~$ ls -la
total 28
drwxr-xr-x  2 root     root     4096 Oct 16 14:00 .
drwxr-xr-x 41 root     root     4096 Oct 16 14:00 ..
-rwsr-x---  1 bandit20 bandit19 7296 Oct 16 14:00 bandit20-do
-rw-r--r--  1 root     root      220 May 15  2017 .bash_logout
-rw-r--r--  1 root     root     3526 May 15  2017 .bashrc
-rw-r--r--  1 root     root      675 May 15  2017 .profile
bandit19@bandit:~$ ./bandit20-do 
Run a command as another user.
  Example: ./bandit20-do id     
```
Seems like it simply takes a command and executes it as bandit20 so let's try and read the password file.
```
bandit19@bandit:~$ ./bandit20-do cat /etc/bandit_pass/bandit20
GbKksEFF4yrVs6il55v6gwY5aVje5f0j
```
And we got our password.

**Password:** GbKksEFF4yrVs6il55v6gwY5aVje5f0j


[Next Level](../Bandit%2020%20--%2021/README.md)
