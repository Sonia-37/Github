# Github
If I ever forget how to use github

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
