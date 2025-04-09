# Github
If I ever forget how to use github
Zofia Sikorska
09.04.2025


##How to start:
- git config --global user.name "Your Name"
- git config --global user.email "your_email@example.com"
- ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

(If you don't have ssh: https://www.bing.com/videos/riverview/relatedvideo?&q=ssh+on+ubuntu&&mid=06F598FA6B7E532920BC06F598FA6B7E532920BC&mmscn=mtsc&aps=0&FORM=VRDGAR
do till localhost will be working)
- cat ~/.ssh/id_rsa.pub
  
- Add the SSH key to your GitHub account under Settings > SSH and GPG keys

- git init
- git add
- git commit -m "Initial commit"

IMPORTANT STEP OTHERWISE, IT MAY WANT TO USE HTTP INSTEAD OF SSH:
- git remote add origin git@github.com:your_username/your_repository.git

- git push -u origin master
(Here you have to be careful; sometimes it's central and you can also change it: git branch -m master main)

## Commands
### Adding files to github
- git add
use . if you want all the files to add
- git commit -m "commit name"
- git push origin master/main

### Seeing difference
- git diff
- git add -u (updated)
- git status

### Branches
- git branch branch_name
- git checkout branch_name
- git diff master..branch_name
- git checkout master
- git merge branch_name
- git push

### Restoring
- git log (all the commits)
- git checkout <commit_ID>
- git checkout <commit ID> file_name (for single file)

### Mergin conflicts
If we try to merge two branches and both of them were edited, we'll get a conflict to resolve this:
- git log --merge
- <<<<<<< HEAD
Content of latest edited branch
=======
Content of the other branch
>>>>>>> branch_1
Delete parts you don't want and try again

### Pulling
- git config --global pull.ff false | true| only
false - always creating a merge commit when pulling (preserving an explicit merge history)
true - fast-foward if possible, if not it will create a merge commit (default behavior)
only - only fast-foward pulls (we won't get an unexpected merge commit, we handle diverged branches manually)
- git pull
- git config --global pull.rebase false | true | only
false - (default), Equivalent to git fetch + git merge origin/branch, preserving a clear merge history
true - rebasing intead of merging, Equivalent to git fetch + git rebase origin/branch, keeps history linear
only - only allow rebasing otherwise aborts, avoiding accidental merges
- git fetch

### Other useful commands:
- git config –global color.ui auto –  Set to display colored output in the terminal
- git help  - Display the main help documentation, showing a list of commonly used Git commands.
- git init <directory>  -  Creates a new Git repository in the specified directory.
- git status –ignored  -  	Displays ignored files in addition to the regular status output.
- git diff –staged or git diff –cached  -  Displays the changes between the staging area (index) and the last commit.
- git diff HEAD  -  Display the difference between the current directory and the last commit
- git notes add - Creates a new note and associates it with an object (commit, tag, etc.).
- git restore <file>  -  	Restores the file in the working directory to its state in the last commit.
- git reset <commit>  -  	Moves the branch pointer to a specified commit, resetting the staging area and the working directory to match the specified commit.
- git rm <file>  -  Removes a file from both the working directory and the repository, staging the deletion.
- git mv  -  Moves or renames a file or directory in your Git repository.
- git show  -  	Shows the details of a specific commit, including its changes.


Resources:
- https://github.com/ylla-lab/BT4BR_2025/tree/master/Exercises_Session_4
- https://www.geeksforgeeks.org/git-cheat-sheet/
- My own experience and fails
