## Level 7 -> Level 8 solution

In this problem we have to find the password for the next level inside
a huge file called data.txt.
The only info we have is the fact that our password is next to the word 'millionth'.
Again grep is our friend here:
`grep 'millionth' ./data.txt`
We should get the following line:
`millionth       cvX2JJa4CFALtqS87jk27qwqGhBM9plV`
