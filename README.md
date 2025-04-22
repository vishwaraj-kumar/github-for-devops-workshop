# 🚀 Git Commands Cheat Sheet for Beginners

This is a quick reference guide for using Git in your local system. These basic commands help you track, stage, commit, and push your code to GitHub.

---

## 🧱 1. Initialize Git Repository
- Creates an empty Git repository in your current directory.

  `git init`

---

## 🛠️ 2. Git Configuration
- Set global Git username/email for all repositories.
```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"`
```

- Set username/email only for the current local repository.
```bash
git config user.name "Your Name"
git config user.email "your@email.com"`
```

- Remove global Git username/email.
```bash
git config --global --unset user.name
git config --global --unset user.email
```

- Remove local Git username/email.
```bash
git config --local --unset user.name
git config --local --unset user.email
```

- Show all Git configuration settings (global + local).

  `git config --list`

- Show only global Git configuration settings.

  `git config --global --list`

- Show only local Git configuration for the current repo.

  `git config --local --list`

- Check current username/email (global or local depending on scope).
```bash
git config user.name
git config user.email
```

---

## 🔍 3. Check File Status
- Shows the current status of files — untracked, staged, or modified.

  `git status`

---

## ➕ 4. Add Files to Staging Area
- Moves a specific untracked file to the staging area.

  `git add <file_name>`

- Adds all untracked or modified files to the staging area in bulk.

  `git add .`

---

## 🔁 5. Unstage a Staged File
- Removes the file from the staging area and moves it back to unstaged.

  `git restore --staged <file_name>`

- Also removes the file from staging but retains it in the working directory.

  `git rm --cached <file_name>`

---

## ✅ 6. Commit Staged Files
- Commits all staged files with a commit message and moves them to tracked state.

  `git commit -m "your message"`

---

## 🧹 7. Remove or Restore Files
- Deletes a file from your working directory.

  `rm <file_name>`

- Restores a deleted or modified file from the last committed version.

  `git restore <file_name>`

---

## 🔙🕒 8. View History and Restore Old Version
- Check commit history:

  `git log --oneline`

- To restore file from old commit:

  `git checkout <commit-id> -- <file_name>`

- save old version as a new file:

  `git show <commit-id>:<file_name> > old-version-file-new_name`

---

## 📜 9. Clean Terminal & View Command History
- Clears the terminal screen.

  `clear`

- Displays a list of all previously used commands.

  `history`

---

## 🌿 10. Rename Branch from ‘master’ to ‘main’
- Renames the default branch to main.

  `git branch -M main`

---

# 🚀 Push Project to GitHub

## 🔗 11. Connect Remote Repository
- Links your local repo to a GitHub remote repository.

  `git remote add origin <repository-https-url>`

---

## 🔑 12. Use Personal Access Token (PAT) Instead of Password

**💡 Steps to Generate PAT:**
- Go to GitHub → Settings → Developer Settings → Personal Access Tokens → Tokens (classic)
- Click Generate new token (classic)
- Enter token name, set expiry, select repo scope, and click Generate Token
- Copy the token immediately and save it somewhere safe.

**🔄 Update Remote URL Using Token:**

  `git remote set-url origin https://<your-token>@<your-repo-url-without-https>`

---

## 🔍 13. Check Connected Remote
- Displays the remote repository URLs connected to your local repo.

  `git remote -v`

---

## 🛰️ 14. Push Your Code from Local to Remote Repo
- Pushes your committed code to the main branch of GitHub.

  `git push -u origin main`

The -u flag sets the upstream (tracking) relationship between your local branch and the remote branch.
After this, you can simply use `git push` or `git pull` without specifying the branch name.

- Pushes code to any specified branch (e.g., master, dev, etc.).

  `git push origin <branch_name>`

  ---

## 🔄 15. Pull Your Code from Remote Repo to Your Local Repo
- It updates your local repository with the latest changes from the remote GitHub repository.

  `git pull origin <your-branch-name>`

---

## 📥 16. Clone a Repository to Your System
- Downloads a complete copy of the remote repository to your local system.

  `git clone <repo-url>`