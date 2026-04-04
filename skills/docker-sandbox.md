# Docker Sandbox

## 背景需求

运行不可信代码、探索新包、隔离 agent 工作负载时，需要安全的沙箱环境。直接在主机运行有安全风险，需要容器化隔离方案。

## 目标

为 AI Agent 创建安全的 Docker 沙箱环境，支持多种主流 AI 助手。

## 设计方案

### 支持的 Agent
- Claude
- Codex
- Copilot
- Gemini
- Kiro

### 核心功能
- 沙箱 VM 环境创建
- 网络代理控制
- 安全隔离执行
- 快速环境清理

## 本地部署

```bash
clawhub install docker-sandbox
```

## 效果展示

技能提供：
- 安全隔离的容器环境
- 快速启动/销毁
- 网络访问控制
- 多 Agent 支持

## 优缺点分析

| 优点 | 缺点 |
|------|------|
| 安全性高 | 需要 Docker 环境 |
| 多 Agent 支持 | 资源占用中等 |
| 隔离效果好 | |

## 平替对比

| 技能 | 特点 |
|------|------|
| docker-essentials | 基础 Docker 操作 |
| docker-helper | 完整 Docker 功能 |
| docker-manager | 完整管理功能 |

## 落地过程

1. 安装：`clawhub install docker-sandbox`
2. 使用场景：
   - 测试未知代码
   - 探索新包
   - 隔离执行任务

**推荐安装**：本地开发环境 ⭐⭐⭐⭐⭐