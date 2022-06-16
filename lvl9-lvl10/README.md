## Level 9 -> Level 10 solution

We know that our password is preceded by several '=' characters.
To solve this problem we'll use the strings command to get the printable characters from data.txt file, after that we will pipe the grep command and use a BRE expression to match the lines containg one or more '=' charcaters.

`bandit9@bandit:~$ strings data.txt | grep '=\+'`
We should get the following output:
```console
========== the*2i"4
=:G e
========== password
<I=zsGi
Z)========== is
A=|t&E
Zdb=
c^ LAh=3G
*SF=s
&========== truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk
```
