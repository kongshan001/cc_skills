# Security Auditor - 安全审计技能

## 基本信息

| 项目 | 内容 |
|------|------|
| **名称** | Security Auditor |
| **Slug** | security-auditor |
| **版本** | 1.0.0 |
| **作者** | jgarrison929 |
| **创建时间** | 2026-02-02 |
| **更新时间** | 2026-03-13 |

## 技能描述

Use when reviewing code for security vulnerabilities, implementing authentication flows, auditing OWASP Top 10, configuring CORS/CSP headers, handling secrets, input validation, SQL injection prevention, XSS protection, or any security-related code review.

安全审计技能，用于代码安全漏洞审查、身份验证流程实现、OWASP Top 10 审计、CORS/CSP 配置、Secrets 处理、输入验证、SQL 注入防护、XSS 防护等。

## 功能列表

- 代码安全漏洞审查
- 身份验证流程实现
- OWASP Top 10 审计
- CORS/CSP 配置
- Secrets 处理
- 输入验证
- SQL 注入防护
- XSS 防护
- 安全代码审查

## 安装方式

```bash
# 使用 ClawHub 安装
npx clawhub@latest install security-auditor

# 或全局安装 ClawHub 后安装
npm i -g clawhub
clawhub install security-auditor
```

## 推荐安装评估

### 本地安装 ⭐⭐⭐⭐⭐
- 适合场景：本地代码审查、开发阶段安全检查
- 优势：即时反馈、快速修复
- 要求：Node.js 环境

### ECS 安装 ⭐⭐⭐⭐⭐
- 适合场景：CI/CD 流水线、自动化安全扫描
- 优势：可集成到自动化流程
- 要求：ECS 实例

## 优缺点分析

### 优点
- 覆盖 OWASP Top 10
- 多场景安全支持
- 适合开发流程集成

### 缺点
- 需要安全知识背景
- 自动化扫描可能有误报

## 平替对比

| 技能 | 对比 |
|------|------|
| secure-api-calls | secure-api-calls 专注调用安全，security-auditor 专注代码审计 |

## 落地过程

1. 安装 ClawHub: `npm i -g clawhub`
2. 安装技能: `clawhub install security-auditor`
3. 配置扫描规则和范围
4. 开始安全代码审查