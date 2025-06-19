# 03 – GitHub Essentials 🌐

Now that you can track changes locally using Git, let’s learn how to connect your project to GitHub and work with remote repositories.

---

## 🧠 What is GitHub?

GitHub is a **cloud-based hosting service** for Git repositories. It allows you to:
- Back up your code online
- Collaborate with others via pull requests
- Showcase your projects publicly or privately

---

## 🆕 Creating a GitHub Repository

1. Go to: [https://github.com](https://github.com)
2. Click the **+ New Repository** button
3. Name your repo (e.g., `my-first-repo`)
4. Do **not** initialize with a README if you're pushing an existing project
5. Click **Create Repository**

You'll see something like:
![image](https://github.com/user-attachments/assets/2a6beae0-9cac-44f5-a312-c16a3ab75581)


---

## 🔗 Connecting Local Repo to GitHub

In your terminal, inside your local repo folder:

```bash
git remote add origin https://github.com/pdk2711/my-first-repo //Repo address
```
To verify if it is added to the local repo folder:
```bash
git remote -v
```

## 📥 Cloning a Repository
If you want to download (clone) a repo to your local system:
```bash
git clone https://github.com/username/repo-name.git
```
This creates a folder and sets up the remote automatically.

## 🚀 Pushing Code to GitHub
This pushes the code from the local repository to the GitHub repository
```bash
git push -u origin main
```
> The -u flag sets origin as the default remote so next time you can just run `git push`

## 🔄 Pulling Changes from GitHub
To get the latest version of the repo:
```bash
git pull origin main
```

🧹 .gitignore: What Not to Track
Create a `.gitignore` file to tell Git what to ignore.
.gitignore generally consists of:
- *.log
- *.class
- node_modules/
- .env
files.

---

🔐 Bonus Tip: Personal Access Tokens
GitHub has deprecated password authentication for pushing. Use a Personal Access Token (PAT) instead:
- Go to Settings > Developer settings > Tokens
- Generate a classic token with repo scope
- Use that token as password when prompted by Git
