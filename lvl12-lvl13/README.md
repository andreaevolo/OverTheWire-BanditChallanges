## Level 12 -> Level 13 solutiin

This challenge is a little bit trickier than the previous ones. We have to find our password
inside a hexdump of a file which has been repeatdly compressed.
The tools we'll use the `cp`, `file`, `strings`, `xxd`, `gzip`, `bzip2` and `tar` commands. 

First thing we'll copy or file in the tmp directory:
```console
bandit12@bandit:~$ cp data.txt /tmp/mydir/data.txt
```
let's navigate to our tmp dir:
```console
bandit12@bandit:/tmp/mydir:$
```
After that we have to convert the hexdump of the file to binary, we can do it with the `xxd`
command:
```console
bandit12@bandit:/tmp/mydir:$ xxd -r data.txt > binary
```
The -r flag is used to convert an hexdump into binary.
Now we can use the `file` command to find out some info about our file. Like the compression
algorithm used.
For example:
```console
bandit12@bandit:/tmp/mydir:$ file binary
binary: POSIX tar archive (GNU)
```
When we have found which compression alghortithm is used we can use on of `gzip`, `bzip2`, `tar` commands to decompress it.

After each decompression we try to use the `strings` command to read the binary.
```console
bandit12@bandit:/tmp/mydir:$ strings mybanary
```
After many decompression we should be able to find the original binary of our file and get the password.

