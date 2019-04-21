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

