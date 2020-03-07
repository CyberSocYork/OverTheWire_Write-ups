# Bandit Level 9

In this level the password is stored in the file `data.txt` in one of the only human readable strings, beginning with several `=` characters.

Although this file has the extension `.txt`, it is binary data. To extract the password we will use the command `strings`. This goes through a binary file and outputs all printable characters in the file. As most of these are just sequences of symbols, we need to narrow down the search somewhat. We therefore `grep` for `==`.
> `strings data.txt | grep "=="`

Once the command runs we get the output:

![0edcbfab.png](../src/0edcbfab.png)

This reveals the password: `truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk`
