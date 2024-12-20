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
---
## Git Commands : Commit Management and Log Viewing
Creates a new commit with the changes that have been staged, using the provided commit message.
```bash
    git commit -m "Your Commit Message"
```
This command stages and commits all modified and deleted tracked files with a single-line message.
```bash
    git commit -a -m "Your Commit Message"
```

Modifies the last commit by adding any staged changes and replacing the commit message with a new one.
```bash
    git commit --amend -m "Your Updated Commit Message"
```
**Note :** *We must **force push** it after **amending** by **`git push --force origin main`**.*

This command shows the differences between changes in the working directory and the repository **highlighting modified lines**.
```bash
    git diff
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
- Press **`space`** to show more recent commits
- Press **`q`** to quit the log and return to the terminal.

Shows the current status of the working directory and staging area, indicating which changes are staged, unstaged, or untracked.
```bash
    git status
```
---
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
---
## Git Command : Branches
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
---
## Git Command : Merging
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
---
## Git Command : Push
The following command pushes the changes in your current branch to the origin remote and the main branch
```bash
    git push origin main
```
When pushing to a remote for the first time
```bash
    git push -u origin main
```
The **`-u`** flag sets **`origin/main`** as the **upstream branch** for future pushes & pulls so you can just use **`git push`** in the future without specifying the **remote** & **branch**.

In certain situations (e.g., when your local branch is not in sync with the remote, or you've rewritten history with **`git rebase`**), you might need to use **`--force`** :
```bash
    git push --force origin main
```
**Note :** This overwrites the remote branch, potentially losing changes made by others.

---
## Git Command : Cloning
The basic command for Git cloning is
```bash
    git clone <repository-url>
```
- **`repository-url` :** This is the **URL** of the **remote repository** you want to clone. It can be provided in either **`HTTPS`**, **`SSH`** or **GIT protocol formats**.

**Example using `HTTPS`**
```bash
    git clone https://github.com/your-username/your-repo.git
```
**Example using `SSH`**
```bash
    git clone git@github.com:your-username/your-repo.git
```
If you want to clone a specific branch you can add the **`-b`** option followed by the branch name
```bash
    git clone -b branch-name https://github.com/your-username/your-repo.git
```
After cloning, the repository is downloaded to your local machine, and you can start working on it.

---
## Git Command : Fetch
Fetches all branches from the remote repository, without merging them into your local branches.
```bash
    git fetch
```
Specify a particular remote repository to fetch from
```bash
    git fetch <remote_name>
```
Fetch a Specific Branch
```bash
    git fetch origin <branch_name>
```
If you have multiple remotes, this fetches from all configured remotes
```bash
    git fetch --all
```
Shows what changes would be fetched from the remote without actually downloading them
```bash
    git fetch --dry-run
```
To check fetched updates for specific branch
```bash
    git log HEAD..origin/<branch-name>
```
---
## Git Command : Pull
If you're working on the main branch
```bash
    git pull
```
To pull changes from the **`main branch`** of the remote repository 
```bash
    git pull <repository_name> <branch_name>
```
---
## Git Command : Rebase
Rebase your current branch onto another branch
```bash
    git checkout feature-branch
```
This command moves the feature-branch on top of the latest commits from the main branch and re-applies your changes.
```bash
    git rebase main
```
To Restores branch to the exact state it was in before the rebase began.
```bash
    git rebase --abort
```
---
## Git Command : Squash
Squash Commits Using `git rebase -i`
### Step 1. Start an Interactive Rebase
To squash commits, we initiate an interactive rebase using the following command:
```bash
    git rebase -i HEAD~n
```
**Note :** Replace **`n`** with the number of recent commits you want to squash. For example, **`git rebase -i HEAD~3`** would open the **last 3 commits** in interactive mode.
### Step 2. Mark Commits for Squashing
Once you run the command, Git will open your editor with a list of commits like this
```sql
    pick abc123 First commit
    pick def456 Second commit
    pick ghi789 Third commit
