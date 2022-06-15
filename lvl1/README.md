## Level 1 solution
First step use the cd command to move to the home directory:
```console
bandit0@bandit:~$ cd /home
```
After you successfully moved to the home directory use the ls command to check if there is the readme file:
```console
bandit0@bandit:~$ ls
readme
```
To check the content of the file simply enter the cat [FILE] command
```console
bandit0@bandit:~$ cat readme
```
You should see the password displayed in the console. Copy it and use it to enter the next level using ssh as you did
in challenge 0.
Be sure to disconnect from the server and login again with the new credentials:
```console
user@desktop:~$ ssh bandit1@bandit.labs.overthewire.org -p 2220
```
Enter the the password from the readme file and you can move to lvl2!
