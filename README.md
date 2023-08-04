# GIt
A reference for useful git commands with explanation of its usage.

## Beginners
1. creates a folder
   ```
   mkdir <DIR NAME>
   ```
2. TO open the folder in vs code.
   ```
   code .
   ```
3. The following command initiallizes an empty git repository.
   ```
   git init
   ```
   >Note:
   >1. Creates .git file which implies this is a repository.
   >2. Deleting .git removes the repository status of the folder.
4. To check for tracked and untracked files.
   ```
   git status
   ```
>Note: Before adding files to track. Add path of file or folder that need not be tracked to .gitignore file.
>   To create the file,
>   ```
>   touch .gitignore
>   ```
>   Then open the .gitignore file and add paths of files and folders that needs to be neglected when syncing to remote repository.
>
5. To track all files.( i.e, add these files to tracked label so that it can be commited later)
   ```
   git add .
   ```
6. To commit changes locally.
   ```
   git commit -m "<COMMIT MESSAGE>"
   ```
7. At times with latest git the branch might be master you can change it to main using,
   ```
   git branch -M main
   ```
## To Sync Changes
Assuming you have now created some files in your directory and you want to save them in your GitHub.
1. To set up remote where the changes need to be saved or synced later
   ```
   git remote add origin <REMOTE GITHUB REPO URL>
   ```
2. To check,
   ```
   git remote -v
   ```
3. To push changes,
   ```
   git push origin <BRANCH NAME>
   ```
   > The following might even come handy for setting the upstream branch
   ```
   git push -u origin <BRANCH NAME>
   ```
   or
   
   ```
   git push --set-upstream origin <branch name>
   ```
   >Note: Once upstream is set next time onwards you can push just using git push.
5. To pull changes, (it does fetch + merge)
   ```
   git pull origin <BRANCH NAME>
   ```
   >Note: if git pull gets aborted due to files in the local might be lost during merge and if you want to override and
   >still merge.
   ```
   git fetch <URL> <branchname>
   ```
   ```
   git reset --hard fetch_head
   ```

## Working with feature branches:
1. To work on a feature without disturbin the main or base branch use the following command to copy and create a new branch
   ```
   git checkout -b <branch name>
   ```
2. To make a copy locally of some repository and then work
   ```
   git clone <REMOTE REPO URL>
   ```
link for reference: https://www.nobledesktop.com/learn/git/stage-commit-files
