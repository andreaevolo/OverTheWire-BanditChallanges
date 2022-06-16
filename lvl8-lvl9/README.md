## Level 7 -> Level 8 solution

We have to find our password inside data.txt, the only issue is that there a lot of
repeated lines. The line we are searching is unique, for that reason we'll use the uniq command in combination with the sort command.

We cannot use the directly the unique command with the -u flag because uniq will not detect repeated lines unless they are adjacent.

`bandit8@bandit:~$ sort data.txt | uniq -u`
That's it , you have found the only unique line which contains our password.
