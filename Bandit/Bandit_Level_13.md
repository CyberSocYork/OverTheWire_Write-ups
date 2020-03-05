# Bandit Level 13  
In this level we are told we need to login to the next level using an ssh private key  
  
When we look what is inside the home directory we find a private key:  
![546df4b1.png](../src/546df4b1.png)  
  
The basis of the command command to get into the next level is:  
> ssh bandit14@localhost  
  
However if we run this we will be asked for a password so instead we need to find the way to use this private key instead of a password  
  
If we look at the help page of ssh we can see that "-i" allows us to use an identiy file  
  
This makes our command:  
> ssh -i sshkey.private bandit14@localhost  
  
After running this command we are logged into bandit14 we are able cat open the password which is: 4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e  