Git Commands
Untracked(local) -> Commit (local) -> Staged(local)-> Push (Master)
Initialize a local folder (master) to be a Git repository: 
git init
[ STATUS ] Check for any changes to local (master) repository: 
git status
git status -s (abbreviated output)
[ ADD ] "Untracked files" or modified files can be registered to the Git repository (staging): 
git add <filename> OR git add --all (for all files)
git add -A . (dot stands for current dir, -A ensures file deletions included)
git add '*.txt'
[ RESET ] Remove file(s) from Git staging area: 
git reset <filename>
git reset --soft HEAD^ (moves commit back one commit level, places changes in staging)
git reset --hard HEAD^ (undo last commit and discards all changes)
git reset --hard HEAD^^ (undo last two commits and discards all changes)
NOTE: Do not perform the previous three commands after a PUSH has already been made
[ COMMIT ] Capture snapshot of changes to files in staging: 
git commit -m ""  (-m <description of changes>)
git commit -am (-a flagged used for files that are still unstaged, skipping the git add step)
git commit --amend -m "commit description" (Adds commit information to existing commit)
[ LOG ] Review changes made to commit
git log
[ PULL ] Get most recent changes from repository (origin) to local (master): 
git pull origin master
[ REMOTE ] Adding a remote reposition to push files for sharing with team
git remote add origin http://<git address> (origin is the name of the remote repository)
git remote -v (provides a list of all remote repositories)
git remote rm <name> (removes the remote repository path)
[ PUSH ] Upload changes to repository (origin): 
git push -u origin master (-u option remembers the last name and branch for simplicity - git push)
Username/Pwds can be saved. See https://help.github.com/articles/caching-your-github-password-in-git/
[ DIFF ] See what is different from last commit
git diff HEAD (HEAD - last commit on the current branch)
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
