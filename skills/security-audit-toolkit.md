# Security Audit Toolkit - 安全审计工具包

## 基本信息

| 项目 | 内容 |
|------|------|
| **名称** | Security Audit Toolkit |
| **Slug** | security-audit-toolkit |
| **版本** | 1.0.0 |
| **作者** | gitgoodordietrying |
| **更新时间** | 2026-02-26 |

## 技能描述

Audit codebases and infrastructure for security issues. Use when scanning dependencies for vulnerabilities, detecting hardcoded secrets, checking OWASP top 10 issues, verifying SSL/TLS, auditing file permissions, or reviewing code for injection and auth flaws.

安全审计工具包，用于审计代码库和基础设施的安全问题。扫描依赖漏洞、检测硬编码 secrets、检查 OWASP Top 10 问题、验证 SSL/TLS、审计文件权限、审查注入和认证缺陷。

## 功能列表

- 依赖漏洞扫描
- 硬编码 secrets 检测
- OWASP Top 10 检查
- SSL/TLS 验证
- 文件权限审计
- 注入漏洞检测
- 认证缺陷审查

## 安装方式

```bash
# 使用 ClawHub 安装
npx clawhub@latest install security-audit-toolkit

# 或全局安装 ClawHub 后安装
npm i -g clawhub
clawhub install security-audit-toolkit
```

## 推荐安装评估

### 本地安装 ⭐⭐⭐⭐⭐
- 适合场景：本地代码审计、安全检测
- 优势：完全离线可用、隐私保护
- 要求：Node.js 环境

### ECS 安装 ⭐⭐⭐⭐
- 适合场景：CI/CD 安全扫描、团队共享
- 优势：可集成到构建流程
- 要求：ECS 实例需安装 Node.js

## 优缺点分析

### 优点
- 全面覆盖安全审计需求
- 可集成到 CI/CD 流程
- 支持多种扫描类型

### 缺点
- 依赖于具体代码结构
- 可能产生误报

## 平替对比

| 技能 | 对比 |
|------|------|
| security-auditor | 更侧重代码审查，本技能更偏重基础设施 |
| openclaw-security-toolkit | 更通用的安全工具集 |

## 落地过程

1. 安装 Node.js 环境
2. 安装 ClawHub: `npm i -g clawhub`
3. 安装技能: `clawhub install security-audit-toolkit`
4. 配置扫描范围和规则
5. 执行安全审计