# GitHub

## 技能描述

Interact with GitHub using the `gh` CLI. Use `gh issue`, `gh pr`, `gh run`, and `gh api` for issues, PRs, CI runs, and advanced queries.

**所有者**: steipete  
**创建时间**: 2026-01-04  
**最新版本**: 1.0.0  
**ClawHub Slug**: `github`

## 功能列表

- GitHub CLI (`gh`) 集成
- Issue 管理（创建、查看、评论）
- Pull Request 管理
- CI/CD 运行查看
- 仓库操作
- GitHub API 查询
- 工作流管理
- 分支操作

## 安装方式

```bash
clawhub install github
```

或指定版本：

```bash
clawhub install github --version 1.0.0
```

## 依赖要求

```bash
# 安装 GitHub CLI
brew install gh  # macOS
# 或
sudo apt install gh  # Ubuntu/Debian
# 或
choco install gh  # Windows
```

## 推荐安装评估

### 本地环境
- ✅ **强烈推荐** - Git 工作流必备
- 适合所有开发者
- 需要配置 GitHub 认证
- 资源占用极低

### ECS/云服务器
- ✅ **推荐** - 适合自动化 CI/CD 场景
- 可用于自动化仓库操作
- 需要 GitHub Token 配置
- 适合机器人账户

## 使用场景

1. Issue 和 PR 管理
2. CI/CD 状态查看
3. 代码审查
4. 仓库克隆和管理
5. GitHub Actions 管理
6. 团队协作
7. 自动化脚本

## 常用命令

```bash
gh issue create --title "Bug" --body "Description"
gh pr create --title "Feature" --body "Description"
gh run list
gh run view
gh api repos/:owner/:repo
```

## 相关技能

- openclaw-github-assistant - OpenClaw GitHub 助手
- github-actions-generator - GitHub Actions 生成器
- github-trending - GitHub 趋势

## 来源

- **ClawHub**: https://clawhub.com/skills/github
- **搜索分数**: 2.833（GitHub 类别高分）