```
**Note :** Change the word pick to **`squash`** (or just s) for the commits you want to squash into the previous one
```sql
    pick abc123 First commit
    squash def456 Second commit
    squah ghi789 Third commit
```
### Step 4. Edit the Commit Message
After marking commits for squashing, Git will prompt you to edit the commit message. You can Combine all messages or use a single message to describe the squashed commit.
### Step 5. Save and Finish
Save and close the editor, and Git will squash the commits into one.

---
## Git Command : Cherry Pick
To apply the changes of a specific commit from another branch to the current branch
```bash
    git cherry-pick <commit-hash>
```
**Note :** Replace **`<commit-hash>`** with the hash of the commit you want to pick.

To apply multiple specific commits
```bash
    git cherry-pick <commit-hash1> <commit-hash2>
```
List the commit hashes you want to apply, separated by spaces.

---
## Git Command : Reset 
Moves the branch pointer to the specified commit but keeps all changes staged.
```bash
    git reset --soft <commit-hash>
```
Moves the branch pointer to the specified commit, unstages all changes but keeps them in the working directory.
```bash
    git reset <commit-hash>
```
Moves the branch pointer to the specified commit and discards all changes in both the staging area and the working directory.
```bash
    git reset --hard <commit-hash>
```
Resets to the latest commit unstaging any changes but keeping them in the working directory.
```bash
    git reset HEAD
```
---
## Git Command : Revert
This command will create a new commit that undoes the changes made by **`<commit-hash>`**.
```bash
    git revert <commit-hash>
```
Git will also prompt for a commit message, explaining that this new commit is a **"revert."**
### Revert Command Example 
Check your commit history
```bash
    git log --oneline
```
Output might look like this
```bash
    3f3bcae (HEAD -> main) Added new feature
    2d8c6a5 Fixed a bug in login
    1a2b3c4 Initial commit
```
Revert the second commit `(2d8c6a5)`. This creates a new commit that undoes the changes introduced by **`2d8c6a5`**.
```bash
    git revert 2d8c6a5
```
Commit log after revert
```bash
    git log --oneline
```
Now it might look like this
```bash
    a1b2c3d Revert "Fixed a bug in login"
    3f3bcae Added new feature
    2d8c6a5 Fixed a bug in login
    1a2b3c4 Initial commit
```
The original **"`Fixed a bug in login`"** commit is still in the history but the changes it introduced have been undone by the new "Revert" commit.

---
## Git Command : Reflog
This shows a list of recent changes to HEAD.
```bash
    git reflog
```
### Step 1. Commit a change
```bash
    git commit -m "Added a new feature"
```
### Step 2. Accidentally reset hard to a previous commit.
```bash
    git reset --hard HEAD~1
```
Now the latest commit is gone from the history.
### Step 3. Use reflog to find the lost commit
This shows a list of recent changes to HEAD. Find the hash of the commit you lost.
```bash
    git reflog
```
### Step 4. Recover the commit
```bash
    git reset --hard <commit-hash>
```
---
## Example of Git Flow
### 1. Creating a Blob
- When you add a file like **`file.txt`** Git calculates its **SHA-1 hash** & stores it in **`.git/objects`**.
- Using **`git hash-object -w file.txt`**, Git writes the file's content as a blob object.
### 2. Storing in `.git/objects`
- Let's say the **SHA-1 hash** of **`file.txt`** is **`bea8d7fee8e7b11c2235ca623935e6ccccd8bac3`**. Git will store this in **`.git/objects/be/a8d7...`**, where **be** is the first two characters and **a8d7**... is the rest of the hViewing the Blobash.
### 3. Viewing the Blob
We can view the contents of the blob using
```bash
    git cat-file -p bea8d7
```
This will show 
```bash
    "This is my first story"
```
### 4. Looking at Other Objects:
We can also inspect other objects, like commits or trees, using **`git cat-file -p <hash>`**.