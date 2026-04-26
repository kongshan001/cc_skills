# OpenClaw GitHub Assistant

> OpenClaw GitHub 助手 - 管理 GitHub 仓库的全面解决方案

## 基础信息

| 项目 | 值 |
|------|-----|
| **Slug** | openclaw-github-assistant |
| **作者** | conorkenn |
| **版本** | 2.0.1 |
| **更新时间** | 2026-04-26 |
| **评分** | ⭐ 3.717 |

## 1. 背景需求

在日常开发中，开发者经常需要在 OpenClaw 中与 GitHub 进行交互，如查看仓库列表、检查 CI 状态、创建 Issue、搜索仓库等。缺乏统一的 GitHub 集成工具会导致效率低下，需要频繁切换到浏览器或使用独立的 CLI 工具。

## 2. 目标

为 OpenClaw 提供一个原生的 GitHub 集成技能，实现：
- 仓库列表查询与管理
- CI/CD 状态检查
- Issue 创建与管理
- 仓库搜索
- 查看最近活动

## 3. 设计方案

### 核心功能模块
- **仓库管理**: 列出用户/组织的仓库，支持过滤和排序
- **CI 状态查询**: 集成 GitHub Actions，获取工作流运行状态
- **Issue 管理**: 创建、查看、更新 Issue
- **仓库搜索**: 通过 GitHub API 搜索仓库和代码
- **活动追踪**: 获取仓库的最新提交、PR、Issue 动态

### 技术架构
- 基于 GitHub REST API v3
- 使用 gh CLI 作为后备方案
- 支持 OAuth 认证和 Personal Access Token

## 4. 本地部署

```bash
# 安装技能
clawhub install openclaw-github-assistant

# 配置认证
export GITHUB_TOKEN=your_personal_access_token

# 验证安装
clawhub list | grep github
```

### 环境要求
- OpenClaw 环境（本地或 ECS）
- GitHub Personal Access Token
- 网络访问 github.com

## 5. 效果展示

```
用户: 查看我的仓库列表
助手: [调用仓库列表API]
├── repo-1 (⭐ 120, last updated: 2026-04-25)
├── repo-2 (⭐ 85, last updated: 2026-04-20)
└── repo-3 (⭐ 42, last updated: 2026-04-15)

用户: 检查 main 分支 CI 状态
助手: ✅ CI 通过 - 2/2 工作流成功
  ├── build (✅ 3m 24s)
  └── test (✅ 5m 12s)
```

## 6. 优缺点分析

### 优点
- ✅ 原生集成，无需切换工具
- ✅ 支持完整的 GitHub API 覆盖
- ✅ 实时获取 CI 状态
- ✅ 2.0.1 版本稳定可靠

### 缺点
- ⚠️ 需要配置 GitHub Token
- ⚠️ API 速率限制
- ⚠️ 部分高级功能需要 gh CLI

## 7. 平替对比

| 技能 | 评分 | 特点 |
|------|------|------|
| openclaw-github-assistant | 3.717 | 功能全面，原生集成 |
| github-cli | 3.655 | gh CLI 封装，更专业 |
| github-workflow | 3.537 | 侧重工作流管理 |
| github-analyzer | 3.524 | 项目分析能力 |

**推荐**: 需要全面 GitHub 管理选 **openclaw-github-assistant**，需要专业 CLI 选 **github-cli**

## 8. 落地过程

### 第一阶段：安装配置 (5分钟)
1. 安装技能: `clawhub install openclaw-github-assistant`
2. 配置 GitHub Token
3. 验证基本功能

### 第二阶段：日常使用 (持续)
- 日常仓库查询
- CI 状态监控
- Issue 管理

### 推荐安装评估

| 场景 | 推荐 | 理由 |
|------|------|------|
| **本地开发** | ⭐⭐⭐⭐⭐ | 轻量级，原生集成体验好 |
| **ECS 服务器** | ⭐⭐⭐⭐⭐ | 适合 CI/CD 流程集成 |
| **个人项目** | ⭐⭐⭐⭐⭐ | 完美满足需求 |

**综合推荐**: ✅ 强烈推荐安装，无论是本地还是 ECS 环境都非常适合。