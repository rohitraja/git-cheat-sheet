# git-cheat-sheet
My Git Cheat Sheet



## Branch ##
#### List Branch
```Shell
git branch  
```

#### List last commits and its msg with upstream branch if any
```Shell
git branch -vv
```

#### Create Branch
```Shell
git branch <new-branch-name>
```

#### Create and Checkout Branch
```Shell
git checkout -b <new-branch-name>   
```


#### Create local branch from remote branch
```Shell
git checkout -b <desired_branch_name> origin/<remote_branch_name>
git checkout -b additional_commands origin/additional_commands

```
#### Checkout Branch 
```Shell
git checkout <Branch Name>  
```


#### Clone Git Repository from scratch
```Shell
git clone https://github.com/rohitraja/git-cheat-sheet.git
```
## Multiple Remote Repostory ##
### Work with multiple remote repositories. 
If you wish to have your same code hosted in multiple remote repositories eg. one on Github and one in Heroku
refer these link for more help [Github1](https://help.github.com/en/articles/adding-an-existing-project-to-github-using-the-command-line)  [Github2](https://git-scm.com/book/en/v2/Git-Basics-Working-with-Remotes)

```Shell
$ git remote add origin <URL>
# Sets the new remote
$ git remote -v
# Verifies the new remote URL
# Eg
heroku	https://git.heroku.com/whispering-caverns-58054.git (fetch)
heroku	https://git.heroku.com/whispering-caverns-58054.git (push)
origin	https://github.com/rohitraja/emaily-udemy.git (fetch)
origin	https://github.com/rohitraja/emaily-udemy.git (push)
$ git push heroku master 
# to push it to heroku
$ git push origin master
# to push to Github
```

## Logs ##

#### List Commit logs
```Shell
git log --oneline --graph
```

#### list Commit logs 
```Shell
git log --oneline --decorate
```

#### Checkout a detached branch to a Commit Id
```Shell
git checkout <commit Id>
```

## Amend the  commit ##
### Amend
```Shell
git commit --amend
```
### Change Last Committed User ### 
Reffer [Link](https://www.git-tower.com/learn/git/faq/change-author-name-email)
```
$ git config user.name "Rohit Pahan"
$ git config user.email "rohit.pahan@org.com"
$ git commit --amend --author="Rohit Pahan <rohit.pahan@org.com>"
```
### Fetch to get info ###
```Shell
git fetch
```
### Pull
```Shell
git pull
```

### Version 
```Shell
git remote -v

```
### Set your local branch to upstream where the push should go  -> : if the branch is created local you need to upstream

```Shell
git push --set-upstream origin <branch name>
```


### Difference
```Shell
 git diff <souce> <destination>
```

### Cherry-Pick
```
git cherry-pick -n <commit> # get your patch, but don't commit (-n = --no-commit)
```


### Merge two branches
```Shell
git checkout <target>
git merge <source>
```
### Abort merge
```Shell
git merge --abort
```
### to discard local changes of specific file (it dont keep it in stash)
```Shell
git checkout <path-to-file> 		: 
```
### Commit 
```Shell
Find out, if we have branch A and it has 10 commits, we want to cherry pick and merge commit#1,4,7 to branch B
```
### Config
```Shell
git config --global --add diff.guitool kdiff3
git config --global --add difftool.kdiff3.path "C:\Program Files\KDiff3\kdiff3.exe"
git config --global --add difftool.kdiff3.trustExitCode false
git config --global --add diff.tool kdiff3
```
### Stash changes 
```Shell
git stash save "Save_Name"
git stash apply stash@{index} //will apply the stash and also kep the stash
git stash pop stash@{index}   //will apply the stash and pop it from stash list
git stash drop stash@{n}      //Delete specific stash
```
### Revert to old commit 
```Shell
git revert c6f37fd
```

### Reset 
```Shell
git reset --hard HEAD
git reset --hard 00b9c34
```

### Undoing the Last Commit
```Shell
git reset --soft HEAD~1
```
## Undo commit and redo ## reffer [stackoverflow](https://stackoverflow.com/questions/927358/how-do-i-undo-the-most-recent-commits-in-git)
```
$ git commit -m "Something terribly misguided"             # (1)
$ git reset HEAD~                                          # (2)
<< edit files as necessary >>                              # (3)
$ git add ...                                              # (4)
$ git commit -c ORIG_HEAD  
```


### Unstage and remove paths only from the index
```
git rm --cached -r <Folder Name>
git rm --cached -r public_html/GrosumCordova/plugins
```


### Config 
```
git config --add remote.origin.proxy ""  //bypass Proxy

git config --global --get http.proxy     // check Proxy
```
### Reflog 
```Shell
git reflog
```
### Difftool 
```Shell
git difftool --tool kdiff3
```


### Push Upstream 
```Shell
 git push --set-upstream origin b1
```


### Include private repos in Package.json of Node project to do npm install 
```Shell
Eg: To include private repositoy in Node project in package.json file

  "dependencies": {
    "repo1": "<protocol>://[<user>[:<password>]@]<hostname>[:<port>][:][/]<path>[#<commit-ish> | #semver:<semver>]
",
    "repo2": "git+https://user123:password123@github.com/abc/xyz.git#master"
 }
 
 Note: If you have "@" in you password you may face issues. 
```












