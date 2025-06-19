# 01 – Getting Started with Git 🛠️

Welcome to the beginning of your Git journey! This section covers what Git is, why it’s useful, and how to get it set up on your system.

---

## 🌐 What is Git?

Git is a **version control system (VCS)** that tracks changes in your code or files. It helps you:
- Keep a history of your work
- Collaborate with others without breaking things
- Revert to older versions if something goes wrong

> Think of Git like “Save points” in a game — you can go back to any point in your project’s history.

---

## ❓Why Use Git?

- 🔄 Track every change you make
- 🧠 Undo mistakes quickly
- 👥 Collaborate without overwriting each other’s code
- 🗃️ Work on multiple features at the same time using **branches**

---

## ⚙️ Installing Git

### 🪟 On Windows:
1. Download from: [https://git-scm.com](https://git-scm.com)
2. Use default settings in the installer.
3. Open "Git Bash" from the Start Menu after installation.

### 🐧 On Linux (Debian/Ubuntu):
  ```bash
  sudo apt update
  sudo apt install git
```

### 🍎 On macOS:
Use Homebrew:
```bash
brew install git
```

### Check the version : 
`git --version`

## 🧑‍💻 Initial Git Setup 
After installing Git, tell it who you are — this info will be linked to every commit.
``` bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

You can confirm the configuration using:
``` bash
git config --list
```

