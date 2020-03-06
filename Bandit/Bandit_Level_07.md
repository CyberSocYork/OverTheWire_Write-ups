# Bandit Level 7

In this level the password is stored in the file `data.txt` next to the word millionth

In this we can use the command `grep`
grep is a command used for searching plaintext data for lines that match a regular expression
The syntax of this command is:
> `grep \\<pattern> \\<file>`

In our case the word we want to look for is millionth so we can use the command:
> `grep "millionth" data.txt`

After we run this command we get the output
![221d9eee.png](../src/221d9eee.png)

Giving us the password: `cvX2JJa4CFALtqS87jk27qwqGhBM9plV`