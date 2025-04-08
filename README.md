# Github
If I ever forget how to use github

How to start:
- git config --global user.name "Your Name"
- git config --global user.email "your_email@example.com"
- ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
(if you don't have ssh: https://www.bing.com/videos/riverview/relatedvideo?&q=ssh+on+ubuntu&&mid=06F598FA6B7E532920BC06F598FA6B7E532920BC&mmscn=mtsc&aps=0&FORM=VRDGAR
do till localhost will be working)
- cat ~/.ssh/id_rsa.pub
  
- Add the SSH key to your GitHub account under Settings > SSH and GPG keys

- git init
- git add
- git commit -m "Initial commit"

IMPORTANT STEP OTHERWISE IT MAY WANT TO USE HTTP INSTEAD OF SSH:
- git remote add origin git@github.com:your_username/your_repository.git

- git push -u origin master (here you have to be careful, somtimes it's main and you can also change it: git branch -m master main)
