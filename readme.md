Common git command - and how to resolve credential issues 

git pull 
git status
git add . 
git commit -m "new feature"
git push 

git branch -a 
git checkout 

printf "protocol=https\nhost=github.com\n" | git credential fill

git config --global credential.helper

git config --list | grep credential

