[TOC]

Git 基础功能列表：
 - 安装Git
 - 创建版本库
 - 远程仓库
 - 分支管理
 - 标签管理
 - GitHub
 - 自定义Git


## 初始化一个Git仓库
使用git init命令。
```
git init
```

## 添加文件到Git仓库
分两步：

1. 使用命令git add <file>，注意，可反复多次使用，添加多个文件；
  ```
  git add readme.txt
  ```
2. 使用命令git commit -m <message>，完成。
  ```
  git commit -m "wrote a readme file. "
  ```
## 查看仓库当前的状态

git status命令可以让我们时刻掌握仓库当前的状态

## 查看上次的修改

git diff

