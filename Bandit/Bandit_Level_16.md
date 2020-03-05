# Bandit Level 16  
  
In this level we need to scan a range of ports to tell which of them has a server running on  
This is called port scanning and is a common security technique  
  
The most common tool for this is "nmap" and can be used with the "-p" to specify port ranges with the format  
> nmap -p \\<start_port>-\\<end_port> localhost  
  
This makes our final command:   
> nmap -p 31000-32000 localhost  
  
which apon running returns:  
![d4ff2223.png](../src/d4ff2223.png)  
  
we can now try both of these ports using the same method as we did in level 15 using openssl  
  
Apon testing both the port 31790 is the correct one and when given the correct password we are given a private key:  
![4f0f31cb.png](../src/4f0f31cb.png)  
  
Which we can now use to login to the next level  
