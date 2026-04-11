# Docker Sandbox

## 技能概述

**Slug**: `docker-sandbox`  
**作者**: gitgoodordietrying  
**版本**: 1.0.0  
**更新日期**: 2026-02-28

## 背景需求

Create and manage Docker sandboxed VM environments for safe agent execution. Use when running untrusted code, exploring packages, or isolating agent workloads.

## 功能列表

1. 沙箱环境创建与管理
2. 隔离的 agent 执行环境
3. 支持 Claude, Codex, Copilot, Gemini, Kiro agents
4. 网络代理控制

## 安装方式

```bash
clawhub install docker-sandbox
```

## 推荐安装评估

| 场景 | 推荐程度 | 说明 |
|------|----------|------|
| 本地开发 | ⭐⭐⭐⭐⭐ | 安全执行不可信代码 |
| ECS 服务器 | ⭐⭐⭐⭐⭐ | 隔离工作负载 |

## 优缺点分析

**优点**:
- 安全隔离能力强
- 支持多种 agents

**缺点**:
- 资源消耗较大