## Level 10 -> Level 11 solution
In this challenge our password is stored in base64 encoded file called data.txt
To solve our problem we'll use the base64 command with -d flag to decode our file.
```console
bandit10@bandit:~$ base64 -d data.txt
The password is IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR
```
