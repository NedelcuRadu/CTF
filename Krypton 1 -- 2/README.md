
# Krypton 1 -> 2
> SSH Info: ssh -p 2222 krypton1@krypton.labs.overthewire.org  
> Password: KRYPTONISGREAT


 ## Level Info
>The password for level 2 is in the file ‘krypton2’. It is ‘encrypted’ using a simple rotation. It is also in non-standard ciphertext format. When using alpha characters for cipher text it is normal to group the letters into 5 letter clusters, regardless of word boundaries. This helps obfuscate any patterns. This file has kept the plain text word boundaries and carried them to the cipher text. Enjoy!

When we check the krypton2 file we get the following ciphertext:
```
krypton1@krypton:/krypton/krypton1$ cat krypton2 
YRIRY GJB CNFFJBEQ EBGGRA
```
Indeed it looks rotated so let's use [`this`](https://www.dcode.fr/caesar-cipher) to crack the Caesar code.


<a href="https://ibb.co/C2zccwm"><img src="https://i.ibb.co/k1x77G5/Krypton1.png" alt="Krypton1" border="0" /></a>

The first result looks like garbage, however the second one is clear plaintext and tells us the password.

**Password:** ROTTEN


[Next Level](https://github.com/ShumaherK/Krypton/tree/master/Krypton%202%20--%203)
