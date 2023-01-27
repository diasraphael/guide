# GIT

To list all the branches
`git branch`

To create a new branch
`git branch branchname`

To Merge
`git checkout branchname`
`git merge master`

To delete a branch
`git branch -d branchname`

To List the commits in the branch
`git log`

git pull
It is the short hand for git fetch and git merge branchname

## Git workflow

![image info](../../images/git-workflow.png)

### Develop

Create feature from develop

Merge it back to develop

Create release from develop

Merge release to master

Merge release to develop

### Master

Create hotfix from master

Merge hotfix to master

Merge hotfix to develop

Git-flow to automate this process

#### Git tags

It is used to mark the release version we use tags

git push --tags will push the tage we have created in local

#### Git stash

Stash will remove the changes from local

To list all the stashed changes

```
git stash list

git stash pop stash@{0} // to select corresponding stash

To delete the list from stash

git stash drop stash@{0}

To see the contents in stashed content

git stash show stash@{0}
```

#### cherrypick

To copy your changes from one branch to another branch

```
git checkout develop

git cherry-pick a3747567
```

The contents from other branch is copied to develop branch as new commit. hash-id can be taken using git log

### Using different names to push changes to github

Each project will have a .git folder, go inside and do the below cmd

```
git config user.name dias

git config user.email diasraphael@gmail.com
```

### Using alias to git cmds

```
git config alias.s status

git s

git config alias.co checkout

git config alias.c commit

git config alias.p push

Inside gitconfig

alias gs 'git status'
```
