# Git Essentials - Git基础技能

## 技能描述
版本控制和协作的Git核心命令和工作流程技能。提供完整的Git使用指南，从基础操作到高级工作流程。

## 功能列表
- **基础设置**: 用户配置、仓库初始化、克隆
- **基本工作流**: 暂存和提交、查看变更、分支管理
- **远程操作**: 远程管理、同步、推送拉取
- **历史与日志**: 历史查看、搜索、bisect
- **撤销操作**: 工作区撤销、暂存区撤销、提交撤销
- **存储管理**: 存储创建、应用、删除
- **变基操作**: 变基、交互式变基、冲突解决
- **标签管理**: 创建、推送、删除标签

## 初始设置
```bash
# 配置用户
git config --global user.name "Your Name"
git config --global user.email "your@email.com"

# 初始化仓库
git init

# 克隆仓库
git clone https://github.com/user/repo.git
git clone https://github.com/user/repo.git custom-name
```

## 基本工作流
### 暂存和提交
```bash
# 检查状态
git status

# 添加文件到暂存区
git add file.txt
git add .
git add -A  # 包括所有更改和删除

# 提交更改
git commit -m "Commit message"

# 添加并提交一步完成
git commit -am "Message"

# 修改最后一次提交
git commit --amend -m "New message"
git commit --amend --no-edit  # 保持消息不变
```

### 查看变更
```bash
# 显示未暂存的更改
git diff

# 显示暂存的更改
git diff --staged

# 显示特定文件的更改
git diff file.txt

# 显示提交之间的更改
git diff commit1 commit2
```

## 分支与合并
### 分支管理
```bash
# 列出分支
git branch
git branch -a  # 包括远程分支

# 创建分支
git branch feature-name

# 切换分支
git checkout feature-name
git switch feature-name  # 现代替代方法

# 创建并切换
git checkout -b feature-name
git switch -c feature-name

# 删除分支
git branch -d branch-name
git branch -D branch-name  # 强制删除

# 重命名分支
git branch -m old-name new-name
```

### 合并
```bash
# 将分支合并到当前分支
git merge feature-name

# 无快进合并
git merge --no-ff feature-name

# 中止合并
git merge --abort

# 显示合并冲突
git diff --name-only --diff-filter=U
```

## 远程操作
### 管理远程
```bash
# 列出远程
git remote -v

# 添加远程
git remote add origin https://github.com/user/repo.git

# 更改远程URL
git remote set-url origin https://github.com/user/new-repo.git

# 删除远程
git remote remove origin
```

### 同步远程
```bash
# 从远程获取
git fetch origin

# 拉取更改（获取+合并）
git pull

# 拉取并变基
git pull --rebase

# 推送更改
git push

# 推送新分支
git push -u origin branch-name

# 强制推送（小心！）
git push --force-with-lease
```

## 历史与日志
### 查看历史
```bash
# 显示提交历史
git log

# 每提交一行
git log --oneline

# 带图形
git log --graph --oneline --all

# 最后N次提交
git log -5

# 按作者提交
git log --author="Name"

# 按日期范围提交
git log --since="2 weeks ago"
git log --until="2024-01-01"

# 文件历史
git log -- file.txt
```

### 搜索历史
```bash
# 搜索提交消息
git log --grep="bug fix"

# 搜索代码更改
git log -S "function_name"

# 显示谁修改了每一行
git blame file.txt

# 查找引入bug的提交
git bisect start
git bisect bad
git bisect good commit-hash
```

## 撤销操作
### 工作区
```bash
# 丢弃文件中的更改
git restore file.txt
git checkout -- file.txt  # 旧方法

# 丢弃所有更改
git restore .
```

### 暂存区
```bash
# 取消暂存文件
git restore --staged file.txt
git reset HEAD file.txt  # 旧方法

# 取消暂存所有
git reset
```

### 提交
```bash
# 撤销最后一次提交（保留更改）
git reset --soft HEAD~1

# 撤销最后一次提交（丢弃更改）
git reset --hard HEAD~1

# 撤销提交（创建新提交）
git revert commit-hash

# 重置到特定提交
git reset --hard commit-hash
```

## 存储管理
```bash
# 存储更改
git stash

# 带消息存储
git stash save "Work in progress"

# 列出存储
git stash list

# 应用最新存储
git stash apply

# 应用并移除存储
git stash pop

# 应用特定存储
git stash apply stash@{2}

# 删除存储
git stash drop stash@{0}

# 清除所有存储
git stash clear
```

## 常用工作流
### 功能分支工作流
```bash
git checkout -b feature/new-feature
# 进行更改
git add .
git commit -m "Add new feature"
git push -u origin feature/new-feature
# 创建PR，合并后
git checkout main
git pull
git branch -d feature/new-feature
```

### 热修复工作流
```bash
git checkout main
git pull
git checkout -b hotfix/critical-bug
# 修复bug
git commit -am "Fix critical bug"
git push -u origin hotfix/critical-bug
# 合并后
git checkout main && git pull
```

### 同步fork
```bash
git remote add upstream https://github.com/original/repo.git
git fetch upstream
git checkout main
git merge upstream/main
git push origin main
```

## 有用别名
添加到`~/.gitconfig`:
```ini
[alias]
    st = status
    co = checkout
    br = branch
    ci = commit
    unstage = reset HEAD --
    last = log -1 HEAD
    visual = log --graph --oneline --all
    amend = commit --amend --no-edit
```

## 推荐安装评估

### 本地部署
**适用场景**:
- 个人开发者、小型团队
- 个人项目版本控制
- 学习Git工作流
- 本地开发环境

**优势**:
- 完全本地化，无网络依赖
- 命令行操作便捷
- 即时反馈和调试
- 学习成本低
- 与本地开发工具集成好

**ECS部署**
**适用场景**:
- 大型开发团队
- 企业级版本控制
- 多仓库管理
- 团队协作需求

**优势**:
- 统一Git环境
- 集成到CI/CD流水线
- 团队权限管理
- 企业级功能支持
- 监控和审计功能
- 安全策略管理

**选择建议**: 个人开发者和小团队推荐本地部署，企业级团队和大规模项目选择ECS部署。