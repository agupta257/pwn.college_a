In this challenge we have to use diff to comapre the output of two commands.
## My Solve

**Flag:** pwn.college{sfyeDDQ_QfdPGLWOmd5_VglMJZY.0lNwMDOxwCN4kjNzEzW}.
In this challenge, I used the diff command to comare the output of two different command outputs and get the real flag.
```bash
hacker@piping~process-substitution-for-input:~$ diff <(/challenge/print_decoys) <(/challenge/print_decoys_and_flag)
59a60
> pwn.college{sfyeDDQ_QfdPGLWOmd5_VglMJZY.0lNwMDOxwCN4kjNzEzW}
```
## What I Learned
Through this challenge, I was able to learn that the diff <(command) <(command) compares the output of two different comands.
## Refernces
Did not use any references for this challenge.
