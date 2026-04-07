# Docker Compose

> Docker Compose 配置和最佳实践

## 技能描述

Docker Compose 技能提供 docker-compose 命令参考和配置最佳实践，包括 healthcheck、depends_on、volumes、网络、profiles 等功能。

## 功能列表

- docker-compose 基本命令
- healthcheck 配置
- depends_on 依赖管理
- 卷挂载配置
- 网络配置
- profiles 使用
- 环境变量优先级
- .dockerignore 配置

## 安装方式

```bash
clawhub install docker-compose
```

## 推荐安装评估

| 环境 | 推荐度 | 说明 |
|------|--------|------|
| 本地开发 | ⭐⭐⭐⭐⭐ | 多容器开发必备 |
| ECS/服务器 | ⭐⭐⭐⭐⭐ | 服务部署必备 |
| CI/CD | ⭐⭐⭐⭐ | 测试环境搭建 |

## 使用前提

- 已安装 Docker 和 docker-compose
- 理解 YAML 语法

## 注意事项

- `deploy.resources` 配置仅在 swarm/stack 模式下生效
- 注意 destructive 命令（如 `docker compose down -v` 会删除卷）
