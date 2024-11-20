# Undoing Changes in Git

Sometimes you need to undo changes in your Git repository. Git provides powerful tools to help you revert commits, reset changes, or stash your work temporarily.

---

## **1. Viewing Status**
Show modified files in the working directory and files staged for your next commit:
```bash
git status
```

## **2. Unstaging Files**
Unstage a file while retaining the changes in the working directory:

```bash
git reset [file]

```
- Soft Reset:
Keeps changes in your working directory and staging area:
```bash
git reset --soft <commit-hash>

```

-  Mixed Reset (Default):
Keeps changes in your working directory but unstages them:
```bash
git reset <commit-hash>

```
-  Hard Reset:
Discards all changes and resets your working directory to a specified commit:
```bash
git reset --hard <commit-hash>
```

## **3. Viewing Differences**
Unstage a file while retaining the changes in the working directory:

```bash
git diff

```
- Viewing Staged Differences**

See the difference of what is changed but not staged:
```bash
git diff --staged
```

## **4. Reverting Commits**

Revert a specific commit without rewriting history. This creates a new commit that undoes the changes introduced by the specified commit:

Steps:
- Find the commit hash of the commit you want to revert:
```bash
git log
```
- Revert the commit:

```bash
git revert <commit-hash>
```

## **5. Stashing Changes**
Temporarily save your changes without committing them:
```bash
git stash
```
- Apply Stashed Changes:
To reapply the stashed changes
```bash
git stash apply
```

- List Stashes:
View all stashed changes:
```bash
git stash list
```
- Drop a Specific Stash:
Delete a specific stash:
```bash
git stash drop stash@{index}
```

## Git Commands Summary

| **Command**                         | **Description**                                                                       |
|-------------------------------------|---------------------------------------------------------------------------------------|
| `git status`                        | Show modified files in the working directory, and files staged for your next commit.  |
| `git add [file]`                    | Add a file as it looks now to your next commit (stage).                               |
| `git reset [file]`                  | Unstage a file while retaining the changes in the working directory.                  |
| `git diff`                          | Show the difference of what has changed but not staged.                               |
| `git diff --staged`                 | Show the difference of what is staged but not yet committed.                          |
| `git commit -m “[descriptive message]”` | Commit your staged content as a new commit snapshot.                                 |
| `git revert <commit-hash>`          | Undo a commit by creating a new commit that reverts the changes.                      |
| `git reset --soft <commit-hash>`    | Move the HEAD to a specific commit, keeping staged changes.                           |
| `git reset <commit-hash>`           | Move the HEAD to a specific commit, unstaging changes.                                |
| `git reset --hard <commit-hash>`    | Permanently reset to a specific commit and discard all changes.                       |
| `git stash`                         | Temporarily save uncommitted changes.                                                |
| `git stash apply`                   | Reapply stashed changes to your working directory.                                    |
| `git stash list`                    | View all stashed entries.                                                            |
| `git stash drop`                    | Remove a specific stash entry.                                                       |
