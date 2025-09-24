In this challenge, we have to learn how to explicitly use relative paths to launch run explicitly in the current directory.
## My Solve

**Flag:**pwn.college{U58bNUhDthu7epkIi3I_b8Gwu7D.QXxUTN0wCN4kjNzEzW}
In this challenge, I executed /challenge/run using a relative path while having a current working directory of /challenge and then i wrote ./run to get the flag.

```bash
hacker@paths~implicit-relative-path:~$ /challenge/run
Incorrect...
You are not currently in the /challenge directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~implicit-relative-path:~$ cd /challenge
hacker@paths~implicit-relative-path:/challenge$ run
bash: run: command not found
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{U58bNUhDthu7epkIi3I_b8Gwu7D.QXxUTN0wCN4kjNzEzW}
```
## What I Learned
Through this challenge, I was able to execute run in the current directory, using . 

## Refernces
Did not use any references for this challenge.
