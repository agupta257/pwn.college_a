In this challenge /challenge/run will give us a flag, but only if you redirect its output to the file myflag.
## My Solve

**Flag:** pwn.college{k8sZxB4HJxYtUQ6nC89dYsANu3v.QX1YTN0wCN4kjNzEzW}
In this challenge, I redirected the output of /challenge/run to myflag using > character and then wrote cat myflag to get the flag.
```bash
hacker@piping~redirecting-more-output:~$ /challenge/run > myflag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-more-output:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{k8sZxB4HJxYtUQ6nC89dYsANu3v.QX1YTN0wCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn > character can redirect the output of any command.
## Refernces
Did not use any references for this challenge.
