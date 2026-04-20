# ClawHub 热门技能调研报告

> Claude Code 热门 Skills 独立调研报告

## 调研概述

- **调研时间**: 2026-04-20
- **数据来源**: ClawHub Registry
- **调研数量**: Top 12 技能

## 技能索引

| 编号 | 技能名称 | Slug | 推荐度 | 适用场景 |
|------|----------|------|--------|----------|
| 1 | Context Driven Development | context-driven-development | ⭐⭐⭐⭐⭐ | AI 开发必备 |
| 2 | Task Development Workflow | task-development-workflow | ⭐⭐⭐⭐⭐ | TDD 开发 |
| 3 | PRD Development | prd-development | ⭐⭐⭐⭐ | 产品需求 |
| 4 | Lowcode Platform Development | lowcode-platform-development | ⭐⭐⭐⭐ | 低代码平台 |
| 5 | Development Coding Agent | dev-coding-agent | ⭐⭐⭐⭐⭐ | 编码开发 |
| 6 | Devloop Agent Pack | devloop-agent-pack | ⭐⭐⭐⭐⭐ | 多 Agent 协作 |
| 7 | COCOS CLI Game Dev | cocos-cli-game-dev | ⭐⭐⭐⭐⭐ | 游戏开发 |
| 8 | CC Godmode | cc-godmode | ⭐⭐⭐⭐⭐ | 自 orchestration |
| 9 | Senior Dev | senior-dev | ⭐⭐⭐⭐⭐ | 生产级开发 |
| 10 | Contract Diagram | contract-diagram | ⭐⭐⭐⭐ | 图表契约 |
| 11 | Vibe Coding Workflow | vibe-coding-workflow | ⭐⭐⭐⭐⭐ | AI 开发工作流 |
| 12 | Vibe Coding Skill | vibe-coding-skill | ⭐⭐⭐⭐⭐ | Vibe Coding |

## 快速安装

```bash
# 安装单个技能
clawhub install <slug>

# 查看所有技能
clawhub list
```

## 推荐技能组合

### 入门组合
- context-driven-development + dev-coding-agent

### 进阶组合
- context-driven-development + task-development-workflow + senior-dev

### 全栈组合
- context-driven-development + devloop-agent-pack + vibe-coding-workflow

## 目录结构

```
cc_skills/
├── README.md
└── skills/
    ├── context-driven-development.md
    ├── task-development-workflow.md
    ├── prd-development.md
    ├── lowcode-platform-development.md
    ├── dev-coding-agent.md
    ├── devloop-agent-pack.md
    ├── cocos-cli-game-dev.md
    ├── cc-godmode.md
    ├── senior-dev.md
    ├── contract-diagram.md
    ├── vibe-coding-workflow.md
    └── vibe-coding-skill.md
```