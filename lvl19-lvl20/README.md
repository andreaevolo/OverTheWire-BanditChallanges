## Level 19 -> Level 20 solution

In this level we have to take advantage of `setuid` to find the next passaword.

Setuid let us run an executable with the permission of the user who own the file.
If we run the executable we get the following output:

```console
bandit19@bandit:~$ ./bandit20-do
Run a command as another user.
  Example: ./bandit20-do id
```

We can run a command as if we were the user bandit20:

```console
bandit19@bandit:~$ ./bandit20-do cat /etc/bandit_pass/bandit20
GbKksEFF4yrVs6il55v6gwY5aVje5f0j
```
