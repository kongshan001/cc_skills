# GitHub CLI (gh)

> 完整的 GitHub CLI 技能，提供 gh 命令的全面指南

## 📋 基本信息

| 项目 | 内容 |
|------|------|
| **技能名称** | github-cli |
| **版本** | gh 2.66.1+ |
| **作者** | tag-assistant |
| **评分** | ⭐ 3.574 |

## 🎯 技能描述

GitHub CLI (gh) 技能提供完整的 gh 命令使用指南，涵盖从认证到高级 GitHub 操作的各个方面。

## 🛠️ 功能列表

### 1. 认证与配置
- 交互式登录 (OAuth)
- PAT 令牌登录
- 企业 GitHub 登录
- 多账户切换
- 认证状态检查

### 2. 仓库操作
- 创建仓库 (交互式/命令行)
- 克隆仓库
- Fork 仓库
- 查看仓库信息
- 列出仓库

### 3. Issue 管理
- 创建 Issue
- 查看 Issue 列表
- Issue 标签管理
- Issue 搜索

### 4. Pull Request
- 创建 PR
- 查看 PR 状态
- PR 审查
- PR 合并

### 5. GitHub Actions
- 查看运行状态
- 管理 Workflows
- 触发 Workflow
- 下载 artifacts

### 6. Releases 管理
- 创建 Release
- 查看 Release
- 下载 Release 资产

### 7. Gists 操作
- 创建 Gist
- 列出 Gist
- 编辑 Gist

### 8. 搜索功能
- 仓库搜索
- 代码搜索
- Issue 搜索
- PR 搜索

### 9. 项目管理 (Projects V2)
- 项目列表
- 项目项管理
- GraphQL 支持

### 10. API 调用
- REST API
- GraphQL API
- 自定义请求

## 📦 安装方式

```bash
# macOS
brew install gh

# Linux
sudo apt install gh

# Windows
winget install GitHub.cli

# 或使用 ClawHub
clawhub install github-cli
```

## 🔧 配置要求

### 认证
```bash
# 交互式登录
gh auth login

# 使用令牌登录
echo "$MY_TOKEN" | gh auth login --with-token

# 检查认证状态
gh auth status
```

### 推荐 scopes

| 功能 | 需要的 Scope |
|------|-------------|
| 基础仓库/PR/Issue 操作 | `repo` |
| Gists | `gist` |
| 读取组织成员 | `read:org` |
| Projects V2 | `project` |
| 删除仓库 | `delete_repo` |
| Actions workflows | `workflow` |

## 📊 推荐安装评估

| 场景 | 推荐度 | 说明 |
|------|--------|------|
| **本地安装** | ⭐⭐⭐⭐⭐ | 强烈推荐，开发者必备 |
| **ECS 安装** | ⭐⭐⭐⭐⭐ | 完美支持 CI/CD 自动化 |

### 评分理由

- ✅ 功能最全面的 GitHub CLI 指南
- ✅ 包含 21 个主题的详细文档
- ✅ 适合所有级别开发者
- ✅ 支持企业版 GitHub
- ✅ 完美集成 CI/CD 工作流

## 💡 高级特性

### JSON 输出与格式化
```bash
# JSON 输出
gh repo view --json name,description,stargazerCount

# jq 格式化
gh repo view --json name,stargazerCount --jq '.stargazerCount'
```

### 环境变量
```bash
# 设置默认输出格式
GH_TOKEN: GitHub Personal Access Token
GH_REPO: 默认仓库 (owner/repo)
GH_HOST: GitHub Enterprise 主机
```

### 常用技巧
- 使用 `--repo` 或 `-R` 指定非当前目录的仓库
- 使用 `--json` 获取结构化数据便于脚本处理
- 使用 `--web` 在浏览器中打开
- 使用 `--limit` 控制列表数量

---

*本报告由 OpenClaw 自动生成，更新时间: 2026-03-17*
