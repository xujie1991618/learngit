﻿git是一个版本控制工具

## 初始化 
git init

## 添加和提交
git add file(文件)
git commit -m "日志"

## 查看状态和不同点
git status
git diff

## 日志和commit后版本回退
git log
git log --pretty=oneline
git reset --hard HEAD^
git reset --hard HEAD~100
git reset --hard commit_id(版本号)
git reflog 

## 工作区和暂存区
git add是将工作区提交到暂存区，暂存区分为stage和HEAD(master)；再使用git commit将stage提交到HEAD(master)中。
cat file查看内容

## 撤销修改
git checkout -- file 
git reset HEAD file 

## 删除文件
rm file
git rm file

## 远程仓库
git remote add origin git@github.com:xujie1991618/learngit.git
git push -u origin master
由于远程库是空的，我们第一次推送master分支时，加上了-u参数，Git不但会把本地的master分支内容推送的远程新的master分支，还会把本地的master分支和远程的master分支关联起来，在以后的推送或者拉取时就可以简化命令。

## 克隆
git clone git@github.com:xujie1991618/learngit.git
