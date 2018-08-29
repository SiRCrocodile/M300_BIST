# M300_BIST
## Command line instructions
``` shell
git global setup
git config --global user.name "<username>"
git config --global user.email "<mail>"
```

## Create a new repository
```shell
git clone git@gitlab.com:git@github.com:SiRCrocodile/M300_BIST.git
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
git remote add origin git@github.com:SiRCrocodile/M300_BIST.git
git add .
git commit -m "Initial commit"
git push -u origin master
```

## Existing Git repository
```shell
cd existing_repo
git remote rename origin old-origin
git remote add origin git@github.com:SiRCrocodile/M300_BIST.git
git push -u origin --all
git push -u origin --tags
```