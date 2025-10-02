In this challenge we have to delete the newlines from the flag.
## My Solve

**Flag:**pwn.college{Yqmy8h4oqk-UfHzQW8YRBa5awUv.0VNxEzNxwCN4kjNzEzW}
In this challenge, I used the tr -d command to delete "\n" from the flag. 
```bash
hacker@data~deleting-newlines:~$ /challenge/run | tr -d "\n"
Your line-split flag: pwn.college{Yqmy8h4oqk-UfHzQW8YRBa5awUv.0VNxEzNxwCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn that \n is used to go to a new line.

## Refernces
Did not use any references for this challenge.
