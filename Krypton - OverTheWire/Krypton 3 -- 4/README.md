
# Krypton 3 -> 4
> SSH Info: ssh -p 2222 krypton3@krypton.labs.overthewire.org   
> Password: CAESARISEASY


 ## Level Info
>Well done. You’ve moved past an easy substitution cipher.  
The main weakness of a simple substitution cipher is repeated use of a simple key. In the previous exercise you were able to introduce arbitrary plaintext to expose the key. In this example, the cipher mechanism is not available to you, the attacker.  
However, you have been lucky. You have intercepted more than one message. The password to the next level is found in the file ‘krypton4’. You have also found 3 other files. (found1, found2, found3)  
You know the following important details:  
The message plaintexts are in English (*** very important) - They were produced from the same key (*** even better!)  
Enjoy.  

This time the level will not be so easy and we will have to crack the code manually, using [frequency analysis](https://learncryptography.com/attack-vectors/frequency-analysis). I recommend [this](https://crypto.interactive-maths.com/frequency-analysis-breaking-the-code.html#encrypt) tool in order to make things a little easier to track.

Our ciphertexts are:
 * [Found1](./Found%201)
 * [Found2](./Found%202)
 * [Found3](./Found%203)
```

```

Using the same [`tool`](https://www.dcode.fr/caesar-cipher) the level becomes trivial.







**Password:** CAESARISEASY


[Next Level](../Krypton%204%20--%205)
