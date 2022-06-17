## Level 14 -> Level 15 solution

As stated in the description of our problem we need to send the current level password to port 30000 on localhost.

To find the current level password we can read the previous level description and we found the path ` /etc/bandit_pass/bandit14`, we can retrive the password from there.

```console
cat /etc/bandit_pass/bandit14
4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e
```
Now that we have the password we have to find a way to send the password to localhost on port 30000.

For this task we'll use the netcat ( nc abbreviated ) which is an utilty tool to send/read data accross network connections:

```console
bandit14@bandit:~$ nc localhost 30000
4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e
Correct!
BfMYroe26WYalil77FoDi9qh59eK5xNr
```
