# mcp-adapter

> Model Context Protocol 适配器

## 概述

**Slug:** mcp-adapter  
**Owner:** lunarpulse  
**版本:** 0.1.0  
**更新时间:** 2026-04-08

## 功能列表

- 集成 Model Context Protocol (MCP) 服务器
- 访问外部工具和数据源
- AI 代理工具发现与执行
- 支持法律数据库、API、数据库连接器、天气服务等

## 使用场景

当需要让 AI 代理发现并执行 MCP 服务器上的工具时使用。

## 安装方式

```bash
clawhub install mcp-adapter
```

## 推荐安装评估

| 场景 | 推荐 | 说明 |
|------|------|------|
| 本地开发 | ✅ 推荐 | 需要 MCP 服务器配合 |
| ECS 服务器 | ✅ 推荐 | 适合服务器部署 MCP 服务 |

## 优缺点分析

**优点:**
- 标准化 MCP 协议集成
- 支持多种数据源类型

**缺点:**
- 需要配置外部 MCP 服务器

## 平替对比

- 与 OpenClaw 原生工具集成方式不同
- 适合需要 MCP 协议标准化的场景
