# Docker Essentials

> Essential Docker commands and workflows for container management, image operations, and debugging.

## 技能概述

Docker Essentials 提供 Docker 容器管理的核心命令和工作流，包括镜像操作、容器调试等常用功能。

## 功能列表

- 容器管理命令
- 镜像操作命令
- 调试和排错命令
- 容器生命周期管理
- 网络和卷管理

## 安装方式

```bash
clawhub install docker-essentials
```

## 推荐安装评估

| 环境 | 推荐度 | 说明 |
|------|--------|------|
| 本地 | ⭐⭐⭐⭐⭐ | 本地开发必备，容器调试方便 |
| ECS | ⭐⭐⭐⭐ | 服务器容器管理必需 |

## 使用示例

```bash
# 列出容器
clawhub docker-essentials ps

# 查看容器日志
clawhub docker-essentials logs <container_id>

# 容器调试
clawhub docker-essentials exec -it <container_id> sh
```

## 优缺点

- ✅ 覆盖 Docker 日常操作
- ✅ 调试命令实用
- ❌ 功能相对基础
