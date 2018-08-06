[TOC]

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
