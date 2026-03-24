# Docker Compose 技能调研

## 基本信息

| 属性 | 值 |
|------|-----|
| **Slug** | docker-compose |
| **名称** | Docker Compose |
| **作者** | ivangdavila |
| **版本** | 1.0.0 |
| **评分** | 3.554 |
| **创建时间** | 2026-02-10 |
| **更新时间** | 2026-02-26 |

## 技能描述

Define multi-container applications with proper dependency handling, networking, and volume management.

定义多容器应用程序，包含正确的依赖处理、网络和卷管理。

## 功能列表

- 多容器应用定义
- 依赖管理
- 网络配置
- 卷管理
- 服务编排

## 安装方式

```bash
clawhub install docker-compose
```

## 推荐安装评估

| 场景 | 推荐度 | 说明 |
|------|--------|------|
| **本地开发** | ⭐⭐⭐⭐⭐ | 强烈推荐，本地多服务开发必备 |
| **ECS 服务器** | ⭐⭐⭐⭐⭐ | 微服务部署必备 |

### 本地安装评估

- **适用人群**: 开发者、DevOps
- **使用频率**: 高频
- **依赖**: Docker + Docker Compose
- **学习成本**: 低

### ECS 安装评估

- **场景**: 微服务部署
- **优势**: 一键部署多服务应用
- **注意**: 生产环境需考虑 Swarm/K8s
