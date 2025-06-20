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

## 🗺️ Visual Git Collaboration Workflow

```
main
 │
 ├──➤ git checkout -b feature-xyz
 │       │
 │       ▼
 │   Work on feature
 │       │
 │       ▼
 │   git add . && git commit -m "message"
 │       │
 │       ▼
 │   git push -u origin feature-xyz
 │       │
 │       ▼
 │  🔁 Open Pull Request on GitHub
 │       │
 │       ▼
 │   ✅ Review & Merge PR
 │       │
 │       ▼
 └────➤ git checkout main
         git pull origin main
         git branch -d feature-xyz
         git push origin --delete feature-xyz
```

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

---

## ⚠️ Merge Conflicts

If two branches change the same line, Git will ask you to resolve a conflict.

e.g.
```bash
<<<<<<< HEAD
This is main branch code
=======
This is feature branch code
>>>>>>> feature-branch
```
Just edit it, delete the conflict markers (<<<<<<<, =======, >>>>>>>), and commit again.

---


## 📌 Pull Requests (PRs) on GitHub

- A Pull Request lets someone propose changes to a repo.
- Steps:
    1. Push your branch
    2. Go to GitHub repo
    3. Click Compare & Pull Request
    4. Add a title and description
    5. Click Create Pull Request

- The team can now:
    * Review changes
    * Leave comments
    * Request changes
    * Merge the PR

---

## 🚨 Delete Merged Branches (Best Practice)
Once merged:

```bash
git branch -d feature-login         # Local delete
git push origin --delete feature-login  # Remote delete
```
---

💡 Tip: Naming Branches
Use clear names:
- feature/login-page
- bugfix/typo-in-readme
- hotfix/deploy-error
