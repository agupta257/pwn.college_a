In this challenge we have to write a script at /home/hacker/solve.sh that takes one argument and if the argument is "pwn", output "college".
## My Solve

**Flag:**pwn.college{Y5C8TB62_N8GYZNJJtEjozMRj1q.0lNzMDOxwCN4kjNzEzW}
In this challenge, I followed the commands to get the flag.
```bash
hacker@chaining~scripting-with-conditionals:~$ echo '#!/bin/bash' > /home/hacker/solve.sh
hacker@chaining~scripting-with-conditionals:~$ echo 'if [ "$1" == "pwn" ]' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-conditionals:~$ echo 'then' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-conditionals:~$ echo '    echo "college"' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-conditionals:~$ echo 'fi' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-conditionals:~$ chmod ugo+x /home/hacker/solve.sh
hacker@chaining~scripting-with-conditionals:~$ /home/hacker/solve.sh pwn
college
hacker@chaining~scripting-with-conditionals:~$ /challenge/run
Correct! Your script properly handles all the conditions.
Here's your flag:
pwn.college{Y5C8TB62_N8GYZNJJtEjozMRj1q.0lNzMDOxwCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn how to use the if statment in Linux.

## Refernces
Did not use any references for this challenge.
