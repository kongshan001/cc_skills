# Secure API Calls Skill 调研报告

> 安全 API 调用技能

## 1. 技能概述

| 项目 | 信息 |
|------|------|
| 名称 | secure-api-calls |
| 版本 | 1.0.3 |
| 作者 | smarcombes |
| 更新时间 | 2026-03-14 |

## 2. 功能描述

Call any API without leaking credentials. Keychains proxies requests and injects real tokens server-side — your agent never sees them.

## 3. 核心功能

- 🔐 安全凭证管理
- 🔑 Keychains 代理
- 🔒 零信任架构
- 🍪 OAuth 支持

## 4. 安装方式

```bash
clawhub install secure-api-calls
```

## 5. 推荐安装评估

### 本地安装 ⭐⭐⭐⭐⭐ (强烈推荐)

- **适用场景**: 本地开发、API 测试
- **优势**: 
  - 凭证安全不泄露
  - 简化 API 调用
  - 支持多种认证方式
- **要求**: 需要配置 Keychains

### 阿里云 ECS ⭐⭐⭐⭐⭐ (强烈推荐)

- **适用场景**: 生产环境、自动化部署
- **优势**: 
  - 保护敏感凭证
  - 适合 CI/CD
  - 零信任安全
- **注意**: 需要配置 Keychains 服务

## 6. 安全特性

- 凭证不暴露给 Agent
- 服务端 Token 注入
- 支持 OAuth
- 零信任架构

---

*生成时间: 2026-03-14*
