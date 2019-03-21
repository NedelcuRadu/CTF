
# Bandit 6 -> 7
> SSH Info: ssh -p2220 bandit6@bandit.labs.overthewire.org  
> Password: DXjZPULLxYr17uwoI01bNLQbtFemEgo7


 ## Level Goal  
>TThe password for the next level is stored somewhere on the server and has all of the following properties:
-owned by user bandit7
-owned by group bandit6
-33 bytes in size

We will search for the file with the specified proprieties using [`find`](https://en.wikipedia.org/wiki/Find_(Unix)) (Do not forget the `/`)
Notice that there is one directory that we are able to acces, so we check it.
```
bandit6@bandit:~$ find / -group bandit6 -user bandit7 -size 33c
find: ‘/run/lvm’: Permission denied
find: ‘/run/screen/S-bandit15’: Permission denied
find: ‘/run/screen/S-bandit14’: Permission denied
find: ‘/run/screen/S-bandit9’: Permission denied
find: ‘/run/screen/S-bandit8’: Permission denied
find: ‘/run/screen/S-bandit31’: Permission denied
find: ‘/run/screen/S-bandit30’: Permission denied
find: ‘/run/screen/S-bandit21’: Permission denied
find: ‘/run/screen/S-bandit26’: Permission denied
find: ‘/run/screen/S-bandit3’: Permission denied
find: ‘/run/screen/S-bandit5’: Permission denied
find: ‘/run/screen/S-bandit25’: Permission denied
find: ‘/run/screen/S-bandit4’: Permission denied
find: ‘/run/screen/S-bandit1’: Permission denied
find: ‘/run/screen/S-bandit0’: Permission denied
find: ‘/run/screen/S-bandit13’: Permission denied
find: ‘/run/screen/S-bandit27’: Permission denied
find: ‘/run/screen/S-bandit22’: Permission denied
find: ‘/run/screen/S-bandit12’: Permission denied
find: ‘/run/screen/S-bandit23’: Permission denied
find: ‘/run/screen/S-bandit19’: Permission denied
find: ‘/run/screen/S-bandit16’: Permission denied
find: ‘/run/screen/S-bandit20’: Permission denied
find: ‘/run/screen/S-bandit24’: Permission denied
find: ‘/run/shm’: Permission denied
find: ‘/run/lock/lvm’: Permission denied
find: ‘/var/spool/rsyslog’: Permission denied
find: ‘/var/spool/cron/crontabs’: Permission denied
find: ‘/var/log’: Permission denied
find: ‘/var/tmp’: Permission denied
find: ‘/var/cache/ldconfig’: Permission denied
find: ‘/var/cache/apt/archives/partial’: Permission denied
/var/lib/dpkg/info/bandit7.password
find: ‘/var/lib/apt/lists/partial’: Permission denied
find: ‘/var/lib/polkit-1’: Permission denied
find: ‘/cgroup2/csessions’: Permission denied
find: ‘/home/bandit28-git’: Permission denied
find: ‘/home/bandit30-git’: Permission denied
find: ‘/home/bandit31-git’: Permission denied
find: ‘/home/bandit5/inhere’: Permission denied
find: ‘/home/bandit27-git’: Permission denied
find: ‘/home/bandit29-git’: Permission denied
find: ‘/tmp’: Permission denied
find: ‘/lost+found’: Permission denied
find: ‘/root’: Permission denied
find: ‘/etc/ssl/private’: Permission denied
find: ‘/etc/lvm/backup’: Permission denied
find: ‘/etc/lvm/archive’: Permission denied
find: ‘/etc/polkit-1/localauthority’: Permission denied
find: ‘/sys/fs/pstore’: Permission denied
find: ‘/proc/tty/driver’: Permission denied
find: ‘/proc/21550/task/21550/fd/6’: No such file or directory
find: ‘/proc/21550/task/21550/fdinfo/6’: No such file or directory
find: ‘/proc/21550/fd/5’: No such file or directory
find: ‘/proc/21550/fdinfo/5’: No such file or directory
find: ‘/boot/lost+found’: Permission denied
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs
                            
```


**Password:** HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs


[Next Level](../Bandit%207%20--%208/README.md)
