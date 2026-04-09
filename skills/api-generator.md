# API Generator

## 技能概述

- **Slug**: api-generator
- **名称**: API Generator
- **作者**: ckchzh
- **版本**: 2.0.0
- **更新时间**: 2026-03-17

## 背景需求

开发 RESTful API 需要编写端点、文档、客户端代码等，工作繁琐且容易出错。自动化生成可以大大提高效率。

## 目标

API code generator. Generate RESTful endpoints, GraphQL schemas, OpenAPI/Swagger docs, API clients, mock servers, authentication, rate limiting.

## 功能列表

- RESTful 端点生成
- GraphQL schema 生成
- OpenAPI/Swagger 文档生成
- API 客户端生成
- Mock 服务器
- 认证实现
- 限流实现

## 安装方式

```bash
clawhub install api-generator
```

## 推荐安装评估

- **本地开发**: ⭐⭐⭐⭐⭐ 强烈推荐
- **ECS 服务器**: ⭐⭐⭐⭐ 推荐

**理由**: API 开发的高效工具，可以自动生成大量样板代码。

## 优缺点分析

### 优点

1. 自动生成代码
2. 支持多种格式
3. 提高开发效率
4. 保证代码一致性

### 缺点

1. 生成代码可能需要调整
2. 学习生成器配置

## 平替对比

| 技能 | 特点 |
|------|------|
| api-doc-writer | 更侧重文档编写 |
| secure-api-calls | 更侧重安全调用 |

## 落地过程

1. 执行 `clawhub install api-generator`
2. 定义 API 规范
3. 激活技能生成代码
4. 审核并集成代码
