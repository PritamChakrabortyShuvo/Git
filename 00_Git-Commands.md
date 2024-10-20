# Git Necessary Commands
## Git Commands : Working with the Staging Area
Stages all modified and new files in the current directory and its subdirectories for the next commit.
```bash
    git add .
```
Stages a specific file for the next commit.
 ```bash
    git add filename
```
Stages all files in the specified directory for the next commit.
```bash
    git add Directory_Name/
```
Unstages a previously staged file keeping its changes in the working directory.
```bash
    git restore --staged filename
```
Discards changes in the specified file in the working directory restoring it to the last committed state.
```bash
    git restore filename
```
## Git Commands : Commit Management and Log Viewing
Creates a new commit with the changes that have been staged, using the provided commit message.
```bash
    git commit -m "Your commit message here"
```
Modifies the last commit by adding any staged changes and replacing the commit message with a new one.
```bash
    git commit --amend -m "Updated commit message"
```
Used to display the commit history of a Git repository.
```bash
    git log
```
Displays a compact view of the commit history, showing each commit on a single line with its abbreviated hash and message.
```bash
    git log --oneline
```
Shows the last <number> of commits.
```bash
    git log -n <number>
```
Displays a graphical representation of the commit history, useful for visualizing branching and merging.
```bash
    git log --graph
```
Filters the commit history to show only commits made by a specific author.
```bash
    git log --author="name"
```
Shows the current status of the working directory and staging area, indicating which changes are staged, unstaged, or untracked.
```bash
    git status
```
## Git Command : Removing Files from Working and Staging Areas
To delete a specific file from both the working directory and the repository run
```bash
    git rm filename
```
To remove an entire directory and its contents
```bash
    git rm -r directoryname/
```
If a file has been modified and we want to remove it without checking for changes (which would normally prevent deletion):
```bash
    git rm -f filename
```
If we want to unstage a file (remove it from the staging area) without deleting it from the working directory, we can use
```bash
    git rm --cached filename
```
### Important Considerations:
- After using **`git rm`** we must commit the changes to finalize the removal in the repository.
- Be cautious when using **`git rm`** especially with the force option as it permanently deletes files from the working directory & may lead to data loss if not handled properly.

## Git Commands : Branches
To create a new branch.
```bash
    git branch <branch_name>
```
Switch to an existing branch.
```bash
    git checkout <branch_name>
```
Create a new branch and switch to it. 
```bash
    git checkout -b <new_branch_name>
```
To delete a branch.
```bash
    git branch -d <branch_name>
```
**Note :** After merging, it's good practice to delete the branch.

If the branch hasn't been merged yet & you still want to delete it.
```bash
    git branch -D <branch-name>
```
To rename the current branch.
```bash
    git branch -m <new-branch-name>
```
To push a local branch to the remote repository.
```bash
    git push origin <branch-name>
```
To pull changes from a specific branch on the remote repository.
```bash
    git pull origin <branch-name>
```
When you create a new branch and push it to the remote you can also set it to track the remote branch.
```bash
    git push -u origin <branch-name>
```
To list all branches.
```bash
    git branch
```
## Git Commands : Merging
### Merging a Branch into the Current Branch
1. First, switch to the branch you want to merge into (often the **`main branch`**)
```bash
    git checkout <target-branch>
```
2. Then, merge the branch you want to bring changes from
```bash
    git merge <source-branch>
```
**Example :** Merging **`feature-login`** into **`main`**
```bash
    git checkout main
```
Then,
```bash
    git merge feature-login
```
### Aborting a Merge
If you run into conflicts or decide not to complete the merge you can cancel it by using
```bash
    git merge --abort
```