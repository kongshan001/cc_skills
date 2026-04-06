# GitHub CLI

> 全面的 GitHub CLI (gh) 参考指南

## 基本信息

| 属性 | 值 |
|------|-----|
| **Slug** | `github-cli` |
| **作者** | 社区 |
| **版本** | gh 2.66.1+ |
| **标签** | github, cli, gh, devops |

## 功能列表

### 认证与配置
- OAuth 交互登录
- PAT 令牌登录
- 多账户切换
- 作用域管理

### 仓库操作
- 创建/克隆/分叉
- 查看/编辑/删除
- 同步 (fork ↔ upstream)

### Issue 管理
- 创建/列表/查看
- 编辑/关闭/重新打开
- 评论/标签/分配

### Pull Request
- 创建/列表/查看
- 合并 (merge/squash/rebase)
- 审查/评论
- 检查 CI 状态

### GitHub Actions
- Workflow 运行列表/查看
- 重新运行/取消
- 下载 artifacts

### Releases
- 创建/列表/下载
- 编辑/删除

### 高级功能
- Projects V2 (GraphQL)
- API (REST & GraphQL)
- Codespaces
- Secrets & Variables

## 安装方式

### macOS
```bash
brew install gh
```

### Ubuntu/Debian
```bash
sudo apt install gh
```

### 验证
```bash
gh auth login
gh --version
```

## 推荐安装评估

### 本地环境 ⭐⭐⭐⭐⭐
- 开发日常使用
- CI/CD 脚本

### ECS 环境 ⭐⭐⭐⭐⭐
- 自动化部署
- 脚本化管理

## 常用命令速查

```bash
# 认证
gh auth login

# 仓库
gh repo create my-project --public --clone
gh repo clone owner/repo
gh repo fork

# Issue
gh issue create --title "Bug" --body "描述"
gh issue list --label bug
gh issue close 123

# PR
gh pr create --fill
gh pr list
gh pr merge 123 --squash
gh pr checks 123

# Actions
gh run list
gh run view 12345
gh run rerun 12345

# API
gh api repos/{owner}/{repo}
gh api graphql -f query='...'
```

## 优缺点分析

### ✅ 优点
- 完整覆盖 GitHub 操作
- 支持 REST/GraphQL API
- 强大的 JSON 输出和 JQ 过滤

### ⚠️ 局限
- 学习曲线较陡
- 需要熟悉命令行

## 替代方案

| 方案 | 特点 |
|------|------|
| GitHub Web UI | 可视化操作 |
| hub CLI | 较老，功能较少 |
| GitHub SDK | 程序化访问 |