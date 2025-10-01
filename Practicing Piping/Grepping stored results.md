In this challenge we have to redirect the output of /challenge/run to /tmp/data.txt and grep that for the flag.
## My Solve

**Flag:**pwn.college{wpevghQV_J22JNVMamJbQJDrS2b.QX4EDO0wCN4kjNzEzW}
In this challenge, I used > character to redirect the output of /challenge/run to /tmr/data.txt and then used the grep command to search for pwn.college in /temp/data.txt.
```bash
hacker@piping~grepping-stored-results:~$ /challenge/run > /tmp/data.txt
hacker@piping~grepping-stored-results:~$ grep pwn.college /tmp/data.txt
pwn.college{wpevghQV_J22JNVMamJbQJDrS2b.QX4EDO0wCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn to use the grep command to search through the resulting file.
## Refernces
Did not use any references for this challenge.
