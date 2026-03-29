# OpenClaw GitHub Assistant

## 1. 背景需求

GitHub 是开发者协作的核心平台，日常操作包括：
- 查看仓库状态和 CI 结果
- 管理 Issues 和 PRs
- 搜索代码和仓库
- 查看活动记录

需要高效的方式让 AI 代理执行这些操作。

## 2. 目标

GitHub 仓库查询和管理：
- 列出仓库、查看信息
- 检查 CI/CD 状态
- 创建和管理 Issues
- PR 创建和评论
- 仓库搜索
- 最近活动查看
- 多仓库支持

## 3. 设计方案

**能力矩阵**：
| 操作 | 说明 |
|------|------|
| 仓库管理 | 列表、信息、拉取 |
| Issues | 创建、评论、标签、关闭 |
| PRs | 查看、评论、合并 |
| CI 状态 | Actions 运行状态 |
| 搜索 | 仓库、代码、用户 |
| 活动 | 最近提交、评论、事件 |

**认证**：使用 GitHub Token（环境变量或配置）

## 4. 本地部署

```bash
clawhub install openclaw-github-assistant
```

**依赖**：
- GitHub CLI (`gh`) 或 API token
- 网络可达 github.com

**验证**：
```bash
gh auth status
# 或
echo $GITHUB_TOKEN | head -c 10
```

## 5. 效果展示

触发示例：
- "查看这个仓库最近的 CI 运行"
- "创建一个 Issue 说构建失败了"
- "搜索包含某个函数的仓库"

执行效果：AI 通过 GitHub API 执行操作，返回结构化结果。

## 6. 优缺点分析

| 优点 | 缺点 |
|------|------|
| 覆盖常见 GitHub 操作 | API 限制（速率） |
| 无需切换到浏览器 | 需要适当权限的 token |
| 多仓库支持 | 复杂操作可能需要手动 |
| 最新版本活跃维护 | 不支持 GitHub Enterprise 特殊功能 |

## 7. 平替对比

| 方案 | 特点 | 适用场景 |
|------|------|----------|
| OpenClaw GitHub Assistant（当前） | OpenClaw 集成，功能全 | OpenClaw 用户 |
| GitHub CLI | 官方 CLI | 熟悉 gh 的用户 |
| GitHub Operations | 自动操作 | 自动化工作流 |

## 8. 落地过程

**推荐安装评估**：
- **本地开发机** ⭐⭐⭐⭐⭐ — 开发者必备
- **ECS 云服务器** ⭐⭐⭐⭐ — 自动化运维

**使用建议**：
1. 配置 GitHub Token 环境变量
2. 优先使用 gh（更方便）
3. 注意 API 速率限制

**版本**：2.0.1 | **作者**：conorkenn | **更新**：2026-03-29