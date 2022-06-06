

### 添加ssh关联授权

```shell
ssh-keygen 
#生成公私钥，默认保存在 C:\Users\QinYe\.ssh
# 复制文件内容到右上角的Settings,进入SSH and GPG keys，添加到key栏中

git remote -v # 查看本地仓库关联的远程仓库的信息

git clone [-o originnn]  url  dir # 将url的仓库重命名复制到本地dir路径
```

### 多人协作

```shell
# gitignore 文件存放忽略的文件
git checkout v1.0 # 切换到某个提交版本
git checkout -b dev2 # 将上述的版本固定到一个新的分支上并切换到该分支
```

