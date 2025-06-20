# 🧾 Git & GitHub Cheatsheet

A handy reference of all the essential Git commands you’ll actually use. Memorize these, and you’re unstoppable. 💥
> Git Swiss Army knife 🛠️
---

## ⚙️ Setup

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --global color.ui auto
```

---

## 🏁 Getting Started
```bash
git init                  # Start a new repo
git clone <url>           # Download a repo
```

---

## 📦 Staging & Committing
```bash
git status                # Check what's changed
git add .                 # Stage all changes
git add <file>            # Stage specific file
git commit -m "message"   # Save changes
```
---

## 🔍 Logs & Diffs
```bash
git log                   # Full commit history
git log --oneline         # Compact view
git diff                  # Show unstaged changes
git diff --cached         # Show staged changes
```
---

## 🌿 Branching & Merging
```bash
git branch                # List branches
git checkout -b new-branch   # Create + switch
git checkout main         # Switch branch
git merge new-branch      # Merge branch into current
git branch -d new-branch  # Delete local branch
```
---

## 🌐 Remote Repos
```bash
git remote -v                      # Show remotes
git remote add origin <url>       # Connect repo
git push -u origin main           # Push first time
git push                          # Push changes
git pull                          # Pull latest changes
```
---

## 🧙‍♂️ Advanced Tricks
```bash
git stash                         # Save unfinished work
git stash pop                     # Reapply stashed work
git cherry-pick <commit-hash>     # Copy specific commit
git rebase main                   # Rebase on main
git reset --soft HEAD~1           # Undo commit (keep code)
```
---

## 🚀 Pull Requests (on GitHub)
1. Push a new branch 
2. Open GitHub → Compare & Pull Request
3. Add description, reviewers
4. Merge when approved!

---

## 🔁 Aliases (Optional, Time-saving)
```bash
git config --global alias.st status
git config --global alias.co checkout
git config --global alias.ci commit
git config --global alias.br branch
```
Now use:
```bash
git st
git co main
git ci -m "quick commit"
```
