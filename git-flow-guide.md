# Git Commands & Workflow Cheat Sheet – Easy PG Project

## This guide helps our team use Git consistently and avoid conflicts while working

## 🔰 1. One-Time Setup (When You First Join the Project)

```bash
# Clone the repository
git clone <repo-url>
cd <repo-folder>

# Checkout the shared dev branch
git checkout dev
git pull origin dev

# Create and switch to your own feature branch
git checkout -b feature/<task>-<yourname>

# Example:
git checkout -b feature/nivedita-tenant-dashboard
```

---

## 🔁 2. Daily Workflow (For Every New Task or Feature)

### Step 1: Make sure you’re up-to-date

```bash
git checkout dev
git pull origin dev
```

### Step 2: Create a new feature branch

```bash
git checkout -b feature/<task>-<yourname>
```

### Step 3: Add and commit changes

```bash
git add .
git commit -m "Short, clear message (e.g. Add complaint form UI)"
```

### Step 4: Push your branch to GitHub

```bash
git push -u origin feature/<task>-<yourname>
```

---

## 📥 3. Raise a Pull Request (PR)

1. Go to GitHub → **Pull Requests → New Pull Request**
2. Base branch = `dev`, Compare = your feature branch
3. Add a clear **description** and **screenshots** (if UI)
4. Assign at least 1 **reviewer**
5. Once approved, merge it into `dev`

---

## 🔄 4. Keeping Your Feature Branch Updated (Avoid Conflicts)

If someone else merged code to `dev` while you were working:

```bash
# Save your work
git add .
git commit -m "WIP: saving progress"

# Switch to dev and pull latest
git checkout dev
git pull origin dev

# Go back to your branch and rebase or merge
git checkout feature/<your-branch>
git rebase dev    # or: git merge dev
```

---

## ✅ General Rules

- Always create branches from `dev`
- Never commit directly to `main` or `dev`
- Small commits > huge monolithic ones
- PRs should be reviewed before merging
- Add screenshots when you update the UI

---

## 🏷️ Suggested Branch Names

| Type     | Prefix Example                  |
| -------- | ------------------------------- |
| UI Page  | `feature/login-ui-nivedita`     |
| Backend  | `feature/payment-api-ravi`      |
| Bug Fix  | `bugfix/fix-nav-redirect-puja`  |
| Refactor | `refactor/dashboard-stats-amit` |

---

Happy Coding! 🚀
