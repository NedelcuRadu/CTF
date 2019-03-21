
# Bandit 23 -> 24
> SSH Info: ssh -p2220 bandit23@bandit.labs.overthewire.org  
> Password: jc1udXuA1tiHqjIsL8yaapX5XIAI6i0n


 ## Level Goal  
>A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.  
**NOTE**: This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!  
**NOTE 2**: Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…

Let's check the cron.d directory and see what is inside for bandit24.

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
bandit22@bandit:/etc/cron.d$ cat cronjob_bandit24
@reboot bandit23 /usr/bin/cronjob_bandit24.sh  &> /dev/null
* * * * * bandit23 /usr/bin/cronjob_bandit24.sh  &> /dev/null
```
Let's try to run the script.


```

```






**Password:** jc1udXuA1tiHqjIsL8yaapX5XIAI6i0n


[Next Level](../Bandit%2024%20--%2025/README.md)
