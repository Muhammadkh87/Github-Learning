# My GitHub Learning Journey

This README document will illustrate what I have learned about using **Git** and **GitHub**.  
It covers common commands, workflows for pushing, pulling, rebasing, and reverting changes.

---

## 📚 What I Learned
- Setting up Git and configuring user information
- Creating repositories (local and remote)
- Staging and committing changes
- Branching and merging
- Pushing and pulling changes with GitHub
- Rebasing and resolving conflicts
- Reverting changes safely
- Working with `.gitignore` and README files

---

## 🔑 Common Git Commands

### 1️⃣ Setup & Configuration
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
git init               # Initialize a new Git repository
git clone <repo-url>   # Clone an existing repository
```

### 2️⃣ Staging & Committing
```bash
git status            # Check the status of files
git add <file>        # Stage a specific file
git add .             # Stage all changes
git commit -m "Message"   # Commit staged changes
```

### 3️⃣ Branching
```bash
git branch                # List branches
git branch <name>         # Create a new branch
git checkout <name>       # Switch to a branch
git checkout -b <name>    # Create and switch to a new branch
git merge <branch>        # Merge a branch into the current one
```

### 4️⃣ Remote Operations
```bash
git remote -v                     # List remote repositories
git remote add origin <repo-url>  # Add a remote repository
git push -u origin main           # Push branch to remote for the first time
git push                          # Push changes
git pull                          # Pull changes
```

### 5️⃣ Rebasing
```bash
git fetch origin
git rebase origin/main    # Rebase current branch onto the latest main
git rebase --continue     # Continue after resolving conflicts
git rebase --abort        # Abort rebase
```

### 6️⃣ Undoing Changes
```bash
git reset <file>          # Unstage a file
git checkout -- <file>    # Discard changes in a file
git revert <commit>       # Create a new commit that undoes a specific commit
git reset --hard <commit> # Reset to a previous commit (⚠️ Dangerous!)
```

---

## 🚀 Workflow: Push, Pull, Rebase, Revert

### ✅ Push Changes
```bash
git add .
git commit -m "Your commit message"
git push origin main
```

### ✅ Pull Changes
```bash
git pull origin main
```

### ✅ Rebase
```bash
git fetch origin
git rebase origin/main
```

### ✅ Revert a Commit
```bash
git revert <commit-hash>
git push origin main
```

---

## 📄 Notes
- Use `git log --oneline --graph` to see commit history.
- Use branches for new features or bug fixes.
- Always **pull/rebase before pushing** to avoid conflicts.

---
