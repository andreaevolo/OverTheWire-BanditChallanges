## Level 0 solution

Verify that ssh is correctly installed on your machine. Write the following command and press enter:
```console
user@desktop:~$ ssh
usage: ssh [-46AaCfGgKkMNnqsTtVvXxYy] [-B bind_interface]
           [-b bind_address] [-c cipher_spec] [-D [bind_address:]port]
           [-E log_file] [-e escape_char] [-F configfile] [-I pkcs11]
           [-i identity_file] [-J [user@]host[:port]] [-L address]
           [-l login_name] [-m mac_spec] [-O ctl_cmd] [-o option] [-p port]
           [-Q query_option] [-R address] [-S ctl_path] [-W host:port]
           [-w local_tun[:remote_tun]] destination [command]
```
After you have successfully verified that ssh is installed on your machine procede with the login.
Make sure you are connecting to the correct port, you can select the port with the -p flag:
```console
user@desktop:~$ ssh bandit0@bandit.labs.overthewire.org -p 2220
```
After that you will be asked to enter the password.
```console
This is a OverTheWire game server. More information on http://www.overthewire.org/wargames

kali@bandit.labs.overthewire.org's password:
```
Et voilà, if everything went ok you should be connected to the bandit lab!
