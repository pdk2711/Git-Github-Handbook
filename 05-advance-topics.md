# 05 – Advanced Git Topics ⚙️

Ready to level up? In this section, we’ll cover some powerful Git tools like `stash`, `rebase`, `cherry-pick`, and `reset`. These aren’t needed every day, but when you *do* need them — they save lives (and codebases).

---

## 🧳 git stash – Save Changes for Later

Imagine you're mid-feature but need to switch tasks. Use `stash` to temporarily shelve changes.

```bash
git stash
```

Bring it back later:
```bash
git stash apply    # keep stash in history
git stash pop      # apply & remove from stash
```

List stashed items:

```bash
git stash list
```

---

## 🧙 git rebase – Clean Commit History
Rebase rewrites commit history. Great for keeping branches clean before merging.

```bash
git checkout feature
git rebase main
```
- This applies your feature commits on top of the latest main.
- Use with caution: don’t rebase public/shared branches.

---

## 🍒 git cherry-pick – Pick a Specific Commit
Want to apply one commit from another branch?
```bash
git cherry-pick <commit-hash>
```
✅ Use `git log` or `git log --oneline` to get the hash.

---

## 🔁 git reset – Undo Commits
### 🧼 Soft Reset: Keep changes, undo commits
```bash
git reset --soft HEAD~1
```

### 🧽 Mixed Reset: Unstage changes
```bash
git reset --mixed HEAD~1
```

### 💣 Hard Reset: Lose everything after a commit (DANGER!)
```bash
git reset --hard HEAD~1
```
> Only use --hard when you're absolutely sure — changes will be lost permanently.

---

## 🎯 Squashing Commits
To combine multiple commits into one:

```bash
git rebase -i HEAD~3
```

- Change pick to squash for 2nd & 3rd commits
- Save and write a new commit message

Result: Clean history, one neat commit!

---

## ⚠️ Pro Tips
- Rebase = rewriting history
- Reset = undo commits
- Cherry-pick = copy a commit
- Stash = pause your work

> ⚠️ NEVER use reset/rebase on shared branches without coordination.

## 🧙 Bonus: Useful Git Configs
```bash
git config --global alias.st status
git config --global alias.ci commit
git config --global alias.co checkout
git config --global alias.br branch
```
Now you can use:
```bash
git st
git ci -m "Shorter commit"
git co main
```

That’s it — you're now officially a Git ninja! 🥷💻








