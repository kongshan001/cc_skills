# C.R.A.B Deploy Agent

## 技能概述

- **Slug**: deploy-agent
- **名称**: C.R.A.B Deploy Agent
- **作者**: sherajdev
- **版本**: 1.1.0
- **更新时间**: 2026-02-27

## 背景需求

全栈应用部署涉及多个步骤：构建、测试、推送到 GitHub、部署到 Cloudflare Pages。每个步骤都需要人工确认以确保安全。

## 目标

Multi-step deployment agent for full-stack apps. Build → Test → GitHub → Cloudflare Pages with human approval at each step.

## 功能列表

- 多步骤部署流程
- 构建步骤
- 测试步骤
- GitHub 推送
- Cloudflare Pages 部署
- 每步骤人工审批
- 部署状态跟踪

## 安装方式

```bash
clawhub install deploy-agent
```

## 推荐安装评估

- **本地开发**: ⭐⭐⭐⭐ 推荐
- **ECS 服务器**: ⭐⭐⭐⭐⭐ 强烈推荐

**理由**: 适合需要安全部署流程的团队，每步骤审批机制可以减少错误。

## 优缺点分析

### 优点

1. 安全的部署流程
2. 每步骤审批
3. 减少部署错误
4. 完整的部署跟踪

### 缺点

1. 流程相对较慢
2. 限于 Cloudflare Pages

## 平替对比

| 技能 | 特点 |
|------|------|
| vercel-deploy | 更侧重 Vercel 平台 |
| web-deploy | 更通用的 Web 部署 |

## 落地过程

1. 执行 `clawhub install deploy-agent`
2. 配置 GitHub 和 Cloudflare
3. 激活技能开始部署流程
4. 每步骤审批后继续
