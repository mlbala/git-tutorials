# Collaborative Workflows in Git

Collaborative workflows enable teams to work together efficiently on the same repository. Key concepts include pull requests, code reviews, and team collaboration practices.

---

## **1. Pull Requests**
A pull request (PR) is a way to propose changes you've made in your branch to be merged into another branch (usually the main branch).

### **Steps to Create a Pull Request:**
1. **Push your branch to the remote repository**
```bash
   git push origin [branch-name]
```
- Go to the repository on your Git hosting platform
- Open a pull request 
  - Selecting your branch as the source and the target branch(e.g., ```main```) for merging.
  - Add a descriptive title and detailed description for the pull request
- Assign reviewers wait for the feedback.

### Best Practices for Pull Requests:
- Use a meaningful title and description for your PR.
- Keep changes small and focused to make reviews easier.
- Ensure all tests pass before creating a PR.

2. **Code Reviews**
Code reviews ensure quality and consistency across the codebase. They involve reviewing changes in pull requests before merging.

Best Practices for Code Reviews:
- For Authors:
  - Write meaningful commit messages.
  - Add comments to clarify complex code.
  - Respond promptly to feedback.

- For Reviewers:
  - Provide constructive feedback.
  - Focus on logic, readability, and adherence to standards.
  - Approve or request changes as necessary.

3. **Team Collaboration**
Effective team collaboration involves:

- Branching Strategies:
  - Feature Branches: ```feature/[branch-name]``` for a new features.
  - Bug Fixes: ```bugfix/[branch-name] ``` for resolving issues.
  - Release Branches : ```release/[branch-name]``` for preparing release.

- Rebasing and Merging:

- **Rebase your branch to keep a clean history:**
```bash
git rebase main
```

- **Merge branches after code reviews are complete:**
``` bash
git merge [branch-name]
``` 
- **Conflict Resolution:**
  Communicate with your team to resolve conflicts collaboratively.
  - Resolve conflicts in your text editor by choosing the desired changes.
  - Stage the resolved files:
  ```bash
    git add [file]
    ```
  - Complete the merge or rebase process
  ```bash
    git rebase --continue
    ```



## Example Workflow:

1. **Create a new feature branch**
```bash
git checkout -b feature/my-new-feature
```
2. **Make changes and commit them**
```bash
git add .
git commit -m "Add new feature"
```

3. **Push the branch to the remote repository**
```bash
git push origin feature/my-new-feature
```

4. Open a pull request for code review.
5. Address feedback and resolve conflicts.
6. Merge the branch into main once approved:
```
bash

git merge feature/my-new-feature
```

7. Delete the feature branch locally and remotely:
```bash

git branch -d feature/my-new-feature
git push origin --delete feature/my-new-feature
```

## Collaborative Workflows in Git

| **Workflow Component**    | **Description**                                                                                   | **Example Command**                                                                 |
|----------------------------|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| **Pull Requests**          | A way to propose changes in your branch to be merged into another branch (usually the main branch). | ```bash<br>git push origin [branch-name]```<br>(Push your branch to the remote repository) |
| **Code Reviews (Authors)** | Authors ensure high-quality changes by writing clear commit messages, clarifying complex code, and responding to feedback. | _No specific command needed; focus on communication._                              |
| **Code Reviews (Reviewers)** | Reviewers focus on logic, readability, and adherence to standards, providing constructive feedback. | _No specific command needed; focus on feedback._                                   |
| **Branching Strategies**   | Use specific branch names like `feature/branch-name`, `bugfix/branch-name`, or `release/branch-name` to organize work. | ```bash<br>git checkout -b feature/my-new-feature```                                |
| **Rebasing**               | Keep a clean history by rebasing your branch before merging.                                      | ```bash<br>git rebase main```                                                      |
| **Merging**                | Merge branches after completing code reviews.                                                    | ```bash<br>git merge [branch-name]```                                              |
| **Conflict Resolution**    | Communicate with your team to resolve merge conflicts collaboratively.                           | _No specific command; manual resolution of conflicts._                             |
| **Deleting a Branch**      | Delete a feature branch locally and remotely after merging.                                       | ```bash<br>git branch -d feature/my-new-feature```<br>```bash<br>git push origin --delete feature/my-new-feature``` |

---

### Notes
- **Pull Requests**: Include a title, description, and reviewers for better collaboration.
- **Code Reviews**: Both authors and reviewers play a role in maintaining quality and consistency.
- **Branching and Merging**: Use a structured workflow to avoid confusion and conflicts.
- **Conflict Resolution**: Prioritize communication and testing.


