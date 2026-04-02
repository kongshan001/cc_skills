# Secure API Calls - 安全 API 调用技能

## 基本信息

| 项目 | 内容 |
|------|------|
| **名称** | Secure API Calls (Keychains) |
| **Slug** | secure-api-calls |
| **版本** | 1.0.3 |
| **作者** | smarcombes |
| **创建时间** | 2026-02-18 |
| **更新时间** | 2026-04-02 |

## 技能描述

Call any API without leaking credentials. Keychains proxies requests and injects real tokens server-side — your agent never sees them.

安全 API 调用技能，Keychains 代理请求并在服务器端注入真实令牌，Agent 永远不会看到凭据。

## 功能列表

- 凭据保护
- API 代理调用
- 服务器端令牌注入
- Zero Trust 架构
- OAuth 支持

## 安装方式

```bash
# 使用 ClawHub 安装
npx clawhub@latest install secure-api-calls

# 或全局安装 ClawHub 后安装
npm i -g clawhub
clawhub install secure-api-calls
```

## 推荐安装评估

### 本地安装 ⭐⭐⭐⭐
- 适合场景：本地开发、安全测试
- 优势：保护本地 API 密钥
- 要求： Node.js 环境

### ECS 安装 ⭐⭐⭐⭐⭐
- 适合场景：生产环境、团队协作
- 优势：集中凭据管理、安全审计
- 要求：ECS 实例

## 优缺点分析

### 优点
- 零信任安全模型
- 凭据永不暴露
- 支持多种认证方式

### 缺点
- 需要配置 Keychain 服务
- 有一定的学习成本

## 平替对比

| 技能 | 对比 |
|------|------|
| security-auditor | 安全审计 vs 安全调用 |

## 落地过程

1. 安装 ClawHub: `npm i -g clawhub`
2. 安装技能: `clawhub install secure-api-calls`
3. 配置 Keychain 服务和凭据
4. 通过代理进行安全 API 调用