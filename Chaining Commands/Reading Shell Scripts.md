In this challenge we have to read the script of /challenge/run in which the password is stored, we have to figure out the password and get the flag.
## My Solve

**Flag:**pwn.college{Mf6jpS5qWcinpxuYE1aCEYRh57o.0lMwgDOxwCN4kjNzEzW}
In this challenge, I wrote cat /challenge/flag to read the script. From the script I got the password which was hack the PLANET. Using this password, I got the flag.
```bash
hacker@chaining~reading-shell-scripts:~$ cat /challenge/run
#!/opt/pwn.college/bash

read GUESS
if [ "$GUESS" == "hack the PLANET" ]
then
        echo "CORRECT! Your flag:"
        cat /flag
else
        echo "Read the /challenge/run file to figure out the correct password!"
fi
hacker@chaining~reading-shell-scripts:~$ /challenge/run
hack the PLANET
CORRECT! Your flag:
pwn.college{Mf6jpS5qWcinpxuYE1aCEYRh57o.0lMwgDOxwCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn cat can be used to read a bash script.

## Refernces
Did not use any references for this challenge.
