## Git Command
### [medium.com](https://levelup.gitconnected.com/10-must-know-git-commands-for-software-engineers-ffc6687d6dfd)

### HEAD
==HEAD== is a pointer or reference to the ==currently checked out branch== or ==latest commit==. After a new commit is created, the HEAD pointer will ==move forward== to the newly created commit.
e.g.:
- branch head
- commit head
### ^ (CARET SYMBOL)
Caret symbol can be used to ==navigate through the project historical timelines==. ==HEAD^== refer to the ==commit preceding to the current commit==. Numerical values (n) can be added to the HEAD, *e.g.: HEAD^n* to precisely determine the number of commits to go back.
```git
git rev-parse HEAD^ / HEAD^5
```
### STAGING
Staging is the area for ==all of the changes to be included in the next commit==. Specific file can be added to the staging area by ==specifying the file name== or all of the changed files can be added by using the ==period symbol (.)==
```git
git add file_name / .
```
Remove staged file from the staging area.
```git
git reset file_name
```
#### ADDING & COMITTING FILE
Instead of using different git commands *git add .* & *git commit -m "commit message"*, single command can be used to perform the adding & committing process.
```git
git commit -am "commit message"
```
#### CREATING & SWITCHING TO NEW BRANCH
Instead of using different git commands *git branch new_branch_name* & *git checkout new_branch_name*, single command can be used to perform the creating and switching to new branch process.
```git
git checkout -b new_branch_name
```
#### DELETE BRANCH
Before ==executing the delete branch== command, make sure to ==checkout to another branch==.
- safe deletion (check if the branch to be deleted had been merged to the current branch)
```git
git branch -d delete_branch
```
- force deletion (does not check for merge)
```git
git branch -D delete_branch
```
- delete remote branch
```git
git push origin -d branch_name
```
#### UPDATE GIT COMMIT
It is possible to update the last commit. The comment can be updated and the content of the staged file can also be updated
```git
git commit --ammend -m "commit message"
```
#### STASHING CHANGES
Git ==prevents branch changing== if changes in the current branch is ==not being committed==. In order to overcome this, the ==changes in the current branch need to be stash==.
- stash changes
```git
git stash
```
- apply stash (keep stash)
```git
git stash apply
```
- apply stash (clear stash)
```git
git stash pop
```
#### REVERT COMMIT
Revert current code base to certain commit (A) using the commit hash key. New commit (B) will be created without the changes within the commit (A). The newly created commit (B) will be the latest commit.
```git
git revert commit_hash
```
#### COMMIT INFO
The hash & the comment of commit can be obtained with *git reflog*
```git
git reflog
```
#### RESET COMMIT
The last commit can be undo using the *git reset* command
- soft reset
	- un-commits the last commit and ==keep its changes from the staging area==.
	- changes ==still== in the code base.
```git
git reset --soft HEAD^
```
- mixed reset
	- un-commits the last commit and ==removes its changes from the staging area==.
	- changes ==still== in the code base.
```git
git reset --mixed HEAD^
```
- hard reset
	- un-commits the last commit and ==removes its changes from the staging area==.
	- changes ==deleted== from the code base.
```git
git reset --hard HEAD^
```
#### GET BRANCH(ES)
- list out local branch(es)
```git
git branch -l
```
- list out remote branch(es)
```git
git branch -r
```
