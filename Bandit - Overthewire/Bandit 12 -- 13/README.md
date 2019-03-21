
# Bandit 12 -> 13
> SSH Info: ssh -p2220 bandit12@bandit.labs.overthewire.org  
> Password: 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu



 ## Level Goal  
>The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)

This is a really long level. At first we will create a new directory and copy the `data.txt` file so we can tinker with it then we will repeat the following steps:  

1.Check the type of the file. (By using [`file`](https://en.wikipedia.org/wiki/File_(command)) )  
2.Rename it by adding the correct extension. (By using [`mv`](https://www.computerhope.com/unix/umv.htm))  
3.Decompress. (Usually by using the type of compression and `-d` option)


```
bandit12@bandit:~$ mkdir /tmp/aqwsed
bandit12@bandit:~$ cp data.txt /tmp/aqwsed
bandit12@bandit:~$ cd /tmp/aqwsed
bandit12@bandit:/tmp/aqwsed$ ls
data.txt
bandit12@bandit:/tmp/aqwsed$ xxd -r data.txt > bandit
bandit12@bandit:/tmp/aqwsed$ file bandit
bandit: gzip compressed data, was "data2.bin", last modified: Tue Oct 16 12:00:23 2018, max compression, from Unix
bandit12@bandit:/tmp/aqwsed$ mv bandit bandit.gz
bandit12@bandit:/tmp/aqwsed$ gzip -d bandit.gz
bandit12@bandit:/tmp/aqwsed$ file bandit
bandit: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp/aqwsed$ mv bandit bandit.bz
bandit12@bandit:/tmp/aqwsed$ bzip2 -d bandit.bz
bandit12@bandit:/tmp/aqwsed$ file bandit
bandit: gzip compressed data, was "data4.bin", last modified: Tue Oct 16 12:00:23 2018, max compression, from Unix
bandit12@bandit:/tmp/aqwsed$ mv bandit bandit.gz
bandit12@bandit:/tmp/aqwsed$ gzip -d bandit.gz
bandit12@bandit:/tmp/aqwsed$ file bandit
bandit: POSIX tar archive (GNU)
bandit12@bandit:/tmp/aqwsed$ mv bandit bandit.tar
bandit12@bandit:/tmp/aqwsed$ tar xvf bandit.tar
data5.bin
bandit12@bandit:/tmp/aqwsed$ file data5.bin
data5.bin: POSIX tar archive (GNU)
bandit12@bandit:/tmp/aqwsed$ mv data5.bin data5.tar
bandit12@bandit:/tmp/aqwsed$ tar xvf data5.tar
data6.bin
bandit12@bandit:/tmp/aqwsed$ file data6.bin
data6.bin: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp/aqwsed$ mv data6.bin data6.bz
bandit12@bandit:/tmp/aqwsed$ bzip2 -d data6.bz
bandit12@bandit:/tmp/aqwsed$ file data6
data6: POSIX tar archive (GNU)
bandit12@bandit:/tmp/aqwsed$ mv data6 data6.tar
bandit12@bandit:/tmp/aqwsed$ tar xvf data6.tar
data8.bin
bandit12@bandit:/tmp/aqwsed$ file data8.bin
data8.bin: gzip compressed data, was "data9.bin", last modified: Tue Oct 16 12:00:23 2018, max compression, from Unix
bandit12@bandit:/tmp/aqwsed$ mv data8.bin data8.gz
bandit12@bandit:/tmp/aqwsed$ gzip -d data8.gz
bandit12@bandit:/tmp/aqwsed$ file data8
data8: ASCII text
bandit12@bandit:/tmp/aqwsed$ cat data8
The password is 8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL
bandit12@bandit:/tmp/aqwsed$ 



```


**Password:** 8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL


[Next Level](../Bandit%2013%20--%2014/README.md)
