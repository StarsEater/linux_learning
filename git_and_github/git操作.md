>

###  git仓库

![img](git操作/document-uid310176labid9805timestamp1548755776759.png)

```shell
git add .
git add file # 将file添加到暂存区，暂存区只是记录修改
git reset -- file / git rm --cached file # 撤销暂存区的修改，回到工作区
git diff # 查看工作区被追踪文件的修改情况
git diff -- cached # 查看暂存区的全部修改
git log #查看版本区的提交记录

git config --global user.email "853138468@qq.com"
git config --global user.name "starsEater"
git config -l / cat -n ~/.gitconfig

git commit -m "commit file" #  提交暂存区
git branch -avv # 产看全部分支信息 

git reset --soft HEAD^ # 撤销最近一次的提交，修改还原到暂存区
git reflog  # 查看版本
git reset --head HEAD@{1} # 回退到特定版本
```



### git 分支操作

```shell
git config --global alias.st status # 别名
git fetch # 将远程仓库的分支信息拉取到本地，刷新本地分支
git rebase origin/master # 本地分支基于远程仓库的master分支
git branch dev # 创建分支dev
git checkout dev #切换到分支
git checkout -b dev # 创建分支并切换到新分支

git push origin dev: dev1 # 将本地分支dev推送到origin的dev1分支上
git branch -u origin/dev dev #将本地分支dev与远程分支origin/dev关联，u是unset-upstream的缩写
git branch --unser-upstream dev #撤销分支对远程分支的跟踪

```

