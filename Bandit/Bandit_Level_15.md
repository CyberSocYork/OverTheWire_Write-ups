# Bandit Level 15  
  
In this level we need to submit the password of the current level to localhost on port 30001 using ssl  
  
To connect we can use the command openssl  
  
This command with the s_client option can be used to connect to our server  
  
"-host" can be used to specify the host being localhost  
"-port" can be used to specify the port being 30001  
  
This makes our final command:  
> openssl s_client -host localhost -port 30001 -ign_eof  
  
Once we run this command we are given a text prompt on which when given the password for the current level we get the password: cluFn7wTiGryunymYOu4RcffSxQluehd  