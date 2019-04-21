Git is a version control system！

Git is free software.

Administrator@se7en5 MINGW64 /f/IDEA/workspace
$ mkdir gitrepository （创建一个目录作为git库）

Administrator@se7en5 MINGW64 /f/IDEA/workspace
$ cd gitrepository/	（进入该目录）

Administrator@se7en5 MINGW64 /f/IDEA/workspace/gitrepository
$ git init			 （初始化仓库）
Initialized empty Git repository in F:/IDEA/workspace/gitrepository/.git/

Administrator@se7en5 MINGW64 /f/IDEA/workspace/gitrepository (master)
$ git add readme.txt	(添加文件到暂存区）

Administrator@se7en5 MINGW64 /f/IDEA/workspace/gitrepository (master)
$ git commit -m "first commit"		（把暂存区的改动提交到本地版本库）
[master (root-commit) 87dfa82] first commit
 1 file changed, 2 insertions(+)
 create mode 100644 readme.txt
 
 git diff filename.suffix	（查看修改）
 
 git status	（查看库的状态）
 
 git log	（查看提交日志记录）

git reflog	（查看历史提交记录和id，时光穿梭机，过去与未来都能看到）

git reset --hard HEAD^	（回退到上一个版本）

git reset --hard id		（回退到指定版本）

git diff HEAD -- filename.suffix	(查看工作区与版本库最新版的区别）

Atention：每次的修改，如果不add到暂存区，是不会被commit的，只有add了的修改才会被commit！

git checkout --filename.suffix	（可以撤销修改）

场景1：当你改乱了工作区某个文件的内容，想直接丢弃工作区的修改时，用命令git checkout -- file。

场景2：当你不但改乱了工作区某个文件的内容，还添加到了暂存区时，想丢弃修改，分两步，第一步用命令git reset HEAD <file>，就回到了场景1，第二步按场景1操作。

场景3：已经提交了不合适的修改到版本库时，想要撤销本次提交，参考版本回退一节，不过前提是没有推送到远程库。

git checkout -b dev （创建并切换到分支dev）

git branch （列出所有分支，当前分支带*）

git merge dev (把dev分支合并到master上）

git branch -d <name> (删除分支）

查看远程库信息，使用git remote -v；

本地新建的分支如果不推送到远程，对其他人就是不可见的；

从本地推送分支，使用git push origin branch-name，如果推送失败，先用git pull抓取远程的新提交；

在本地创建和远程分支对应的分支，使用git checkout -b branch-name origin/branch-name，本地和远程分支的名称最好一致；

建立本地分支和远程分支的关联，使用git branch --set-upstream branch-name origin/branch-name；

从远程抓取分支，使用git pull，如果有冲突，要先处理冲突。

git tag v1.0 		（打标签在最新的commit，方便穿梭）

git tag 		(查看所有标签）

git tag v0.9 f52c633	（为历史commit打标签）

git show <tagname>	  （查看标签信息）

git tag -d v1		  (删除标签）






