# Docker Compose

> Docker Compose - 多容器应用编排专家

## 基础信息

| 项目 | 值 |
|------|-----|
| **Slug** | docker-compose |
| **作者** | ivangdavila |
| **版本** | 1.0.0 |
| **更新时间** | 2026-02-26 |
| **评分** | ⭐ 3.585 |

## 1. 背景需求

现代应用通常由多个服务组成（Web 服务、数据库、缓存等）。单独管理每个容器会增加复杂性。Docker Compose 允许通过 YAML 文件定义和运行多容器应用。

## 2. 目标

提供 Docker Compose 的完整工作流支持：
- compose 文件编写
- 多容器应用管理
- 依赖处理和网络配置
- 卷和数据管理

## 3. 设计方案

### 核心功能模块
- **文件生成**: 根据需求生成 docker-compose.yml
- **服务管理**: up/down/restart 等操作
- **网络配置**: 自定义网络和 DNS
- **卷管理**: 数据持久化和共享

### 技术架构
- 基于 docker-compose CLI
- 支持 Compose Specification
- 集成 Docker 网络和卷

## 4. 本地部署

```bash
# 安装技能
clawhub install docker-compose

# 确保 docker-compose 已安装
docker-compose --version

# 或使用 Docker CLI 内置 compose
docker compose version
```

### 环境要求
- Docker Engine 20.10+
- docker-compose 或 Docker CLI (compose plugin)

## 5. 效果展示

```
用户: 创建一个 Node.js + Redis 应用
助手: [生成 docker-compose.yml]
version: '3.8'
services:
  app:
    build: .
    ports:
      - "3000:3000"
    depends_on:
      - redis
  redis:
    image: redis:alpine

用户: 启动所有服务
助手: [执行 docker compose up -d]
✓ redis Started
✓ app Started
```

## 6. 优缺点分析

### 优点
- ✅ 多容器编排能力
- ✅ 依赖自动处理
- ✅ 评分较高（3.585）

### 缺点
- ⚠️ 依赖 docker-compose
- ⚠️ 不适合单机单容器
- ⚠️ 网络配置相对复杂

## 7. 平替对比

| 技能 | 评分 | 特点 |
|------|------|------|
| docker-compose | 3.585 | 多容器编排 |
| docker-essentials | 3.744 | 单容器管理 |
| docker-sandbox | 3.585 | 沙箱环境 |

**推荐**: 多容器选 **docker-compose**，单容器选 **docker-essentials**

## 8. 落地过程

### 第一阶段：安装配置 (5分钟)
1. 安装技能: `clawhub install docker-compose`
2. 确保 docker-compose 可用

### 第二阶段：日常使用 (持续)
- 生成 compose 文件
- 管理多容器应用

### 推荐安装评估

| 场景 | 推荐 | 理由 |
|------|------|------|
| **本地开发** | ⭐⭐⭐⭐⭐ | 多服务开发必备 |
| **ECS 服务器** | ⭐⭐⭐⭐⭐ | 微服务部署 |
| **简单项目** | ⭐⭐⭐ | 单容器无需 |

**综合推荐**: ✅ 推荐安装，适合多服务应用开发和部署。