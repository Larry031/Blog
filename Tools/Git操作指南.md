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

### github Q&A
#### 1.Q:github图片无法加载（图裂）

  A：因为无法访问raw.githubusercontent.com（github 的素材服务器）造成，需要修改本地hosts文件。
  
- raw.githubusercontent.com的IP经常更换，所以可以先通过[ipaddress](https://www.ipaddress.com/)查询IP

<img width="800"  src="https://github.com/Larry031/Note/blob/master/%E9%99%84%E4%BB%B6/%E6%9F%A5%E8%AF%A2GithubUsercontent%E7%9A%84IP%E5%9C%B0%E5%9D%80.png"/>

- 然后修改hosts文件

<img width="800"  src="https://github.com/Larry031/Note/blob/master/%E9%99%84%E4%BB%B6/%E4%BF%AE%E6%94%B9hosts%E6%96%87%E4%BB%B6.png"/>
- 刷新DNS Win+R -> cmd -> config /flushdns
#### 2.Q:github访问速度慢或连接不上

 A：CND域名遭到DNS污染
 
 - 修改主机hosts文件
 ```
140.82.113.4 github.com

140.82.114.10 nodeload.github.com

140.82.113.5 api.github.com

140.82.114.10 codeload.github.com

185.199.108.153 training.github.com

185.199.108.153 assets-cdn.github.com

185.199.108.153 document.github.com

185.199.108.154 help.github.com

185.199.108.153 githubstatus.com

199.232.69.194 github.global.ssl.fastly.net

199.232.96.133 raw.github.com

199.232.96.133 raw.githubusercontent.com

199.232.96.133 cloud.githubusercontent.com

199.232.96.133 gist.githubusercontent.com

199.232.96.133 marketplace-screenshots.githubusercontent.com

199.232.96.133 repository-images.githubusercontent.com

199.232.96.133 user-images.githubusercontent.com

199.232.96.133 desktop.githubusercontent.com

199.232.96.133 avatars.githubusercontent.com

199.232.96.133 avatars0.githubusercontent.com

199.232.96.133 avatars1.githubusercontent.com

199.232.96.133 avatars2.githubusercontent.com

199.232.96.133 avatars3.githubusercontent.com

199.232.96.133 avatars4.githubusercontent.com

199.232.96.133 avatars5.githubusercontent.com

199.232.96.133 avatars6.githubusercontent.com

199.232.96.133 avatars7.githubusercontent.com

199.232.96.133 avatars8.githubusercontent.com
```

- 刷新DNS Win+R -> cmd -> config /flushdns
