## Level 6 -> Level 7 solution
In this challenge we have to locate the password which is stored somewhere unknown on the server.
The only info we have is the file size, the file owner and the group owners.
We'll use again the find command in combination with the grep command to filter out the search result.
First of all let's cd to the root directory:
`bandit6@bandit:$ cd /`
After that we'll run:
    bandit6@bandit:/$ find -size 33c -group bandit6 -user bandit7 2>&1 | grep -v 'Permission denied'
let's break down this statement.
first we use `find -size 33c -group bandit6 -user bandit 7 2>&1` which describe a file of 33 bytes, owned by the group bandit6 and the user bandit 7. The `2>&1` expression basically redirect the stderr and stdout to the same place.
For a detailed explanation [click here](https://www.brianstorti.com/understanding-shell-script-idiom-redirect/).
We use the `|` pipe operator to send the output from the find query to the grep command.
The `grep -v 'Permission denied'` is filtering out all the lines which contain the 'Permission denied' string.
After that we get the following output:

    ./bandit7.password
We have found our password!

