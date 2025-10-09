In this challenge we have to chain /challenge/first-failure and /challenge/second using the || operator.
## My Solve

**Flag:**pwn.college{wgCEzd17bSqOR7q6DsFDvOQAAbP.01M0MDOxwCN4kjNzEzW}
In this challenge, I used the || in between /challenge/first-failure and /challenge/second to chain them.
```bash
hacker@chaining~handling-failure:~$ /challenge/first-failure || /challenge/second
Nice chaining! Flag: pwn.college{wgCEzd17bSqOR7q6DsFDvOQAAbP.01M0MDOxwCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn that || operator allows you to run a second command only if the first command fails. Either the first command succeeds OR the second command will run.

## Refernces
Did not use any references for this challenge.
