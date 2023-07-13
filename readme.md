# Git

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
5. x
