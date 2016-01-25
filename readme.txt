Git is a version control system.
Git is free software.

一、安装
默认安装后
 git config --global user.name "moguanghua"
 git config --global user.email "587970@qq.com"

二、创建版本库
现在总结一下今天学的两点内容：
初始化一个Git仓库，使用git init命令。
添加文件到Git仓库，分两步：
第一步，使用命令git add <file file2>，注意，可反复多次使用，添加多个文件；
第二步，使用命令git commit -m "描述"，完成。

要随时掌握工作区的状态，使用git status命令
如果git status告诉你有文件被修改过，用git diff可以查看修改内容（git diff readme.txt）

三、版本回退
git log <--pretty=oneline> 命令显示从最近到最远的提交日志
回退版本 git reset --hard HEAD^ git reset --hard HEAD^^ git reset --hard HEAD~100 git reset --hard commit_id
要重返未来，用git reflog查看命令历史，以便确定要回到未来的哪个版本。

四、撤销修改
场景1：当你改乱了工作区某个文件的内容，想直接丢弃工作区的修改时，用命令git checkout -- file。
场景2：当你不但改乱了工作区某个文件的内容，还添加到了暂存区时，想丢弃修改，分两步，第一步用命令git reset HEAD file，就回到了场景1，第二步按场景1操作。
场景3：已经提交了不合适的修改到版本库时，想要撤销本次提交，参考版本回退一节，不过前提是没有推送到远程库。

五、删除文件
命令git rm用于删除一个文件。

六、注册GITHUB，并设置

七、关联一个远程库
git remote add origin git@github.com:moguanghua79/learngit.git
关联后，使用命令git push -u origin master第一次推送master分支的所有内容；
此后，每次本地提交后，只要有必要，就可以使用命令git push origin master推送最新修改；

