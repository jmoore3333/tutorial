Tutorial by Jake Moore
# Introduction
Welcome to my Git Command Line Tutorial for Computer Science students! In this tutorial, you will learn the basics of using Git from the command line, focusing on key concepts like branches, stashes, and rebasing.
## Setup
# Creating your directory
In Git, directories (or folders) are an integral part of managing and organizing the files within a repository. 
Create a directory using
`mkdir simple_code`<br>`cd simple_code`
# initialize the repository
Turning the repository into a git repository will allow for the history to be tracked
`git init`
# set up the python virtual environment
A Python virtual environment is a self-contained directory that contains its own Python interpreter and a set of libraries, allowing you to work on a Python project with dependencies that might be different from those in your system-wide Python installation.
`python3 -m venv venv` then activate the environment with `source venv/bin/activate`
# First script
Lets create a simple program, you can use your own or follow allong with mine. I will create simpleMath.py and make it a simple addition function for now
`def add(x,y):`<br>`
return x + y`<br>`
print(add(2,9))`
# Track the file
Lets take the script and move it from the working tree(where we currently are) and add it to the staging area. Then we'll commit it
`git add simpleMath.py`
`git commit -m "Initial commit: A simple addition function"`
## Branches
# creating a branch
When you create a branch, you're creating a new line of development that allows you to isolate changes. The default branch in Git is typically named main or master, and this is where the latest stable code resides.
`git checkout -b feature-multiplication`
# Implementing multiplication
Since multiplication is also simple math it is only right that we add it to our simpleMath.py
`def multiplication(x, y): `<br>`
return x * y `<br>`
print(multiplication(3, 8)`
# lets commit the new feature
This will save our changes in a new branch
`git add simpleMath.py`
`git commit - m "Add multiplication function"`
# stashing
Stashes are useful for saving work that you don't yet want to commit, such as work in progress.
`git stash` to save your changes and `git stash pop` to resume
# merging and merge conflict resolution
In Git, merging is the process of combining changes from different branches. It's a common operation when working collaboratively or maintaining multiple lines of development. The primary goal is to integrate the changes seamlessly, preserving a linear history.
Merge conflicts occur when Git is unable to automatically merge changes from different branches due to conflicting modifications in the same part of a file. This won't happen here so to merge your branch back into the main branch use `git checkout main`
`git merge feature-multiplication`
## push github
A remote repository is the 4th and final type of data store on git. The first 3 being working tree, staging area, and local repository.
Create a remote repository on github and do not initialize it. Then link your local repository to the new remote one. You can do this with
`git remote add origin <insert url or repository here>`<br>``
`git branch -M main`
`git push -u origin main`
## Conclusion
Well done if you have made it this far. You have completed this basic git tutorial, feel free to try and add subtraction, division, or anything else to simpleMath.py if you wish to try on your own without a guide.
