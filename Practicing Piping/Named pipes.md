In this challenge we have to create a /tmp/flag_fifo file and redirect the stdout of /challenge/run to it.
## My Solve

**Flag:**pwn.college{sJvGh4QIMfjnwNrSZ6k2yF4Ngm1.01MzMDOxwCN4kjNzEzW}
In this challenge, I first removed the /tmp/flag_fifo file using the rm command and then i created the fifo file using mkfifo, then i redirected the stdout of 
/challenge/run to it using > operator.
```bash
hacker@piping~named-pipes:~$ rm /tmp/flag_fifo
hacker@piping~named-pipes:~$ mkfifo /tmp/flag_fifo
hacker@piping~named-pipes:~$ /challenge/run > /tmp/flag_fifo
hacker@piping~named-pipes:~$ cat /tmp/flag_fifo
You've correctly redirected /challenge/run's stdout to a FIFO at
/tmp/flag_fifo! Here is your flag:
pwn.college{sJvGh4QIMfjnwNrSZ6k2yF4Ngm1.01MzMDOxwCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn that using fifo files can be made which do not take any space.
## Refernces
Did not use any references for this challenge.
