# Git Workflow - Git 工作流自动化技能

## 1. 背景需求

Git 是现代软件开发的核心工具，但复杂的 Git 操作（如解决冲突、管理分支、创建 PR）往往耗时且容易出错。开发者需要：

- 简化的 Git 操作流程
- 自动化的 PR 创建和管理
- 分支管理优化
- 提交规范自动化

## 2. 目标

Git Workflow 是一系列 Claude Code 插件的集合，专注于自动化 Git 工作流，提高开发效率。

## 3. 设计方案

### 包含的插件

| 插件 | 功能 |
|------|------|
| commit | 智能提交和提交信息生成 |
| create-pr | 自动创建 Pull Request |
| fix-github-issue | GitHub Issue 自动修复 |
| analyze-issue | Issue 分析和处理 |
| bug-fix | Bug 修复工作流 |
| create-worktrees | Git Worktrees 管理 |
| pr-review | PR 审查和反馈 |
| husky | Git Hooks 集成 |

### 核心功能

1. **智能提交**
   - 自动生成符合规范的提交信息
   - 智能识别变更类型
   - 提交前自动检查

2. **PR 自动化**
   - 自动创建 PR
   - 生成 PR 描述
   - 自动关联 Issue

3. **Issue 驱动开发**
   - 从 Issue 创建分支
   - 自动修复并提交
   - 关联 PR 和 Issue

## 4. 本地部署

### 安装方式

```bash
# 安装所有 Git 工作流插件
/plugin install commit
/plugin install create-pr
/plugin install fix-github-issue
/plugin install bug-fix

# 或安装 marketplace
/plugin marketplace add ccplugins/marketplace
/plugin install git-workflow
```

### 环境要求

- Git 已安装
- Claude Code 已安装
- GitHub 账户（用于 PR 功能）

## 5. 效果展示

### 使用示例

**提交代码：**
```
"Commit my changes with a proper message"
# → 自动分析变更，生成提交信息

/commit
# → 交互式提交
```

**创建 PR：**
```
"Create a PR for this feature"
# → 自动创建 PR，包含变更描述

/create-pr
# → 交互式创建 PR
```

**修复 Issue：**
```
"Fix the login bug reported in issue #42"
# → 创建分支，修复 bug，提交并创建 PR
```

### 输出示例

```
✅ Changes committed:
   commit 3a5f7b2
   Author: Developer <dev@example.com>
   Date: Thu Mar 19 2026
   
   fix: resolve login redirect issue
   
   - Fix redirect loop after logout
   - Add session validation
   - Update tests

✅ Pull Request created:
   Title: fix: resolve login redirect issue (#42)
   URL: https://github.com/org/repo/pull/156
```

## 6. 优缺点分析

### 优点

| 优势 | 说明 |
|------|------|
| 自动化程度高 | 减少重复性 Git 操作 |
| 规范统一 | 自动生成规范的提交信息 |
| Issue 集成 | 与 GitHub Issue 无缝集成 |
| 工作流完整 | 覆盖提交到 PR 全流程 |

### 缺点

| 劣势 | 说明 |
|------|------|
| GitHub 依赖 | 主要面向 GitHub |
| 权限需求 | 需要 GitHub token |
| 学习曲线 | 多个插件需要熟悉 |

## 7. 平替对比

| 工具 | 定位 | 优势 | 劣势 |
|------|------|------|------|
| Git Workflow | Git 工作流自动化 | Claude 集成、智能化 | GitHub 专用 |
| GitHub CLI | GitHub 命令行 | 官方支持、稳定 | 功能基础 |
| GitHub Desktop | 图形化工具 | 直观易用 | 自动化有限 |

## 8. 落地过程

### 使用场景

```bash
# 日常提交
"Commit the new feature with a proper message"

# Issue 驱动开发
"Fix the bug in issue #123"

# 创建 PR
"Create a PR for this feature branch"

# 综合工作流
"Take issue #45, create a branch, fix it, and create a PR"
```

### 最佳实践

- 安装所有 Git Workflow 插件以获得完整功能
- 配置 GitHub token 以使用 PR 功能
- 遵循 conventional commits 规范

---

**推荐安装方式**：本地开发环境（Desktop/Laptop）

**资源链接**：Git Workflow 类别 - ccplugins/awesome-claude-code-plugins
