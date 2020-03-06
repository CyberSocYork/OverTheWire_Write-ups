# Bandit Level 8

In this level the password is stored in the file `data.txt` and is the only unique line of text that occours only once

For this we can use the `uniq` command with the argument `-u` and this will return all unique lines in the file

So when we run the command:
> `uniq -u data.txt`

The output isnt as expected:
![fcc45504.png](../src/fcc45504.png)

The reason we aren't getting a single output is that the `uniq` command cannot find duplicate lines if they are not adjacent so we need another command to do this for us
This command is the `sort` command. This will sort the lines and then we can pipe the output of that command into our `uniq -u` command to get the unique line
So once we run the command:
> `sort data.txt | uniq -u`

The output is a signle line giving us the password: `UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR`
