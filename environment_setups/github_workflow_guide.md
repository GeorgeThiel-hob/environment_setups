# GitHub Workflow Guide

Quick reference for common Git operations.

---

## 1. Download Project from GitHub

### Your Own Repository
```bash
cd C:\your_projects_folder
git clone https://github.com/YOUR_USERNAME/REPO_NAME.git
cd REPO_NAME
```

### Someone Else's Repository (Fork First)
```bash
# 1. Fork on GitHub website (click "Fork" button)
# 2. Clone your fork
git clone https://github.com/YOUR_USERNAME/FORKED_REPO.git
cd FORKED_REPO

# 3. Add original repo as upstream
git remote add upstream https://github.com/ORIGINAL_OWNER/REPO_NAME.git
```

---

## 2. Update Repository After Local Changes

### Basic Workflow
```bash
# 1. Check what changed
git status

# 2. Stage changes
git add .

# 3. Commit with message
git commit -m "Description of what you changed"

# 4. Push to GitHub
git push
```

### Working Across Multiple Devices
```bash
# Before starting work (pull latest changes)
git pull

# After finishing work
git add .
git commit -m "Your changes"
git push
```

---

## 3. Best Practices

### Always Pull Before Starting Work
```bash
git pull
```
Prevents conflicts when working on multiple devices.

### Commit Frequently
```bash
# After completing a logical chunk of work
git add .
git commit -m "Clear description of what changed"
git push
```

### Write Clear Commit Messages
- ✅ Good: `"Add LASSO model training and evaluation"`
- ✅ Good: `"Fix missing value imputation bug"`
- ❌ Bad: `"update"`, `"changes"`, `"final version"`

### Use .gitignore
Create `.gitignore` to exclude:
```
.venv/
__pycache__/
.ipynb_checkpoints/
.DS_Store
.vscode/
```

---

## 4. Common Commands
```bash
# View status
git status

# View commit history
git log --oneline

# Discard local changes to a file
git checkout -- filename.py

# Undo last commit (keep changes)
git reset --soft HEAD~1

# Pull latest changes
git pull

# Push your changes
git push
```

---

## 5. Workflow Summary

**Daily routine:**
```bash
git pull              # Start: get latest
# ... make changes ...
git add .
git commit -m "msg"
git push              # End: upload
```

**Between devices:**
```bash
# Device A (end)
git add .
git commit -m "Work from Device A"
git push

# Device B (start)
git pull              # Get Device A's work
```

---

## Quick Reference

| Command | Description |
|---------|-------------|
| `git clone URL` | Download repository |
| `git status` | Check what changed |
| `git add .` | Stage all changes |
| `git commit -m "msg"` | Save changes with message |
| `git push` | Upload to GitHub |
| `git pull` | Download from GitHub |
| `git log` | View history |

---

**Remember:** Pull → Change → Add → Commit → Push