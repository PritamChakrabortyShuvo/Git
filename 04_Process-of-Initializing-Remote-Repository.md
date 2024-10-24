# Process of Initializing a Remote Repository
## Step 1. Initialize a Local Repository
Navigate to the directory where you want to create the repository. After that initialize the repository
```bash
    git init
```
## Step 2. Add Files and Create the First Commit
Stage the files you want to track
```bash
    git add .
```
Commit the changes 
```bash
    git commit -m "Initial commit"
```
## Step 3. Renamed the Branch name to `main`
The command is used to **rename** the **current branch** to **main**. The **`-M`** flag makes sure the branch is renamed forcefully even if a branch with the name **main** already exists.
```bash
    git branch -M main
```
**Note :** This is the **new name** for the **current branch**. It’s common for users to **rename** the **default branch** from **`master`** to **`main`** which has become a widely adopted standard in recent years.
## Step 4. Create a Remote Repository
Go to a Git hosting platform. Create a new repository, give it a name & copy the repository URL (usually in HTTPS or SSH format).
## Step 5. Link the Local Repository to the Remote
Add the remote URL to your local repository
```bash
    git remote add origin https://github.com/your-username/your-repo-name.git
```
Verify the remote
```bash
    git remote -v
```
## Step 6. Push the Local Repository to the Remote
Push the initial commit to the remote repository
```bash
    git push -u origin main
```
Now, the local repository is synced with the remote repository & we can push or pull changes as needed.