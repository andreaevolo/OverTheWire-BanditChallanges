## Level 5 -> Level 6 solution

In this challenge we have to find a file inside the inhere directory.
The problem is... we don't his name!
Don't worry we still have some info about the file we are looking for, his size and the fact that is not an executable.
We use the find command to help us.
```console
bandit5@bandit:~$ find . -size 1033c
./maybehere07/.file2
```
With the -size option 1033c we have specified that we a looking for a file which weight 1033 bytes.
