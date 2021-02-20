### git基本命令

说明 | 命令 |备注
------------ | -------------- | ------------
列出分支 | `git branch` 
创建分支 | `git branch <branchname>`
切换分支  | `git checkout <branchname>`
创建并切换分支  | `git checkout -b <branchname>`
删除分支  | `git branch -d <branchname>`
合并分支  | `git merge <branchname>`  | 合并不仅仅是简单的文件添加、移除，也会合并修改
比较文件的不同 | `git diff`
查看仓库当前状态，显示有变更的文件 | `git status`
初始化仓库 | `git init`
拷贝远程仓库，下载一个项目 | `git clone` | 可用http或ssh
提交暂存区到本地仓库 | `git commit` | 常用 `git commit -m '(提交说明)'`
回退版本 | `git reset`
删除工作区文件 | `git rm`
移动或重命名工作区文件 | `git mv`
查看历史提交记录 | `git log` | `--author= --oneline --graph`
以列表形式查看指定文件的历史 | `git blame <file>`
远程仓库操作 | `git remote`
从远程获取代码库 | `git fetch`
下载远程代码并合并 | `git pull`
上传远程代码并合并 | `git push`
git标签 | `git tag -a v0.1 <commit id>`
