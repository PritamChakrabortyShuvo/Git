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