---
tags:
  - git
  - version-control
  - basic
links:
  - "[[Version Control Systems]]"
source:
aliases:
  - git
---
> [!TIP]
> You can learn more about Git and GitHub on [Roadmap.sh](https://roadmap.sh/git-github)

**Git** is a distributed version control system initially created by Linus Torvalds to manage the development of the Linux kernel but has since been widely adopted by developers around the world. It allows developers to track changes in source code, collaborate in teams, manage branches for new features or bug fixes, and revert to earlier versions when needed.

With Git, you can:
- Track every change to files (versioning)
- Restore previous states of a project
- Create branches to develop new features in isolation
- Merge code from different branches safely
- Collaborate with others via remote repositories (e.g., [[GitHub]], [[GitLab]], [[Bitbucket]])

**Cheatsheet**
```bash
# Configuration
git config --global user.name "Your Name"
git config --global user.email "you@example.com"

# Initialize or Clone a Repo
git init                      # Initialize a new repository
git clone <url>               # Clone an existing repository

# Tracking Changes
git status                    # Show the current status
git add <file>                # Stage a specific file
git add .                     # Stage all changes
git commit -m "Your message"  # Commit change

# View History
git log                       # View commit history
git diff                      # Show unstaged changes

# Branching & Merging
git branch                    # List branches
git branch <name>             # Create a new branch
git checkout <name>           # Switch to a branch
git checkout -b <name>        # Create and switch to a branch
git merge <name>              # Merge branch into current one

# Remote Repositories
git remote add origin <url>   # Add a remote repository
git push -u origin main       # Push for the first time
git push                      # Push changes
git pull                      # Pull changes

# Useful Commands
git stash                     # Temporarily save changes
git stash pop                 # Reapply stashed changes
git reset --hard <commit>     # Reset to a specific commit
git revert <commit>           # Revert a commit (creates a new one)

```

> [!TIP]
> Use `git log --oneline --graph --all` for a compact visual overview of the commit history.

**Sources**

- [Official Docs](https://git-scm.com/doc)
- [Interactive Learning](https://learngitbranching.js.org)
- [GitHub Education - Cheatsheet](https://education.github.com/git-cheat-sheet-education.pdf)
- [Roadmap.sh - Git GitHub](https://roadmap.sh/git-github)
