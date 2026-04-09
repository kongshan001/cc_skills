# Claude Code Skills 调研报告

> 基于 ClawHub 热门技能的完整调研

## 调研说明

本调研报告分析了 ClawHub 平台 Top 20 热门技能，为每个技能生成详细分析报告，包含功能描述、使用场景、安装方式和部署评估。

## 技能列表

### 第一批：开发工具与基础设施

| 技能名称 | 描述 | 版本 | 适用场景 | 报告链接 |
|---------|------|------|----------|---------|
| docker-essentials | Docker 基础命令与工作流 | 1.0.0 | 容器管理、镜像操作、调试 | [📄](./skills/docker-essentials.md) |
| docker-sandbox | Docker 沙箱环境管理 | 1.0.0 | 安全隔离执行、不受信任代码运行 | [📄](./skills/docker-sandbox.md) |
| python-executor | Python 代码安全执行 | 0.1.5 | 快速原型开发、数据分析 | [📄](./skills/python-executor.md) |
| lsp-python | Python LSP 集成 | 1.1.0 | 代码质量检查、补全、诊断 | [📄](./skills/lsp-python.md) |
| python-code-test | Python 测试自动生成 | 1.0.3 | 自动生成测试用例、执行测试 | [📄](./skills/python-code-test.md) |
| openclaw-github-assistant | GitHub 仓库管理助手 | 2.0.1 | 仓库管理、CI 状态、Issue | [📄](./skills/openclaw-github-assistant.md) |
| github-cli | GitHub CLI 全面参考 | 1.0.0 | gh 命令查询、PR/Issue/Actions | [📄](./skills/github-cli.md) |
| github-search | GitHub 仓库深度搜索 | 1.0.0 | 技术调研、开源项目发现 | [📄](./skills/github-search.md) |

### 第二批：部署与 API

| 技能名称 | 描述 | 版本 | 适用场景 | 报告链接 |
|---------|------|------|----------|---------|
| vercel-deploy | Vercel 部署管理 | 1.0.0 | 前端应用部署、环境变量管理 | [📄](./skills/vercel-deploy.md) |
| deploy-agent | C.R.A.B 多步骤部署 | 1.1.0 | 全栈应用安全部署流程 | [📄](./skills/deploy-agent.md) |
| web-deploy | 多平台 Web 部署 | 1.0.0 | Vercel/Railway/GitHub Pages | [📄](./skills/web-deploy.md) |
| secure-api-calls | 安全 API 调用 | 1.0.3 | 凭证保护、零信任 API 调用 | [📄](./skills/secure-api-calls.md) |
| api-generator | API 代码生成器 | 2.0.0 | REST/GraphQL/OpenAPI 生成 | [📄](./skills/api-generator.md) |
| api-doc-writer | API 文档助手 | 1.0.1 | REST API 文档编写 | [📄](./skills/api-doc-writer.md) |

### 第三批：云服务与游戏

| 技能名称 | 描述 | 版本 | 适用场景 | 报告链接 |
|---------|------|------|----------|---------|
| hetzner-cloud | Hetzner Cloud CLI | 1.0.0 | 服务器/网络/防火墙管理 | [📄](./skills/hetzner-cloud.md) |
| cloud-storage | 多云存储管理 | 1.0.1 | 跨云提供商文件管理 | [📄](./skills/cloud-storage.md) |
| cloud-architect | 云架构设计 | 0.1.0 | 架构设计、迁移规划、成本优化 | [📄](./skills/cloud-architect.md) |
| text-game-arcade-universe-v3 | 综合文字游戏大厅 | 1.0.0 | 17+ 种 ASCII 棋牌/益智游戏 | [📄](./skills/text-game-arcade-universe-v3.md) |
| identity-guess-game | 身份猜猜猜 | 1.0.0 | 多人互动推理游戏 | [📄](./skills/identity-guess-game.md) |

## 调研统计

- **总技能数量:** 19 个
- **更新时间:** 2026-04-09
- **涵盖领域:**
  - Docker/容器 (2个)
  - Python 开发 (3个)
  - GitHub 工具 (3个)
  - 部署工具 (3个)
  - API 工具 (3个)
  - 云服务 (3个)
  - 游戏 (2个)

## 部署建议

### 本地开发推荐 ⭐⭐⭐⭐⭐
- **必装:** docker-essentials, lsp-python, python-code-test, openclaw-github-assistant, github-cli, github-search, secure-api-calls
- **推荐:** python-executor, vercel-deploy, web-deploy, api-generator, text-game-arcade-universe-v3

### ECS 服务器推荐 ⭐⭐⭐⭐⭐
- **必装:** docker-essentials, docker-sandbox, openclaw-github-assistant, deploy-agent, hetzner-cloud, cloud-storage, secure-api-calls
- **推荐:** python-code-test, cloud-architect, api-generator

## 快速安装

```bash
# 安装所有推荐技能
clawhub install docker-essentials docker-sandbox
clawhub install python-executor lsp-python python-code-test
clawhub install openclaw-github-assistant github-cli github-search
clawhub install vercel-deploy deploy-agent web-deploy
clawhub install secure-api-calls api-generator api-doc-writer
clawhub install hetzner-cloud cloud-storage cloud-architect
```

---

*生成时间: 2026-04-09*
*调研工具: ClawHub CLI v0.6.0*
*数据源: https://clawhub.com*
