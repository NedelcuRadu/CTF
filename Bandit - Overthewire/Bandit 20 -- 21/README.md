
# Bandit 20 -> 21
> SSH Info: ssh -p2220 bandit20@bandit.labs.overthewire.org  
> Password: GbKksEFF4yrVs6il55v6gwY5aVje5f0j


 ## Level Goal  
>There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).  
**NOTE: Try connecting to your own network daemon to see if it works as you think.**

For this level we will need two terminals, one for the port and one for sending the password.
Let's create the listening port first and pipe in the password.

```
bandit20@bandit:~$ echo "GbKksEFF4yrVs6il55v6gwY5aVje5f0j" | nc -l -p 4004
```

Now let's use the binary on our newly-created port from the second terminal.

```
bandit20@bandit:~$ ./suconnect 4004
Read: GbKksEFF4yrVs6il55v6gwY5aVje5f0j
Password matches, sending next password

```
And we got our password on the other terminal.

**Password:** gE269g2h3mw3pwgrj0Ha9Uoqen1c9DGr

We could also just let the port run in the background and use only one connection like this: (notice the `&`)
```
bandit20@bandit:~$ echo "GbKksEFF4yrVs6il55v6gwY5aVje5f0j" | nc -l -p 4004 &
[4] 20650
bandit20@bandit:~$ ./suconnect 4004
Read: GbKksEFF4yrVs6il55v6gwY5aVje5f0j
Password matches, sending next password
gE269g2h3mw3pwgrj0Ha9Uoqen1c9DGr
[4]   Done                    echo "GbKksEFF4yrVs6il55v6gwY5aVje5f0j" | nc -l -p 4004
```

[Next Level](../Bandit%2021%20--%2022/README.md)
