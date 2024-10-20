# Introduction to Git
<div align="center">
    <img src="Diagrams/Git-Logo.png" alt="Project Logo" width=20%>
</div>

## What is Git?
Git is a **distributed version control system** designed to **track changes** in **source code** during software development. It allows multiple **developers to collaborate on a project** keeping a history of changes, facilitating collaboration & ensuring that every modification can be **traced**, **merged** or **reverted** as needed.

## Key Features of Git
- **Content Tracker :** Git **captures snapshots of the entire project directory** & its **contents**. Instead of saving just file changes, Git stores the state of the whole project at the time of each commit efficiently managing versions and history across the project.
<div align="center">
    <img src="Diagrams/Content-Tracker.png" alt="Project Logo" width=80%>
</div>

- **Distributed :** Every developer has a complete **copy of the entire repository** including its history on their own machine.
<div align="center">
    <img src="Diagrams/Distributed.png" alt="Project Logo" width=50%>
</div>

- **Version Control :**  Git tracks changes to files over time allowing us to **go back in time to view**, **manage** & **review the history** of a project. This makes it easy to **restore previous versions** & keep a detailed log of modifications.
<div align="center">
    <img src="Diagrams/Version-Control.png" alt="Project Logo" width=70%>
</div>

- **Branching and Merging :** Git allows developers to work on different features or fixes in parallel through **branches** which can later be merged into the main codebase.
<div align="center">
    <img src="Diagrams/Branching-Merging.png" alt="Project Logo" width=70%>
</div>

## Git Repository Types
Git supports two main types of repositories.
1. **Local Repository**
2. **Remote Repository**

<div align="center">
    <img src="Diagrams/Local-Remote-Repository-Architecture.png" alt="Project Logo" width=90%>
</div>

### 1. Local Repository 
This is a repository stored on our **local machine** where **we can work independently**. Each developer has a complete copy of the project including the **entire version history**. Changes are made **locally** & **can be committed to the local repository** without needing to connect to any **remote server**. In a Local Repository, Git manages changes through **three main areas** :
1. **Working Area**
This is the directory **where we actively make changes to files**. Any **edits**, **additions** or **deletions** happen here but they are **not yet tracked** by **Git** until **we stage them**.
2. **Staging Area (also known as the Index)**
The staging area is a **holding space** between the **working area & the repository**. When we decide to track certain changes **we add them to the staging area** with **`git add`**. It holds a snapshot of what will be included in the next commit.
3. **Commit**
Once changes are staged, we can create a commit using **`git commit`** which **saves the staged changes** to the local repository. Each commit is a snapshot of the project's state at that point in time allowing us to go back in time if needed.

These three areas form the basic workflow in Git ensuring changes are carefully managed before being permanently recorded in the repository.
### 2. Remote Repository
A **remote repository is hosted on a server** & is typically used to **share code among team members** or **backup the project**. Multiple developers can collaborate by pushing their changes to and pulling updates from the remote repository. Popular **remote hosting services** include **GitHub**, **GitLab** & **Bitbucket**.
## Git Add
### What is git add?
**Git add** is a command **used to stage changes in Git** preparing them to be included in the **next commit**. It doesn’t actually commit the changes it simply **moves modified or new files from the working area to the staging area** (also known as the "index"). This step is crucial in Git’s workflow because only staged changes can be committed.
### Key Concepts of git add
1. Staging Changes
2. Staging
3. Tracking New Files
4. Removing Changes from Staging
## Git Commit
### What is Commit?
**Git commit** represents a **snapshot of the project at a specific point in time**. It stores changes made to the files in a repository and forms the backbone of Git's version control.

A commit includes:
- **Author information (name and email)**
- **Commit message (a brief description of the changes)**
- **Changes (diff) (what was added, modified or deleted)**
### Commit Message Guidelines
- **Be clear :** The message should describe the changes and why they were made.
- **Use imperative mood :** Commit messages should describe what the commit does when applied, such as:
    - **`"Fix typo in README"`**
    - **`"Add new authentication method"`**
#### Here are more concise descriptions for different types of Git commits:
- **Added Image :** Included a new image or diagram.
- **Fixed Typo :** Corrected a spelling mistake.
- **Fixed Syntax :** Corrected errors in code or formatting.
- **Added Bold Text :** Highlighted important keywords.
- **Fixed Heading :** Edited or restructured a heading.
- **Updated Image :** Replaced an outdated diagram with a new one.
- **Refined Content :** Improved the clarity or readability of text.
- **Fixed Comments :** Improved explanations in code comments.
## Understanding the Areas in Git
### Working Area
#### Definition
The working area is the local directory where you create and modify files for your project. This area contains all the files and folders that you are currently working on.
#### Characteristics
- **Untracked Changes :** Any new files or changes made to existing files are considered untracked by Git until you explicitly stage them.
- **Local Modifications :** You can freely edit files in this area without affecting the repository history. This is where you do all your development work.
- **Visibility :** Files in the working area can be seen and modified using any text editor or Integrated Development Environment (IDE).

