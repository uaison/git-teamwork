# git团队合作流程（持续更新）

## 创建项目

1. 创建远程仓库，github.com中点击new repository，仓库名 git-teamwork，复制仓库地址 git@github.com:uaison/git-teamwork.git

2. 本地文件夹初始化 `git init`

3. 设置远端仓库地址 `git clone git@github.com:uaison/git-teamwork.git`

### 建立开发分支

1. 新建开发分支 `git branch dev`

2. 开发分支推送到远程仓库 `git push dev`

3. 建立本地到上游（远程仓库）的关联 `git branch --set-upstream-to=origin/dev`

### 分支操作

1. 删除本地分支 `git branch -d dev`

2. 删除远端分支 `git push --delete origin dev`

3. 新建本地分支 `git branch dev`

4. 新建远程分支 `git push origin dev`

5. 将本地分支与远程分支关联 `git branch --set-upstream-to=origin/dev`

6. 将master分支合并到当前分支 `git merge master`

7. 分支重命名
```
git branch -m oldDev newDev
git push --delete origin oldDev
git push origin newDev
git branch --set-upstream-to=origin/newDev
```


### 标签管理

1. 标签列表 `git tag`

2. 新建本地标签 `git tag -a v1.0 -m "commit message"`

3. 新建标签推送到远端 `git push origin v1.0`

4. 删除本地标签 `git tag -d v1.0`

5. 删除本地标签后，同步到远端标签 `git push origin :refs/tags/v1.0`

### 团队协作

1. 克隆远端dev分支 `git clone -b dev git@github.com:uaison/git-teamwork.git`

2. 提交前获取最新代码 `git pull`

3. 添加修改内容到git源码 `git add .`

4. 提交修改内容到缓存区 `git commit -m "commit message"`

5. 修改推送到远程仓库 `git push`
