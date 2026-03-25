# CSharp Developer 技能调研报告

## 1. 背景需求

C# 和 .NET 是企业级应用开发的主流选择。随着 .NET 8+ 的发布，性能和跨平台能力大幅提升，需要专业的 C# 开发技能。

## 2. 目标

为 Claude Code 提供 C# 应用开发能力：
- .NET 8+ 应用开发
- ASP.NET Core API
- Blazor Web 应用
- Entity Framework Core
- 异步模式
- CQRS 架构

## 3. 设计方案

### 核心能力
- **Minimal APIs**: 轻量级 API 开发
- **Entity Framework Core**: ORM 和数据库操作
- **异步模式**: async/await 最佳实践
- **CQRS**: 命令查询职责分离

### 技术栈
- .NET 8+
- ASP.NET Core
- Blazor
- Entity Framework Core
- MediatR

## 4. 本地部署

```bash
# 安装 CSharp Developer 技能
clawhub install csharp-developer
```

### 推荐安装评估
| 环境 | 推荐度 | 说明 |
|------|--------|------|
| 本地 | ⭐⭐⭐⭐⭐ | .NET 开发首选 |
| ECS | ⭐⭐⭐⭐ | 适合 CI/CD 部署 |

## 5. 效果展示

典型应用场景：
- 企业级 Web API
- 实时应用（SignalR）
- 桌面应用（WPF/WinUI）
- 微服务架构

## 6. 优缺点分析

### 优点
- 覆盖现代 .NET 技术栈
- 支持企业级架构模式
- 跨平台开发

### 缺点
- 版本较新，文档可能不完整
- 需要 .NET 开发基础

## 7. 平替对比

| 技能 | 特点 |
|------|------|
| csharp-developer | .NET 8+ 企业级开发 |
| php-full-stack-developer | PHP 企业级开发 |

## 8. 落地过程

1. 执行 `clawhub install csharp-developer`
2. 创建 .NET 项目
3. 根据指导实现 API 和业务逻辑
4. 配置数据库和部署

---
*调研时间: 2026-03-25*
*来源: ClawHub*
