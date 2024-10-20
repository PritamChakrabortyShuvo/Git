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
    <img src="Diagrams/Repository-Types.png" alt="Project Logo" width=70%>
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