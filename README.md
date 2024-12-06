
# GitHub Repository Creation and File Upload with GitHub CLI

This repository demonstrates the process of creating a GitHub repository, uploading a file (`hello.txt`), and setting the default branch to `main` using GitHub CLI (`gh`) and Git.

## Prerequisites

Before starting, ensure that you have the following tools installed on your system:

- **[Chocolatey](https://chocolatey.org/)**
- **[Git](https://git-scm.com/)**
- **[GitHub CLI (`gh`)](https://cli.github.com/)**

If you don't have GitHub CLI installed, you can install it using Chocolatey:

```bash
choco install gh -y
```

## Steps to Create a Repository and Upload Files

### 1. **Install GitHub CLI (`gh`)**
Install the `gh` tool via Chocolatey:

```bash
choco install gh -y
```

### 2. **Open a New Command Prompt**
To open a new Command Prompt window, run:

```bash
start cmd && exit
```

### 3. **Check the `gh` Version**
Verify that GitHub CLI is installed successfully by checking the version:

```bash
gh --version
```

### 4. **Login to GitHub Using GitHub CLI**
Authenticate with your GitHub account using the following command:

```bash
gh auth login
```

Follow the prompts to authenticate via the web browser.

### 5. **Create a New Directory and Initialize a Git Repository**
Create a new directory and navigate into it, then initialize it as a Git repository:

```bash
mkdir test
cd test
git init
```

### 6. **Create the `hello.txt` File and Add It to the Staging Area**
Create the file `hello.txt` with the message "Hello, world!" and add it to the Git staging area:

```bash
echo "Hello, world!" > hello.txt
git add hello.txt
```

### 7. **Commit the File**
Commit the changes to the local Git repository:

```bash
git commit -m "Initial commit with hello.txt"
```

### 8. **Create a New GitHub Repository**
Create a new public repository on GitHub using GitHub CLI:

```bash
gh repo create test --public
```

### 9. **Set the Remote URL**
Add the remote GitHub repository URL to your local Git configuration. Replace `USERNAME` with your GitHub username:

```bash
git remote add origin https://github.com/USERNAME/test.git
```

### 10. **Rename the Branch from `master` to `main`**
Rename the default branch from `master` to `main`:

```bash
git branch -m master main
```

### 11. **Push the Changes to the `main` Branch**
Push the `main` branch to the GitHub repository:

```bash
git push origin main
```

### 12. **Set the Default Branch to `main` on GitHub**
Set the default branch to `main` on the remote GitHub repository:

```bash
git remote set-head origin main
```

### 13. **Update the Repository on GitHub to Use `main` as the Default Branch**
Use GitHub CLI to set the default branch to `main`:

```bash
gh repo edit --default-branch main
```

## Conclusion

By following these steps, you'll have created a GitHub repository, added a `hello.txt` file, committed it, and set the default branch to `main`. You can now continue working with your repository on GitHub.

---

### Additional Notes:
- Replace `USERNAME` with your actual GitHub username when running the commands.
- If any issues arise, ensure that GitHub CLI and Git are correctly installed and configured.
