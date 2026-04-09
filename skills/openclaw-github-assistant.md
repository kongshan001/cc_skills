# OpenClaw GitHub Assistant

## 技能概述

- **Slug**: openclaw-github-assistant
- **名称**: OpenClaw GitHub Assistant
- **作者**: conorkenn
- **版本**: 2.0.1
- **更新时间**: 2026-04-09

## 背景需求

GitHub 是最流行的代码托管平台，开发者需要管理仓库、检查 CI 状态、创建 issue、搜索仓库等日常操作。

## 目标

Query and manage GitHub repositories - list repos, check CI status, create issues, search repos, and view recent activity.

## 功能列表

- 列出仓库
- 检查 CI 状态
- 创建 Issue
- 搜索仓库
- 查看最近活动
- 仓库管理

## 安装方式

```bash
clawhub install openclaw-github-assistant
```

## 推荐安装评估

- **本地开发**: ⭐⭐⭐⭐⭐ 强烈推荐
- **ECS 服务器**: ⭐⭐⭐⭐⭐ 强烈推荐

**理由**: GitHub 是开发工作流的核心，此技能可以高效管理 GitHub 仓库和协作。

## 优缺点分析

### 优点

1. 一站式 GitHub 管理
2. 提高协作效率
3. 快速查看项目状态
4. 自动化日常操作

### 缺点

1. 需要 GitHub 认证
2. 部分功能依赖 gh CLI

## 平替对比

| 技能 | 特点 |
|------|------|
| github-cli | 更侧重 CLI 参考 |
| github-search | 更侧重搜索功能 |

## 落地过程

1. 执行 `clawhub install openclaw-github-assistant`
2. 配置 GitHub 认证
3. 激活技能进行仓库管理
