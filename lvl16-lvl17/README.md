#Level 16 -> Level 17 solution

In this level we can retrive our new password by submitting the current level password to a port in the range 31000 to 32000.
To find out which port has a server listening on it we use `nmap` a port scanning tool, with the `-p` flag to specify a range of ports to scan.


```console
bandit16@bandit:~$ nmap -p 31000-32000 localhost

Starting Nmap 7.40 ( https://nmap.org ) at 2022-06-18 16:28 CEST
Nmap scan report for localhost (127.0.0.1)
Host is up (0.00029s latency).
Not shown: 996 closed ports
PORT      STATE    SERVICE
31046/tcp open     unknown
31518/tcp filtered unknown
31691/tcp open     unknown
31790/tcp open     unknown
31960/tcp open     unknown
```
To find out which server speaks SSL try to connect to the server as we did in the previous challenge.
When you find the correct server simply enter the current level password and you'll get a private RSA key to pass to the next level.

