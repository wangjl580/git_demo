# Git

## 用法

1. 进入需要文件管理的目录
2. 为了更好地使用 git, 我们同时也记录每一个施加修改的人. 这样人和修改能够对应上. 所以我们在 git 中添加用户名 user.name 和 用户 email user.email
   * git config --global user.name "wjl"
   * git config --global user.email "<396292346@qq.com>"

3. 初始化 git init  
4. 查看版本库的状态 git status  或者 git status -s  # 查看状态 简单的形式
5. 添加进版本库 git add 1.py  或者 git add . # 加入所有
6. 提交改变 git commit -m "create 1.py"   -m 自定义这次改变的信息

7. 查看提交的更改 git log

## 分支

1. 创建分支 git branch dev  或者 git checkout -b dev
2. 查看分支  git branch
3. 切换分支 git checkout master
4.
