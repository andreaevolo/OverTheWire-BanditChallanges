## Level 3 -> Level 4 solution

First of all let's navigate to the inhere directory using the cd command:
```console
bandit3@bandit: ~$ cd /inhere
```
After that let's use the ls command:
```console
bandit3@bandit: ~$ ls
```
Ummm nothing shows up...
Let's see if there is a useful option to use for showing hidden files with the ls command.
```console
bandit3@bandit: ~$ man ls
```
We should get the following output:
```console
LS(1)                                               User Commands                                               LS(1)

NAME
       ls - list directory contents

SYNOPSIS
       ls [OPTION]... [FILE]...

DESCRIPTION
       List  information  about the FILEs (the current directory by default).  Sort entries alphabetically if none of
       -cftuvSUX nor --sort is specified.

       Mandatory arguments to long options are mandatory for short options too.

       -a, --all
              do not ignore entries starting with .

       -A, --almost-all
```
Looks like the -a option suits or needs!
```console
bandit3@bandit: ~$ ls -a
. .. .hidden
```
perfect, we have found or hidden file, now simply open it and get your password.
