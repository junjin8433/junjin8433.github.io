---
layout: post
section-type: post
title: Basic operations of Git
category: tech
tags: [ 'tutorial' ]
---

## set git global username&useremail
```zsh
git config --global user.name "junjin8433"
git config --global user.email "michael-johns@qq.com"
```

## create a new repository
create a new floder and cd into it, then excute:

```zsh
git init
```

## clone a repository to local machine
```zsh
git clone username@host:repository
```

## add & commit
```zsh
git add <filename>
git add .
git commit -m "commit info"
```

## push the change
master can be any branch

```zsh
git push origin master
```
if the local repository hasn't been linked to any remote server,you should:

```zsh
git remote add origin <server>
```

## branch
create a branch and switch into it

```zsh
git checkout -b branch_name
```
switch back to master:

```zsh
git checkout master
```
delete a branch

```zsh
git branch -d branch_name
```

## update & merge
update local repository to newest

```zsh
git pull
```
merge another branch with current one,it may not success everytime

```zsh
git merge <branch>
```

## reset to old version
'reset' only changes the HEAD, you need to push it

```zsh
git reset -hard <version_number>
git push origin master
```
