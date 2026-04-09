# Docker Sandbox

## 技能概述

- **Slug**: docker-sandbox
- **名称**: Docker Sandbox
- **作者**: gitgoodordietrying
- **版本**: 1.0.0
- **更新时间**: 2026-02-28

## 背景需求

在运行不受信任的代码、探索软件包或隔离 Agent 工作负载时，需要一个安全的沙箱环境来保护主机系统。

## 目标

Create and manage Docker sandboxed VM environments for safe agent execution. Use when running untrusted code, exploring packages, or isolating agent workloads. Supports Claude, Codex, Copilot, Gemini, and Kiro agents with network proxy controls.

## 功能列表

- 创建隔离的 Docker 沙箱环境
- 管理沙箱生命周期
- 支持多种 Agent (Claude, Codex, Copilot, Gemini, Kiro)
- 网络代理控制
- 安全隔离执行

## 安装方式

```bash
clawhub install docker-sandbox
```

## 推荐安装评估

- **本地开发**: ⭐⭐⭐⭐⭐ 强烈推荐
- **ECS 服务器**: ⭐⭐⭐⭐⭐ 强烈推荐

**理由**: 对于运行不受信任的代码或需要隔离环境的场景至关重要。适合安全要求高的开发环境。

## 优缺点分析

### 优点

1. 提供强大的安全隔离
2. 支持多种主流 Agent
3. 可控制网络访问
4. 适合测试不受信任的代码

### 缺点

1. 需要 Docker 环境
2. 有一定的资源开销

## 平替对比

| 技能 | 特点 |
|------|------|
| docker-essentials | 更侧重基础命令 |
| docker-compose | 专注于容器编排 |

## 落地过程

1. 执行 `clawhub install docker-sandbox`
2. 配置网络代理策略
3. 在需要隔离执行时激活此技能
