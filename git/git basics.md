## Git configuration 

After installing git in local environment, list configuration and set username and email address in global configuration if it is not there.

```shell
git config --list

# set up email and username in local repository enviroment
git config --global --username=dhananjay
git config --global --email=dhananjay.singh011@gmail.com
```

## Set up project 

```shell
#create report repository 
git init
#create some files within the folder and add into repository 
git add .
#do first commit
git commit -m "first commit comment" # -m = adding comment with commit
```

## Add remote repository 

```shell
#add remote repository to local repository 
git remote add origin 'remote-repository-url'

#push local current branch to remote master branch
git push -u origin master #-u = upstream
```

## Create new branch

```shell
#create new branch from current branch
#it only create branch but didn't switch to new branch 
git branch 'new-branch-name'

#create new branch from current branch and checkout also
git checkout -b 'new-branch-name'

```









