Git Commands
Untracked(local) -> Commit (local) -> Staged(local)-> Push (Master)
Initialize a local folder (master) to be a Git repository: 
git init
[ STATUS ] Check for any changes to repository: 
git status
git status -s (abbreviated output)
[ ADD ] "Untracked files" or modified files can be registered to the Git repository (added to staging): 
git add <filename> OR git add --all (for all files)
git add -A . (dot stands for current dir, -A ensures file deletions included)
git add '*.txt'
Remove file(s) from Git staging area: 
git reset <filename>
[ COMMIT ] Capture snapshot of changes to files in staging: 
git commit -m "" (-m flag = message)
git commit -am (-a flagged used for files that are still unstaged, skipping the git add step)
Review changes made to commit
git log
[ PULL ] Get most recent changes from repository (origin) to local (master): 
git pull origin master
[ PUSH ] Upload changes to repository (origin): 
git push -u origin master
[ DIFF ] See what is different from last commit
git diff HEAD
See what's different between files in stage
git diff --staged (--staged same as --cached)
See what changes made in unstaged files
git diff
[ CHECKOUT ] Revert changes back to last commit's state
git checkout --<filename>  (double dash informs command line there are no more options to follow after --)
[ BRANCH ] Create a branch off of master
git branch <branch_name>
Switch to the branch
git checkout <branch_name>
git checkout -b <branch_name> (creates new branch and switches focus to this branch
[ RM ] Remove files from disk and stage the change
git rm '*.txt'
git commit -am "Remove files"  (if files were deleted without git rm, this will commit and delete files)
Switch back to master
git checkout master
Merge branch back to master
git merge <branch_name>
Delete branch after merging is successful
git branch -d <branch_name>
Update changes to repository (origin)
git push
[ GITIGNORE ] Ignore certain files for Git
cat .gitignore
*.[oa] (any files ending in .a or .o)
*~ (any files ending with a ~)