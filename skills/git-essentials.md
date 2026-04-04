# Git Essentials

## 背景需求

Git 是现代开发最基础的版本控制工具，但复杂操作（如变基、交互式变基、子树管理）常需要记忆大量命令和参数。开发者需要一个统一的技能来处理日常 Git 操作和工作流。

## 目标

提供一套完整的 Git 基本命令和工作流，覆盖版本控制、分支管理、协作等核心场景。

## 设计方案

### 技能结构
- **核心功能**：add, commit, push, pull, branch, merge, checkout
- **高级功能**：rebase, bisect, worktree, reflog, subtree, submodule
- **协作功能**：cherry-pick, merge conflict resolution

### 触发词
- git 操作相关命令

## 本地部署

```bash
clawhub install git-essentials
```

## 效果展示

技能提供以下能力：
- 基本版本控制操作
- 分支创建与管理
- 高级操作（变基、调试、恢复）
- 并行开发环境管理

## 优缺点分析

| 优点 | 缺点 |
|------|------|
| 覆盖基础到高级操作 | 缺乏 GUI 集成 |
| 作者活跃，维护及时 | 文档较少 |
| 轻量级，无外部依赖 | |

## 平替对比

| 技能 | 特点 |
|------|------|
| git-workflows | 更适合高级用户，处理复杂场景 |
| git-helper | 偏重基础操作 |
| git-cli | 基础命令行工具 |

## 落地过程

1. 安装：`clawhub install git-essentials`
2. 使用示例：
   - 分支管理：`git branch feature-x`
   - 变基操作：交互式变基整理提交历史
   - Bug 追踪：使用 bisect 定位问题

**推荐安装**：本地开发环境 ⭐⭐⭐⭐⭐