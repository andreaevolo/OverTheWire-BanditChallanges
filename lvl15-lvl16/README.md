## Level 15 -> Level 16 solution

In this challenge we get introduced to the concept of TSL and openSSL.
As in the previous challenge we have to send the current level password to
port 30001 on localhost, but this time we have to use SSL encryption.

Let's get the current level password:
```console
cd /etc/bandit_pass/
```
```console
cat bandit15
```
Now that we have the password we can connect to localhost.
To use SSL encyption we need to use the `openssl` in combination with s_client which implenet a generic SSL/TLS client which connects to a remote host using SSL/TLS.

```console
openssl s_client -connect localhost:30001
```

After that you can enter the current level password and you'll get the pass for the next level.
