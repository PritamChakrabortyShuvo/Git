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