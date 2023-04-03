**git 常用命令**

`git init`	初始化本地仓库



`git config --global user,name "<name>" `	设置本地仓库使用者用户名

`git config --global user.email "<email>"`	设置本地仓库使用者邮箱

`git config --global color.ui auto`	UI颜色自动设置



`git status`	查看当前提交状态

`git status -s` 	查看简短的提交状态



`git clone <远程仓库地址>` 	拉取远程仓库资源



`git add .`	提交当前目录下所有更改到暂存区

`git add <文件名>`	提交制定文件更改到遵到暂存区



`git commit -a` 	直接从工作区提交到本地仓库

`git commit -m "<description>"`	提交到本地仓库（两个参数可叠加使用 `-am`）



`git push <分支名(可选)>`	提交到远程仓库，默认提交到当前分支远程仓库，也可以提交指定分支

`git push <源名称> <分支名>`	提交本地仓库到远程原名称下的指定分支

`git push -u(–set-upstream) <源名称> <分支名>`	设置这个源的分支为上游分支，用于首次创建分支未设置上游分支。

`git push --force <源名称> <分支名>`	强制推送本地分支到远程源名称下的制定分支。

`git push <源名称> --delete <分支名>`	删除远程源名称下的指定分支



`git pull (<源名称>)`	拉取当前分支远程仓库

`git pull <源名称> <分支名>:<分支名>`	拉取远程源名称下的分支与指定分支合并

`git pull <源名成> <分支名>`	拉取远程源名称下的分支与当前分支合并



`git checkout <分支名>`	切换分支

`git checkout -b <分支名>`	分支存在则切换分支，若不存在则创建一个新的分支并切换到新分支

`git checkout -b <分支名> <源名称>/<远程分支名>`	创建分支并从远程分支拉取

`git checkout .`	暂存区所有文件替换工作区文件

`git checkout --<文件名>`	暂存区指定文件替换工作区文件

`git checkout <文件名>` 	暂存区指定文件替换工作区文件

`git checkout HEAD .`	把本地仓库所有文件回写到暂存区和工作区，**会清除暂存区和工作区的所有更改**

`git check HEAD <文件名>`	把本地仓库指定文件回写到暂存区和工作区，**会清除暂存区和工作区的指定文件的更改**



`git remote`	查看远程源

`git remote -v`	查看远程源包括地址

`git remote add <源名称> <远程仓库地址>` 	添加源名称的远程仓库

`git remote show <远程仓库地址>`	查看远程仓库信息

`git remote rm <源名称(仓库名)>`	删除远程源 

`git remote rename <旧仓库名> <新仓库名>`	修改仓库名称



`git branch`	查看本地分支，当前分支会有*****号

`git branch <分支名>`	本地创建分支

`git branch main -u <源名称/分支名>`	更改上游分支

`git branch -a	`	查看本地及远程分支

`git branch -r`	查看远程分支

`git branch -v`	查看本地分支并记录最后一次修改备注

`git branch -vv`	查看本地分支并查看此分支的上游分支

`git branch --track`	创建分支并从远程分支拉取

`git branch -d <分支名>`	删除本地分支

`git branch -r -d <源名称>/<分支名>`	删除远程分支本地分支不影响



`git tag`	查看所有标签

`git tag -a v1.0`	创建一个带注解的1.0标签 ，**输入完成后会进入vi编辑器输入标签内容**

`git tag -a v0.9 <commit-id>`	为制定提交版本追加标签， **输入完成后会进入vi编辑器输入标签内容**

`git tag -s <标签名> -m<标签内容>`	PGP签名标签命令



`git diff`	比较工作区与暂存区的差异

`git diff HEAD <文件名>`	比较指定文件工作区与本地仓库的差异

`git diff --cached <文件名>`	比较指定文件暂存区与本地仓库的差异

`git diff --staged <文件名>`	比较指定文件暂存区与本地仓库的差异

`git diff <commit-id> <文件名>`	比较工作区与指定commit-id的差异

`git diff --cached <commit-id> <文件名> `	比较暂存区与指定commit-id的差异

`git diff <commit-id> <commit-id>`	比较两个commit-id之间的差异



`git reset HEAD`	暂存区回滚，从本地仓库回写到暂存区，不会修改工作区

`git reset --soft HEAD`	回退到指定版本

`git reset --soft HEAD~3` 	回退到上上上一个版本

`git reset --soft HEAD^^^` 	回退到上上上一个版本

`git reset --hard HEAD~3`	放弃暂存区修改并回退到上上上个版本



`git rm <文件名>`	从暂存区和工作区删除指定文件

`git rm -f <文件名>`	强制从暂存区和工作区删除指定文件

`git rm -r <文件名>`	递归删除指定目录下的所有文件和文件夹。**如果参数为*，则删除当前目录下的所有文件及文件夹**

`git rm --cached <文件名>`	从暂存区删除指定文件



`git mv <文件名> <新文件名>`	重命名文件

`git mv -f <文件名> <新文件名>`	新文件名已存在，强制重命名



`git swtich <分支名>`	切换分支

`git swtich -c <分支名>`	分支存在则切换分支，若不存在则创建一个新的分支并切换到新分支

`git swtich -c <分支名> <源名称>/<远程分支名>`	创建分支并从远程分支拉取



`git merge`	拉取远程分支并合并到当前分支



`git fetch <源名称>`	拉取远程源数据

`git fetch <源名称>/<分支名>`	拉取远程仓库的所有变更到当前分支

`git fetch -p`	拉取远程分支



`git log `	查看历史提交记录

`git log --decorate`	查看标签

`git log --oneline`	查看历史提交记录简洁版

`git log --reverse`	逆向查看提交记录

`git log --author=<用户名>`	查看该用户的所有提交

`git log --since={2020-04-18}`	查看该日期以后的提交

`git log --before={3.weeks.ago}`	查看3周内的提交

`git log --after={2020-04-18}`	查看该日期以后的提交

`git log --no-merges`	隐藏合并分支的提交

`git log --graph`	查看分支合并图

`git log --graph --pretty=oneline --abbrev-commit`	作用同上，更简洁明了



`git blame <文件名>`	以列表形式查看提交	



`ssh-keygen -t rsa -C "git远程仓库注册邮箱"`	创建本地SSH验证密钥，添加到git远程仓库SSH账号验证中

`ssh -T git@github.com`	验证SSH密钥是否创建成功

WIN10
SHA256:Cc1PqnOjeSINniOgY4+V1fWdSsoqn5xi5Tw5nNLeY6o