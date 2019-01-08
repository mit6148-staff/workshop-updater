# workshop-updater
Tool to more easily update Catbook workshops

## Making a change
- Clone all catbook repos: `./init`
    - This adds other workbooks as git remotes, so we can transfer commits across repos
- Make a change you want and **commit**
- Run copy: `./copy [WORKSHOP NUM] [BRANCH] [WORKSHOP NUM] [BRANCH]`

## Tips
- View all branches a workshop has with `git branch -a`
- Push all changed branches in a repo with `git push --all`

## Example
I made a change in workshop 3 on step 1. I want to update all future branches.
```
./copy 3 step1 3 step2
./copy 3 step1 3 step3   # or ./copy 3 step2 3 step3
./copy 3 step1 3 step4
./copy 3 step1 4 master  # fetch/copy across repos
./copy 4 master 4 step0
...
```

I might add a script to automate this sequence of copies, but it's nice to have manual control over the process, because you may encounter several merge conflicts.
