---
layout: post
title: Git Commands
---

## Git setup
#### Git installation
```console
brew install git
git --version
> git version 2.31.1
```
#### Git initialization
```
cd [path\to\your\dir]
git init

# check initialization
ls -a
git status
```
#### renaming default git branch from 'master' to 'main'
```
# global configuration
git config --global init.defaultBranch main

# New repo & git version >= 2.28.0
git init --initial-branch=main [or]
git init -b main

# New repo & git version < 2.28.0
# the branch `master` doesnot actually exist. It is created only at first commit.
git init
git checkout -b main

# rename the present branch to main
git branch -m main
```
#### configuring username and email
```
git config --global user.name "your name"
git config --global user.email "your@email.com"
```
#### 
