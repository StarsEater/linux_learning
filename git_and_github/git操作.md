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

git push -u origin dev # 推送dev并跟踪远程分支

git push origin :dev #删除远程分支dev
git branch -D dev dev2 # 删除本地分支dev dev ,主要需要切换到其他分支
git branch -m dev dev1 # 修改本地分支dev为dev1
```

### git 多人协作

```shell
git commit -m 'fix #1 添加文件' # 完成1号issue
# 提PR
# create a merge commit: 在组长仓库的master分支上生成新的提交，且保留PR中的所有提交信息
# squash and merge: 压缩合并，PR的提交全部提交压缩成一个
# rebase and merge: 不会生成新的提交

git pull --rebase = git fetch + git rebase # 同步主仓库

git tag v1.0 -m '发布版本1.0' # v1.0标签并备注,，保存在.git/refs/tags
git tag -d v1.0 # 删除tag v1.0
git push origin v1.0 # 推送tag
git push origin :refs/tags/v1.0
```

