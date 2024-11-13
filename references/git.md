---
creation date: 2024-11-04 13:30
tags:
  - dev/tools
  - shell/cli
---
```yaml
os::macOs
command::git
desc::git config
```

## how to have a global git ignore

```bash
echo ".DS_Store" >> ~/.gitignore_global
echo "._.DS_Store" >> ~/.gitignore_global
echo "**/.DS_Store" >> ~/.gitignore_global
echo "**/._.DS_Store" >> ~/.gitignore_global
git config --global core.excludesfile ~/.gitignore_global
```

## Switching to another branch with git worktree

Let’s say you’re working on a feature, and you have many edited or new files. Suddenly, you have to fix a commit on the main branch. You’d typically either commit and stash your changes and switch to main or create another copy of the entire repository somewhere else to have a clean state.

With git worktree, you can create another worktree, something like “a copy of the repo inside your repo”, which you can delete after making changes:

```sh
git worktree add ./fix-critical-bug main  
# go to the fix-critical-bug directory, commit and push solution on the main branch  
git worktree remove ./fix-critical-bug  
# return to working on your feature
```

## Hunting bugs with git bisect

Imagine the following scenario: Your code is not working properly, but you can’t figure out what’s wrong. You just know that a week ago, everything ran fine.

Git bisect can help you pinpoint the exact commit a bug was introduced. You run _git bisect start_, mark the good and bad commits (with _git bisect good / git bisect bad <hash>). Git will automatically switch to the commit in the middle. You can mark it as good or bad and then git will switch again to commit in the middle between the good and bad commit, repeating this process until the guilty commit was found.

![](Pasted%20image%2020241110225852.png)

Starting with a bad (step 1) and good (step 2) commit, _git bisect_ will jump to the commits in between (steps 3 and 4) to narrow down the commit where an error was introduced (step 5).