### Staging Area
#### Definition 
The staging area (also known as the index) is an intermediate space where changes are prepared before being committed to the repository. It acts as a buffer between the working area and the committed state.
#### Characteristics
- **Marked for Inclusion :** When you add files to the staging area using the git add command, you mark them for inclusion in the next commit. This allows you to select which changes you want to commit.
- **Snapshot of Changes :** The staging area holds a snapshot of the changes you have staged. This snapshot will be saved in the next commit allowing you to control what gets committed.
- **Selective Committing :** You can stage individual files or specific changes within files, giving you fine-grained control over your commit history.

### Committed Files
#### Definition
Committed files are those that have been saved to the Git repository. A commit is a snapshot of the project at a specific point in time.
#### Characteristics
- **Tracked Changes :** Once files are committed git tracks their changes allowing you to revisit the commit history at any time.
- **Commit History :** Each commit is associated with a unique identifier (hash) and contains metadata, including the author, date & commit message. This history allows you to understand the evolution of your project.
- **Revisions :** Committed files can be reverted, modified or compared with other commits using various Git commands. This feature is crucial for collaboration & maintaining the integrity of the project over time.
<div align="center">
    <img src="Diagrams/Areas-in-Git.png" alt="Project Logo" width=80%>
</div>

## Git Branches
Git **branches** are an essential feature of version control that **allow us to work on different versions of a project simultaneously**. Branches enable **isolated development** meaning we can work on **new features**, **bug fixes** or **experiments** without **affecting the main codebase**. Here’s how Git branches work:
### 1. Main Branch (Master/Main)
- The main branch is typically where the stable version of the code resides. It’s the default branch when a repository is initialized & it’s often called main (formerly master).
- It holds production-ready code & all features or changes eventually get merged back into this branch.
### 2. Feature Branches
- A feature branch is a separate branch created from the main branch where we can develop new features or make changes.
- This branch keeps changes isolated until they are complete and ready to be merged into the main codebase.
### 3. Branch Creation
We can create a branch at any point. A branch is simply a pointer to a specific commit in the project’s history. Once a branch is created any commits made on that branch will not affect other branches.
### 4. Switching Branches
- Switching between branches allows us to move back and forth between different lines of development. This makes it easy to pause work on one feature and work on another or go back to a previous version of the project.
### 5. Merging Branches
- When a branch is ready to be integrated with the main code we merge it back into the main branch. This can be a fast-forward merge or a more complex three-way merge if the two branches have diverged.
### 6. Conflicts
- If changes from different branches overlap Git may encounter conflicts during a merge. Conflicts need to be manually resolved before the merge can complete.
### 7. Branch Management Best Practices
- **Use Meaningful Names :** Name branches based on the feature or task, making it easy to understand the purpose of each branch.
- **Merge frequently :** To avoid large, complicated merges, it’s a good idea to merge branches back into the main branch regularly.
- **Delete branches :** After a branch has been merged, it’s often deleted to keep the repository clean.

Let's dive into branch merging and management in a **team environment**.
#### 1. Merging Branches
Merging in Git combines the changes from one branch into another, often to incorporate new features or fixes into the **`main branch`**. There are two common types of merges:
- **Fast-Forward Merge :** If there are no new commits on the **`main branch`**, Git can move the branch pointer forward without creating a new commit this is called a **Fast-Forward Merge**. It happens automatically if the branches haven’t diverged.
- **Three-Way Merge :** Happens when both the main and feature branches have new commits. Git creates a new commit to combine changes from both branches.
#### 2. How to Merge
1. **Switch to the Main Branch** (where the changes need to go).
2. **Merge the Feature Branch into the Main Branch**.
3. **Resolve Conflicts if any occur** (e.g., both branches changed the same line of code).
#### 3. Merge Conflicts
1. When two branches change the same part of a file, Git cannot automatically merge and shows a conflict.
2. We edit the file to choose which changes to keep.
3. After resolving, commit the merge to finalize it.
#### 4. Working in Teams
- **Use Feature Branches :** Each developer works on their own branch for a task or feature. Once done they merge their branch into the **`main branch`**.
- **Merge Frequently :** To avoid conflicts keep merging changes from the main branch into your **`feature branch`** regularly.
- **Pull Requests (PRs) :** Before merging into the **`main branch`** the team can review the changes in a pull request to ensure everything looks good.
#### 5. Best Practices
- **Keep Branches Short :** Don't work on a **`feature branch`** for too long before merging it. Smaller, more frequent merges are easier to manage.
- **Review code before Merging :** Use pull requests to get feedback from the team before adding changes to the main branch.
- **Handle Conflicts Early :** Resolve conflicts as soon as they come up so they don’t pile up.
<div align="center">
    <img src="Diagrams/Branching.png" alt="Project Logo" width=70%>
</div>