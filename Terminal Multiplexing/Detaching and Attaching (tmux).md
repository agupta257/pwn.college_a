In this challenge we have to detach and reattach from tmux.
## My Solve

**Flag:**pwn.college{Yx67bKel4Wz01cniIlX020T5Ng4.0VO4IDOxwCN4kjNzEzW}
In this challenge, I first lauched tmux. Then I detached from it using Ctrl+B and then pressing d. After that I wrote /challenge/run for it to run in the background and reattached to tmux by typing tmux attach.
```bash
tmux
/challenge/run
tmux attach
```

## What I Learned
Through this challenge, I was able to learn that to detach from tmux, we use the command Ctrl+B d and to reattach we use the commd temux attach.
## Refernces
Did not use any references for this challenge.
