# Git - A Distributed Version Control System (VCS)

Difference between central vs ditributed version control system: 


Check Version - make sure it's installed correctly

```
git --version
```

Set Global Configuration Variables - add my name to checkin and commit 
```
git config --global user.name "Kai Cui"
git config --global user.email "kaicuixxxx@gmail.com"

git config --list
```



### Additional Resources: 
1. Pro Git Book https://git-scm.com/book/en/v2



Common git command - and how to resolve credential issues 

`git pull`
`git status`
`git add . `
`git commit -m "new feature"`
`git push `

`git branch -a `
`git checkout `

`printf "protocol=https\nhost=github.com\n" | git credential fill`

`git config --global credential.helper`

`git config --list | grep credential`

create a new branch 
`git branch new-branch` 

display all branch 
`git branch -a` 

after create a new local branch and made changes - when to merge changes to main do 

`git checkout main` 

then 
`git pull origin main`

then 
`git merge new-branch` 

then 
`git push origin main` 

After the change has been applied delete that branch 
`git branch -d new-branch` -- this deletes it locally 

then 
`git push origin --delete new-branch` -- this delelets it remotely 


