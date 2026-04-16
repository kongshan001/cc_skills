# ClawHub 热门技能调研报告

> 自动化调研 ClawHub 热门 Skills 并生成独立调研文档

## 技能索引

| # | 技能名称 | 描述 | 推荐安装 |
|---|---------|------|---------|
| 1 | [context-driven-development](./skills/context-driven-development.md) | 项目上下文管理，将上下文视为可管理工件 | 本地 ⭐⭐⭐⭐⭐ |
| 2 | [task-development-workflow](./skills/task-development-workflow.md) | TDD优先的开发工作流，含任务追踪和PR审查 | 本地 ⭐⭐⭐⭐⭐ |
| 3 | [prd-development](./skills/prd-development.md) | 产品需求转Coding Agent可执行文档 | 本地 ⭐⭐⭐⭐⭐ |
| 4 | [lowcode-platform-development](./skills/lowcode-platform-development.md) | Vue2+Element低代码平台自动化生成 | 本地 ⭐⭐⭐⭐⭐ |
| 5 | [dev-coding-agent](./skills/dev-coding-agent.md) | 增强型编码Agent，支持OpenCode集成 | 本地 ⭐⭐⭐⭐⭐ |
| 6 | [devloop-agent-pack](./skills/devloop-agent-pack.md) | 多Agent协作的产品驱动开发循环 | 本地 ⭐⭐⭐⭐⭐ |
| 7 | [cocos-cli-game-dev](./skills/cocos-cli-game-dev.md) | Cocos游戏项目创建、构建、修改 | 本地 ⭐⭐⭐⭐⭐ |
| 8 | [cc-godmode](./skills/cc-godmode.md) | 自编排多Agent开发工作流 | 本地 ⭐⭐⭐⭐⭐ |
| 9 | [senior-dev](./skills/senior-dev.md) | 生产级开发工作流，含GitHub/Vercel集成 | 本地 ⭐⭐⭐⭐⭐ |
| 10 | [contract-diagram](./skills/contract-diagram.md) | 以图表作为AI开发的契约约定 | 本地 ⭐⭐⭐⭐⭐ |
| 11 | [vibe-coding-workflow](./skills/vibe-coding-workflow.md) | 5阶段AI辅助开发工作流 | 本地 ⭐⭐⭐⭐⭐ |
| 12 | [vibe-coding-skill](./skills/vibe-coding-skill.md) | Vibe Coding 5阶段流程指导 | 本地 ⭐⭐⭐⭐⭐ |
| 13 | [ai-dlc](./skills/ai-dlc.md) | AI驱动的软件开发生命周期自适应工作流 | 本地 ⭐⭐⭐⭐⭐ |
| 14 | [auto-dev-pipeline](./skills/auto-dev-pipeline.md) | 单人公司完整自动化开发流程 | 本地 ⭐⭐⭐⭐⭐ |
| 15 | [hybrid-dev](./skills/hybrid-dev.md) | 本地模型规划+Copilot编码+验证 | 本地 ⭐⭐⭐⭐⭐ |
| 16 | [tdd](./skills/tdd.md) | 测试驱动开发TDD工作流 | 本地 ⭐⭐⭐⭐⭐ |
| 17 | [aidlc](./skills/aidlc.md) | AI-DLC自适应工作流（另一版本） | 本地 ⭐⭐⭐⭐⭐ |
| 18 | [cc-godmode-5-11-3](./skills/cc-godmode-5-11-3.md) | cc-godmode 5.11.3版本 | 本地 ⭐⭐⭐⭐⭐ |
| 19 | [coze-studio](./skills/coze-studio.md) | AI Agent可视化开发平台 | 本地 ⭐⭐⭐⭐⭐ |
| 20 | [web-module-runner](./skills/web-module-runner.md) | 现代Web应用一体化开发工具 | 本地 ⭐⭐⭐⭐⭐ |

## 安装方式

```bash
# 安装所有技能
for skill in context-driven-development task-development-workflow prd-development lowcode-platform-development dev-coding-agent devloop-agent-pack cocos-cli-game-dev cc-godmode senior-dev contract-diagram vibe-coding-workflow vibe-coding-skill ai-dlc auto-dev-pipeline hybrid-dev tdd aidlc cc-godmode-5-11-3 coze-studio web-module-runner; do
  clawhub install $skill
done
```

## 调研日期

2026-04-16

## 推送仓库

https://github.com/kongshan001/cc_skills