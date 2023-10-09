# Getting Started with Git
Check if you have git installed:
    git --version

If version exists, good to go, else download
For windows go to gitforwindows and follow the download procedure
For Mac users : brew install git
For linux(ubuntu) : apt install git

# Configure git
Configure your username and email
    git config --global user.name "jimmykimunyi-dev"
    git config --global user.email "jimmykimunyi@gmail.com"

# git init
Create a folder you want to start your project on
Move inside the folder
Initialize by running :
    git init - This command initializes a new repository
    
To remove a repo run:
    rm -rf .git - this removes an existing git repo

# git add
To add the files you are working on to the repo run :
    git add . - this adds all the files in the working directory to a git repo
    git add filename - when you enter a certain file name, only that file is added to the git repo.

# git status 
Gives the info of the changes made.

# git commit
This describes the changes made and requires you leave a message of the changes made
    git commit -m "web development"
    