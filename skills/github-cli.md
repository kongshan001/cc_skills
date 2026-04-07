# GitHub CLI

> GitHub CLI (gh) 命令行参考

## 技能描述

GitHub CLI 技能提供 gh 命令的完整参考，包括认证、仓库管理、Issue、PR、Actions 等操作。

## 功能列表

- gh 认证配置
- 仓库创建/克隆/列表
- Issue 管理（创建、列表、评论）
- Pull Request 创建和审查
- GitHub Actions 查看和触发
- 代码搜索
- 提交历史查看

## 安装方式

```bash
# macOS
brew install gh

# Ubuntu/Debian
sudo apt install gh

# 或使用 clawhub
clawhub install github-cli
```

## 推荐安装评估

| 环境 | 推荐度 | 说明 |
|------|--------|------|
| 本地开发 | ⭐⭐⭐⭐⭐ | Git 操作必备 |
| CI/CD | ⭐⭐⭐⭐⭐ | 自动化脚本必备 |
| ECS/服务器 | ⭐⭐⭐⭐ | 服务器 Git 操作 |

## 使用前提

- 已安装 gh CLI
- GitHub Personal Access Token (PAT)

## 注意事项

- 示例中使用 GH_TOKEN 等环境变量，注意保护令牌
- `gh auth token` 会暴露令牌到终端输出
