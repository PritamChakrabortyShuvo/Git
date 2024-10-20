# Installation Process of Git on Windows and Linux
To install Git from scratch, we can follow the steps for different operating systems. Since I am using Windows 11 as my base machine, I will start with the installation for Windows but I’ll also include steps for Linux.
## Installation Process of Git on Windows
### Step 1. Download Git
- Visit the official [Git Website](#https://git-scm.com).
- Click on the "Download for Windows" button.
- Download the executable file.
### Step 2. Run the Installer
#### 1. Locate and Open the Downloaded **`.exe`** File
- Navigate to your Downloads folder (or the folder where you saved the installer).
- Look for a file named something like **`Git-<version>-64-bit.exe`**.
- Double-click the file to start the installation process.
#### 2. Follow the Prompts in the Installation Wizard
- A setup window will appear. Click Next to proceed through the steps.
#### 3. Select Components (if prompted)
- You might be asked to choose additional components to install. The default options are usually sufficient, but ensure that "Git Bash Here" and "Git GUI Here" are selected for convenience.
#### 4. Important Settings
- **Adjusting PATH :** Choose "Use Git from the command line and also from 3rd-party software."
- **Choose the SSH executable :** "Use bundled OpenSSH" is recommended.
- **Configure the line ending conversions :** Choose "Checkout as-is, commit Unix-style line endings."
#### 5. Complete the Installation
Continue following the wizard until you reach the final screen. Click Install to begin the installation.
Once the installation is complete, click Finish to exit the wizard.
### Step 3. Verify Installation
Open Command Prompt or PowerShell and Run :
```bash
    git --version
```
This will output the installed Git version if successful.
### Step 4. Set Up Git Configuratio
Open Git Bash or Command Prompt. In the terminal window enter the following command replacing **`"Your Name"`** with your actual name:
```bash
    git config --global user.name "Your Name"
```
Next enter the following command replacing **`"your.email@example.com"`** with your actual email address:
```bash
    git config --global user.email "your.email@example.com"
```
This command sets your email address, which will be linked to your Git commits.
### Step 5. Verify Your Configuration
To ensure that your username and email are set correctly, run the following command
```bash
    git config --global --list
```
This will display your Git configuration settings, and you should see your username and email listed.
## Installation Process of Git on Ubuntu(Linux)
### Step 1. Update the System
Open the terminal and run the following commands:
```bash
sudo apt update
```
And,
```bash
    sudo apt upgrade
```
### Step 2. Install Git
To install Git run
```bash
    sudo apt install git
```
### Step 3. Verify Installation
After installation check the version to ensure it's installed correctly.
```bash
    git --version
```
### Step 4. Set up Git Configuration
To configure Git with your username and email
```bash 
    git config --global user.name "Your Name"
```
And,
```bash
    git config --global user.email "your.email@example.com"
```