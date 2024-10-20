# Git Necessary Commands

## Git Commands: Working with the Staging Area
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