# OpenClaw GitHub Assistant

## 技能概述

- **技能名称**: OpenClaw GitHub Assistant
- **Slug**: openclaw-github-assistant
- **版本**: 2.0.1
- **作者**: conorkenn
- **创建时间**: 2026-02-11
- **更新时间**: 2026-03-22

## 背景需求

在日常开发中，开发者经常需要与 GitHub 进行交互，包括查看仓库列表、检查 CI 状态、创建 Issue、搜索仓库等操作。这些任务通常需要在浏览器和命令行之间切换，缺乏统一的自动化解决方案。

## 目标

为 OpenClaw 提供一个全面的 GitHub 助手技能，能够自动化完成常见的 GitHub 操作，减少手动操作成本。

## 功能列表

1. **仓库列表查询** - 列出用户或组织的仓库
2. **CI 状态检查** - 查看仓库的 CI/CD 执行状态
3. **Issue 管理** - 创建、查看、更新 GitHub Issues
4. **仓库搜索** - 搜索 GitHub 仓库
5. **最近活动查看** - 查看仓库的最新活动

## 安装方式

```bash
clawhub install openclaw-github-assistant
```

## 推荐安装评估

- **本地开发**: ⭐⭐⭐⭐⭐ 非常适合，在本地机器上即可使用
- **ECS 服务器**: ⭐⭐⭐⭐ 适合，需要配置 GitHub Token

## 优缺点分析

### 优点
- 功能全面，覆盖常用 GitHub 操作
- 安装简单，集成方便
- 支持自动化操作，减少手动干预

### 缺点
- 需要 GitHub API Token
- 部分高级功能可能需要额外配置

## 平替对比

| 技能 | 评分 | 特点 |
|------|------|------|
| github-cli | 3.596 | 更侧重 CLI 命令参考 |
| github-ops | 3.530 | 更侧重仓库创建和 Release 管理 |
| github-search | 3.491 | 更侧重仓库搜索功能 |

## 落地过程

1. 安装技能: `clawhub install openclaw-github-assistant`
2. 配置 GitHub Personal Access Token
3. 根据需要调用相应功能
