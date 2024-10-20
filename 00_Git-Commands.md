# Git Necessary Commands
## Git Commands: Working with the Staging Area
This section explores how to efficiently manage changes in Git before committing them. It covers commands like **`git add`** to stage changes, **`git restore --staged`** to unstage them. These tools allow for fine-tuning what gets included in each commit.

This section explores how to efficiently manage changes in Git before committing them. It covers commands like **`git add`** to stage changes, **`git restore --staged`** to unstage them. These tools allow for fine-tuning what gets included in each commit.
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
## Git Commands: Commit Management and Log Viewing
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
## Git Command: Removing Files from Working and Staging Areas
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
