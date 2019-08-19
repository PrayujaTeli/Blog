## [Rebasing and merging](https://prayuja-teli.github.io/Blog/Git)     


> ## Rebasing <br/>

The rebase re-writes the changes of one branch onto another without creating a new commit.<br/>


#### How to do it<br/>
Rebase the feature branch onto the master branch using the following commands.<br/>
$ git checkout feature<br/>
$ git rebase master<br/>


>## What Is Git Merge?<br/>

Git merge allows you to merge branches from Git.
Merging is a common practice for developers using version control systems. Whether branches are created for testing, bug fixes, or other reasons, merging commits changes to another location. To be more specific, merging takes the contents of a source branch and integrates it with a target branch. In this process, only the target branch is changed. The source branch history remains.<br/>
 
#### Merging Pros and Cons<br/>

#### Pros:<br/>

Simple to use and understand and familiar.</br>
Maintains the original context of the source branch.<br/>
The commits on the source branch are separated from other branch commits. This can be useful if you want to take the feature and merge it into another branch later.<br/>
Preserves your commit history and keeps the history graph semantically correct.<br/>

#### Cons:<br/>
History can become intensely polluted by lots of merge commits because multiple people are working on the same branch in parallel. Visual charts of your repository can become a mess.<br/>
Debugging using git bisect can become harder.<br/>

#### How to do it<br/>
Merge the master branch into the feature branch using the checkout and merge commands.<br/>
$ git checkout feature<br/>
$ git merge master<br/>
 
(or)<br/>
 
$ git merge master feature<br/>



























