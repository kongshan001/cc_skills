# Docker Essentials

> Docker 命令行速查和最佳实践

## 技能描述

Docker Essentials 是一个 Docker 命令行参考技能，提供常用的 Docker 和 docker-compose 命令及工作流程指南。包括容器构建、运行、管理、网络、卷等操作。

## 功能列表

- 容器生命周期管理（run, start, stop, rm）
- 镜像构建和操作（build, pull, push, tag）
- 卷管理（volume create/ls/rm）
- 网络配置（network create/ls/connect）
- 日志和调试（logs, exec, inspect）
- 清理命令（prune, system df）
- docker-compose 基础操作

## 安装方式

```bash
clawhub install docker-essentials
```

或手动安装：

```bash
mkdir -p skills/docker-essentials
# 复制 SKILL.md 到 skills/docker-essentials/
```

## 推荐安装评估

| 环境 | 推荐度 | 说明 |
|------|--------|------|
| 本地开发 | ⭐⭐⭐⭐⭐ | 本地 Docker 环境必备 |
| ECS/服务器 | ⭐⭐⭐⭐⭐ | 服务器运维必备 |

## 使用前提

- 已安装 Docker CLI
- 已安装 docker-compose（可选）

## 注意事项

- 示例命令包含环境变量传递（如 POSTGRES_PASSWORD），避免复制含敏感信息的命令
- 挂载主机路径和传递环境变量是正常用法，需注意安全
