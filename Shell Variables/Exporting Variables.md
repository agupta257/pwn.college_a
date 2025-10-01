In this challenge we have to invoke /challenge/run with the PWN variable exported and set to the value COLLEGE and the COLLEGE variable set to the value PWN but 
not exported.
## My Solve

**Flag:**pwn.college{szoj9xV5rz2XQpbNoAJQ9pDcnPZ.QXyYTN0wCN4kjNzEzW}
In this challenge, I first set the value of the PWN variable as COLLEGE and then I set the value of the COLLEGE variable as PWN, then i exported the PWN variable and 
invoked /challenge/run.

```bash
hacker@variables~exporting-variables:~$ PWN=COLLEGE
You've set the PWN variable to the proper value!
hacker@variables~exporting-variables:~$ COLLEGE=PWN
You've set the PWN variable to the proper value!
hacker@variables~exporting-variables:~$ export PWN
hacker@variables~exporting-variables:~$ /challenge/run
CORRECT!
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great
job! Here is your flag:
pwn.college{szoj9xV5rz2XQpbNoAJQ9pDcnPZ.QXyYTN0wCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn that the export operator exports the variable which u want to export.
## Refernces
Did not use any references for this challenge.
