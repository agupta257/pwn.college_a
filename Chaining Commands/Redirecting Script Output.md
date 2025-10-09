In this challenge we have to create a script that calls the /challenge/pwn command followed by the /challenge/college command, and pipe the output of the script into a single invocation of the /challenge/solve command.
## My Solve

**Flag:**pwn.college{kAq5667ItScUXQaa7cdnnYGYleK.QX4ETO0wCN4kjNzEzW}
In this challenge, I followed the instructions to get the flag.
```bash
hacker@chaining~redirecting-script-output:~$ echo "/challenge/pwn" > x.sh
hacker@chaining~redirecting-script-output:~$ echo "/challenge/college" >> x.sh
hacker@chaining~redirecting-script-output:~$ bash x.sh | /challenge/solve
Correct! Here is your flag:
pwn.college{kAq5667ItScUXQaa7cdnnYGYleK.QX4ETO0wCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn that we can pipe the output of a script into a single invocation of a command.

## Refernces
Did not use any references for this challenge.
