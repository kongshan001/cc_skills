# Git Helper

## 背景需求

日常开发中频繁使用 Git 基本命令（status、pull、push、branch、log），需要一个统一的入口来简化操作。

## 目标

提供常用 Git 操作的快速入口。

## 设计方案

### 核心功能
- git status：查看仓库状态
- git pull：拉取更新
- git push：推送提交
- git branch：分支管理
- git log：查看提交历史

## 本地部署

```bash
clawhub install git-helper
```

## 效果展示

技能提供常用 Git 命令的统一执行入口。

## 优缺点分析

| 优点 | 缺点 |
|------|------|
| 轻量级 | 功能较基础 |
| 简单易用 | 无高级功能 |
| 快速上手 | |

## 平替对比

| 技能 | 特点 |
|------|------|
| git-essentials | 基础+高级操作 |
| git-workflows | 高级操作 |
| git-cli | 基础 CLI |

## 落地过程

1. 安装：`clawhub install git-helper`
2. 使用：直接调用常用 Git 命令

**推荐安装**：本地开发环境 ⭐⭐⭐☆☆