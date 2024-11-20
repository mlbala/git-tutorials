## **Branching and Merging in Git**

Learn how to manage branches and view commit history using Git commands.

---

### **1. Listing Branches**
List all branches in your repository. A `*` will appear next to the currently active branch:
```bash
git branch
```
### **2. Creating a New Branch**
Create a new branch at the current commit:
```bash
git branch [branch-name]
```

### **3. Switching Branches**
Switch to another branch and check it out into your working directory:
```bash
git checkout [branch-name]
```
- Contiune add modify code/files then commit it
```bash
git add .
git commit -m "commmit message"
```
### **4. Merging Branches**
Merge the specified branch’s history into the current one:
```bash
git merge [branch]

```

### **5. Viewing Commit History**
Show all commits in the current branch’s history:
```bash
git log
```

- View Detailed history To show patches (diffs) for the last 3 commits:
``` bash
git log -p -3
```

## Git Branching and History Commands Summary

| **Command**                  | **Description**                                                                 |
|------------------------------|---------------------------------------------------------------------------------|
| `git branch`                | List all branches. A `*` will appear next to the currently active branch.       |
| `git branch [branch-name]`  | Create a new branch at the current commit.                                       |
| `git checkout [branch-name]` | Switch to another branch and check it out into your working directory.          |
| `git merge [branch]`         | Merge the specified branch’s history into the current branch.                   |
| `git log`                    | Show all commits in the current branch’s history.                               |
| `git log -p -3`              | Show patches (diffs) for the last 3 commits in the current branch’s history.     |
