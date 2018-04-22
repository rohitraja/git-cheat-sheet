# git-cheat-sheet
My Git Cheat Sheet


### List Branch
```Shell
git branch  
```

### Create Branch
```Shell
git branch <new-branch-name>
```

### Create and Checkout Branch
```Shell
git checkout -b <new-branch-name>   
```
### Checkout Branch 
```Shell
git checkout <Branch Name>  
```


### Clone Git Repository from scratch
```Shell
git clone https://github.com/rohitraja/git-cheat-sheet.git
```

### List Commit logs
```Shell
git log --oneline --graph
```

### list Commit logs 
```Shell
git log --oneline --decorate
```

### Checkout a detached branch to a Commit Id
```Shell
git checkout <commit Id>
```

### Amend the  commit
```Shell
git commit --amend
```
### Fetch to get info 
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
git push --set-upstream origin <branch name>  ```
```


### Difference
```Shell
 git diff <souce> <destination>
```


### create local branch from remote branch
```Shell
git checkout -b sf origin/serverfix           : 
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
git stash
```
### Revert to old commit 
```Shell
git revert c6f37fd
```

### Rest 
```Shell
git reset --hard 00b9c34
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





1. So this config file is global or local. ?
   yes it has global and local copy of config file. 


2. From the same repository you can commit with different user name. if multiple users are configured. 

3. When you do commit. Only the last changes you have added using "git add <file>" will go to state, not the one one which you have't added. 






