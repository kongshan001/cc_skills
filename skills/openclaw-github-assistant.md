# OpenClaw GitHub Assistant

> OpenClaw GitHub API 操作助手

## 技能描述

OpenClaw GitHub Assistant 提供在 OpenClaw 中直接操作 GitHub API 的能力，包括仓库管理、CI、Issue、PR 等。

## 功能列表

- 列出仓库
- 查看 CI 运行状态
- 管理 Issue（创建、列表、评论）
- 管理 Pull Request
- 创建仓库
- 代码搜索
- 提交历史查看

## 安装方式

```bash
clawhub install openclaw-github-assistant
```

## 环境变量配置

```bash
export GITHUB_TOKEN=your_personal_access_token
export GITHUB_USERNAME=your_username
```

或在 OpenClaw 配置中添加：
```json
{
  "github": {
    "token": "your_pat",
    "username": "your_user"
  }
}
```

## 推荐安装评估

| 环境 | 推荐度 | 说明 |
|------|--------|------|
| 本地开发 | ⭐⭐⭐⭐⭐ | 集成 GitHub 操作必备 |
| 自动化工作流 | ⭐⭐⭐⭐⭐ | CI/CD 集成必备 |
| ECS/服务器 | ⭐⭐⭐⭐ | 服务器端 Git 操作 |

## 使用前提

- GitHub Personal Access Token（建议使用最小权限 scope）
- 网络连接

## 注意事项

- 推荐使用最小权限 scope（避免使用 full repo scope）
- 令牌具有创建/删除仓库等破坏性权限，需妥善保管
- 建议存储在平台的 secret manager 中
