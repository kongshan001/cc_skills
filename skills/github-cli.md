# GitHub CLI

> GitHub CLI 全面参考 - gh 命令行工具专家

## 基础信息

| 项目 | 值 |
|------|-----|
| **Slug** | github-cli |
| **作者** | tag-assistant |
| **版本** | 1.0.0 |
| **更新时间** | 2026-04-26 |
| **评分** | ⭐ 3.655 |

## 1. 背景需求

GitHub CLI (gh) 是 GitHub 官方提供的命令行工具，可替代浏览器完成大部分 GitHub 操作。在 OpenClaw 中集成 gh CLI 可以显著提升 GitHub 相关操作的效率。

## 2. 目标

提供全面的 gh CLI 参考和使用指南：
- 仓库管理
- Issue 和 PR 操作
- GitHub Actions 工作流
- API 调用和脚本化

## 3. 设计方案

### 核心功能模块
- **仓库操作**: 创建、克隆、fork、列表
- **Issue 管理**: 创建、列表、查看、评论、关闭
- **PR 操作**: 创建、审查、合并、检查状态
- **Actions**: 触发工作流、查看运行状态
- **API 调用**: 自定义 API 请求

### 技术架构
- 基于 gh CLI
- 支持 gh extension
- 集成 GitHub API

## 4. 本地部署

```bash
# 安装技能
clawhub install github-cli

# 安装 gh CLI (如未安装)
brew install gh  # macOS
# 或
sudo apt install gh  # Ubuntu

# 认证
gh auth login
```

### 环境要求
- gh CLI 2.0+
- GitHub 认证

## 5. 效果展示

```
用户: 创建一个新 Issue
助手: [执行 gh issue create]
Title: 修复登录页面样式问题
Body: 描述问题...
Labels: bug
✓ Issue created: #42

用户: 查看最近的 PR 状态
助手: [执行 gh pr list]
#42 修复登录问题  [open]
#41 优化首页性能  [merged]
```

## 6. 优缺点分析

### 优点
- ✅ 官方 CLI，稳定性高
- ✅ 功能全面，覆盖率高
- ✅ 支持脚本化和自动化
- ✅ 评分高（3.655）

### 缺点
- ⚠️ 依赖外部 gh CLI
- ⚠️ 需要单独认证
- ⚠️ 无原生 API 能力

## 7. 平替对比

| 技能 | 评分 | 特点 |
|------|------|------|
| github-cli | 3.655 | gh CLI 封装 |
| openclaw-github-assistant | 3.717 | 原生 API 集成 |
| github-workflow | 3.537 | 工作流管理 |

**推荐**: 需要脚本化选 **github-cli**，需要原生集成选 **openclaw-github-assistant**

## 8. 落地过程

### 第一阶段：安装配置 (10分钟)
1. 安装技能: `clawhub install github-cli`
2. 安装 gh CLI
3. 执行 gh auth login

### 第二阶段：日常使用 (持续)
- Issue/PR 管理
- 工作流操作
- 自动化脚本

### 推荐安装评估

| 场景 | 推荐 | 理由 |
|------|------|------|
| **本地开发** | ⭐⭐⭐⭐⭐ | 效率提升明显 |
| **ECS 服务器** | ⭐⭐⭐⭐⭐ | 适合 CI/CD |
| **自动化脚本** | ⭐⭐⭐⭐⭐ | 完美支持 |

**综合推荐**: ✅ 强烈推荐，适合需要频繁操作 GitHub 的开发者。