# 🌟 Ultimate Git Commands Guide: From Beginner to Professional 🚀

## 📘 Table of Contents
1. [Introduction](#introduction)
2. [Basic Configuration](#basic-configuration)
3. [Repository Creation](#repository-creation)
4. [Basic Workflow Commands](#basic-workflow-commands)
5. [Branching and Merging](#branching-and-merging)
6. [Remote Repository Management](#remote-repository-management)
7. [Advanced Git Commands](#advanced-git-commands)
8. [Stashing and Cleaning](#stashing-and-cleaning)
9. [Debugging and Inspection](#debugging-and-inspection)
10. [Advanced Techniques](#advanced-techniques)
11. [Troubleshooting](#troubleshooting)
12. [Best Practices](#best-practices)

## 📍 Introduction

Git is a distributed version control system that tracks changes in source code during software development. This comprehensive guide covers Git commands for developers at all levels.

## 🔧 Basic Configuration

### Setting Up Git
```bash
# Configure global user name
git config --global user.name "Your Name"

# Configure global email
git config --global user.email "your.email@example.com"

# Set default editor
git config --global core.editor "vim"

# List all configurations
git config --list

# Get specific configuration
git config user.name
```

### SSH Key Setup
```bash
# Generate SSH key
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

# Start SSH agent
eval "$(ssh-agent -s)"

# Add SSH key to agent
ssh-add ~/.ssh/id_rsa
```

## 🏗️ Repository Creation

### Creating Repositories
```bash
# Initialize a new repository
git init

# Clone an existing repository
git clone https://github.com/username/repository.git

# Clone a specific branch
git clone -b branch_name https://github.com/username/repository.git

# Clone with depth (shallow clone)
git clone --depth 1 https://github.com/username/repository.git
```

## 📝 Basic Workflow Commands

### Adding and Committing
```bash
# Add specific file
git add filename

# Add all changes
git add .

# Commit with message
git commit -m "Commit message"

# Commit all tracked, modified files
git commit -am "Commit message"

# Amend last commit
git commit --amend

# Amend commit without changing message
git commit --amend --no-edit
```

### Checking Status and Differences
```bash
# Check repository status
git status

# Show differences
git diff

# Show staged differences
git diff --staged

# Compact status
git status -s
```

## 🌿 Branching and Merging

### Branch Management
```bash
# List branches
git branch

# List all branches (local and remote)
git branch -a

# Create new branch
git branch new-branch-name

# Switch to branch
git checkout branch-name

# Create and switch to new branch
git checkout -b new-branch-name

# Rename branch
git branch -m old-name new-name

# Delete local branch
git branch -d branch-name

# Delete remote branch
git push origin --delete branch-name
```

### Merging and Rebasing
```bash
# Merge branch into current branch
git merge branch-name

# Rebase current branch
git rebase branch-name

# Interactive rebase
git rebase -i HEAD~3

# Abort rebase
git rebase --abort
```

## 🌐 Remote Repository Management

### Remote Operations
```bash
# Add remote repository
git remote add origin https://github.com/username/repository.git

# List remotes
git remote -v

# Fetch from remote
git fetch origin

# Pull changes
git pull origin main

# Push to remote
git push origin branch-name

# Push all branches
git push --all origin

# Set upstream branch
git push -u origin branch-name
```

## 🔬 Advanced Git Commands

### Logging and History
```bash
# Show commit log
git log

# Compact log
git log --oneline

# Log with graph
git log --graph --oneline --decorate

# Search commits by message
git log --grep="search term"

# Show commits by author
git log --author="Name"
```

## 🧹 Stashing and Cleaning

### Stash Management
```bash
# Stash changes
git stash

# Stash with message
git stash save "Message"

# List stashes
git stash list

# Apply latest stash
git stash apply

# Apply specific stash
git stash apply stash@{2}

# Pop (apply and remove) latest stash
git stash pop

# Drop stash
git stash drop
```

### Cleaning Repository
```bash
# Remove untracked files
git clean -f

# Remove untracked directories
git clean -fd

# Dry run (show what would be deleted)
git clean -n
```

## 🕵️ Debugging and Inspection

### Blame and Bisect
```bash
# Show who changed each line
git blame filename

# Find commit that introduced a bug
git bisect start
git bisect bad
git bisect good commit-hash
```

## 🚀 Advanced Techniques

### Cherry-Picking
```bash
# Apply specific commit to current branch
git cherry-pick commit-hash

# Cherry-pick without committing
git cherry-pick -n commit-hash
```

### Submodules
```bash
# Add submodule
git submodule add https://github.com/username/repository.git

# Initialize submodules
git submodule init

# Update submodules
git submodule update
```

## 🛠️ Troubleshooting

### Undoing Changes
```bash
# Discard local changes
git checkout -- filename

# Unstage files
git reset HEAD filename

# Revert last commit (create new commit)
git revert HEAD

# Reset to previous commit
git reset --hard HEAD~1
```

## 📋 Best Practices

1. Commit often
2. Write clear, descriptive commit messages
3. Use feature branches
4. Pull before pushing
5. Never force push to shared branches
6. Use .gitignore
7. Review changes before committing

## 📚 Learning Resources
- [Official Git Documentation](https://git-scm.com/doc)
- [GitHub Learning Lab](https://lab.github.com/)
- [Atlassian Git Tutorials](https://www.atlassian.com/git/tutorials)

## 🤝 Contribution
Contributions and suggestions are welcome! Please open an issue or submit a pull request.

## 📄 License
[MIT LICENSE ]

---

**Remember:** Practice makes perfect! The more you use Git, the more comfortable you'll become with these commands.