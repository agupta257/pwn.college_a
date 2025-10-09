In this challenge we have to chain the programs /challenge/first-success and /challenge/second.
## My Solve

**Flag:**pwn.college{8cklGJyzHMjz_HaYEhTrYtoCWUE.0lM0MDOxwCN4kjNzEzW}
In this challenge, I used the && operator in between /challenge/first-success and /challenge/second to chain them together.
```bash
hacker@chaining~building-on-success:~$ /challenge/first-success && /challenge/second
Nice chaining! Flag: pwn.college{8cklGJyzHMjz_HaYEhTrYtoCWUE.0lM0MDOxwCN4kjNzEzW}
```
## What I Learned
Through this challenge, I was able to learn that the && operator allows you to run a second command only if the first command succeeds, both the conditions must be true.
## Refernces
Did not use any references for this challenge.
