---
layout: default
title: Git Commands
---
## Git setup
### Git installation
```console
brew install git
git --version
> git version 2.31.1
```
### Git initialization
```console
cd [path\to\your\dir]
git init

# check initialization
ls -a
git status
```
### renaming default git branch from 'master' to 'main'
```console
# change global configuration to automatically set default branch name to main in new repos 
git config --global init.defaultBranch main

# IF: New repo & git version >= 2.28.0
git init --initial-branch=main [or]
git init -b main

# IF: New repo & git version < 2.28.0
# the branch `master` does not actually exist. It is created only at first commit.
git init
git checkout -b main

# IF: Old repo, go to `master` branch and then rename it to `main`
git checkout master
git branch -m main
```
### configuring username and email
```console
git config --global user.name "your name"
git config --global user.email "your@email.com"
```
### set remote repo's `url` and remote repo's name as `origin`
```console
git remote set-url origin [github path to your repo]
```
