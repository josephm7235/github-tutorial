# GitHub Tutorial

_by Joseph Medrano_

---
## Git vs. GitHub
* Git: Is a function which keeps snapshot of code when one add and commits  
* GitHub: Is dependent of git as it uses git features in order to take snapshots of code however GitHub allows for the snapshot to be stored in a cloud in which one can retrive their code for later usage. It also allows for tracking files for collaboration

---
## Initial Setup
#### Creating a git hub account:
It is important to have a git hub account as it will allow you to share your repository with your peers and retrive projects
1. Go to [Github.com](https://github.com/login) and click create a account
2. When creating your account include username and email and decide on password (make sure to fill out remaning sections)
3.  **After make sure to verify your email after creating git account** 

#### Creating a SHH key:  
Creating a SHH key is important as it will allow the user to push their commits to a remote repository in which if they lose their local repo they can retrive their commits from the remote repo
1. Go to [Github.com](https://github.com/login) and drag your mouse to the top right corner onto profile icon then click setting
2. Click the left side bar and go to SHH and GPG
3. Make a new SHH key and title it as c9.io
4. Switch to [c9.io](https://c9.io/)
5. `cd ~/workspace` followed by `mkdir new_repo` or `cd existing repo`
6. After do `git init` and `touch file_name` open and edit file
7. `git add file_name` after make sure to `git commit -m " "` if you are unnable to do `git push` then switch back to [Github.com](https://github.com/login) and create a new repo
8. After copy down SHH key in remote repo both `git remote add origin git@github.com:yourname/reponame.git` and `git push -u origin master`
9. Switch back to c9 and paste them **seperately**
10. Now you can push :D

---
## Repository Setup
* _git init_ is a command used to in your directory in order to turn the directory into a repository that will allow for the usage of git commands   
   1. First ensure that you are in your workspace and not in a file or directory
   2. In your workspace proceed to type `mkdir` followed by the directory name you want in order to create a new directory
   3. `cd` into said directory and then type `git init` to turn directory to a local repo

* _git add_ will allow the user to add a specific file to the stage that will allow it to taken as a snapshot when the user commits
1. After doing `git init` create a file do this by doing `touch filename` 
2. Edit your file
3. Now do `git add filename` this will add your changes to the stage

* _git commit_ works when the user adds a file to the stage from their you are able to do git commit which will save anything that is on the stage to your repo.
1. Once you have added a file to the stage you are now able to commit your file
2. Do `git commit -m " Present tense description"`

---
## Workflow & Commands
* _git status_ is used in order to see if you successfully committed your changes
   1. After you `git commit -m " "` proceed to do `git status` youll recieve a update if your file has been modified and commited  
* _git add_ similar to your repo setup you'll repeat set 1-3 whenever you want add a file to the stage
* _git commit_ repeat steps **1-2** from repo setup
* _git push_ is the process of pushing all your previous commits into your remote repo 
1. After you have `git commit -m ""` you'll know what to push this will only work if you have copied your SHH key if not do so
2. Once you have done that do `git push` and it will push your commits onto your remote repo

---
## Rolling Back Changes
* **undo edits** in order to undo a edit that you did in a file then  do `git checkout -- filename` 
* **undo add** in order to unstage a file you must `git reset HEAD filename`
* **undo commits** in order to undo a commit there are three possible ways of undoing 
   * `git reset --soft HEAD~1` = this will undo the last commit you did however your file will remain  
   * `git reset HEAD~1` = Will undo your last commit but will also unstage your file   
   * `git reset --hard HEAD~1` = Your commits will undo and the file file will unstage while deleting all the changes
* **undo a push** in order to undo a push you must `git reset -- hard HEAD~1

