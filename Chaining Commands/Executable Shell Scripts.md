In this challenge we have to create a shellscript that will invoke /challenge/solve, make it executable, and run it without explicitly invoking bash.
## My Solve

**Flag:**pwn.college{Ym9RvBXc9HylAl3oH8gOpI0Vh8W.QX0cjM1wCN4kjNzEzW}
In this challenge, I followed the commands to get the flag.
```bash
hacker@chaining~executable-shell-scripts:~$  echo "/challenge/solve" > x.sh
hacker@chaining~executable-shell-scripts:~$ chmod ugo+x x.sh
hacker@chaining~executable-shell-scripts:~$ /home/hacker/x.sh
Congratulations on your shell script execution! Your flag:
pwn.college{Ym9RvBXc9HylAl3oH8gOpI0Vh8W.QX0cjM1wCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn that we can avoid to invoke bash if our shell script is executable and can be can invoked by its relative or absolute path.

## Refernces
Did not use any references for this challenge.
