In this challenge, we are required to run the program using a relative path while having a current working directory of /.
## My Solve
**Flag:**pwn.college{k18Z7hz2tCi5QFNg7k6fs5Wk-Nm.QX5QTN0wCN4kjNzEzW}

In this challenge, I executed /challenge/run using a relative path while having a current working directory of / and then i wrote challenge/run to get the flag.
```bash
hacker@paths~implicit-relative-paths-from-:~$ /challenge/run
Incorrect...
You are not currently in the / directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{k18Z7hz2tCi5QFNg7k6fs5Wk-Nm.QX5QTN0wCN4kjNzEzW}
```
## What I Learned
Through this challenge, I was able to learn that relative path is any path that does not start at root and relative path is interpreted relative to your current working directory.

## Refernces
Did not use any references for this challenge.
