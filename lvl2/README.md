## Level 2 solution

First of all let's locate the - file.
After that you could try to use:
```
cat -
```
But as you can see nothing will be printed to the console.
Since the - as an argument refers to the redirection operator from/to stdin or stdout, you will need to specify the full path 
to the file:
```console
cat ./-
```
Or take the stdin content and use it as an input for the cat command:
```console
cat < -
```
Your password should be printed to the console.
