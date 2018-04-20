# SYSTEM ALIAS

## 进入相关目录 && 进入目录打开编辑器

```SH
TBD...

```

## 常用目录

```sh
## vscode
alias code='/Applications/Visual\ Studio\ Code\ .app/Contents/Resources/app/bin/code'
alias gm='git add . && git commit -m'
alias gp='git push'
alias gr='git rebase -i HEAD\~3'
alias logs='git reflog'
alias g='git'
alias gmend='git add . && git commit --amend'
alias gs='git status'
alias gd='git diff'
alias g='git'
alias zshrc="vi \~/.zshrc"
alias y='yarn'
alias aliyun='ssh root@aliyun'
alias ck='git checkout'
alias log='git log --oneline --decorate'
alias tree='git log --oneline --decorate --graph'
alias g='git'
alias ck='git checkout'
alias   gf='git fetch'
alias ga='git add .'
```

## 设置默认文件类型打开

```sh
alias -s text='vi'
alias -s js='vi'
alias -s md='vi'
alias -s css='vi'
alias -s h='vi'
alias -s ts='code'
alias -s jsx='code'
alias -s tsx='vi'
alias logdb='mongod  --dbpath /tmp/data'
```

```sh
export PATH=/usr/local/mongodb/bin:${PATH}
```

## chrome

```sh
alias chrome="/Applications/Google\ Chrome.app/Contents/MacOS/Google\ Chrome"
alias chrome-canary="/Applications/Google\ Chrome\ Canary.app/Contents/MacOS/Google\ Chrome\ Canary"
alias chromium="/Applications/Chromium.app/Contents/MacOS/Chromium"
```

Usage

```sh

## Step1
cp shell_alias.txt ~/.shell_alias

## Step2

## .zshrc / .bash_profile
test -f \~/.shell\_alias && source \~/.shell\_alias # .zshrc or .bash_profile

```