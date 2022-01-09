svn和git的区别：

svn:是增量式的管理方式。 版本控制在服务器， 服务器宕机。历史版本数据丢失。 

git: .GIT是分布式的. 本地有版本管理， 避免单点故障。 



本地库：存历史版本  git commit

暂存区： 临时存储  git add 

工作区： 写代码



代码托管中心：

局域网： gitLab

外网： github, 码云。

本地库和远程库：

本地到远程库： push 

远程库下载到本地： clone

本地更新： pull

克隆远程库：fork  

团队外：

![Snipaste_2022-01-09_19-52-15](E:\github\gitLearn\Image\Snipaste_2022-01-09_19-52-15.png)

初始化本地库：

![Snipaste_2022-01-09_20-00-16](E:\github\gitLearn\Image\Snipaste_2022-01-09_20-00-16.png)

设置签名命令： 

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

   git status:

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