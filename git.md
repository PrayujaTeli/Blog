
## [Git and Git command](https://prayuja-teli.github.io/Blog/git)     

> ## History of Git-Hub

Founded	February 8, 2008; 11 years ago.<br/>
Launched	April 10, 2008; 11 years ago.<br/>

GitHub, a subsidiary of Microsoft, is an American web-based hosting service for version control using Git. It is mostly used for computer code.<br/>


> ## History of Git

Developer(s)	Junio Hamano and others.<br/>
Initial release	7 April 2005; 14 years ago.<br/>

Git- is a distributed version control system for tracking changes in source code during software development.<br/>

> ## Git Commands<br/>

#### git clone<br/>

The "clone" command downloads an existing Git repository to your local computer.<br/>
*Syntax* -git clone repository path<br/>

Cloning to a specific folder<br/>
*Syntax* - git clone <repo> <directory><br/>
  
 -l = When the repository to clone from is on a local machine<br/>

#### CLONE OVER HTTPS:<br/>
*Syntax* - $ git clone https://username@repositarypath<br/>
#### CLONE OVER SSH:<br/>
*Syntax* - $ git clone ssh://git@repositarypath<br/>
 
#### Git Pull<br/>

The "pull" command is used to download and integrate remote changes.<br/>
Before using "git pull", make sure the correct local branch is checked out. Then, to perform the pull, simply specify which remote branch you want to integrate:<br/>
$ git checkout repositarypath<br/>
$ git pull origin repositarypath<br/>

#### git pull does two things.<br/>
Updates the current local working branch (currently checked out branch)<br/>
Updates the remote tracking branches for all other branches<br/>

#### Install/set up Git<br/>

sudo apt-get install git<br/>

Tell Git who you are<br/>

First, you need to tell Git who you are:<br/>

git config --global user.email "you@example.com"<br/>
git config --global user.name "Your Name"<br/>


#### Create a new branch<br/>
you’re going to create a new branch, based on master, for new work to go into:<br/>
*Syntax* $ git checkout -b name<br/>

#### git push<br/>
The "push" command is used to publish new local commits on a remote server.git-push - Update remote refs along with associated objects<br/>
*Syntax* - git push origin repositarypath<br/>

#### Important Options<br/>

--all Pushes all local branches.<br/>
--tags  Pushes all local tags.<br/>
--delete Deletes the specified remote branch.<br/>

> ## The tree structure of command<br/>
git add <filename>
now commit your code
git commit -m "added some changes to my repo!"
push changes in master branch to GitHub
git push origin master


#### git commit<br/>
The "commit" command is used to save your changes to the local repository.<br/>

#### Important Options<br/>
-m <message>  Sets the commit's message. Make sure to provide a concise description that helps your teammates (and yourself) understand what happened.<br/>
-a Includes all currently changed files in this commit. <br/>
--amend Rewrites the very last commit with any currently staged changes and/or a new commit message.<br/>
  
  
#### Git status<br/>
git status will list any files that are changed<br/>

![git](https://user-images.githubusercontent.com/50698539/58624031-e2c58900-82ec-11e9-95cc-cfc84c464476.png)










