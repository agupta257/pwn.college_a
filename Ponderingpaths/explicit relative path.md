In this challenge we have to use . in your relative paths.
## My Solve

**Flag:**pwn.college{gGuXFNC52mk1375VTq1uiCRp83s.QXwUTN0wCN4kjNzEzW}
In this challenge, I executed /challenge/run using a relative path while having a current working directory of / and then i wrote ./challenge/run to get the flag.

```bash
hacker@paths~explicit-relative-paths-from-:~$ /challenge/run
Incorrect...
You are not currently in the / directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~explicit-relative-paths-from-:~$ cd /
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{gGuXFNC52mk1375VTq1uiCRp83s.QXwUTN0wCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn that every directory has two implicit entries that you can reference in paths: . and ... 

## Refernces
Did not use any references for this challenge.
