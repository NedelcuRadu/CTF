
# Bandit 22 -> 23
> SSH Info: ssh -p2220 bandit22@bandit.labs.overthewire.org  
> Password: Yk7owGAcWjwMVRwrTesJEwB7WVOiILLI


 ## Level Goal  
>A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.  
**NOTE:** Looking at shell scripts written by other people is a very useful skill. The script for this level is intentionally made easy to read. If you are having problems understanding what it does, try executing it to see the debug information it prints.

Let's check the cron.d directory and see what is inside for bandit23.

```
bandit22@bandit:~$ cd /etc/cron.d
bandit22@bandit:/etc/cron.d$ ls -la
total 24
drwxr-xr-x  2 root root 4096 Oct 16 14:00 .
drwxr-xr-x 88 root root 4096 Oct 16 14:00 ..
-rw-r--r--  1 root root  120 Oct 16 14:00 cronjob_bandit22
-rw-r--r--  1 root root  122 Oct 16 14:00 cronjob_bandit23
-rw-r--r--  1 root root  120 Oct 16 14:00 cronjob_bandit24
-rw-r--r--  1 root root  102 Oct  7  2017 .placeholder
bandit22@bandit:/etc/cron.d$ cat cronjob_bandit23
@reboot bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
* * * * * bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
```
Let's try to run the script.


```
bandit22@bandit:/etc/cron.d$ /usr/bin/cronjob_bandit23.sh
Copying passwordfile /etc/bandit_pass/bandit22 to /tmp/8169b67bd894ddbb4412f91573b38db3
```

Interesting, it sends the password to somewhere we can read it, however we already have the password for bandit22.
Let's see how it works.

```
bandit22@bandit:/etc/cron.d$ cat /usr/bin/cronjob_bandit23.sh
#!/bin/bash

myname=$(whoami)
mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)

echo "Copying passwordfile /etc/bandit_pass/$myname to /tmp/$mytarget"

cat /etc/bandit_pass/$myname > /tmp/$mytarget

```
Now we know how the /tmp/ file path is generated so let's create the one for bandit23. 

```
bandit22@bandit:/etc/cron.d$ $(echo I am user bandit23 | md5sum | cut -d ' ' -f 1)
-bash: 8ca319486bfbbc3663ea0fbe81326349: command not found
bandit22@bandit:/etc/cron.d$ cat /tmp/8ca319486bfbbc3663ea0fbe81326349
jc1udXuA1tiHqjIsL8yaapX5XIAI6i0n
```

**Password:** jc1udXuA1tiHqjIsL8yaapX5XIAI6i0n


[Next Level](https://github.com/ShumaherK/Bandit-Writeups/blob/master/Bandit%2023%20--%2024/README.md)
