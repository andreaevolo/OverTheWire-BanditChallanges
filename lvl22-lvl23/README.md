## Level 22 -> Level 23 solution

Repeate the steps from the previous level.
Let's see what's inside the cronjob this time:
```console
bandit22@bandit:/usr/bin$ cat cronjob_bandit23.sh
#!/bin/bash

myname=$(whoami)
mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)

echo "Copying passwordfile /etc/bandit_pass/$myname to /tmp/$mytarget"

cat /etc/bandit_pass/$myname > /tmp/$mytarget
```

the variable whoami gets assigned to the user who is execting the script:

bandit22@bandit:/usr/bin$ cronjob_bandit23.sh
Copying passwordfile /etc/bandit_pass/bandit22 to /tmp/8169b67bd894ddbb4412f91573b38db3

The line `(echo I am user $myname | md5sum | cut -d ' ' -f 1` generate a token from the md5sum hash function based on the name that is provided.
If we pass the name bandit23 to the variable myname we should get the token for the next level:
```console
bandit22@bandit:/usr/bin$ myname=bandit23
bandit22@bandit:/usr/bin$ echo I am user $myname | md5sum | cut -d ' ' -f 1
8ca319486bfbbc3663ea0fbe81326349
```
And now we can simply do this:
```console
bandit22@bandit:/usr/bin$ cat /tmp/8ca319486bfbbc3663ea0fbe81326349
jc1udXuA1tiHqjIsL8yaapX5XIAI6i0n
```
We can pass to the next level.
