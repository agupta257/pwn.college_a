In this challenge we have to find the flag by removing a specific column in the /challenge/run output.
## My Solve

**Flag:**pwn.college{MHPj22C9MkaghjKXldjtY4WH38G.01NxEzNxwCN4kjNzEzW}
In this challenge, I used the cut command to extract the flag characters, then I used tr -d to remove the newlines from those characters.
```bash
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run | cut -d " " -f 2 | tr -d "\n"
pwn.college{MHPj22C9MkaghjKXldjtY4WH38G.01NxEzNxwCN4kjNzEzW}
```

## What I Learned
Through this challenge, I was able to learn that the cut command is used to grab specific columns of the data.

## Refernces
Did not use any references for this challenge.
