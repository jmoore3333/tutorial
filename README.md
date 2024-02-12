Tutorial by Jake Moore
# Introduction
Welcome to my Git Command Line Tutorial for Computer Science students! In this tutorial, you will learn the basics of using Git from the command line, focusing on key concepts like branches, stashes, and rebasing.
## Setup
# Creating your directory
Create a directory using
`mkdir simple_code`<br>`cd simple_code`
# initialize the repository
Turning the repository into a git repository will allow for the history to be tracked
`git init`
# set up the python virtual environment
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
Branches allow you to make changes that are isolated from the main code
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
to merge your branch back into the main branch use `git checkout main`
`git merge feature-multiplication`
## push github
A remote repository is the 4th and final type of data store on git. The first 3 being working tree, staging area, and local repository.
Create a remote repository on github and do not initialize it. Then link your local repository to the new remote one. You can do this with
`git remote add origin <insert url or repository here>`<br>``
`git branch -M main`
`git push -u origin main`
## Conclusion
Well done if you have made it this far. You have completed this basic git tutorial, feel free to try and add subtraction, division, or anything else to simpleMath.py if you wish to try on your own without a guide.
