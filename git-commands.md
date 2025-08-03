# Git-commands
git config --list
checks list of configs.

git config --global user.name "name"
// sets global username to specified.

git config --global user.email "email"
// sets global email to specified email.

git clone "url from github" 
// makes a clone of the code

git status
// shows status of files unmodified U, modified M

git log 
// shows all commits

git add "filename"
// adds file

git add .
// adds everything

git commit -m "message"
// commits with a message

git commit -am "message"
// adds and commits all tracked modified files in one step (but not new/untracked files)

git push origin "branch name"
// pushes code to branch

git push -u origin branchname
// remembers the origin so next time we can only use git push

# pushing to remote server

git init 
// creates a git repo for those without a repo already(external code)

git remote add origin "url"
// tells git where to push when pushing to remote server. we need to create a repo in github and then add it's url to this command

git remote rm origin
// removes the remote origin url

git remote -v
// verify the push and pull url

git push origin <branchname>
// pushes current code to specified branch.


# pushing to remote ssh server
git remote set-url origin <git@github.com:user.git>
// sets origin (especially good for private repos)

git remote rm origin
// removes origin

# git-branches

git branch
// shows branches

git branch -M master
// forcefully renames current branch to master

git checkout branchname
// switch to specified branch

git checkout -b branchname
// creates a new branch with specified branchname

git branch -d branchname
// deletes the specified branchname
// note: checkout of the specified branch first.

# merging-branches
git diff <filename>
// compares with specified file

git merge <filename>
// merges current file with specified file

// note: 
// better way is to create a pull request in github and merge 

git pull origin <filename>
// pulls the merged document from remote server to local

# merge conflicts:
// best way to resolve is merge locally and when we get error we can manually change it 


# staged(added) changes reset:
git reset <filename>
// resets the specified file and makes it unmodified again.
// note: when we add something we don't want to commit we can use this.

git reset
// resets everything 

# commited changes reset:
git reset HEAD~1
// HEAD~1 points to one commit before the current commit

git reset HEAD~2 
// HEAD~2 points to two commits before the current commit

# commited changes(for many changes) reset:
git reset <commit hash>
// can copy the commit hash by using git log
// the changes made will still be visible(the code written in the commmits after the current selected commit), the code isn't deleted.

git reset --hard <commit hash>
// all the extra changes made after the selected commit will also get deleted

# extras
ls -a 
// hidden files

ls 
// all files

ls -la
// all hidden files



