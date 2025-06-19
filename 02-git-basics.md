# 02 – Git Basics 🚦

Now that Git is installed and configured, let's start using it to manage a project. This section covers: 
- creating a Git repository
- tracking files
- committing changes
- exploring the commit history.

---

## 🛠️ Initializing a Git Repository

To turn any folder into a Git project:

```bash
mkdir hello-git // Creates a directory named hello-git
cd hello-git // Opens the directory
git init // Initilizes the directory in git
```
---

## 📁 Git Workflow
![Git Workflow Image](https://media2.dev.to/dynamic/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Fvpxeexqyfvf4hw3zxtbn.png)

| Area | Meaning |
|------|---------|
| Working Directory | Your actual project files |
| Staging Area | Temporary storage before a commit |
| Repository | Final saved snapshot (commit) |

## 📝 Tracking Files with `git add`
Once you modify or create files, Git sees them as untracked. 
You need to add them to staging:
```bash
git add filename
```
To add everything:
```bash
git add .
```

## 💾 Saving Changes with `git commit`
Once files are staged:
```bash
git commit -m "Meaningful commit message"
```

## 🔄 Checking Status with `git status`
This shows:
- Untracked files
- Staged changes
- Files with changes not yet staged
  
✅ Always run this before committing.

```bash
git status
```

## 📚 Viewing History with `git log`

```bash
git log
```
Use `q` to quit log view.

## 🧐 Viewing Changes with `git diff`

Before staging:
```bash
git diff filename
```

After staging (compare staged vs last commit):
```bash
git diff --cached filename
```

## 🔄 Summary of Common Commands
```bash
git init                     // Start a new Git repo
git add filename             // Stage a file
git add .                    // Stage all changes
git commit -m "message"      // Commit staged changes
git status                   // Show current state
git log                      // Show commit history
git diff                     // See what's changed
```
