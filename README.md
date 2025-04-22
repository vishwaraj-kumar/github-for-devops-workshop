# 🚀 Git Commands Cheat Sheet for Beginners

This is a quick reference guide for using Git in your local system. These basic commands help you track, stage, commit, and push your code to GitHub.

---

## 🧱 1. Initialize Git Repository
```bash
git init
```
Creates an empty Git repository in your current directory.

---

## 🔍 2. Check File Status
```bash
git status
```
Shows the current status of files — untracked, staged, or modified.

---

## ➕ 3. Add Files to Staging Area
```bash
git add <file_name>
```
Moves a specific untracked file to the staging area.

```bash
git add .
```
Adds all untracked or modified files to the staging area in bulk.

---

## 🔁 4. Unstage a Staged File

```bash
git restore --staged <file_name>
```
Removes the file from the staging area and moves it back to unstaged.

```bash
git rm --cached <file_name>
```
Also removes the file from staging but retains it in the working directory.

---

## ✅ 5. Commit Staged Files

```bash
git commit -m "your message"
```
Commits all staged files with a commit message and moves them to tracked state.

---

## 🧹 6. Remove or Restore Files

```bash
rm <file_name>
```
Deletes a file from your working directory.

```bash
git restore <file_name>
```
Restores a deleted or modified file from the last committed version.

---

## 📜 7. Clean Terminal & View Command History

```bash
clear
```
Clears the terminal screen.

```bash
history
```
Displays a list of all previously used commands.

---

## 🌿 8. Rename Branch from ‘master’ to ‘main’

```bash
git branch -M main
```
Renames the default branch to main.

---

# 🚀 Push Project to GitHub

## 🔗 9. Connect Remote Repository

```bash
git remote add origin <repository-https-url>
```
Links your local repo to a GitHub remote repository.

---

## 🔑 10. Use Personal Access Token (PAT) Instead of Password

**💡 Steps to Generate PAT:**
- Go to GitHub → Settings → Developer Settings → Personal Access Tokens → Tokens (classic)
- Click Generate new token (classic)
- Enter token name, set expiry, select repo scope, and click Generate Token
- Copy the token immediately and save it somewhere safe.

**🔄 Update Remote URL Using Token:**

```bash
git remote set-url origin https://<your-token>@<your-repo-url-without-https>
```
---

## 🔍 11. Check Connected Remote

```bash
git remote -v
```
Displays the remote repository URLs connected to your local repo.

---

## 🛰️ 12. Push Your Code

```bash
git push -u origin main
```
Pushes your committed code to the main branch of GitHub.

The -u flag sets the upstream (tracking) relationship between your local branch and the remote branch.
After this, you can simply use git push or git pull without specifying the branch name.

```bash
git push origin <branch_name>
```
Pushes code to any specified branch (e.g., master, dev, etc.).