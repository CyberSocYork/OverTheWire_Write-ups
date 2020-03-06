# Narnia Level 0  
  
In this level we have a binary narnia0 that runs suid as narnia1 and the source code  
  
THe source code is as follows:  
```c  
#include <stdio.h>  
#include <stdlib.h>  
  
int main(){  
    long val=0x41414141;  
    char buf[20];  
  
    printf("Correct val's value from 0x41414141 -> 0xdeadbeef!\\n");  
    printf("Here is your chance: ");  
    scanf("%24s",&buf);  
  
    printf("buf: %s\\n",buf);  
    printf("val: 0x%08x\\n",val);  
  
    if(val==0xdeadbeef){  
        setreuid(geteuid(),geteuid());  
        system("/bin/sh");  
    }  
    else {  
        printf("WAY OFF!!!!\\n");  
        exit(1);  
    }  
  
    return 0;  
}  
```  
In this challenge we are told to change the value of the variable val to 0xdeadbeef  
  
Here we can exploit scanf to input more data than necessary and commit a buffer overflow attack  
  
The variable val is placed on the stack and we have our buffer buf is placed above it as Stacks grow from high memory addresses to low memory addresses. ![956e4133.png](../src/956e4133.png)  
  
If we place more information onto the stack than the stack can hold we can overwrite the contents of the variable val  
  
If we run the program we get the output  
![03300bec.png](../src/03300bec.png)  
  
Here we see that we have not overwritten val as there is still free space in the stack  
  
If we instead fill the input box with letters lets see what happens:  
![740561a8.png](../src/740561a8.png)  
  
Here we see that val is now equal to 0x58575655  
  
if we convert this to ASCII we can see what it now contains  
![ed6190ce.png](../src/ed6190ce.png)  
  
As you can see val now contains XWVU which is the 24th to 21st letter of our input string  
This means that we over flow val after 20 characters but why is it backwards?  
  
This is due to endianness which refers to the order of bytes within a binary representation of a number  
  
The numbers in this are stored in reverse order for each 4byte section  
So our string is stored as:  
> String: ABCDEFGHIJKLMNOPQRSTUVWXYZ  
> Endian Representation: DCBAHGFELKJIPONMTSRQXWVUZY  
  
