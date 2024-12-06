
# GitHub Repository Creation and File Upload

This repository guides you through the steps to create a new GitHub repository, add a file (`hello.txt`), commit it, and set up the repository with `main` as the default branch using GitHub CLI (`gh`) and Git.

## Prerequisites

Before starting, ensure that you have the following tools installed on your system:

- **[Chocolatey](https://chocolatey.org/)**
- **[Git](https://git-scm.com/)**
- **[GitHub CLI (`gh`)](https://cli.github.com/)**

If you don't have GitHub CLI installed, you can install it using Chocolatey with the following command:

```bash
choco install gh -y
```

## Steps to Create a Repository and Push Files

### 1. **Install GitHub CLI**
   - Install the `gh` tool via Chocolatey:

   ```bash
   choco install gh -y
   ```

### 2. **Open a New Command Prompt**
   - Open a new Command Prompt to start working:

   ```bash
   start cmd && exit
   ```

### 3. **Login to GitHub Using `gh`**
   - Log in to your GitHub account using the GitHub CLI:

   ```bash
   gh auth login
   ```

   Follow the prompts to authenticate.

### 4. **Create a New Directory and Initialize Git**
   - Create a new directory, navigate into it, and initialize a new Git repository:

   ```bash
   mkdir test
   cd test
   git init
   ```

### 5. **Create and Add `hello.txt`**
   - Create the `hello.txt` file with the message "Hello, world!" and add it to the Git staging area:

   ```bash
   echo "Hello, world!" > hello.txt
   git add hello.txt
   ```

### 6. **Commit the File**
   - Commit the file with a message:

   ```bash
   git commit -m "Initial commit with hello.txt"
   ```

### 7. **Create a New GitHub Repository**
   - Create a new public repository on GitHub using the GitHub CLI. Replace `USERNAME` with your GitHub username:

   ```bash
   gh repo create test --public
   ```

### 8. **Add Remote Origin**
   - Add the remote GitHub repository to your local Git configuration. Replace `USERNAME` with your GitHub username:

   ```bash
   git remote add origin https://github.com/USERNAME/test.git
   ```

### 9. **Push Changes to GitHub**
   - Push the changes to the `main` branch of the GitHub repository:

   ```bash
   git push -u origin main
   ```

### 10. **Rename the Default Branch to `main`**
   - If your local branch is named `master`, rename it to `main`:

   ```bash
   git branch -m master main
   ```

   - Switch to the `main` branch (if not already on it):

   ```bash
   git checkout main
   ```

### 11. **Push the `main` Branch to GitHub**
   - Push the newly renamed `main` branch to GitHub:

   ```bash
   git push origin main
   ```

### 12. **Set the Default Branch on GitHub**
   - Set `main` as the default branch using GitHub CLI:

   ```bash
   git remote set-head origin main
   ```

### 13. **Delete the Remote `master` Branch**
   - If `master` still exists on the remote repository, delete it:

   ```bash
   git push origin --delete master
   ```

### 14. **Confirm Default Branch Change on GitHub**
   - Set the default branch on GitHub to `main` using the GitHub CLI:

   ```bash
   gh repo edit --default-branch main
   ```

---

## Conclusion

After completing these steps, you will have created a new GitHub repository, added a file (`hello.txt`), and pushed it to the `main` branch. The `master` branch has been deleted, and `main` is now the default branch for the repository.

---

### Additional Notes:
- If you encounter any issues, make sure GitHub CLI and Git are properly installed and configured.
- This guide assumes that you have permission to create and manage repositories on GitHub.
