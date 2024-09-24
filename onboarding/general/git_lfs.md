# Git Large File Storage (LFS)

## Introduction
Git Large File Storage (LFS) is an extension for Git designed to improve handling of large files. It replaces large files in your repository with links to files stored on a remote server, making the repository lighter and speeding up cloning and synchronization processes.

## How Does Git LFS Work?
When you add a large file to the repository, Git LFS replaces it with a "pointer" in Git, while the actual file is uploaded to the LFS server. This ensures that when you clone the repository or switch between branches, only the current versions of large files are automatically downloaded.

## Installation and Setup

### Installation
Install Git LFS using a package manager or download the installer from the official [Git LFS](https://git-lfs.com) site.  
**For Mac:**  
In newer versions, you also need to install [brew](https://brew.sh).  
To do this, run the following command in the terminal (better to copy from the site):  
`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`  
After installation, the terminal will output 2 more commands that need to be run (copy and execute them as they appear).  
Then you can run:  
`brew install git-lfs`  
Since the projects will already be configured, no further actions are needed.

### Initialization
Initialize Git LFS in your repository with the command:
`git lfs install`

## How It Works - In Detail
Select the types of files to track with LFS using the `track` command. For example, for PSD files:  
`git lfs track "*.psd"`  
This will create a `.gitattributes` file with rules for tracking the files.

### Working with Files
Add and commit files as usual. Git will automatically synchronize large files with the LFS server:  
`git add file.psd`  
`git commit -m "Added new design in PSD format"`  
`git push`

### Issues
#### If a file does not load into Git LFS
Run this command in the repository:  
`git lfs migrate import --include="*.obj"`  
Replace `obj` with the required file extension; it will re-index the data.  
Source of the solution: https://github.com/git-lfs/git-lfs/issues/2947.
