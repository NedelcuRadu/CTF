
# Bandit 4 -> 5
> SSH Info: ssh -p2220 bandit4@bandit.labs.overthewire.org  
> Password: pIwrPrtPN36QITSp3EQaw936yaFoFgAB

 ## Level Goal  
>The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.

We will repeat the steps from the previous level then use [`cat`](https://en.wikipedia.org/wiki/Cat_(Unix)) in order to read all of them.

```
bandit4@bandit:~/inhere$ cat ./*
����������~%	C[�걱>��| ����U"7�w���H��ê�Q��(���#����T�v��(�ִ�����A*�
2J�Ş؇_�y7�.A��u��#���w$N?c�-��Db3��=���=<�W�����ht�Z��!��{�U
 �+��pm���;��:D��^��@�gl�Q��@�%@���ZP*E��1�V���̫*����koReBOKuIDDepwhWk7jZC0RTdopnAYKh
FPn�
    '�U���M��/u
               XS
�mu�z���хN�{��Y�d4�����]3�����9(�
```
There is a bunch of garbage, but we can notice a string that looks like our password.

**Password:** koReBOKuIDDepwhWk7jZC0RTdopnAYKh


[Next Level](../Bandit%205%20--%206/README.md)
