# Bandit Level 21  
  
For this level we are told to look at a program that is running at regular intervals and that liiking in /etc/cron.d could help  
  
Well apon inspection of cron.d we are greeted with 3 useful cronjobs:  
![0ec1d8ef.png](../src/0ec1d8ef.png)  
  
if we look at the contents of  cronjob_bandit22 we see this:  
![463e0a99.png](../src/463e0a99.png)  
  
It is clearly running a program named "/usr/bin/cronjob_bandit22.sh"  
  
After running this command we are given the output:  
![08b9b26f.png](../src/08b9b26f.png)  
  
From this we can see the program is trying to access a file named /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv  
  
If we look at the contents of this file we are greeted with a single string being the password: Yk7owGAcWjwMVRwrTesJEwB7WVOiILLI  
