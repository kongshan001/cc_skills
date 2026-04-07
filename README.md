# Claude Code Skills 调研报告

> ClawHub 热门技能调研 - 自动化生成

## 索引

| # | 技能名称 | Slug | 评分 | 分类 | 推荐安装 |
|---|---------|------|------|------|----------|
| 1 | Docker Essentials | docker-essentials | 3.735 ⭐ | DevOps | 本地/ECS |
| 2 | Docker Compose | docker-compose | 3.569 ⭐ | DevOps | 本地/ECS |
| 3 | Docker Sandbox | docker-sandbox | 3.575 ⭐ | DevOps | 本地/ECS |
| 4 | GitHub CLI | github-cli | 3.634 ⭐ | DevOps | 本地/ECS |
| 5 | GitHub Actions Generator | github-actions-generator | 3.508 ⭐ | DevOps | 本地 |
| 6 | OpenClaw GitHub Assistant | openclaw-github-assistant | 3.702 ⭐ | DevOps | 本地/ECS |
| 7 | Test Runner | test-runner | 3.672 ⭐ | 测试 | 本地/ECS |
| 8 | Test Master | test-master | 3.623 ⭐ | 测试 | 本地/ECS |
| 9 | Test Patterns | test-patterns | 3.572 ⭐ | 测试 | 本地/ECS |
| 10 | Python Executor | python-executor | 3.531 ⭐ | Python | 本地/ECS |
| 11 | LSP Python | lsp-python | 3.439 ⭐ | Python | 本地 |
| 12 | Agentic Coding | agentic-coding | 3.590 ⭐ | 开发流程 | 本地 |
| 13 | Vibe Coding | vibe-coding | 3.500 ⭐ | 开发流程 | 本地 |

## 分类统计

### 🐳 DevOps 类 (5)
- docker-essentials, docker-compose, docker-sandbox, github-cli, github-actions-generator, openclaw-github-assistant

### 🧪 测试类 (3)
- test-runner, test-master, test-patterns

### 🐍 Python 开发类 (2)
- python-executor, lsp-python

### ⚙️ 开发流程类 (2)
- agentic-coding, vibe-coding

## 热门搜索关键词

基于 ClawHub 搜索热度：

| 关键词 | Top 技能 |
|--------|----------|
| docker | docker-essentials, docker-sandbox, docker-compose, docker-ctl |
| github | openclaw-github-assistant, github-cli, github-workflow, github-actions-generator |
| test | test-runner, test-master, test-patterns, test-generator |
| python | python-executor, lsp-python, friendly-python |
| coding | agentic-coding, vibe-coding, coding-agent |

## 安装方式

```bash
# 安装单个技能
clawhub install <slug>

# 示例
clawhub install docker-essentials
clawhub install python-executor
clawhub install test-runner
```

## 本地部署 vs ECS 部署

| 技能 | 本地 | ECS | 说明 |
|------|------|-----|------|
| docker-essentials | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | 通用性强，两端都适合 |
| docker-compose | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | 多容器部署必备 |
| docker-sandbox | ⭐⭐⭐⭐ | ⭐⭐⭐⭐ | 安全隔离运行不受信任代码 |
| github-cli | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | 日常工具，两端都需要 |
| github-actions-generator | ⭐⭐⭐ | ⭐⭐⭐ | 快速生成 CI 工作流 |
| openclaw-github-assistant | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | 集成 GitHub 操作 |
| test-runner | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | 多框架测试运行 |
| test-master | ⭐⭐⭐⭐ | ⭐⭐⭐⭐ | 测试策略和自动化 |
| test-patterns | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ | 多语言测试模式 |
| python-executor | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | 远程 Python 沙箱 |
| lsp-python | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | 代码检查和格式化 |
| agentic-coding | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ | 需要持久化，本地更合适 |
| vibe-coding | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ | 快速原型，本地迭代更快 |

## 技能文件

所有技能调研报告保存在 `skills/` 目录：

### DevOps
- [Docker Essentials](skills/docker-essentials.md)
- [Docker Compose](skills/docker-compose.md)
- [Docker Sandbox](skills/docker-sandbox.md)
- [GitHub CLI](skills/github-cli.md)
- [GitHub Actions Generator](skills/github-actions-generator.md)
- [OpenClaw GitHub Assistant](skills/openclaw-github-assistant.md)

### 测试
- [Test Runner](skills/test-runner.md)
- [Test Master](skills/test-master.md)
- [Test Patterns](skills/test-patterns.md)

### Python
- [Python Executor](skills/python-executor.md)
- [LSP Python](skills/lsp-python.md)

### 开发流程
- [Agentic Coding](skills/agentic-coding.md)
- [Vibe Coding](skills/vibe-coding.md)

## 贡献

欢迎提交 PR 添加更多技能调研报告！

## 来源

- ClawHub: https://clawhub.com
- 技能仓库: https://github.com/kongshan001/cc_skills
