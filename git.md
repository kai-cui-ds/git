# Git - A Distributed Version Control System (VCS)

Difference between central vs ditributed version control system: 


### Check Version - make sure it's installed correctly

```
git --version
```

### Set Global Configuration Variables - add my name to checkin and commit 
```
git config --global user.name "Kai Cui"
git config --global user.email "kcxx@gmail.com"

git config --list
```

### Get Help
```
git help config 
git config --help

git help <verb>
git <verb> --help
```

## Case One: Have Local Code Based - need git tracking
```
git init
git status
```

### Ignore Certain Files 
```
touch .gitignore
```
.gitignore is a text file I can add fil names that will be ignored 

### Add Files to Staging Area 
```
git add -A 
git add *

git add .gitignore 
```

### Remove Files from Staging Area 
```
git reset 
git reset file_name.py
```

### Commite Changes 
```
git commit -m "initial commit"
```


### Get Hash Number of the Commit 
```
git log
```


## Case Two: Tracking Exisitng Remote Git Repo 
### Clone Git Repo
```
git clone <url>
``` 

### View Info about the Repo
```
git remote -v
git branch -a
```

### View Changes 
```
git diff
```

### Push Changes 
Need to pull changes first because other devoplers might have made changes. origin is the name of the repo. master is the name of the branch
```
git pull 
git push origin master 
```


## Common Workflow 
### Create Branch for Desired Feature 
This commit is commiting changes to the local branch called divide-func. It has no effect on local master branch or remote master branch. 
```
git branch divide-func
git checkout divide-func
git add 
git commit -m "new feature divide function"
```

### Push Branch to Remote Repo 
-u tells git to associate local divide-func branch with the remote divide-func branch 

origin is the repo's name 

divide-func is the remote branch name 
```
git push -u origin divide-func
```

### Merge Branch 
--merged tells what branch has been merged

while in the master local branch, merge divide-fun into it 
```
git checkout master
git pull origin master 
git branch --merged 
git merge divide-func 
```

### Push Changes to Remote Master Branch 
```
git push origin master
```

### Delete Branch 
first one deletes local branch, then need to push that to remote too 
```
git branch -d divide-func 
git branch -a 
git push origin --delete divide-func
```

### How to resolve credential issues 
```
printf "protocol=https\nhost=github.com\n" | git credential fill

git config --global credential.helper

git config --list | grep credential
```


## Additional Resources: 
1. Pro Git Book https://git-scm.com/book/en/v2
2. Corey Schafter 


