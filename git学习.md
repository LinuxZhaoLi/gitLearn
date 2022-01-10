## svn和git的区别：

svn:是增量式的管理方式。 版本控制在服务器， 服务器宕机。历史版本数据丢失。 

git: .GIT是分布式的. 本地有版本管理， 避免单点故障。 



本地库：存历史版本  git commit

暂存区： 临时存储  git add 

工作区： 写代码



## 代码托管中心：

局域网： gitLab

外网： github, 码云。

本地库和远程库：

本地到远程库： push 

远程库下载到本地： clone

本地更新： pull

克隆远程库：fork  

## 团队外：

![Snipaste_2022-01-09_19-52-15](E:\github\gitLearn\Image\Snipaste_2022-01-09_19-52-15.png)

初始化本地库：

![Snipaste_2022-01-09_20-00-16](E:\github\gitLearn\Image\Snipaste_2022-01-09_20-00-16.png)

## 设置签名命令： 

1. 项目级别/仓库级别 保存地址： .git/config  

   1. git config user.name tom_pro
   2. git config user.email zhanshengli@qq.com

2. 系统用户级别   保存地址： ~/.gitconfig  

   1. git config --glabel user.name tom_glb
   2. git config --glabel user.email zhaoshengli@qq.com 

3. 优先级别

   1. ​	就近原则： 如果两个级别都有。 使用项目级别签名
   2. ​    如果只有用户级别： 使用的用户级别

   ![Snipaste_2022-01-09_20-12-05](E:\github\gitLearn\Image\Snipaste_2022-01-09_20-12-05.png)

   ## git status:

    on branch master :  在master 分支

   No commit yet: 没有可提交的。

   untracked files: 未追踪的文件。 

   （use "git add <file>..." to include in what will be commited）使用git add 命令将他包含到将要提交的地方。 

   nothing added to commit bu untracked files present (use git add track)

没有添加任何提交的未跟踪文件(使用git add track)  

warning : LF will be replace by CRLF in good.txt. 

The file will have its original line endings in your working directory . 

该文件将在您的工作目录中以其原始行结尾。  

use "git rm --cached <file>..." to unstage    从暂存区释放文件。 撤销添加

Please enter the commit message for your changes. Lines starting 。 

请为您的更改输入提交消息，行开始。  

git commit -m "xx" 提交到本地库。 

Changes not staged for commit:  未提交的更改:  

(use "git add <file>..." to update what will be committed ： 更新的缓存区

(use "git restore <file>..." to discard changes in working directory

(使用“git restore <file>…”丢弃工作目录中的更改  

no changes added to commit (use "git add" and/or "git commit -a")

没有添加到提交的更改(使用“git add”和/或“git commit -a”)  

## P15 版本的前进和后退：

git log   完整 查看日志：

git log --pretty=oneline  

git log online   

git reflog  移动到版本需要多少步。 

```
7259f27 (HEAD -> master) HEAD@{0}: commit: modify git
1f32f2f HEAD@{1}: commit (initial): add git.md
```



## P17: 前进和后退

git reset --hard  后退。   git reset --hard 1f32f2f 

## P18: 其他方式切换版本

^ 后退一个版本，n个回退n步。 

~3 后退3个版本

## P19: hard和soft 以及mixed参数

soft 移动本地库。  本地不会变。 

mixed:    移动本地库和暂存区。 

hard移动本地库， 暂存区， 工作区。

## P20 删除文件找回

提交后的记录是不可磨灭的。 

git reset --hard 5647ff

## p21 添加到暂存区的文件删除找回

rm applet.txt

git add apple.txt 添加到暂存区

git reset --hard 5647ff

## P22  删除文件小结

前提： 删除前文件提交到本地库

## P23 比较文件

git diff 文件名   工作区和暂存区进行比较

git diff hard   工作区和本地库进行对比

## p24 分支概述

不想影响主干。 

分支独立。 

删除分支，不影响其他业务。 

主干合并。 

![Snipaste_2022-01-09_21-48-30](E:\github\gitLearn\Image\Snipaste_2022-01-09_21-48-30.png)

分支的好处：

同时推行多个功能开发， 提高开发效率。 

删除分支，不影响主干。 

## P25 分支操作

git status 

git branch -v   查看所有分支

git branch hot_fix 创建分支

git checkout hot_fix 切换分支

合并分支：

1. 切换到受修改的分支（被合并）

2. 执行merge命令 

   git merge [分支名]    已修改的分支

## P26 解决冲突



![Snipaste_2022-01-10_06-43-30](E:\github\gitLearn\Image\Snipaste_2022-01-10_06-43-30.png)

all conficts fixed but you are still merging.   冲突已解决，但是仍处于合并中。

## P27 hash

1. 加密后长度固定。MD5 16位十六进制数
2. 输入确定， 算法确定， 结果确定
3. 校验文件。 
4. 服务器计算文件： sha-1   下载文件计算文件： sha-1   进行对比。

## P28 数据管理机制

提交后： 有历史记录。 版本保存修改。 svn ： 保存有变化的数据。 

git : 快照流。 指针。 

提交对象： hash值。 提交时间， 提交者。

## P29 分支管理的本质

移动指针。 

![Snipaste_2022-01-10_07-02-38](E:\github\gitLearn\Image\Snipaste_2022-01-10_07-02-38.png)

## P30 github账号： 

## P31 修改头像

点击头像， you profile  

## P32 本地库和远程库交互

创建本地库。 

## P34创建远程库

创建远程库。 

不创建redmie文件。 

## P35  远程库地址

git remote add origin https://github.com/LinuxZhaoLi/gitLearn.git

origin  地址别名

## P36 推送操作

 git push origin master

## P37 克隆

git clone   

1. 把远程库下载
2. 创建地址别名
3. 初始化本地库

## P38 加入团队

error 403 没有权限。**合作者** 

setting --> collaborators  --> add collaborator. 

## P39 远程库修改的拉去

git fetch origin master  抓取远程库。

抓取下来不会修改本地文件。 

查看下载内容： 

checkout origin/master

合并：

git merge / origin/master 



## P40 协同开发冲突

不是在最新版本上修改的 

## P41 跨团队协同操作演示

fork  + pull request 

现在 fork的都是别人的。 

本地修改，上传远程库。 

create pull request 

Confirm merge  确认合并。

## P40 ssh 免密

ssh-keygen -t rsa -C zhaoshengli@qq.com 

cat id_rsa.puk 复制到github  个人设置： ssh and GPG keys.

新建远程库别名： git remote add origin_ssh ssh地址。

## P47 特定文件

.project 文件  和开发文件无关。需要忽略。

## P48 忽略文件

https://github.com/github/gitignore

在 C: / 用户/lenovo/   下载添加 Java.gitignor 文件。

修改： gitconfig 文件

添加：

[core]

​	excludesfile = c:\user\Lenovo\Java.gitignore 











