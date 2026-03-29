# GitHub CLI

## 1. 背景需求

GitHub CLI (`gh`) 是官方命令行工具，但命令复杂难以记忆：
- Repo 管理命令繁多
- Issues 和 PRs 操作复杂
- Actions 和 Releases 交互
- Search 功能强大但参数多
- API 调用需要构造

需要一个完整的命令速查助手。

## 2. 目标

提供全面的 GitHub CLI 参考：
- Repos：创建、克隆、fork、列表
- Issues：创建、评论、标签、状态
- PRs：创建、审查、合并
- Actions：运行、状态、日志
- Releases：创建、发布、查看
- Gists：创建、编辑
- Search：代码、仓库、issues
- Projects v2：看板管理
- API：GraphQL/REST 调用
- Secrets 和 variables：管理
- Labels：管理
- Codespaces：管理

## 3. 设计方案

**命令分类速查**：
```
gh repo          # 仓库操作
gh issue         # Issue 管理
gh pr            # PR 管理
gh action        # Actions 管理
gh release       # 发布管理
gh search        # 搜索
gh api           # API 调用
gh secret        # Secrets 管理
```

**认证管理**：登录、退出、状态检查。

## 4. 本地部署

```bash
clawhub install github-cli
```

**依赖**：
- gh CLI 已安装

**验证**：
```bash
gh --version
gh auth status
```

## 5. 效果展示

触发示例：
- "创建一个新的仓库"
- "列出我所有的 PR"
- "搜索最近的星标超过 100 的仓库"

执行效果：AI 生成正确的 gh 命令并执行。

## 6. 优缺点分析

| 优点 | 缺点 |
|------|------|
| 命令覆盖全面 | 需要学习命令格式 |
| 减少查阅文档时间 | 不如 API 灵活 |
| 交互式和脚本模式 | 复杂操作可能需要管道 |
| 官方支持 | 版本更新可能改变行为 |

## 7. 平替对比

| 方案 | 特点 | 适用场景 |
|------|------|----------|
| GitHub CLI（当前） | 命令速查，官方工具 | 日常操作 |
| OpenClaw GitHub Assistant | API 层集成 | AI 代理操作 |
| GitHub API | 底层控制 | 复杂场景 |

## 8. 落地过程

**推荐安装评估**：
- **本地开发机** ⭐⭐⭐⭐⭐ — 开发者必备
- **ECS 云服务器** ⭐⭐⭐⭐ — 自动化脚本

**使用建议**：
1. 配合 GitHub token 使用
2. 使用 `--json` 输出便于解析
3. 常用命令可以 alias

**版本**：1.0.0 | **作者**：tag-assistant | **更新**：2026-03-29