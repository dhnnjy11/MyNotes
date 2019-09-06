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

## Create and using branch

```shell
#create new branch from current branch
#it only create branch but didn't switch to new branch 
git branch 'new-branch-name'

#create new branch from current branch and checkout 
git checkout -b 'new-branch-name'

#checkout to different branch
git checkout 'branch-name'
```

Some time we need to check if branch has been merged with our master branch, for this purpose we have some command to check 

<b>if use -v or --verbose it displays the information regarding the command</b>

```shell
git branch --merged

git branch --no-merged

git branch -v

```

## Stash the changes 

In some situations, when we want to checkout to other branch but didn't want to commit existing changes, In that case stash is useful to save changes into snapshots and move to another branch. while come back to branch apply stash and get changes back. 

Note : Be careful while applying stash because by default it take the recent stash but to implement specific stash give name of stash that can get by stash list command. 

```shell
#stash the changes 
git stash

#list the stash
git stash list

#get back the stash 
git stash apply

#get back the particular stash
git stash apply 'stash_name'

#clear all stash 
git stash clear
```

## Delete the branch

```shell
#delete the local branch only if it has been already pushed or merged
git branch -d "branch-name"		#-d= --delete

#delete the branch regardless of its pushed and merged status 
git branch -D "branch-name" 	#-D = --delete --force
```

## Merging with another branch

Merge current branch with another local branch 

```shell
git merge "another-branch"
```

## Checking logs

```shell
git log 
git log --oneline
git log --oneline --decorate
git log --graph --all
# --oneline -> show log in one line
# --graph -> show log in graph in graph form 
# --all -> show log that tha is not even merged 
```











