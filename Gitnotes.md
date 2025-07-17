# Git Notes

This file contains key Git commands, usage examples, and notes that I regularly refer to while working on projects and documenting my learning.

---

## 1. Git Project Setup

```bash
git init                           # Start a new Git repo
git clone <repo-url>              # Clone an existing repo from GitHub

git remote add origin <url>       # Connect local repo to remote
git remote -v                     # Show connected remote repos
```

## 2. Add, Commit, and Push

```bash
git add <filename>                # Stage a file for commit
git add .                         # Stage all files
git commit -m "Message"           # Commit with a message
git push origin main              # Push to main branch
git push -u origin main           # Set default upstream for future pushes
``` 

## 3. Pulling and Fetching

```bash
git branch                        # List branches
git branch <name>                # Create a new branch
git checkout <branch-name>       # Switch to a branch
git checkout -b <new-branch>     # Create + switch to a new branch
git push origin <branch-name>    # Push branch to remote
```

## 4. Branching

```bash
git branch                        # List branches
git branch <name>                # Create a new branch
git checkout <branch-name>       # Switch to a branch
git checkout -b <new-branch>     # Create + switch to a new branch
git push origin <branch-name>    # Push branch to remote
```

## 5. Deleting Branches

```bash
git branch -d <branch-name>       # Delete branch locally
git push origin --delete <name>   # Delete branch from remote
```

## 6. Status and Log

```bash
git status                        # Show changed/unstaged files
git log                           # Show commit history
git log --oneline                 # Short log (one commit per line)
```

## 7. Undo & fix

```bash
git restore <file>                # Undo changes to a file
git reset --soft HEAD~1           # Undo last commit (keep changes)
git reset --hard HEAD~1           # Undo last commit and changes
git checkout -- <file>            # Revert file to last commit
```

## 8. Common Config

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --list                 # View all current config
```

## 9. Sync Your Repo

```bash
git pull --no-rebase origin main   # Merge changes from GitHub (safe)
git push origin main               # Push new commits to GitHub
```

## 10. View Remote URL or Change it

```bash
git remote -v                      # View current remote
git remote set-url origin <url>   # Change remote URL
```

---
