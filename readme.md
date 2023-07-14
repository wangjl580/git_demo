# Git 代码版本管理

## 用法

1. 进入需要文件管理的目录
2. 为了更好地使用 git, 我们同时也记录每一个施加修改的人. 这样人和修改能够对应上. 所以我们在 git 中添加用户名 user.name 和 用户 email user.email
   * git config --global user.name "wjl"
   * git config --global user.email "<396292346@qq.com>"

3. 初始化 git init  
4. 查看版本库的状态 git status  或者 git status -s  # 查看状态 简单的形式
5. 添加进版本库 git add 1.py  或者 git add . # 加入所有
6. 提交改变
   1. git commit -m "create 1.py"   -m 自定义这次改变的信息  
   2. git commit -am 'change 3 in dev'  # -a 表示直接加入并提交分支
   3. git commit --amend --no-edit 2.py

## 回到过去

### 对于整个目录

  1. 查看提交的更改
    1. git log  
    2. 或者 git log --oneline
    3. 或者 git log --oneline 1.py
  2. 查看所有的id  git reflog --oneline
  3. 回到过去 git reset --hard 01c4346  或者 git reset --hard HEAD@{7}

### 对于单个文件

  1. git checkout 0c04910 -- 1.py   # 针对1.py

## 分支

1. 创建分支
   1. git branch dev  
   2. 或者 git checkout -b dev
2. 查看分支  git branch
3. 切换分支 git checkout master
4. 删除分支 git branch -d dev
5. 合并分支
   1. 首先处于 master 分支
   2. git merge --no-ff -m 'keep merg info' dev # 合并dev到master
   3.

## github  网上的资源

1. 理解 git 是本地管理库, github 是 online 管理库

### github 用法  

1. 在 github 注册一个 github 账户 或者gitee
2. 然后添加你的一个 online 版本库 repository:
3. 增加远程仓库 在需要上传的目录中 执行: git remote add origin <git@github.com>:wangjl580/git_demo.git  # 增加的仓库名称为 origin 网址为 ...
4. 添加一个额外的远程仓库 git remote add gitee <https://gitee.com/wangjl580/git_learn.git>  # > 添加多个远程仓库时, 名称不能一样
5. 推送 git push -u origin master # 把master 推送到 名称为origin的远程仓库, 使用-u选项的主要好处是，它将设置默认的上游分支。这意味着在接下来的推送操作中，你只需执行git push命令
6. 更改远程仓库的URL git remote set-url origin <https://gitee.com/wangjl580/git_learn.git> #  重置远程仓库origin 的URL为 https...
7. 如果要删除名为 origin 的远程仓库，可以运行以下命令：git remote remove origin # 或者 git remote rm origin # 请注意，删除远程仓库不会影响本地仓库的内容，它只是删除了与远程仓库的关联。
