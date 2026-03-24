# ClawHub 热门技能调研报告

本仓库收集了 ClawHub 平台上最热门的 AI Agent Skills 调研报告。

## 调研方法

1. 使用 `clawhub search` 获取热门技能列表
2. 使用 `clawhub inspect <slug>` 获取技能详细信息
3. 为每个技能生成独立调研报告

## 技能索引

| # | 技能 Slug | 名称 | 评分 | 分类 | 推荐场景 |
|---|-----------|------|------|------|----------|
| 1 | git-essentials | Git Essentials | 3.776 | 开发工具 | 本地/ECS |
| 2 | docker-essentials | Docker Essentials | 3.723 | 容器化 | 本地/ECS |
| 3 | test-runner | Test Runner | 3.662 | 测试 | 本地开发 |
| 4 | git-workflows | Git Workflows | 3.717 | 开发工具 | 本地开发 |
| 5 | docker-compose | Docker Compose | 3.554 | 容器化 | 本地/ECS |
| 6 | test-master | Test Master | 3.609 | 测试 | 本地开发 |
| 7 | docker-ctl | Docker Ctl | 3.552 | 容器化 | 本地/ECS |
| 8 | test-patterns | Test Patterns | 3.565 | 测试 | 本地开发 |
| 9 | code | Code | 3.641 | 开发工具 | 本地开发 |
| 10 | git | Git | 3.679 | 开发工具 | 本地/ECS |
| 11 | test-specialist | Test Specialist | 3.492 | 测试 | 本地开发 |
| 12 | git-helper | Git Helper | 3.624 | 开发工具 | 本地/ECS |
| 13 | explain-code | Explain Code | 3.539 | 开发工具 | 本地开发 |
| 14 | test-generator | Test Generator | 3.440 | 测试 | 本地开发 |
| 15 | python-script-generator | Python Script Generator | 3.423 | Python | 本地/ECS |
| 16 | lsp-python | LSP Python | 3.427 | Python | 本地开发 |
| 17 | game-developer-skill | Game Developer Skill | 3.425 | 游戏开发 | 本地开发 |
| 18 | fullstack-developer | Fullstack Developer | 3.412 | 全栈 | 本地/ECS |
| 19 | test-case-generator | Test Case Generator | 3.410 | 测试 | 本地开发 |
| 20 | git-summary | Git Summary | 3.581 | 开发工具 | 本地/ECS |

## 分类统计

### 开发工具类 (8)
- git-essentials, git-workflows, git, git-helper, git-summary, code, explain-code

### 测试类 (6)
- test-runner, test-master, test-patterns, test-specialist, test-generator, test-case-generator

### 容器化类 (3)
- docker-essentials, docker-compose, docker-ctl

### Python 类 (2)
- python-script-generator, lsp-python

### 游戏开发类 (1)
- game-developer-skill

### 全栈类 (1)
- fullstack-developer

## 安装方式

```bash
# 安装单个技能
clawhub install <skill-slug>

# 例如安装 git-essentials
clawhub install git-essentials
```

## 报告结构

每个技能报告包含：
1. 基本信息（名称、作者、版本、评分）
2. 技能描述
3. 功能列表
4. 安装方式
5. 推荐安装评估（本地/ECS）

## 更新日志

- 2026-03-24: 初始版本，包含 20 个热门技能调研报告

## 相关链接

- ClawHub: https://clawhub.com
- OpenClaw: https://docs.openclaw.ai
