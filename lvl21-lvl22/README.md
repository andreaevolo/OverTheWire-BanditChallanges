## Level 21 -> Level 22 solution

In this challenge we have to find out which program is running at regular intervals from `cron`,
the time-based job scheduler.
We have an hint, we should investigate `/etc/cron.d` directory and see what command is being executed.

```console
bandit21@bandit:/etc/cron.d$ ls -l
total 24
-rw-r--r-- 1 root root  62 May 14  2020 cronjob_bandit15_root
-rw-r--r-- 1 root root  62 Jul 11  2020 cronjob_bandit17_root
-rw-r--r-- 1 root root 120 May  7  2020 cronjob_bandit22
-rw-r--r-- 1 root root 122 May  7  2020 cronjob_bandit23
-rw-r--r-- 1 root root 120 May 14  2020 cronjob_bandit24
-rw-r--r-- 1 root root  62 May 14  2020 cronjob_bandit25_root
```

We have a list of files, let's try to open them and see whats inside.
In the cronjob_bandit22 we have:
```console
bandit21@bandit:/etc/cron.d$ cat cronjob_bandit22
@reboot bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
* * * * * bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
```
Let's check what's inside /usr/bin/cronjob_bandit22.sh:
```console
bandit21@bandit:/usr/bin$ cat cronjob_bandit22.sh
#!/bin/bash
chmod 644 /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
cat /etc/bandit_pass/bandit22 > /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
```
Let's cat the content of the `/tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv` file:
```console
bandit21@bandit:/usr/bin$ cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
Yk7owGAcWjwMVRwrTesJEwB7WVOiILLI
```
That's it!.
