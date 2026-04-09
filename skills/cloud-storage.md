# Cloud Storage

## 技能概述

- **Slug**: cloud-storage
- **名称**: Cloud Storage
- **作者**: ivangdavila
- **版本**: 1.0.1
- **更新时间**: 2026-02-25

## 背景需求

现代应用通常使用多个云存储服务，需要统一管理不同提供商的文件存储，并考虑成本和安全。

## 目标

Manage files across cloud providers with authentication, cost awareness, and multi-provider operations.

## 功能列表

- 多云提供商支持
- 文件管理
- 认证管理
- 成本感知
- 跨提供商操作

## 安装方式

```bash
clawhub install cloud-storage
```

## 推荐安装评估

- **本地开发**: ⭐⭐⭐⭐ 推荐
- **ECS 服务器**: ⭐⭐⭐⭐⭐ 强烈推荐

**理由**: 适合使用多云存储或需要统一管理存储资源的团队。

## 优缺点分析

### 优点

1. 多云支持
2. 统一接口
3. 成本优化
4. 简化管理

### 缺点

1. 配置复杂
2. 各平台差异

## 平替对比

| 技能 | 特点 |
|------|------|
| hetzner-cloud | 更侧重 Hetzner |
| cloud-architect | 更侧重架构设计 |

## 落地过程

1. 执行 `clawhub install cloud-storage`
2. 配置各云提供商凭证
3. 激活技能进行管理
