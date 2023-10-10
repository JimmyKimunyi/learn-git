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

# git push
This alllows you to push the code in your machine to a remote server e.g github

# Intro to Github
This is a platform for hosting and collaborating on Git repositories
Create a new repo and copy the ssh path to the repo

# git remote
This enables you to create aremote connection between your local machine and the repo in your remote server.
run : 
    git remote add origin "ssh path to your github repo"
    git branch -M main
    git branch - shows all the branches in the directory

# git push
To push a project from your local machine to github, run:
    git push -u origin main

If you already initialized the origin run :
    git push

# git pull
This allows you to pull code from github to your local machine
    git pull

# branches
A branch represents an independent line of development
main is the default branch
commands : 
    git branch : shows the branch you are in in your local machine
    git branch -r : shows the branch you are in on github
    git branch -a : shows all the branches in your local machine and github

To create a new branch run :
    git branch frontend-react

To switch from one branch to another run :
    git checkout frontend-react
    
    