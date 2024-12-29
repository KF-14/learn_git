# Git 简单使用教程

## 初始化仓库

在项目目录下初始化一个新的 Git 仓库：

```bash
git init
```

## 克隆仓库

从远程仓库克隆一个项目：

```bash
git clone <repository_url>
```

## 查看状态

查看当前工作目录的状态：

```bash
git status
```

## 添加文件到暂存区

将文件添加到暂存区：

```bash
git add <file_name>
```

添加所有文件到暂存区：

```bash
git add .
```

## 撤销操作

```bash
git restore README.md # 撤销还没没有被放到暂存区的修改，直接撤销了文件
git restore --staged README.md # 撤销已经放到暂存区的修改，将修改也就是撤销git add但是文件还没有撤销
```
## 提交更改

将暂存区的更改提交到本地仓库：

```bash
git commit -m "提交信息"
```

## 查看提交历史

查看提交历史记录：

```bash
git log
```

## 推送到远程仓库

将本地仓库的更改推送到远程仓库：

```bash
git push origin <branch_name>
```

## 拉取远程仓库的更改

从远程仓库拉取最新的更改：

```bash
git pull origin <branch_name>
```

## 创建分支

创建一个新分支：

```bash
git branch <branch_name>
```

查看当前分支：

```bash
git branch
```

## 切换分支

切换到指定分支：

```bash
git checkout <branch_name>
```

创建分支并切换成这个分支：

```bash
git checkout -b <branch_name>
```

好像已经有了新的命令：
```bash
git switch -c dev # 创建并切换
```

```bash
git switch main # 切换分支
```
git switch 是 Git 2.23 版本引入的一个新命令，如果你使用的是 Git 的旧版本，可能无法使用 git switch 命令

## 合并分支

将指定分支合并到**当前分支**：

```bash
git merge <branch_name>
```

## 删除分支

删除本地分支：

```bash
git branch -d <branch_name>
```

删除远程分支：

```bash
git push origin --delete <branch_name>
```

## 查看分支

查看所有分支：

```bash
git branch -a
```

## 配置用户信息

配置用户名和邮箱：

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

## 忽略文件

创建 `.gitignore` 文件并添加要忽略的文件或目录：

```
# 忽略所有 .log 文件
*.log

# 忽略 node_modules 目录
node_modules/
```
