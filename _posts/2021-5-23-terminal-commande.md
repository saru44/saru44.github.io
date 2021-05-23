---
layout: default
title: Terminal Commands
---
### Placeholder for last used command
`!!`
### repeat the last argument of the previous command
`!$`
### folder sizes
#### Individually count the size of each folder in a directory
`for d in envs/*; do du -sh $d; done`
#### count the sizes together and also count the pkgs folder
`du -sh envs/* pkgs`
### customize the prompt display. use ~, change color, 
### prompt in new line add new line after every command
```
sudo nano /private/etc/zshrc
# add the following below the PS1 line
PS1="%B%F{green}%n@%m %1~%b%f "$'\n'"%# "`
source /private/etc/zshrc
```
### zsh for humans(Z4H): pre-customized configuration for zsh
https://github.com/romkatv/zsh4humans






