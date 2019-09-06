## Add remote repository

```shell
#add remote repository to local repository 
git remote add origin 'remote-repository-url'

#push local current branch to remote master branch
git push -u origin master #-u = upstream
```



## Fetch the updates from remote branch 

```shell
#for all branches from remote origin
git fetch origin

# fetch all branches commits from all remotes
git fetch --all

git fetch origin 'remote-branch-name'
```

After fetch command its only half work done, we need to merge the changes in order to update our local branch. 

## Merging with the branch

At the time of updating our local branch by remote repository, it is needed to give branch name for merging or pulling.

```shell
git merge origin 'remote-branch-name'
```

But if we don't want to use to command for fetching and then merging, we do same thing with one command. 

At the time of merge, their is possibility of getting some conflict. If you have no confidence it is better to abort the merge

```shell
get merge --abort
```

## Fetch and Merge with the branch

```shell
git pull origin 'remote-branch-name'
```

why use two command if we have one command to do both fetching and merging, well it depend on use case, if you want to check the changes on remote branch and then merge it you can do it by fetching and then merging with branch. It is good to have more options when requirment can be changed. 







