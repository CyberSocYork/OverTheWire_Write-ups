# Bandit Level 10

In this level the password is stored in the file `data.txt` which contains base64 encoded data

When we view the contents of the file we are greeted with this:
![b612b8db.png](../src/b612b8db.png)

To read this file we need to use the command `base64`
This command is used to encode and decode from and to base64

The specific argument we are going to use is `-d` as this is used to decode data from base64 .
This makes our command
> `base64 -d data.txt`

And after running this we get he password as: `IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR`
