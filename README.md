# Claude Code Skills 调研报告

> Claude Code 热门 Skills 调研与文档化

## 概览

本仓库收录 ClawHub 热门 Skills 的独立调研报告，涵盖四大方向：

| 方向 | 说明 |
|------|------|
| 🐳 DevOps/Docker | 容器管理、构建、部署 |
| 🐍 Python 开发 | 脚本生成、测试、代码质量 |
| 🎮 游戏开发 | AI 系统、寻路、行为树 |
| 🧪 自动化测试 | Playwright、E2E、测试策略 |
| ⚙️ 开发者工具 | GitHub CI/CD、CLI |

## 索引表

| 技能名称 | 版本 | 方向 | 本地评分 | ECS评分 | 作者 | 更新日期 |
|---------|------|------|---------|---------|------|---------|
| [docker-essentials](skills/docker-essentials.md) | 1.0.0 | DevOps | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | arnarsson | 2026-02-26 |
| [docker-sandbox](skills/docker-sandbox.md) | 1.0.0 | DevOps | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | gitgoodordietrying | 2026-02-28 |
| [docker-helper](skills/docker-helper.md) | 2.0.0 | DevOps | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | ckchzh | 2026-03-17 |
| [docker-manager](skills/docker-manager.md) | 1.0.2 | DevOps | ⭐⭐⭐ | ⭐⭐⭐⭐⭐ | sxliuyu | 2026-03-17 |
| [docker-compose-generator](skills/docker-compose-generator.md) | 1.0.1 | DevOps | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | sunshine-del-ux | 2026-03-29 |
| [python-script-generator](skills/python-script-generator.md) | 1.0.0 | Python | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | sunshine-del-ux | 2026-03-29 |
| [python-code-test](skills/python-code-test.md) | 1.0.3 | Python | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ | zhouhh2017 | 2026-03-29 |
| [game-ai](skills/game-ai.md) | 1.0.0 | 游戏 | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ | thb32133451 | 2026-03-04 |
| [playwright-pro](skills/playwright-pro.md) | 2.1.1 | 测试 | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | alirezarezvani | 2026-03-10 |
| [e2e-testing-patterns](skills/e2e-testing-patterns.md) | 1.0.0 | 测试 | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | wpank | 2026-02-26 |
| [playwright-browser-automation](skills/playwright-browser-automation.md) | 2.0.0 | 测试 | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | spiceman161 | 2026-03-29 |
| [openclaw-github-assistant](skills/openclaw-github-assistant.md) | 2.0.1 | 开发者工具 | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | conorkenn | 2026-03-29 |
| [cicd-pipeline](skills/cicd-pipeline.md) | 1.0.0 | 开发者工具 | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | gitgoodordietrying | 2026-02-25 |
| [github-cli](skills/github-cli.md) | 1.0.0 | 开发者工具 | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | tag-assistant | 2026-03-29 |
| [test-runner](skills/test-runner.md) | 1.0.0 | 测试 | ⭐⭐⭐⭐ | ⭐⭐⭐⭐ | cmanfre7 | 2026-02-26 |
| [computer-use-skill](skills/computer-use-skill.md) | 1.0.1 | 自动化 | ⭐⭐⭐⭐ | ⭐⭐⭐ | smallcosmos | 2026-03-29 |
| [screen-capture-hub](skills/screen-capture-hub.md) | 1.0.0 | 工具 | ⭐⭐⭐⭐⭐ | ⭐⭐ | datappt8 | 2026-03-29 |

## 安装方式

```bash
# 安装单个技能
clawhub install <skill-name>

# 例如安装 docker-essentials
clawhub install docker-essentials
```

## 调研范围

1. **游戏客户端开发** — Game AI Systems 等
2. **Python 开发** — 脚本生成、代码测试
3. **自动化测试** — Playwright 系列、E2E 测试模式
4. **DevOps/开发者工具** — Docker 系列、GitHub CI/CD

## 数据来源

- ClawHub Registry (https://clawhub.com)
- 搜索关键词：docker, python, game, test, playwright, github, ci cd

---
*最后更新：2026-03-29*