## [Rebasing and Merging](https://prayuja-teli.github.io/Blog/Git)     


 ## Merging <br/>

Merging is a common practice for developers using version control systems. Whether branches are created for testing, bug fixes, or other reasons, merging commits changes to another location. To be more specific, merging takes the contents of a source branch and integrates it with a target branch. In this process, only the target branch is changed. 

#### Merging Pros and Cons<br/>

#### Pros:<br/>

1. Simple to use and understand and familiar.<br/>
2. Maintains the original context of the source branch.<br/>
3. The commits on the source branch are separated from other branch commits. This can be useful if you want to take the feature and merge it into another branch later.<br/>
4. Preserves your commit history and keeps the history graph semantically correct.<br/>

#### Cons:<br/>
1. History can become intensely polluted by lots of merge commits because multiple people are working on the same branch in parallel.<br/>
2. Visual charts of your repository can become a mess.<br/>

#### How to do it<br/>
Merge the master branch into the feature branch using the checkout and merge commands.<br/>
$ git checkout feature<br/> 
Feature is branch from Git master.<br/>
$ git merge master<br/>
 
(or)<br/>
 
$ git merge master feature<br/>

#### Git Checkout -<br/>

A checkout is the act of switching between different versions of a target entity.<br/>


 ## Rebasing <br/>
 
The rebase re-writes the changes of one branch onto another without creating a new commit.<br/>
 
#### Rebasing Pros and Cons <br/>

#### Pros: <br/>
1. Code history is simplified, linear and readable.<br/>
2. Manipulating a single commit history is easier than a history of many separate feature branches with its additional commits.<br/>
3. Clean, clear commit messages make it better to track a bug or when a feature was introduced.<br/>

#### Cons: <br/>

1. Rebasing doesn't work with pull requests, because you can't see what minor changes someone made. Rewriting of history is bad for teamwork!<br/>
2. It requires more work when dealing with conflicts. Using rebase to keep your feature branch updated requires that you resolve similar conflicts again and again.<br/>
3. While with merging, once you solve the conflicts, you're set. You have to resolve the conflict in the order they were created to continue the rebase.<br/>

#### How to do it<br/>
Rebase the feature branch onto the master branch using the following commands.<br/>
$ git checkout feature<br/>
$ git rebase master<br/>

#### When to use rebase and when to use merging?<br/>

If the feature branch you are getting changes from is shared with other developers, merging is recommended, because the rebasing process will create inconsistent repositories.<br/>
For individuals, rebasing makes a lot of sense.<br/>
If you want to see the history completely same as it happened, you should use merge. Merge preserves history whereas rebase rewrites it.<br/>











