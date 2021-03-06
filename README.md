# Git commands
  
-- basic setup (git) -- 

	$ git config --global user.name "your name"                     
	$ git config --global user.email "your_email@entity.com"
	$ git config --global color.ui true

-- create new project git -- 

	$ cd 'my folder name' # go in your root project folder or create one with mkdir folder
	$ git init # set folder to git control

-- git add files to git index	--

	$ git add .
	$ git add <file>
	$ git add --all
	$ git add *.txt
	$ add docs/*.txt
	$ add docs/
	$ git add file_name 

 -- git commit --  

	$ git commit -m "my first commit" 
	$ git commit -a -m "my second commit"
	$ git commit --amend # Changing the Last Commit
	$ git commit --amend # if you want to reuse the previous commit message as-is.


 -- pushing changes --  

	$ git push origin master

-- clone repo -- 

	$ git clone https://github.com/startup-entity-development/server-side.git
	$ git clone https://github.com/startup-entity-development/server-side.git git-demo

-- discarding the Last Commit--

	$ git reset HEAD~
	
-- check the repo status -- 

	$ git status
 
-- git log --

	$ git log --
	$ git log --oneline --stat
	$ git log --oneline --graph
	
--git remote --

	$ git remote add origin https://github.com/startup-entity-development/server-side.git
	$ git remote set-url origin https://github.com/startup-entity-development/server-side.git
	$ git remote rm <name/origin>
	$ git remote -v
	$ git remote show origin
	$ git remote prune origin

-- show changes between commit,  working tree and etc --

	$ git diff 
	$ git diff --staged

-- create a new branch --

	$ git branch nameBranch

--  switch back to master -- 

	$ git checkout master

-- display a list with the branches --

	$ git branch
	$ git branch -d nameBranch

-- delete the branch and merge into the master --

	$ git branch -D nameBranch 

-- delete the branch without asking --
	
	$ git checkout -b amend-my-name

-- git tag -- 

	$ git tag
	$ git tag -a <version> -m "V x.xx.xx"
	
-- git fork --

	$ git remote add upstream https://github.com/startup-entity-development/server-side.git
	$ git fetch upstream
	$ git merge upstream/master9


-- GIT REBASE --

-- The rebase is used when working with branches this makes the branches catch up with the master without affecting it --

-- join the current branch with the master (this cannot be seen as a merge) --

	$ git rebase

-- when a conflict occurs, there are the following options: --
-- when we resolve conflicts --continue continues the sequence of the rebase where it was paused --

	$ git rebase --continue

-- skip the conflict and continue --
	$ git rebase --skip

-- Returns to the beginning of the rebase --
	$ git rebase --abort

-- to rebase a specific branch --
	$ git rebase <nameBranch>


-- OTHER COMMANDS --


-- removes a file from HEAD and puts it in the status of not worked --

	$ git checkout -- <file>

-- create a branch based on an online one --

	$ git checkout -b newlocalbranchname origin/branch-name

-- check for changes and update the repository --

	$ git pull origin <nameBranch>


-- join the current branch with the specified one --
	$ git merge <nameBranch>

-- verify changes in the repository online with the local --
	$ git fetch

-- delete a file from the repository --
	$ git rm <file>

-- Synchronizing your local changes with the upstream repository -- 
	
	$ cd foldername -Change the current working directory to your local project.

-- Change to your desired branch -- 

	$ git checkout branch_name
	$ git remote -v # check the origin as a remote

-- if the origen is not remote -- 

	$ add git remote add upstream https://github.com/startup-entity-development/learningGit.git 

-- Sync your local repository with the upstream (the original one) --

	$ git fetch upstream

-- Perform merge --

	$ git merge upstream/master

-- and the end push your local changes to your repository--

	$ git push
	
-- SHH KEY AND GITHUB --

	$ ls -al ~/.ssh # to see if existing SSH keys are present

-- create new ssh key -- 

 	$ssh-keygen -t ed25519 -C "your_email@example.com" # don't use blank passphrase 

-- Adding your SSH key to the ssh-agent --
	
	$ eval "$(ssh-agent -s)" # start the ssh-agent in the background.
	$ ssh-add ~/.ssh/id_ed25519 # Add your SSH private key to the ssh-agent. 
     	copy the content of id_ed25519.pub that is your ssh-key ;)
