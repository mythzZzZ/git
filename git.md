git 暂存区

版本号（合并文件  定位文件）

idea连接gitee github

![image-20240201163308815](https://zhangwenkang666.oss-cn-beijing.aliyuncs.com/image-20240201163308815.png)



![image-20240201163634359](https://zhangwenkang666.oss-cn-beijing.aliyuncs.com/image-20240201163634359.png)



![image-20240201164257559](https://zhangwenkang666.oss-cn-beijing.aliyuncs.com/image-20240201164257559.png)



![image-20240201164819919](https://zhangwenkang666.oss-cn-beijing.aliyuncs.com/image-20240201164819919.png)



git 指令



```shell
git --version
```

创建仓库

```shell
git init

克隆仓库

git clone url
git clone url rename

配置用户
git config --global user.name 'mythzZzZ' 
配置邮箱地址
git config --global user.email '183772635@qq.com'

暂存区的状态
git status

把工作区中新建的文件添加到暂存区
（不同的分支是不同的工作区，工作区中的文件应该还没有正式写进磁盘，要暂存区commit之后才存入磁盘（磁盘也是本地仓库））
工作区add文件到暂存区-》》暂存区commit到磁盘（本地仓库）
git add file.name


把暂存区所有文件commit到磁盘仓库
 git commit -m 操作的名字
 
 显示提交的历史记录
 git log --oneline


删除文件操作
删除操作和 新增操作是一样的
先在文件夹删除文件 然后add  然后commit

误删除
把工作区的文件删除了，但是文件之前commit到磁盘仓库过，可以从磁盘仓库恢复文件到工作区

git restore filename



如果当前工作区删除了，然后最近的一次commit磁盘也删除了，这时候要从历史记录中恢复

git reset --hard 版本号(这个版本号可以从 git log --oneline中查看)
(reset的一个坏处，会丢失 git log --oneline中的版本信息)

为了避免 reset的缺点
使用revert

git revert 版本号（恢复这个版本号之前的那个版本）



#############################################################################
分支

创建分支
git branch branch.name

查看分支
git branch -v

切换分支
git checkout branch.name

创建分支且切换分支
git checkout -b branch.name

删除分支
git branch -d branch.name


合并分支
先切换到master在合并
git merge branch.name

有冲突后 手动修改文件 然后add 后commit就算合并成功



标签操作
给提交版本号创建别名
git tag 别名 版本号

查看标签
git tag 

删除标签
git tag -d 别名



连接到远程仓库
git remote

推送到远程车库之前先拉取一次
git pull origin

推送到远程仓库
git push origin

查看当前远程连接的仓库 
git remote -v


```

