In this challenge we have to read the manual page of challenge and get the flag.
## My Solve

**Flag:**pwn.college{IpKB3tt8JpKHbqwcHOX6JSwoxVQ.QX0ETO0wCN4kjNzEzW}
In this challenge, I first used help challenge. Using this i found the --secret VALUE argument. Using this argument I got the flag.
```bash
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!

    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "IpKB3tt8".
hacker@man~help-for-builtins:~$ challenge --secret IpKB3tt8
Correct! Here is your flag!
pwn.college{IpKB3tt8JpKHbqwcHOX6JSwoxVQ.QX0ETO0wCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn that we can use help to look up for builtins.
## Refernces
Did not use any references for this challenge.
