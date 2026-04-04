# Git Workflows

## 背景需求

当需要执行高级 Git 操作（如变基、调试、并行开发、环境恢复）时，基础命令不够用。复杂工作流需要更专业的工具支持。

## 目标

提供高级 Git 操作能力，支持复杂开发场景。

## 设计方案

### 核心功能
- **变基**：交互式变基、压缩提交
- **调试**：git bisect 定位 bug
- **并行开发**：git worktree 多分支同时开发
- **恢复**：reflog 恢复误操作
- **子模块**：subtree/submodule 管理
- **冲突解决**：merge conflict 处理
- **精选**：cherry-pick 跨分支
- **大型项目管理**：monorepo 支持

## 本地部署

```bash
clawhub install git-workflows
```

## 效果展示

技能提供：
- 高级版本控制操作
- 多分支并行开发
- 项目恢复与回滚
- Monorepo 支持

## 优缺点分析

| 优点 | 缺点 |
|------|------|
| 功能全面 | 学习曲线较高 |
| 适合高级用户 | 需要一定 Git 基础 |
| 活跃维护 | |

## 平替对比

| 技能 | 特点 |
|------|------|
| git-essentials | 基础操作 |
| git-helper | 常用操作速查 |
| git-cli | 基础 CLI |

## 落地过程

1. 安装：`clawhub install git-workflows`
2. 使用场景：
   - 整理提交历史：交互式变基
   - 定位 Bug：git bisect
   - 同时开发多特性：git worktree

**推荐安装**：本地开发环境 ⭐⭐⭐⭐⭐