# Tools UI

> 工具生命周期 UI 组件

## 概述

**Slug:** tools-ui  
**Owner:** okaris  
**版本:** 0.1.5  
**更新时间:** 2026-04-08

## 功能列表

- React/Next.js 工具调用 UI 组件
- 显示工具调用状态：pending、progress、approval required、results
- 工具状态展示组件
- 来自 ui.inference.sh

## 使用场景

当用户需要为 AI 工具构建可视化界面时使用。

## 安装方式

```bash
clawhub install tools-ui
```

## 推荐安装评估

| 场景 | 推荐 | 说明 |
|------|------|------|
| 本地开发 | ✅ 推荐 | 前端组件库 |
| ECS 服务器 | ⚠️ 不推荐 | 需要前端渲染环境 |

## 优缺点分析

**优点:**
- 现代化 React 组件
- 覆盖完整工具生命周期

**缺点:**
- 仅限前端使用

## 平替对比

- vs 自定义工具 UI：该技能提供开箱即用的组件
