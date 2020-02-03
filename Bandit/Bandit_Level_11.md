# Bandit Level 11  
  
In this level the password is stored in the file data.txt where all lowercase and uppercase letters have been rotated by 13 positions  
  
When we cat open the file we are greeted with some text that we cannot understand  
This is because the string has been encrypted using a ceasar cipher  
To break this we need to use the tr command which is used for translating characters in strings  
  
The format of this command is:  
> tr [originalString] [NewStrings]  
  
So for us we need to shift both uppercase and lowercase characters  
This makes our original characters 'A-Za-z' as we have A-Z uppercase and a-z lowercase  
Now we want to shift it by 13 so our new letters are 'N-ZA-Mn-za-m' as we are changing the uppercase to N-Z and A-M and the lowercase to n-z and a-m  
This makes our final command  
> cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'  
  
Once this command is run we are greeted with the password being: 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu  
