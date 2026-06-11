# Code Manual
Personal reference manual containing notes, patterns, and quick-lookup guides for multiple programming languages. Designed to speed up development by keeping answers within reach.

### Index:
1. [Git](#git)

## Git

### Commands:

---
_Returns the version of Git software installed on the system._
```Git
git --version
```
**(OR)**
```Git
git -v
```
---
_Tells if a folder contains a Git repository or not, i.e. if that folder and its contents are being tracked or not._
```Git
git status
```
---
_Used to initialise a new Git repo._
```Git
git init
```
---
_Add certain files or folders to the repo as trackable files._
```Git
git add <file_name>
```
---
_Add all the files in the current (actively present directory in the terminal) directory to stage and not anything else that is part of the repo but not part of current directory._
```Git
git add .
```
---
_To add all files in a repo to stage irrespective of current directory._
```Git
git add --all
```
**(OR)**
```Git
git add -A
```
---
_Adds only new or modified files to stage. If something is deleted, it won't be staged._
```Git
git add *
```
---
_Unstage already staged files._
```Git
git reset
```
---
_Delete all staged and unstaged changes._
```Git
git reset --hard
```
---
_This resets all the changes made after this particular commit, so it reverts all code back to this commit._
```Git
git reset <commit_id>
```

_This resets all the changes made after this particular commit, so it reverts all code back to this commit. This allows you to go skip <number> of commits and go to the previous one to see how the code was in that commit. So if you have commit one, commit two, commit three and commit four. If you are on commit four and use git commit HEAD~2, you skip two commits (commit three and commit two) and will see how files were in commit one._
```Git
git reset HEAD~<number>
```
---
_To commit or save a checkpoint of the trackable files._
```Git
git commit -m "custom message"
```
---
_This shows a log of all the commits made to a given repo._
```Git
git log
```
---
_Shorter version of the original log._
```Git
git log --oneline
```
---
_This is used to configure Git, like change some settings of the git software. 'global' for all repos, 'local' for only that repo._
```Git
git config (--global/--local)
```
---
_Shows all the available and existing branches and signifies HEAD branch with * symbol._
```Git
git branch
```
---
_Create a new branch with name <branch_name>._
```Git
git branch <branch_name>
```
---
_Change the HEAD to point to another branch._
```Git
git checkout <branch_name>
```
**(OR)**
```Git
git switch <branch_name>
```
---
_Creates a new branch and changes the head to that new one. (-c signifies create and -b signifies branch)._
```Git
git switch -c <branch_name>
```
**(OR)**
```Git
git checkout -b <branch_name>
```
---
_Merges <branch_name> branch to the branch to which HEAD points to._
```Git
git merge <branch_name>
```
---
_Deletes a branch._
```Git
git branch -d <branch_name>
```
---
_Force deletes a branch._
```Git
git branch -D <branch_name>
```
---
_Used to compare the commited version of a file with the staged version of the same file. It shows the differences and what changed from one version to another._
```Git
git diff --staged
```
---
_Used to compare between two commit versions._
```Git
git diff <commit_id1>..<commit_id2>
```
---
_Add your current incomplete changes to a stash._
```Git
git stash
```
---
_Shows a list of all the stashes made._
```Git
git stash list
```
---
_To restore the changes saved to stash and remove it from stash._
```Git
git stash pop stash@{<id>}
```
---
_To restore the changes saved to stash and keep it in stash still._
```Git
git stash apply stash@{<id>}
```
---
_This allows you to go back in time and see how the code was in that specific commit. You can return to end of the timeline by using command 'git switch master'._
```Git
git checkout <commit_id>
```
---
_This allows you to go skip <number> of commits and go to the previous one to see how the code was in that commit. So if you have commit one, commit two, commit three and commit four. If you are on commit four and use git commit HEAD~2, you skip two commits (commit three and commit two) and will see how files were in commit one. You can return to end of the timeline by using command 'git switch master'._
```Git
git checkout HEAD~<number>
```
---
_Once you have checked the state of the file at some commit id, you can use this command to return to where you were before you came back in time, not always to the end of that branch._
```Git
git reflog
```
---
_It reverts this file to its last commit state only._
```Git
git restore <file_name>
```
---
_To remove files from staged to working._
```Git
git restore --staged <file_name>
```
---
_Rename the HEAD branch to a new name._
```Git
git branch -M <new_name>
```
---
_To see what the remote repo is, its url and stuff._
```Git
git remote -v
```
---
_To add a remote GitHub repo for your local repo._
```Git
git remote add <name> <url>
```
---
_To change the name of the remote repo._
```Git
git remote rename <old_name> <new_name>
```
---
_Removes the remote repo from being connected to the local repo._
```Git
git remote remove <name>
```
---
_This command pushes only a specific local branch to GitHub._
```Git
git push <remote_name> <local_branch>
```
---
_Sets an upstream branch._
```Git
git push --set-upstream <remote_name> <local_branch>
```
**(OR)**
```Git
git push -u <remote_name> <local_branch>
```
---
_To copy or download a remote repo as a local repo._
```Git
git clone <url>
```
---
_It removes a file even if it has unstaged changes._
```Git
git rm --forced <file_name>
```
---
_It keeps the file intact on the system but removes it from the repository, so it is no longer tracked._
```Git
git rm --cached <file_name>
```
---
_Delete untracked files._
```Git
git clean
```
---