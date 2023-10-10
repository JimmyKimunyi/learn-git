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
    
# merging
To merge a branch to the main branch run :
    git push -u origin "your-branch" - pushes the branch to git hub and creates a new branch if it didnt already exist.

In github goto pull request, create a pull request & merge
Once verified pull the branch to your local machine.
    git pull - pulls the updates on github to your machine
    git log - to see the updates made

# workflows
Its always a good practice to pull the changes from the main branch
Create a new branch
Then work on the feature/bug you want to implement /fix
Rebase your changes based on the master branch
If there are conflicts try to resolve them first
Squash all of your local commits then rebase master.
This involves removing you commit ,adding your updates on top then adding the commit, this ensures you only resolve conflicts once then you are good to go

# dealing with conflicts
A conflict occurs say when person A made updates to repo A , then person B tries to make other changes without first pulling the changes made.
This resuts to a conflict

# merging conflicts
When you run:
    git pull

git tries to take Person A changes and tries to merge with Person B changes but often fails.
To solve this fix the conflict, below is an example:
    <<<<<<<<<HEAD (Current Change)
        <p> This is the first paragraph </p>
    =========
        <h1> this is another paragraph </h1>
    >>>>>>>>> weyifviwbwuivwbu75247874fx0x327dg (Incoming change)

To fix the above you may try:
Start by removing the "<<<<>>>>", "=========", "HEAD", "weyifviwbwuivwbu75247874fx0x327dg"
Then just arrange the code in the desired order
    <p> this is the first paragraph </p>
    <h1> this is another paragrapgh </h1>

Now add and commit changes then push
Its a good practice to mention the "fix conflict"

# rebase
In a situation where you want to commit to main branch but your commits are delyed behind the main branch "rebase" helps solve this
Rebase takes all the commits from the main branch and tries to implement your changes on top of it

# git rebase
run:
    git rebase

Incase a merge confluct arise, similar to the situation of merging conflicts, you first fix the conflicts then run :
    git rebase --continue
    git add .
    git commit -m "commit message"
    git push

Just incase the above doesnt work you may force the push by running :
    git push -f

It a good practise when you make a PR you squash and merge so that you only have to solve the conflict once

# git clients
These are gui tools for working with github

# gitpod
This is an online tool by github that helps you have a VSCode environment online to do your projects

# git hub portfolio
The projects in github can be used as a portfolio.
Try to modify your page to look nice

# exploring github