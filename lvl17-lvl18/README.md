diff -u passwords.new passwords.old
--- passwords.new       2020-05-07 20:14:35.528729706 +0200
+++ passwords.old       2020-05-07 20:14:35.376729786 +0200
@@ -39,7 +39,7 @@
 sydIUj42mUfYK9xw1S9aPPB72rgagnxh
 pcpkwztEjxg5EK0HABjmEvGUSCSdQW4F
 LlomcOUT6d7lA2cJrYhCEhCChKCPrRao
-kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd
+w0Yfolrc5bwjS4qw5mq1nnQi6mF03bii
 TVzFbgWpqUPE4fwAJPCz4rT7GemAZUjz
 WCETP1i90TZJSbKZ24ly5rhNKva8sSdy
 2o4oJXwgWyWIdKb9WpNDFUcWXlcghSzR## Level 17 -> Level 18 solution

The password for the next level is in password.new and is the only line that has been changed betwen passwords.old and passwords.new .

To help us solve this challenge we'll use the `diff` command, which displays the differences between the contents of files.

We use the `-u` flag to unified output format an improved version of the context format.

```console
diff -u passwords.new passwords.old
--- passwords.new       2020-05-07 20:14:35.528729706 +0200
+++ passwords.old       2020-05-07 20:14:35.376729786 +0200
@@ -39,7 +39,7 @@
 sydIUj42mUfYK9xw1S9aPPB72rgagnxh
 pcpkwztEjxg5EK0HABjmEvGUSCSdQW4F
 LlomcOUT6d7lA2cJrYhCEhCChKCPrRao
-kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd
+w0Yfolrc5bwjS4qw5mq1nnQi6mF03bii
 TVzFbgWpqUPE4fwAJPCz4rT7GemAZUjz
 WCETP1i90TZJSbKZ24ly5rhNKva8sSdy
 2o4oJXwgWyWIdKb9WpNDFUcWXlcghSzR
```
We can notice in our output that some lines are preceded by a `-` and a `+` char, the minus symbol rappresent the lines that have been removed and plus symbol the one that are added.
Given this information we can grab the line that have been remove and use it to access the next level.

