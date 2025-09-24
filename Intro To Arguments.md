In this challenge, to get the flag, we must run the hello command with a single argument of hackers.
## My Solve
**Flag:**pwn.college{cJ1gLpf5eeUNvWlZXVjYFrCSfMv.QX4YjM1wCN4kjNzEzW}
For this challenge, I first understood that a command line consists of a command space arrguments. There can be multiple arguments as shown in the example. When you type a line of text and hit enter, the shell parses
your input into a command and its arguments. Looking at the example of echo given by the challenge. I ran the hello command followed by the hackers argument as stated in the challenge to obtain the flag.
```bash
hacker@hello~intro-to-arguments:~$ hello hackers
Success! Here is your flag:
pwn.college{cJ1gLpf5eeUNvWlZXVjYFrCSfMv.QX4YjM1wCN4kjNzEzW}
```
## What I learned
Through this challenge, I was able to learn about command and its arguments, how there can be multiple arguments to a single command and how the shell parses your input into a command and its arguments.
I was also able to learn about the command echo and how it echoes the argument back into the terminal.

## References
Did not use any reference for this challenge.
