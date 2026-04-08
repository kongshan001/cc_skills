# WebMCP (brunobuddy)

> 网页 MCP 自动化

## 概述

**Slug:** webmcp  
**Owner:** brunobuddy  
**版本:** 1.0.0  
**更新时间:** 2026-02-25

## 功能列表

- 浏览和自动化网页
- 通过 WebMCP API 发现工具
- window.navigator.modelContext 工具调用
- 替代 DOM 抓取方式

## 使用场景

当需要自动化暴露 WebMCP API 的网站时使用。

## 安装方式

```bash
clawhub install webmcp
```

## 推荐安装评估

| 场景 | 推荐 | 说明 |
|------|------|------|
| 本地开发 | ✅ 推荐 | 需要目标网站支持 WebMCP |
| ECS 服务器 | ✅ 推荐 | 可用于自动化任务 |

## 优缺点分析

**优点:**
- 结构化工具调用
- 无需 DOM 解析

**缺点:**
- 需要网站支持 WebMCP
