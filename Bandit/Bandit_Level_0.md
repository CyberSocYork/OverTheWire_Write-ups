# Bandit Level 0

The goal of this level is to login to the game using ssh.

The standard syntax for ssh is:
> ssh user@domain -p port

so using the username bandit0 and port given 2220 we can log into the server

Once we enter the server we need to see which files are in the folder
To do this we use the ls command which will list all files and directories in the current directory
Once we run the command
> ls

We get output showing us there is a file called readme

We now need to open the file readme
For this we can use the command cat which is short for "concatenation"
This command can be used to open files and so if we use the command:
> cat readme

The command returns the password: boJ9jbbUNNfktd78OOpsqOltutMc3MY1
