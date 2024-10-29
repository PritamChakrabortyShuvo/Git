# Process of Initializing a Empty Local Repository
## Step 1. Create a Directory
Create a **empty Directory** named "**My-First-Repository**"
## Step 3. Initialize the Git Repository
Run the following command to initialize a new Git repository
```bash
    git init
```
This command creates a **hidden** **`.git`** **directory** in your project folder which **Git uses to track changes**.
## Step 2. Check the Status of the Empty Repository
To see the status of this run :
```bash
    git status
```
This will show you **which files are untracked**, **modified** or **staged**. For example
<div align="center">
    <img src="Diagrams/Empty-Git-Status.png" alt="Project Logo" width=70%>
</div>
The message you are seeing **indicates that you've initialized a new Git repository** but **have not yet made any commits**. Here’s a breakdown of what this means and the steps to move forward:

**Explanation of the Message**
- **On branch master :** You are currently on the default branch **called master** (or main in some configurations).
- **No commits yet :** This means you haven’t made any commits to your repository yet.
- **Nothing to commit (create/copy files and use "git add" to track) :** There are **no files in the staging area to commit**. Git is **prompting you to create** or **copy files** into your working directory, stage them & then commit.
## Step 3. Create or Modify Files
You can create a new file in your working area. For example
```bash
    echo "Hello, Git!" > example.txt
```
## Step 4. Check the Status Again
To see the **status of your files** use
```bash
    git status
```
This will show you which files are untracked, modified or staged.

<div align="center">
    <img src="Diagrams/Git-Status.png" alt="Project Logo" width=70%>
</div>

## Step 5. Stage the Changes
To add the file to the staging area, use
```bash
    git add example.txt
```
You can also **stage all changes** in the working area with
```bash
    git add .
```
## Step 5. Check the Status Again
Run **`git status`** to confirm that the file is now **staged for commit**. It should appear under "**`Changes to be committed.`**"
```bash
    git status
```
<div align="center">
    <img src="Diagrams/Git-Status-02.png" alt="Project Logo" width=70%>
</div>

## Step 6. Committing Changes
Once you're ready to save your changes run
```bash
    git commit -m "Initial commit"
```
The **`-m`** **flag allows you to add a commit message** inline describing the changes made.
## Step 7. Verify the Commit
To **confirm that your changes** have been **committed** you can use
```bash
    git log
```
<div align="center">
    <img src="Diagrams/Git-Log.png" alt="Project Logo" width=70%>
</div>

This will display a **log of commits** made in the repository including the **latest commit**.

## Workflow 
<div align="center">
    <img src="Diagrams/Git-Areas.png" alt="Project Logo" width=90%>
</div>
