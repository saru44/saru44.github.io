---
layout: default
title: Github Setup
---

# Setting up Github and Git in MacOS Big Sur 
## Github pages setup
### Ruby and Jekyll installation
```
which ruby
/usr/bin/ruby

ruby -v
ruby 2.6.3p62 (2019-04-16 revision 67580) [universal.arm64e-darwin20]
```
#### Install homebrew (if not already installed)
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
#### Install *rbenv* to manage ruby installations in a separate environment (without disturbing system ruby installation)
```
# install rbenv via homebrew
brew install rbenv

# setup rbenv integration with the shell
rbenv init

# check your rbenv installation
curl -fsSL https://github.com/rbenv/rbenv-installer/raw/HEAD/bin/rbenv-doctor | bash
```
#### install latest stable ruby version
```
# list latest stable releases of ruby
rbenv install --list
2.6.7
2.7.3
3.0.1
...

# install the 3.x.x version of ruby shown in the list
rbenv install 3.0.1

# check different versions of ruby installed on the system (* is default/global version)
rbenv versions
* system
  3.0.1 (set by /Users/saru/.rbenv/version)

# set the 3.x.x as the global version 
rbenv global 3.0.1

# make sure 3.x.x is the default/global version now
rbenv versions
  system
* 3.0.1 (set by /Users/saru/.rbenv/version)
```
#### install jekyll gem locally (avoid global install)
```
gem install --user-install bundler jekyll
```
#### Set PATH variables
```
# check default terminal 
echo $SHELL
/bin/zsh

# append the X.X with the first 2 digits of ruby version. Here version is 3.0.1. So, X.X is 3.0
# for zsh terminal, 
echo 'export PATH="$HOME/.gem/ruby/X.X.0/bin:$PATH"' >> ~/.zshrc

# source the changes from .zshrc and restart the zsh shell
source ~/.zshrc
exec zsh

# check whether ruby path is in PATH variable
gem env

# Remove any duplicates from the PATH. For zsh, 
typeset -U PATH
```


