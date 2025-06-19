# 04 – Collaboration with Git & GitHub 🤝

Git is not just for solo projects — it's a powerful tool for **team collaboration**. This section covers how to work with branches, collaborate via GitHub, and manage pull requests.

---

## 🌿 What is a Branch?

A **branch** is like a parallel universe of your code. You can safely make changes without affecting the `main` branch.

```bash
git branch branch-name
```
Switch to it:
```bash
git checkout branch-name
```
OR do both in one step:
```bash
git checkout -b branch-name
```
---
## 🔁 Branch Workflow

1. Create a new branch
2. Make changes and commit
3. Push the branch to GitHub
4. Open a Pull Request (PR)
5. Review & merge into main

---

## 📤 Pushing a Branch to GitHub
```bash
git push -u origin branch-name
```
This will create a new branch on GitHub. You’ll get a prompt to open a Pull Request (PR).

---

## 🔄 Merging Branches Locally
Switch back to main:

```bash
git checkout main
git merge branch-name
```
If there are no conflicts, the branch will be merged.




