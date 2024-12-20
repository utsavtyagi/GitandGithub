
# Git and GitHub

## 1. Introduction to Git and GitHub

### What is Git?
Git is a distributed version control system that helps track changes in your code. It allows collaboration among multiple developers and keeps a history of all changes made to a project.

### What is GitHub?
GitHub is a web-based platform that uses Git for version control and provides a space to host and manage your code repositories. It also facilitates collaboration with features like pull requests, issue tracking, and code reviews.

---

## 2. Installing Git

### For Windows:
1. Download Git from [git-scm.com](https://git-scm.com/).
2. Run the installer and follow the prompts:
   - Choose the default branch name (main).
   - Configure PATH settings (use default settings).
   - Complete the installation.



### For Linux:
- Use your package manager to install Git:
  ```bash
  sudo dnf update
  sudo dnf install git
  ```

---

## 3. Setting Up Git

After installing Git, configure your user information:
```bash
git config --global user.name "Your Name"
git config --global user.email "youremail@example.com"
```

Verify your configuration:
```bash
git config --list
```

---

## 4. Installing Git Extension in Visual Studio Code

1. Open Visual Studio Code.
2. Go to the Extensions view by clicking the Extensions icon or pressing `Ctrl+Shift+X`.
3. Search for "GitLens" or "GitHub" in the Extensions Marketplace.
4. Click **Install** to add the extensions.

---

## 5. Basic Git Commands with Examples

### 1. Initialize a Repository
Create a new Git repository:
```bash
git init
```
This creates a `.git` folder in your project directory.

### 2. Check Repository Status
Check the status of your repository:
```bash
git status
```
This shows untracked, modified, or staged files.

### 3. Add Files to Staging Area
Add a specific file to the staging area:
```bash
git add file_name
```
Add all files:
```bash
git add .
```

### 4. Commit Changes
Commit staged changes with a message:
```bash
git commit -m "Your commit message"
```

### 5. View Commit History
View the commit history:
```bash
git log
```
View a simplified commit history:
```bash
git log --oneline
```

### 6. Checkout a Branch
Switch to an existing branch:
```bash
git checkout branch_name
```
Create and switch to a new branch:
```bash
git checkout -b new_branch_name
```

---

## 6. Working with Remote Repositories

### 1. Add a Remote Repository
Link a remote repository:
```bash
git remote add origin https://github.com/your-username/repo-name.git
```

### 2. Push Changes
Push changes to the remote repository:
```bash
git push -u origin branch_name
```

### 3. Pull Changes
Fetch and merge changes from the remote repository:
```bash
git pull origin branch_name
```

### 4. Clone a Repository
Copy a remote repository to your local machine:
```bash
git clone https://github.com/username/repo-name.git
```

### 5. Sync Forked Repository
If you have forked a repository and want to sync it with the original (upstream) repository:
```bash
git remote add upstream https://github.com/original-owner/original-repo.git
git fetch upstream
git merge upstream/main
```

---

## 7. Forking and Contributing to Repositories

### 1. Fork a Repository
- Go to the repository on GitHub you want to contribute to.
- Click the **Fork** button to create a copy of the repository in your account.

### 2. Clone Your Forked Repository
Download your forked repository to your local machine:
```bash
git clone https://github.com/your-username/repo-name.git
```

### 3. Make Changes Locally
Create a new branch for your changes:
```bash
git checkout -b feature-branch
```
Make your changes and commit them:
```bash
git add .
git commit -m "Describe your changes"
```

### 4. Push Changes to Your Fork
Push your changes to your forked repository:
```bash
git push origin feature-branch
```

### 5. Create a Pull Request
- Navigate to the original repository on GitHub.
- Click **Pull Request** and select the branch you want to merge.
- Add a description of your changes and submit the pull request.

---

## 8. Merging Branches

### Merge a Branch into Another
Switch to the branch you want to merge into (e.g., main):
```bash
git checkout main
```
Merge the feature branch:
```bash
git merge feature-branch
```

Resolve conflicts if they arise, then commit the merge.

### Delete a Merged Branch
After merging, delete the feature branch:
```bash
git branch -d feature-branch
```

---

## 9. Using .gitignore

A `.gitignore` file specifies files or directories that Git should ignore. Example:
```plaintext
node_modules/
*.log
.env
```

Create a `.gitignore` file in the root of your repository and list files or patterns to ignore.

---

## 10. Additional Commands

### Undo Changes
- Undo unstaged changes:
  ```bash
  git checkout -- file_name
  ```
- Remove staged changes:
  ```bash
  git reset HEAD file_name
  ```
- Undo the last commit:
  ```bash
  git reset --soft HEAD~1
  ```

### Stash Changes
Save changes temporarily without committing:
```bash
git stash
```
Apply stashed changes:
```bash
git stash apply
```

---

## 11. Best Practices
- Commit frequently with clear messages.
- Always pull the latest changes before starting new work.
- Use branches for new features or bug fixes.
- Regularly push your work to avoid data loss.

---

By following this guide, you can confidently start using Git and GitHub for version control and collaboration!
