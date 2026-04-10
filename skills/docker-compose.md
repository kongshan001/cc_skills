# Docker Compose

> 技能Slug: docker-compose  
> 版本: 1.0.0  
> 作者: ivangdavila  
> 更新时间: 2026-02-26

## 技能描述

Define multi-container applications with proper dependency handling, networking, and volume management.

定义多容器应用程序，包含适当的依赖处理、网络和卷管理。

## 功能列表

- 多容器编排
- 依赖处理
- 网络配置
- 卷管理
- 服务发现

## 安装方式

```bash
# 使用 clawhub 安装
clawhub install docker-compose

# 或使用 npx
npx clawhub@latest install docker-compose
```

## 推荐安装评估

### 本地开发环境 ✅ 推荐

- 适合微服务开发
- 快速搭建本地环境
- 需要 Docker Compose 插件

### ECS/服务器 ✅ 推荐

- 生产环境服务编排
- 适合容器化微服务部署

## 适用场景

1. 本地微服务开发
2. 开发/测试环境搭建
3. 生产环境服务编排
4. CI/CD 流水线

## 替代技能对比

| 技能 | 特点 | 适用场景 |
|------|------|----------|
| docker-compose | 多容器编排 | 微服务 |
| kubernetes-devops | K8s 编排 | 生产级大规模部署 |