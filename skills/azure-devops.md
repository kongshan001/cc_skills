# Azure DevOps

## 技能概述

- **技能名称**: Azure DevOps
- **Slug**: azure-devops
- **版本**: 1.0.0
- **作者**: PALs-Software
- **创建时间**: 2026-02-09
- **更新时间**: 2026-03-01

## 背景需求

使用 Azure DevOps 的开发者需要一个统一的工具来管理项目、仓库、分支、PR 和工作项。缺乏自动化工具会增加手动操作成本。

## 目标

提供全面的 Azure DevOps 管理技能，支持项目、仓库、分支、PR、工作项和构建状态的查询与管理。

## 功能列表

1. **项目列表** - 列出 Azure DevOps 项目
2. **仓库管理** - 列出仓库和分支
3. **PR 管理** - 创建和管理 Pull Requests
4. **工作项管理** - 管理 Azure DevOps 工作项
5. **构建状态** - 检查构建执行状态
6. **DevOps 工作流** - 自动化 DevOps 工作流

## 安装方式

```bash
# 安装 Azure CLI (如未安装)
az extension add azure-devops

# 安装技能
clawhub install azure-devops
```

## 推荐安装评估

- **本地开发**: ⭐⭐⭐⭐ 适合 Azure 用户
- **ECS 服务器**: ⭐⭐⭐⭐⭐ Azure 必备

## 优缺点分析

### 优点
- 专注 Azure DevOps
- 功能全面
- 适合团队使用

### 缺点
- 限于 Azure 生态系统
- 需要 Azure 账号

## 平替对比

| 技能 | 评分 | 特点 |
|------|------|------|
| devops | 3.713 | 更通用的 DevOps |
| senior-devops | 3.554 | 更高级，支持多云 |
| devops-automation-pack | 3.520 | 更侧重自动化脚本 |

## 落地过程

1. 安装 Azure CLI 并配置: `az devops login`
2. 安装技能: `clawhub install azure-devops`
3. 连接 Azure DevOps 组织
4. 开始使用各种管理功能
