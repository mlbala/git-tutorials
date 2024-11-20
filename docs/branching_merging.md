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

# Resolving Merge Conflicts in Git

Merge conflicts occur when changes in two branches cannot be merged automatically. Git requires manual intervention to resolve the conflicts.

---

## **Steps to Resolve Merge Conflicts**

1. **Attempt to Merge Branches**
   Start by merging the branch into your current branch:
   ```bash
   git merge [branch-name]
   ```
2. **Identify Conflicted Files Git**
```bash
got status
```
3. **Open Conflicted Files**
Open the conflicted files in your text editor. You’ll see conflict markers like:

```<<<<<<< HEAD
Your changes
=======
Changes from the other branch
>>>>>>> [commit-hash]
```

4. **Resolve the Conflicts**

- Decide which changes to keep:
  - Keep your changes.
  - Keep the other branch’s changes.
  - Combine both changes.
- Edit the file to remove the conflict markers (<<<<<<<, =======, >>>>>>>).

5. **Mark the Conflicts as Resolved**

After resolving the conflicts in all files, stage them:
```bash
git add [file]
```

6. **Complete the Merge**
Finish the merge process by committing the changes:
```bash
git commit -m "Resolve merge conflicts"
```
### Abort the Merge (Optional)
If you want to cancel the merge and return to the state before the merge began:
```bash
git merge --abort

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
