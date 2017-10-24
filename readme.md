git是一个版本控制工具

## 初始化 
  `git init`

## 添加和提交
  `git add <file>`(提交文件)</br>
  `git commit -m "日志"` </br>
  `git add -A` (提交所有) </br>

## 查看状态和不同点
  `git status` (查看状态)</br>
  `git diff` (查看不同点)</br>

## 日志和commit后版本回退
  `git log` </br>
  `git log --pretty=oneline` (日志简略)</br>
  `git reset --hard HEAD^` (版本回退)</br>
  `git reset --hard HEAD~100` </br>
  `git reset --hard <commit_id>` (版本号) </br>
  `git reflog` </br>

## 工作区和暂存区
  git add是将工作区提交到暂存区，暂存区分为stage和HEAD(master)；再使用git commit将stage提交到HEAD(master)中。 </br>
  `cat <file>` (查看文件内容) </br>

## 撤销修改
  `git checkout -- <file>` </br>
  `git reset HEAD <file>` </br>

## 删除文件
  `rm <file>`</br>
  `git rm <file>`</br>

## 远程仓库
  `git remote add origin git@github.com:xujie1991618/learngit.git` (关联远程库)</br>
  `git push -u origin master` (第一次push)</br>
  由于远程库是空的，我们第一次推送master分支时，加上了-u参数，Git不但会把本地的master分支内容推送的远程新的master分支，还会把本地的master分支和远程的master分支关联起来，在以后的推送或者拉取时就可以简化命令。 </br>

## 克隆
  `git clone git@github.com:xujie1991618/learngit.git` </br>

## 创建合并分支
  `git checkout -b <name>` </br>
  git checkout命令加上-b参数表示创建并切换，相当于以下两条命令：</br>
  `git branch <name>` (创建分支)</br>
  `git checkout <name>` (切换分支)</br>
  `git branch` (查看分支)</br>
  `git merge <name>` (合并分支)</br>
  `git branch -d <name>` (删除分支)</br>
  ·git branch -D <name>· (强制删除)</br>
  
## 解决冲突
  `git log --graph --pretty=oneline --abbrev-commit` (分支合并图)</br>
  
## 分支管理策略
  `git merge --no-ff -m "merge with no-ff" <name>` </br>
  因为本次合并要创建一个新的commit，所以加上-m参数，把commit描述写进去。</br>
## bug分支
  `git stash` (储藏)</br>
  `git stash list` (查看储藏)</br>
  `git stash apply` (恢复)</br>
  `git stash drop` (删除)</br>
  `git stash pop` (恢复并删除)</br>
  一是用`git stash apply`恢复，但是恢复后，stash内容并不删除，你需要用`git stash drop`来删除；</br>
  另一种方式是用`git stash pop`，恢复的同时把stash内容也删了。</br>
## 多人协作
  `git remote` (查看远程库)</br>
  `git remote -v` (查看远程库详情)</br>
  
## 标签
  `git tag` (查看所有标签) </br>
  `git tag <name>` (建标签)</br>
  `git tag <name> <commit_id>` </br>
  `git show <tagname>` (查看标签内容)</br>
  `git tag -a <tagname> -m "说明" <commit_id>` (创建标签和说明)</br>
  `git tag -s v0.2 -m "signed version 0.2 released" <commit_id>` (使用PGP签名)</br>
  `git tag -d <tagname>` (删除标签)</br>
  `git push origin <tagname>` (推送标签)</br>
  `git push origin --tags` (推送所有标签)</br>
  如果标签已经推送到远程，要删除远程标签就麻烦一点，先从本地删除,然后，从远程删除。删除命令也是push，但是格式如下:
  `git push origin :refs/tags/<tagname>`