# OpenClaw GitHub Assistant

> 查询和管理 GitHub 仓库 - 列出仓库、检查 CI 状态、创建 Issue、搜索仓库和查看最近活动

## 📋 基本信息

| 项目 | 内容 |
|------|------|
| **技能名称** | openclaw-github-assistant |
| **版本** | 1.0.0+ |
| **作者** | OpenClaw |
| **许可证** | MIT-0 |
| **评分** | ⭐ 3.0 |
| **安装数** | 85 (当前) / 90 (总) |

## 🎯 技能描述

OpenClaw GitHub Assistant 是一个用于与 GitHub API 交互的技能，支持以下功能：

- 列出用户仓库
- 检查 CI 状态
- 创建 Issue
- 搜索仓库
- 查看最近活动
- 创建仓库
- 创建 Pull Request

## 🛠️ 功能列表

1. **仓库管理** - 列出、创建、克隆仓库
2. **CI/CD 检查** - 查看 Actions 运行状态
3. **Issue 管理** - 创建、查看、搜索 Issue
4. **Pull Request** - 创建和管理 PR
5. **代码搜索** - 搜索仓库和代码
6. **活动追踪** - 查看最近提交和活动

## 📦 安装方式

```bash
# 使用 ClawHub 安装
clawhub install openclaw-github-assistant

# 或手动安装
git clone https://github.com/openclaw/skills/openclaw-github-assistant ./skills/openclaw-github-assistant
```

## 🔧 配置要求

### 环境变量

| 变量名 | 必需 | 说明 |
|--------|------|------|
| `GITHUB_TOKEN` | 是 | GitHub Personal Access Token |
| `GITHUB_USERNAME` | 是 | GitHub 用户名 |

### Token 权限要求

建议使用最小权限原则：
- **只读操作**: `public_repo` (仅公共仓库)
- **读写操作**: `repo` (完整仓库权限)

> ⚠️ 注意：`repo` 权限具有破坏性操作能力（创建/删除/修改仓库和 Issue），请谨慎使用。

## 📊 推荐安装评估

| 场景 | 推荐度 | 说明 |
|------|--------|------|
| **本地安装** | ⭐⭐⭐⭐⭐ | 强烈推荐，适合日常 GitHub 操作 |
| **ECS 安装** | ⭐⭐⭐⭐⭐ | 完美支持，适合服务器自动化 |

### 评分理由

- ✅ 功能完整，覆盖常用 GitHub 操作
- ✅ 安全评估通过，无恶意代码
- ✅ 安装机制安全，无外部代码下载
- ✅ 认证机制标准，使用官方 API
- ✅ 适合自动化工作流

## 🔐 安全评估

- ✅ 目的和能力一致
- ✅ 指令范围明确
- ✅ 安装机制安全
- ✅ 凭证要求合理

## 📝 使用示例

```bash
# 列出用户仓库
gh repo list

# 检查 CI 状态
gh run list

# 创建 Issue
gh issue create --title "Bug report" --body "Description"

# 搜索仓库
gh search repos keyword
```

---

*本报告由 OpenClaw 自动生成，更新时间: 2026-03-17*
