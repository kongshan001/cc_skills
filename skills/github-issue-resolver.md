# GitHub Issue Resolver

> 自主发现、分析和修复 GitHub Issue 的 Agent - 配备 5 层安全护栏系统

## 📋 基本信息

| 项目 | 内容 |
|------|------|
| **技能名称** | github-issue-resolver |
| **版本** | 1.0.0 |
| **作者** | Ashwinhegde19 |
| **评分** | ⭐ 3.443 |

## 🎯 技能描述

GitHub Issue Resolver 是一个自主 Agent，用于发现、分析和修复开源 GitHub Issue。它配备 5 层安全护栏系统，确保操作安全可控。

## 🛠️ 功能列表

### 1. Issue 发现
- 自动获取开放 Issue
- 过滤 PR
- 按严重程度/影响/ effort/新鲜度评分
- 推荐最佳 Issue

### 2. 安全护栏系统 (5 层)
- **层1**: 加载护栏配置
- **层2**: 验证范围 (repo, branch, path)
- **层3**: 检查操作门 (auto/notify/approve)
- **层4**: 命令白名单验证
- **层5**: 审计日志

### 3. 修复流程
- 克隆仓库到沙箱
- 创建安全分支
- 探索代码库
- 制定修复计划
- 实现修复
- 运行测试
- 创建 PR (需用户批准)

## ⚠️ 关键规则 (不可违反)

- ❌ 永不触碰保护分支 (main, master, production)
- ❌ 永不修改 .env, secrets, CI 配置
- ❌ 永不强制推送
- ❌ 未经明确批准不修改依赖文件
- ❌ 永不修改自己的 skill/plugin 文件
- ❌ 一次只处理一个 Issue
- ❌ 所有危险操作需要用户批准
- ❌ 所有操作记录到 audit/ 目录

## 📦 安装方式

```bash
# 使用 ClawHub 安装
clawhub install github-issue-resolver
```

## 🔧 配置要求

### 必需文件
- `guardrails.json` - 护栏配置
- `references/guardrails-guide.md` - 护栏指南

### 必需脚本
- `scripts/guardrails.py` - 护栏验证
- `scripts/recommend.py` - Issue 推荐
- `scripts/sandbox.py` - 沙箱执行
- `scripts/audit.py` - 审计日志

### 环境要求
- Python 3+
- git

## 📊 推荐安装评估

| 场景 | 推荐度 | 说明 |
|------|--------|------|
| **本地安装** | ⭐⭐⭐⭐ | 推荐，适合贡献开源 |
| **ECS 安装** | ⭐⭐⭐⭐ | 可用，适合自动化任务 |

### 评分理由

- ✅ 5 层安全护栏确保安全
- ✅ 完整的 Issue 处理工作流
- ✅ 审计日志完整
- ⚠️ 需要 Python 环境
- ⚠️ 权限较大，需谨慎使用

## 🔐 安全特性

- 保护分支识别
- 敏感文件检查
- 操作审计日志
- 用户批准流程
- 沙箱执行环境

## 📝 使用流程

```bash
# 1. Phase 1 - Issue 发现
python3 scripts/guardrails.py repo <owner/repo>
python3 scripts/recommend.py

# 2. Phase 2 - 修复
python3 scripts/guardrails.py issue_lock <issue_number>
# ... 分析和实现修复

# 3. Phase 3 - 测试
python3 scripts/sandbox.py run npm test

# 4. Phase 4 - 创建 PR (需批准)
# 永远不自动创建 PR，需用户明确批准
```

---

*本报告由 OpenClaw 自动生成，更新时间: 2026-03-17*
