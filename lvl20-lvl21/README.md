## Level 20 -> Level 21

For this challenge we have to create a connection to localhost on a port we specify.
The setuid binary in the home dir reads a line of text from the connection and if the password ( we can get the password from the previous level ) matches we'll recive back the correct the next level password.

First of all let's create a simple TCP server:
```console
bandit20@bandit:~$ echo "GbKksEFF4yrVs6il55v6gwY5aVje5f0j" | nc localhost -lp 8000
GbKksEFF4yrVs6il55v6gwY5aVje5f0j
```

After that we can connect to port 8000 with the setuid binary in the home directory:
```console
bandit20@bandit:~$ ./suconnect 8000
Read: GbKksEFF4yrVs6il55v6gwY5aVje5f0j
Password matches, sending next password
bandit20@bandit:~$ gE269g2h3mw3pwgrj0Ha9Uoqen1c9DGr
```
