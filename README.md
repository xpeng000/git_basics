# git_basics

Basic Git commands:

git config —global user.name “Rachel Peng“ //set up user name 
git config —global user.email “xpeng@brandeis.edu” //set up email 

//I created an empty folder “git_stuff” on my desktop and cd into this folder
git init // initialize a repository for this folder

touch index.html //“touch” will create a file, e.g. index.html

//now we have made a change in the repo, and we need to add the html file to the staging area
git add . //add all changes 
git add index.html //only add one file 
git add index1.html index2.html index3.html //add multiple files 

git commit -m “added html file” //commit changes with a string message 

git commit -am “message” //shortcut: combines git add . and git commit -m “message”

git push //push to GitHub repo

git status //show the status of the GitHub repo 
On branch master
nothing to commit, working tree clean

git log //show all commit history on the branch you’re on
commit 57be0239ebcaf3e25e33d9259b537aacbe279ddc (HEAD -> master)
Author: Rachel Peng <xpeng@brandeis.edu> //with the user name and email we entered
Date:   Fri Aug 7 14:25:52 2020 +0800

    added html file


Git Branches 

- Why do we need it?
	In larger projects, developers often want to implement new features, while leaving existing code untouched. This is achieved by branching. When working with source code with multiple developers, each developer could be responsible for creating one feature, which is implemented in a branch, isolated from other branches. This is extremely useful because the changes made on one branch isn’t going to mess up other branches. 
	We’re on the master branch by default. 
- How to create another branch?
	git branch rachel //this will create another branch “rachel”
- How to switch to another branch?
	git checkout rachel //switch to branch “rachel”
- How to see all the branches?
	git branch //this will show all current branches 
- Can you make branches inside a branch?
	Yes! This is a common practice in larger scale projects. Subbranches inherit code from their master branch. 
- When to make branches?
	It’ll dependent on your project, but a new branch has the copy all your current code when created. 

More on: https://www.youtube.com/watch?v=JTE2Fn_sCZs by Codemy School 


Merging  

-  Why do we need it?
	When developers are done with working on their branches (fully tested now) and want to add their code to the master branch, merging combines code on the other branches to the master branch.
- How to merge?
	1. Go to the branch you want to merge INTO using git checkout (e.g. git checkout master)
	2. git merge rachel <the name of the branch you’re trying to merge FROM>
	Note that the other branch (rachel) is deleted after merging with the master branch.  

More on: https://www.youtube.com/watch?v=0iuqXh0oojo by Codemy School 














