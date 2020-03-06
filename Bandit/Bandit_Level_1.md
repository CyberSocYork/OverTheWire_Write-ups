# Bandit Level 1

THe password for the nert file is located in a file called `-` located in the home directory

When first attempting to open the file due to the name being `-` linux interprets this as part of the command and proceeds to just run the usual cat command

To mitigate this use specify that it is a file in this directory by using `./` making the command
> `cat ./-`

This works opening the file successfully giving the password: `CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9`
