# M300_BIST
## Command line instructions
``` shell
git global setup
git config --global user.name "Robin Augstburger"
git config --global user.email "robin.augstburger@edu.tbz.ch" 
```

## Create a new repository
```shell
git clone git@gitlab.com:robin.augstburger/M300.git
cd M300
touch README.md
git add README.md
git commit -m "add README"
git push -u origin master
```

## Existing folder
```shell
cd existing_folder
git init
git remote add origin git@gitlab.com:robin.augstburger/M300.git
git add .
git commit -m "Initial commit"
git push -u origin master
```

## Existing Git repository
```shell
cd existing_repo
git remote rename origin old-origin
git remote add origin git@gitlab.com:robin.augstburger/M300.git
git push -u origin --all
git push -u origin --tags
```