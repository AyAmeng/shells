# Git 骚操作

## HA

```sh
to be continue...
```

## git fsck

```sh

# Dangling blob
git reflog expire --expire=now --all
git gc --prune=now

```

## git remote

```sh
git remote -v # 当前的远程地址

git remote set-url origin $URL # 设置当前仓库的远程地址到$URL

git remote set-branches [--add] <name> <branch>... 
git remote set-url [--push] <name> <newurl> [<oldurl>] 
git remote set-url --add <name> <newurl> 
git remote set-url --delete <name> <url>

```
