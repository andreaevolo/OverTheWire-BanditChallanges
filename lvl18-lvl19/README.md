## Level 18 -> Level 19 solution

In this challenge we need to find a way to get our password, even if we get automatically disconnected.
Luckily we can execute commands remotely.
We know that our file should be in the home dir, let's check to be sure:

```console
$ ssh bandit18@bandit.labs.overthewire.org -p 2220 ls
This is a OverTheWire game server. More information on http://www.overthewire.org/wargames

bandit18@bandit.labs.overthewire.org's password:
readme
```
Now we can simply use cat to print our new password to the console:
```console
Now we can simply use cat to print the password:

ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme
This is a OverTheWire game server. More information on http://www.overthewire.org/wargames

bandit18@bandit.labs.overthewire.org's password:
IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x
```
