# git-cheat-sheet
My Git Cheat Sheet


### Commit : this command will commit all the changes regardless of add.
```Shell
git commit -a -m "msg"    
```
### Difference
```Shell
 git diff <souce> <destination>
```
### Commit logs
```Shell

git log --oneline --graph
```
### List Branch
```Shell

git branch  
```

### Create Branch
```Shell
git branch b1   
```

### Checkout Branch 
```Shell
git checkout <Branch Name>  
```
### Fast Merge 
```Shell

Merge via ->> fast forward
```
### recusive statagy 
```Shell

Merge via
```

### Log of commits
```Shell
git log --oneline --decorate
```


### Checkout 
```Shell
git checkout <versionid>
```


### Checkout Branch  : if you want to create branch from that older version.
```Shell
git checkout -b <new-branch-name>   
```

### Amend the  commit
```Shell
git commit --amend
```
### Commit 
```Shell
export https_proxy = www-proxy.us.oracle.com:80  :  proxy command to bypass vpn
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






