# Bandit Level 18  
  
In this level when we ssh we are booted out immidiatly  
  
This is due to someone modifying he bashrc so that it logs us out on login so we need to find a way to login and ignore the bashrc  
  
One way to do this is to use the "-t" argument which forces a psuedo-terminal  
  
This allows us to use our psuedo terminal to run /bin/sh which is a different kind of shell to allow us to navigate the server  
   
 This makes our command:  
 > ssh -t bandit18@bandit.labs.overthewire.org -p 2220 /bin/sh  
   
 Which after we run we are greeted with  
![e15268ab.png](../src/e15268ab.png)  
  
This shell looks slightly different to bash we were using before however functions almost identically  
  
We can now cat open the file in the root directory to get the password: IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x  