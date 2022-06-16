## Level 11 -> Level 12 solution
This challenge require us to use a very simple encryption alghorithm called ROT13.
Basically we have substitute each letter with the letter 13 places further in the alphabet.
Check this [link](https://en.wikipedia.org/wiki/ROT13) for further explanation.
To help us we will us the `tr` command. use `man tr` or `tr --help` for further information.
We use this snippet to solve our challenge:
```console
bandit11@bandit:~$ cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
The password is 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu
```
Let's explaine what it does. We'll focus on the second part of the statment:

`tr 'A-Za-z' 'N-ZA-Mn-za-m'`
We are instructing the tr command to substitue the first group of characters with the second group.
