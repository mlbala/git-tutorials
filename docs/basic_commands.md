# Step-by-Step Guide: Creating a Git Repository and Using Basic Git Commands

This guide walks you through creating a Git repository, initializing it, and using basic Git commands such as `git init`, `git add`, `git commit`, and `git status`.

---

## 📂 **1. Create a New Git Repository**

### **Steps:**
1. Open your terminal or command prompt.

2. Navigate to the directory where you want to create your repository:
   ```bash
   cd /path/to/your/folder
```
3. Initialize a new Git repository:
   ```bash
   git init
```
- This command sets up a new Git repository in the current directory. It creates a hidden .git folder to track changes.

## 📝 **2. Add Files to the Repository**
#### Steps:
- 1. Create or move files into your project directory.
- 2. Use the following command to add specific files to the staging area:
```bash
   git add filename 
   ```
- 3. To add all files in the directory to the staging area, use:
```bash
   git add . 
   ```
## ✅  **3. Commit Changes**
#### Steps:
- 1. Once files are staged, you can commit them with a message:
```bash
   git commit -m "Your commit message"
 
   ```
## 🔍 **4. Check the Status of Your Repository
**
#### Steps:
- 1. To see the current status of your repository, including staged and unstaged changes, use:
```bash
   git status
 
   ```

#  📤 **5. Commit Changes**

The `git push` command is used to upload your local repository changes to a remote repository. This is an essential step when collaborating with others or backing up your work.

---

## **Steps to Push Changes to a Remote Repository**

### 1. Add a Remote Repository
Before pushing, ensure your repository is linked to a remote repository (e.g., GitHub, GitLab). Use the following command to add a remote:
```bash
git remote add origin <remote-repository-URL>
```

### 2. Push to  Remote Repository
Before pushing, ensure your repository is linked to a remote repository (e.g., GitHub, GitLab). Use the following command to add a remote:
```bash
git push -u origin main

```

# 🎉 Congratulations!

You now know how to use the `git push` command to upload your work to a remote repository. 

Keep pushing changes regularly to:
- Collaborate effectively
- Safeguard your code

Happy coding! 🚀
