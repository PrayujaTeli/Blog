
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
git add filename<br/>
now commit your code<br/>
git commit -m "added some changes to my repo!"<br/>
push changes in master branch to GitHub<br/>
git push origin master<br/>


#### git commit<br/>
The "commit" command is used to save your changes to the local repository.<br/>

#### Important Options<br/>
-m <message>  = Sets the commit's message. Make sure to provide a concise description that helps your teammates (and yourself) understand what happened.<br/>
-a  = Includes all currently changed files in this commit. <br/>
--amend  = Rewrites the very last commit with any currently staged changes and/or a new commit message.<br/>
  
  
#### Git status<br/>
git status will list any files that are changed<br/>

![git](https://user-images.githubusercontent.com/50698539/58624031-e2c58900-82ec-11e9-95cc-cfc84c464476.png)


#### git branch<br/>

1.Create a new branch<br/>
*syntax*- git checkout -b branch_name<br/>
2.Push your branch to the remote repository<br/>
*syntax*- git push -u origin branch_name<br/>

The command will create a local branch 
git checkout --track origin/branch_name

#### git merge<br/>
The "merge" command is used to integrate changes from another branch.<br/>
Use the merge command to merge branches.<br/>
*syntax* - $ git merge <commit><br/>
  
#### To merge branches<br/>

git checkout a(you will switch to branch a)<br/>
git merge b (this will merge all changes from branch b into branch a)<br/>
git commit -a (this will commit your changes)<br/>

#### git tag<br/>

Tag operation allows giving meaningful names to a specific version in the repository.<br/>
There are two types of tags in Git: <br/>
1.Annotated<br/>
2.lightweight.<br/>

#### 1.Annotated Tag
User can provide a tag name with -a option and provides a tag message with –m option.If you want to tag a particular commit.<br/>
Command -<br/>
git tag -a  identifier -m message<br/>
Now another user can view all the available tags by using the Git tag command with –l option also user can use the Git show command followed by its tag name to view more details about tag in which below details will be displayed - author name, release notes, tag-message, Name of Tagger and Date of Tag, Commit statements.<br/>

#### 2. Lightweight Tags<br/>
Lightweight tags are the simplest way to add a tag to your git repository because they store only the hash of the commit they refer to. They are created with the absence of the -a, -s, or -m options and do not contain any extra information.
Command-<br/>
git tag  identifier<br/>

#### Listing tags - 
git tag <br/>
For special Keyword search use wildcard<br/>
git tag -l ‘wildcard’<br/>
Note -User can give wildcards to sort the output.<br/>
when you call git tag you do not get to see the contents of your annotations. To preview them you must add -n to your command: git tag -n <br/>
After n user can mention number to show that much amount of output on the screen.<br/>

#### Editing tags - <br/>

git tag -a -f tag_identifier commit_id <br/>

Instead of having to delete it and re-add the tag you can simply replace it while keeping the existing description. Choose the place in your commit history with <commit_id> where you want the tag moved to and add -f or -force to your command.

#### Deleting tags - <br/>

User can use the following command to delete tags from the local as well as the remote repository.<br/>
git tag -d identifier<br/>

#### Publishing tags -<br/>
git push <location> <tag_identifier><br/>
A tag is just a reference to your local repository and it is not automatically pushed to the remote repository with the rest of the code. Instead, you can git push the tag individually, or you can run git push --tags which will push all tags at once.<br/>
  
#### Sorting tags -<br/>
git tag --sort=type<br/>
When looking at a project with lots of tags, using the sort option can come in handy. Supported types are:<br/>
refname (sorts in a lexicographic order),<br/>
version:refname or v:refname (here tag names are treated as versions).<br/>
git tag -l --sort=-version:refname "wildcard"<br/>


#### Feel free to share feedback please.
