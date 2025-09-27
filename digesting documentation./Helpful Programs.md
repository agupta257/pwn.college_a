In this challenge we have to ivoke /challenge/challenge properly in order for it to get the flag.
## My Solve

**Flag:** pwn.college{8gtecttDx5aUhSrnkP02GTx5lbP.QX3IDO0wCN4kjNzEzW}
In this challenge I first used the --help argument. It showed the was to get the flag. Then I used the -p argument to get the secret value. The secret value was 850. So, I then used the -g 850 argument to get the
flag.

```bash
hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 850
hacker@man~helpful-programs:~$ /challenge/challenge -g 850
Correct usage! Your flag: pwn.college{8gtecttDx5aUhSrnkP02GTx5lbP.QX3IDO0wCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn that the --help argument helps to run the man page.

## Refernces
Did not use any references for this challenge.
