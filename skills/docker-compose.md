# Docker Compose

## 技能概述

- **技能名称**: Docker Compose
- **Slug**: docker-compose
- **版本**: 1.0.0
- **作者**: ivangdavila
- **创建时间**: 2026-02-10
- **更新时间**: 2026-02-26

## 背景需求

现代应用通常由多个容器组成，需要协调管理。Docker Compose 是定义和管理多容器应用的标准工具，但配置复杂。

## 目标

提供 Docker Compose 技能，帮助开发者定义多容器应用，实现正确的依赖处理、网络管理和卷管理。

## 功能列表

1. **多容器定义** - 定义多容器应用
2. **依赖处理** - 容器启动顺序管理
3. **网络管理** - 容器网络配置
4. **卷管理** - 数据卷挂载和管理
5. **服务编排** - 协调多个服务

## 安装方式

```bash
# 安装 Docker Compose (如未安装)
apt-get install docker-compose

# 安装技能
clawhub install docker-compose
```

## 推荐安装评估

- **本地开发**: ⭐⭐⭐⭐⭐ 本地开发必备
- **ECS 服务器**: ⭐⭐⭐⭐⭐ 微服务部署必备

## 优缺点分析

### 优点
- 多容器管理标准
- 配置简单
- 适合开发环境

### 缺点
- 生产环境推荐使用 Kubernetes
- 需要 Docker 基础

## 平替对比

| 技能 | 评分 | 特点 |
|------|------|------|
| docker-essentials | 3.721 | 更侧重基础 Docker |
| docker-sandbox | 3.565 | 更侧重沙箱环境 |
| docker-ctl | 3.550 | 更侧重控制操作 |

## 落地过程

1. 确保 Docker 和 Docker Compose 已安装
2. 安装技能: `clawhub install docker-compose`
3. 编写 docker-compose.yml
4. 使用技能中的最佳实践管理多容器应用
