# Bandit Level 30  
  
This is another git level so we clone in the same way as in previous  
  
This time when we open the README we get:  
![27727d44.png](../src/27727d44.png)  
  
and when looking at the log we get:  
![f713b1d9.png](../src/f713b1d9.png)  
  
This clearly tells me that we are looking for something else  
  
After an explore in the .git directory I stubmble apon the packedrefs file  
  
This contains refs in our repo and when opened we see two refs:  
![42fb5c7b.png](../src/42fb5c7b.png)  
  
Here we have a ref called secret that is a tag  
  
If we now run the git command:  
> git tag  
  
We see that we get a single tag called "secret" output  
  
I can now show this tag using the command:  
> git show secret  
  
Which outputs our password which is: 47e603bb428404d265f59c42920d81e5  