In this challenge we have to write a script at /home/hacker/solve.sh that takes one argument, if the argument is "hack", output "the planet" ,if the argument is "pwn", output "college" ,if the argument is "learn", 
output "linux" and for any other input, output "unknown".
## My Solve

**Flag:**pwn.college{MSWeoVBuMaJgPqdrm-WjcS79mmx.0FOzMDOxwCN4kjNzEzW}
In this challenge, I followed the instructions to get the flag.
```bash
hacker@chaining~scripting-with-multiple-conditions:~$ cat solve.sh
#!/bin/bash
if [ "$1" == "hack" ]
then
    echo "the planet"
elif [ "$1" == "pwn" ]
then
    echo "college"
elif [ "$1" == "learn" ]
then
    echo "linux"
else
    echo "unknown"
fi
hacker@chaining~scripting-with-multiple-conditions:~$ /challenge/run
Correct! Your script properly handles all the conditions with elif.
Here's your flag:
pwn.college{MSWeoVBuMaJgPqdrm-WjcS79mmx.0FOzMDOxwCN4kjNzEzW}
```
## What I Learned
Through this challenge, I was able to learn how to use the elif statment in Linux.

## Refernces
Did not use any references for this challenge.

