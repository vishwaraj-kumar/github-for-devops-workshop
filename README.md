# 🚀 Git Commands Cheat Sheet for Beginners

This is a quick reference guide for using Git in your local system. These basic commands help you track, stage, commit, and push your code to GitHub.

---

## 🧱 1. Initialize Git Repository
- Creates an empty Git repository in your current directory.

  `git init`

---

## 🔍 2. Check File Status
- Shows the current status of files — untracked, staged, or modified.

  `git status`

---

## ➕ 3. Add Files to Staging Area
- Moves a specific untracked file to the staging area.

`git add <file_name>`

- Adds all untracked or modified files to the staging area in bulk.

`git add .`

---

## 🔁 4. Unstage a Staged File
- Removes the file from the staging area and moves it back to unstaged.

`git restore --staged <file_name>`

- Also removes the file from staging but retains it in the working directory.

`git rm --cached <file_name>`

---

## ✅ 5. Commit Staged Files
- Commits all staged files with a commit message and moves them to tracked state.

`git commit -m "your message"`

---

## 🧹 6. Remove or Restore Files
- Deletes a file from your working directory.

`rm <file_name>`

- Restores a deleted or modified file from the last committed version.

`git restore <file_name>`

---

## 📜 7. Clean Terminal & View Command History
- Clears the terminal screen.

`clear`

- Displays a list of all previously used commands.

`history`

---

## 🌿 8. Rename Branch from ‘master’ to ‘main’
- Renames the default branch to main.

`git branch -M main`

---

# 🚀 Push Project to GitHub

## 🔗 9. Connect Remote Repository
- Links your local repo to a GitHub remote repository.

`git remote add origin <repository-https-url>`

---

## 🔑 10. Use Personal Access Token (PAT) Instead of Password

**💡 Steps to Generate PAT:**
- Go to GitHub → Settings → Developer Settings → Personal Access Tokens → Tokens (classic)
- Click Generate new token (classic)
- Enter token name, set expiry, select repo scope, and click Generate Token
- Copy the token immediately and save it somewhere safe.

**🔄 Update Remote URL Using Token:**

`git remote set-url origin https://<your-token>@<your-repo-url-without-https>`

---

## 🔍 11. Check Connected Remote
- Displays the remote repository URLs connected to your local repo.

`git remote -v`

---

## 🛰️ 12. Push Your Code
- Pushes your committed code to the main branch of GitHub.

`git push -u origin main`

The -u flag sets the upstream (tracking) relationship between your local branch and the remote branch.
After this, you can simply use `git push` or `git pull` without specifying the branch name.

- Pushes code to any specified branch (e.g., master, dev, etc.).

`git push origin <branch_name>`
