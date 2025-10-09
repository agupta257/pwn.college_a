In this challenge we have to write a script at /home/hacker/solve.sh that takes one argument, if the argument is "pwn", output "college", for any other input, output "nope".
## My Solve

**Flag:**pwn.college{wjAd87e6LlDSdeCbnk2Vv5oYFo3.01NzMDOxwCN4kjNzEzW}
In this challenge, I followed the commands to get the flag.
```bash
hacker@chaining~scripting-with-default-cases:~$ #!/bin/bash
hacker@chaining~scripting-with-default-cases:~$ if [ "$1" == "pwn" ]
> then
> echo "college"
> else
> echo "nope"
> fi
hacker@chaining~scripting-with-default-cases:~$ chmod ugo+x /home/hacker/solve.sh
hacker@chaining~scripting-with-default-cases:~$ /challenge/run
Here's your flag:
pwn.college{wjAd87e6LlDSdeCbnk2Vv5oYFo3.01NzMDOxwCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn how to use the if-else statement in Linux.

## Refernces
Did not use any references for this challenge.
