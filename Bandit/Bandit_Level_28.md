# Bandit Level 28  
  
In this level we are asked to clone a repo again to find the password  
  
We can clone the repo in a similar fashion to the last level however when we look inside the README we are greeted with this:  
![bfe3fdc6.png](../src/bfe3fdc6.png)  
  
Someone has redacted some information from the file  
  
To see all previous versions of the file we can use the command:  
> git log  
  
which once executed returns:  
![3df79b43.png](../src/3df79b43.png)  
  
Here we see there are a bunch of different commits of the file which we could instead look at  
  
I am going to only rollback one commit as the most recent fixed the data leak so I instead wish for my local repo to be at comit 186a1038cc54d1358d42d468cdc8e3cc28a93fcb  
  
To do this I use the command:  
> git checkout 186a1038cc54d1358d42d468cdc8e3cc28a93fcb  
  
To point my repo at that commit  
  
After running the command I view the README file we get:  
![b6012fe1.png](../src/b6012fe1.png)  
  
Giving us the password: bbc96594b4e001778eee9975372716b2  
