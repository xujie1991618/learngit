git是一个版本控制工具

## 初始化 
  git init 

## 添加和提交
  git add file(文件)</br>
  git commit -m "日志" </br>

## 查看状态和不同点
  git status </br>
  git diff </br>

## 日志和commit后版本回退
  git log </br>
  git log --pretty=oneline </br>
  git reset --hard HEAD^ </br>
  git reset --hard HEAD~100 </br>
  git reset --hard commit_id(版本号) </br>
  git reflog </br>

## 工作区和暂存区
  git add是将工作区提交到暂存区，暂存区分为stage和HEAD(master)；再使用git commit将stage提交到HEAD(master)中。 </br>
  cat file查看内容 </br>

## 撤销修改
  git checkout -- file </br>
  git reset HEAD file </br>

## 删除文件
  rm file</br>
  git rm file</br>

## 远程仓库
  git remote add origin git@github.com:xujie1991618/learngit.git </br>
  git push -u origin master </br>
  由于远程库是空的，我们第一次推送master分支时，加上了-u参数，Git不但会把本地的master分支内容推送的远程新的master分支，还会把本地的master分支和远程的master分支关联起来，在以后的推送或者拉取时就可以简化命令。 </br>

## 克隆
  git clone git@github.com:xujie1991618/learngit.git </br>

## 创建合并分支
  git checkout -b <name> </br>
  git checkout命令加上-b参数表示创建并切换，相当于以下两条命令：</br>
  git branch <name> (创建分支)</br>
  git checkout <name> (切换分支)</br>
  git branch (查看分支)</br>
  git merge <name> (合并分支)</br>
  git branch -d <name> (删除分支)</br>