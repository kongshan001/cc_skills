# GitHub CLI

## 技能概述

- **技能名称**: GitHub CLI
- **Slug**: github-cli
- **版本**: 1.0.0
- **作者**: tag-assistant
- **创建时间**: 2026-02-15
- **更新时间**: 2026-03-22

## 背景需求

GitHub CLI (gh) 是一个强大的命令行工具，但功能众多，命令复杂。开发者经常需要查阅文档才能正确使用各种功能。缺乏一个统一的参考指南。

## 目标

提供全面的 GitHub CLI 参考技能，帮助开发者快速查找和使用 gh 命令。

## 功能列表

1. **仓库操作** - 创建、克隆、 Fork 仓库
2. **Issue 管理** - 创建、列表、关闭 Issue
3. **PR 操作** - 创建、审查、合并 PR
4. **Actions 管理** - 查看工作流、触发执行
5. **Release 管理** - 创建、发布版本
6. **Gist 操作** - 创建、管理代码片段
7. **搜索功能** - 搜索仓库、代码、Issue
8. **Projects v2** - 管理项目板
9. **API 调用** - 执行自定义 API 请求
10. **Secrets/Variables** - 管理仓库密钥

## 安装方式

```bash
# 安装 GitHub CLI
brew install gh

# 安装技能
clawhub install github-cli
```

## 推荐安装评估

- **本地开发**: ⭐⭐⭐⭐⭐ 非常适合
- **ECS 服务器**: ⭐⭐⭐⭐ 适合

## 优缺点分析

### 优点
- 功能最全面的 GitHub CLI 参考
- 覆盖 gh 命令的各个方面
- 持续更新

### 缺点
- 主要是参考文档性质
- 需要配合 gh CLI 使用

## 平替对比

| 技能 | 评分 | 特点 |
|------|------|------|
| openclaw-github-assistant | 3.676 | 更侧重自动化操作 |
| github-ops | 3.530 | 更侧重仓库操作 |
| github-actions-generator | 3.461 | 更侧重 Actions 生成 |

## 落地过程

1. 安装 GitHub CLI: `brew install gh` 或 `apt install gh`
2. 认证: `gh auth login`
3. 安装技能: `clawhub install github-cli`
4. 开始使用各种 gh 命令参考
