# Claude Code Skills 调研报告

> ClawHub 热门技能调研 - 自动化生成

## 索引

| # | 技能名称 | Slug | 评分 | 分类 | 推荐安装 |
|---|---------|------|------|------|----------|
| 1 | Docker Essentials | docker-essentials | 3.734 ⭐ | DevOps | 本地/ECS |
| 2 | Agentic Coding | agentic-coding | 3.590 ⭐ | 开发流程 | 本地 |
| 3 | Vibe Coding | vibe-coding | 3.500 ⭐ | 开发流程 | 本地 |
| 4 | E2E Testing Patterns | e2e-testing-patterns | 3.596 ⭐ | 测试 | 本地/ECS |
| 5 | Python Executor | python-executor | 3.530 ⭐ | Python | 本地/ECS |
| 6 | LSP Python | lsp-python | 3.437 ⭐ | Python | 本地 |
| 7 | GitHub CLI | github-cli | 3.632 ⭐ | DevOps | 本地/ECS |
| 8 | OpenClaw GitHub Assistant | openclaw-github-assistant | 3.701 ⭐ | DevOps | 本地/ECS |

## 分类统计

### 🐳 DevOps 类 (3)
- docker-essentials, github-cli, openclaw-github-assistant

### 🧪 测试类 (1)
- e2e-testing-patterns

### 🐍 Python 开发类 (2)
- python-executor, lsp-python

### ⚙️ 开发流程类 (2)
- agentic-coding, vibe-coding

## 热门搜索关键词

基于 ClawHub 搜索热度：

| 关键词 | Top 技能 |
|--------|----------|
| python | python-executor, lsp-python, friendly-python |
| coding | agentic-coding, vibe-coding, coding-agent |
| docker | docker-essentials, docker-sandbox, docker-compose |
| github | openclaw-github-assistant, github-cli, github-workflow |
| testing | e2e-testing-patterns, vitest-testing, e2e-testing |

## 安装方式

```bash
# 安装单个技能
clawhub install <slug>

# 示例
clawhub install docker-essentials
clawhub install python-executor
clawhub install e2e-testing-patterns
```

## 本地部署 vs ECS 部署

| 技能 | 本地 | ECS | 说明 |
|------|------|-----|------|
| docker-essentials | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | 通用性强，两端都适合 |
| python-executor | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | 沙箱执行，本地/服务器均可 |
| lsp-python | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | 代码检查，本地更方便 |
| e2e-testing-patterns | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | CI/CD 场景更多在 ECS |
| github-cli | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | 日常工具，两端都需要 |
| agentic-coding | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ | 需要持久化，本地更合适 |
| vibe-coding | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ | 快速原型，本地迭代更快 |

## 技能文件

所有技能调研报告保存在 `skills/` 目录：

- [Docker Essentials](skills/docker-essentials.md)
- [Agentic Coding](skills/agentic-coding.md)
- [Vibe Coding](skills/vibe-coding.md)
- [E2E Testing Patterns](skills/e2e-testing-patterns.md)
- [Python Executor](skills/python-executor.md)
- [LSP Python](skills/lsp-python.md)
- [GitHub CLI](skills/github-cli.md)
- [OpenClaw GitHub Assistant](skills/openclaw-github-assistant.md)

## 贡献

欢迎提交 PR 添加更多技能调研报告！

## 来源

- ClawHub: https://clawhub.com
- 技能仓库: https://github.com/kongshan001/cc_skills