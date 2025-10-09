In this challenge we have to write a script at /home/hacker/solve.sh that takes two arguments and outputs them in reverse order.
## My Solve

**Flag:**pwn.college{4GmanczEm40kMI8dTh1Zs92cyf5.0VNzMDOxwCN4kjNzEzW}
In this challenge, I followed the instructions to get the flag.
```bash
hacker@chaining~scripting-with-arguments:~$ echo '#!/bin/bash' > /home/hacker/solve.sh
hacker@chaining~scripting-with-arguments:~$ echo 'echo "$2 $1"' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-arguments:~$ chmod ugo+x /home/hacker/solve.sh
hacker@chaining~scripting-with-arguments:~$ /home/hacker/solve.sh pwn college
college pwn
hacker@chaining~scripting-with-arguments:~$ /challenge/run
Correct! Your script properly reversed the arguments.
Here's your flag:
pwn.college{4GmanczEm40kMI8dTh1Zs92cyf5.0VNzMDOxwCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn that scripts can accept arguments.

## Refernces
Did not use any references for this challenge.
