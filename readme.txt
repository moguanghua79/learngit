Git is a version control system.
Git is free software.

创建版本库
现在总结一下今天学的两点内容：
初始化一个Git仓库，使用git init命令。
添加文件到Git仓库，分两步：
第一步，使用命令git add <file file2>，注意，可反复多次使用，添加多个文件；
第二步，使用命令git commit -m "描述"，完成。

要随时掌握工作区的状态，使用git status命令
如果git status告诉你有文件被修改过，用git diff可以查看修改内容（git diff readme.txt）

版本回退
git log <--pretty=oneline> 命令显示从最近到最远的提交日志
回退版本 git reset --hard HEAD^ git reset --hard HEAD^^ git reset --hard HEAD~100 git reset --hard commit_id
要重返未来，用git reflog查看命令历史，以便确定要回到未来的哪个版本。