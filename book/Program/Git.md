# Git

## 安装
ubuntu、debian、deepin
```
apt-get install git
```

centos、redhat
```
yum install git
```

windows
[下载地址：](https://git-scm.com/downloads)

--------------------------------------------------
## 使用

### 克隆代码
$ git clone [仓库地址] [别名]
or
$ git clone https://[用户名]:密码@https仓库地址 [仓库地址] [别名]

创建仓库并拉取代码
$ git init .
$ git remote add origin [仓库地址]
$ git pull origin master

第一次提交
$ git add 测试.txt
$ git commit -m "提交说明"
$ git push origin master -u  (第一次提交要带-u)

配置不用每次都输账号密码的方式 百度云 git-config.zip 解压缩到 用户.git目录


### 发布、提交
工作模式
$ git add    添加改动
$ git commit 提交到本地仓库
$ git pull   拉取远程并合并
$ git push   推送

查看工作目录下的文件改动
$ git status

查看所有文件改动
$ git diff

查看两次提交之间的差异
$ git log #查看提交
$ git diff <id1> <id2>

查看改动记录
$ git log

查看某次提交
$ git show <id>

查看特定文件的特定提交
$ git show <id>:<file>
