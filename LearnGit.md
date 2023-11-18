# LearnGit
## Git学习笔记
### 1. 创建版本库
#### 1.1 初始化一个Git仓库
    git init
#### 1.2 添加文件到Git仓库

暂存一个文件：
    git add <file>
暂存多个文件：

    git add <file1> <file2> <file3>
#### 1.3 提交文件到Git仓库
提交暂存区的文件到仓库：

    git commit -m <message>
### 2. 查看仓库状态
    git status
### 3. 查看修改内容
    git diff <file>
### 4. 查看提交历史
HEAD指向的版本就是当前版本，因此，Git允许我们在版本的历史之间穿梭，使用命令：

    git reset --hard commit_id

穿梭前，用git log可以查看提交历史，以便确定要回退到哪个版本。
    git log
### 5. 查看命令历史
    git reflog
### 6. 暂存区
我们把文件往Git版本库里添加的时候，是分两步执行的：
第一步是用git add把文件添加进去，实际上就是把文件修改添加到暂存区；
第二步是用git commit提交更改，实际上就是把暂存区的所有内容提交到当前分支。

操作过程：

第一次修改 -> git add -> 第二次修改 -> git commit

你看，我们前面讲了，Git管理的是修改，当你用git add命令后，在工作区的第一次修改被放入暂存区，准备提交，但是，在工作区的第二次修改并没有放入暂存区，所以，git commit只负责把暂存区的修改提交了，也就是第一次的修改被提交了，第二次的修改不会被提交。

第一次修改 -> git add -> 第二次修改 -> git add -> git commit

现在，把第二次修改提交了。

### 7. 撤销修改
#### 7.1 丢弃工作区的修改
注意要加 -- ，否则会变成切换分支的命令。

    git checkout -- <file>

#### 7.2 撤销暂存区的修改
    git reset HEAD <file>
    git checkout -- <file>
#### 7.3 撤销版本库的修改
    git reset --hard HEAD^