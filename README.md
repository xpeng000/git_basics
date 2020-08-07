# Git Basics

### Basic Git commands 

set up user name

    git config —global user.name “Rachel Peng“ 		     

set up email

    git config —global user.email “xpeng@brandeis.edu” 	 

I created an empty folder “git_stuff” on my desktop and cd into this folder 

initialize a repository for this folder

    git init 						                   

“touch” will create a file, e.g. index.html

    touch index.html 					               

Now we have made a change in the repo, and we need to add the html file to the staging area

add all changes

    git add . 						             

only add one file

    git add index.html 				        	 

add multiple files 

    git add index1.html index2.html index3.html 		

commit changes with a string message

    git commit -m “added html file” 
    
shortcut: combines git add . and git commit -m “message”

    git commit -am “message” 				

push to GitHub repo

    git push 						

show the status of the GitHub repo

    git status 						 

this is what I have on my terminal after git status:

    On branch master
    nothing to commit, working tree clean

show all commit history on the branch you’re on

    git log 					

this is what I have on my terminal after git log:

    commit 57be0239ebcaf3e25e33d9259b537aacbe279ddc (HEAD -> master)
    Author: Rachel Peng <xpeng@brandeis.edu> //with the user name and email we entered
    Date:   Fri Aug 7 14:25:52 2020 +0800
                added html file 








### Git Branches 

- Why do we need it?

In larger projects, developers often want to implement new features, while leaving existing code untouched. This is achieved by branching. When working with source code with multiple developers, each developer could be responsible for creating one feature, which is implemented in a branch, isolated from other branches. This is extremely useful because the changes made on one branch isn’t going to mess up other branches. We’re on the master branch by default. 

- How to create another branch?

        git branch rachel //this will create another branch “rachel”

- How to switch to another branch?

        git checkout rachel //switch to branch “rachel”

- How to see all the branches?

        git branch //this will show all current branches 

- Can you make branches inside a branch?

Yes! It is a common practice in larger scale projects. Subbranches inherit code from their master branch. 

- When to make branches?

It’ll depend on your project, but a new branch has the copy of all your current code when created. 

More on: https://www.youtube.com/watch?v=JTE2Fn_sCZs by Codemy School 








### Merging 

-  Why do we need it?

When developers are done with working on their branches (fully tested now) and want to add their code to the master branch, merging combines code on the other branches to the master branch.

- How to merge?
1. Go to the branch you want to merge INTO using git checkout (e.g. git checkout master)
2. git merge command (rachel is the name of the branch you’re trying to merge FROM) 

           git merge rachel 
Note that the other branch (rachel) is deleted after merging with the master branch.  

More on: https://www.youtube.com/watch?v=0iuqXh0oojo by Codemy School 














