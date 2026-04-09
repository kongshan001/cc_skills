# Secure API Calls

## 技能概述

- **Slug**: secure-api-calls
- **名称**: Secure API Calls
- **作者**: smarcombes
- **版本**: 1.0.3
- **更新时间**: 2026-04-09

## 背景需求

在调用 API 时，凭证（如 API keys、tokens）容易泄露，造成安全风险。需要一种安全的方式来调用 API 而不暴露凭证。

## 目标

Call any API without leaking credentials. Keychains proxies requests and injects real tokens server-side — your agent never sees them.

## 功能列表

- 安全 API 调用
- 凭证隔离
- Keychains 代理
- 服务端 token 注入
- OAuth 支持
- 零信任架构

## 安装方式

```bash
clawhub install secure-api-calls
```

## 推荐安装评估

- **本地开发**: ⭐⭐⭐⭐⭐ 强烈推荐
- **ECS 服务器**: ⭐⭐⭐⭐⭐ 强烈推荐

**理由**: 安全是开发中的重要考量，此技能可以有效保护 API 凭证不被泄露。

## 优缺点分析

### 优点

1. 保护 API 凭证
2. 零信任安全架构
3. 支持 OAuth
4. 服务端 token 注入

### 缺点

1. 需要额外的基础设施
2. 配置复杂度

## 平替对比

| 技能 | 特点 |
|------|------|
| api-generator | 更侧重 API 生成 |
| api-doc-writer | 更侧重文档编写 |

## 落地过程

1. 执行 `clawhub install secure-api-calls`
2. 配置 Keychains 服务
3. 注册 API 凭证
4. 通过技能安全调用 API
