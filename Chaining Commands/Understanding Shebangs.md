In this challenge we have to create a script at /home/hacker/solve.sh that has a proper shebang and outputs "hack the planet".
## My Solve

**Flag:** pwn.college{wabSHQ_PGDteug7IXrPcP5dZcwh.0VOzMDOxwCN4kjNzEzW}
In this challenge, I followed the instructions to get the flag.
```bash
hacker@chaining~understanding-shebangs:~$ echo '#!/bin/bash' > /home/hacker/solve.sh
hacker@chaining~understanding-shebangs:~$ echo 'echo "hack the planet"' >> /home/hacker/solve.sh
hacker@chaining~understanding-shebangs:~$ chmod ugo+x /home/hacker/solve.sh
hacker@chaining~understanding-shebangs:~$ /challenge/run
Testing your script...
Perfect! Your flag:
Flag: pwn.college{wabSHQ_PGDteug7IXrPcP5dZcwh.0VOzMDOxwCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn that if the program file starts with the characters #! (shebang), Linux treats the file as an interpreted program, and 
the contents of the rest of the line as the path to the interpreter.

## Refernces
Did not use any references for this challenge.
