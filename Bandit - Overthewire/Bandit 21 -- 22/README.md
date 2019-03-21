
# Bandit 21 -> 22
> SSH Info: ssh -p2220 bandit21@bandit.labs.overthewire.org  
> Password: gE269g2h3mw3pwgrj0Ha9Uoqen1c9DGr


 ## Level Goal  
>A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

Let's check the cron.d directory and see what is inside for bandit22.

```
bandit21@bandit:~$ cd /etc/cron.d
bandit21@bandit:/etc/cron.d$ ls -la
total 24
drwxr-xr-x  2 root root 4096 Oct 16 14:00 .
drwxr-xr-x 88 root root 4096 Oct 16 14:00 ..
-rw-r--r--  1 root root  120 Oct 16 14:00 cronjob_bandit22
-rw-r--r--  1 root root  122 Oct 16 14:00 cronjob_bandit23
-rw-r--r--  1 root root  120 Oct 16 14:00 cronjob_bandit24
-rw-r--r--  1 root root  102 Oct  7  2017 .placeholder
bandit21@bandit:/etc/cron.d$ cat cronjob_bandit22
@reboot bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
* * * * * bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null

```
Looks like it executes a shell script and discard the result. Let's check it


```
bandit21@bandit:/etc/cron.d$ /usr/bin/cronjob_bandit22.sh
chmod: changing permissions of '/tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv': Operation not permitted
/usr/bin/cronjob_bandit22.sh: line 3: /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv: Permission denied
```
That file seems interesting, let's read it.

```
bandit21@bandit:/etc/cron.d$ cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
Yk7owGAcWjwMVRwrTesJEwB7WVOiILLI
```
Looks like our password.

**Password:** Yk7owGAcWjwMVRwrTesJEwB7WVOiILLI


[Next Level](../Bandit%2022%20--%2023/README.md)
