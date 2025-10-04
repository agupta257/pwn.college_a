In this challenge we have to change the user to zardus and run /challenge/run.
## My Solve

**Flag:**pwn.college{ATYpBeZcmexqL_SHUbllyU4P7ov.QX2UDN1wCN4kjNzEzW}
In this challenge, I changed the user to zardus using su and then entered the password dont-hack-me. Then I run /challenge/run to get the flag.
```bash
hacker@users~other-users-with-su:~$ su zardus
Password:dont-hack-me
zardus@users~other-users-with-su:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{ATYpBeZcmexqL_SHUbllyU4P7ov.QX2UDN1wCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn to switch users using su.

## Refernces
Did not use any references for this challenge.
