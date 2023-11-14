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
