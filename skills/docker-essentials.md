# Docker Essentials

## 技能描述

Docker Essentials 是由 arnarsson 开发的 Docker 技能，提供容器管理、镜像操作和调试的常用命令和工作流程。

## 功能列表

### 容器生命周期
- `docker run` - 运行容器（后台、端口映射、环境变量、卷挂载）
- `docker ps` - 列出运行中/所有容器
- `docker start/stop/restart` - 容器管理
- `docker rm` - 容器删除

### 容器检查与调试
- `docker logs` - 查看日志（跟踪、尾随、戳记）
- `docker exec` - 在容器中执行命令（交互shell、用户指定）
- `docker inspect` - 容器详情检查

### 镜像管理
- `docker build` - 从 Dockerfile 构建
- `docker pull/push` - 镜像拉取/推送
- `docker tag` - 镜像标记
- `docker rmi` - 镜像删除
- `docker image prune` - 清理未使用镜像

### Docker Compose
- `docker-compose up/down` - 服务启动/停止
- `docker-compose logs` - 查看服务日志
- `docker-compose exec` - 在服务中执行命令
- `docker-compose scale` - 服务扩展

### 网络与存储
- `docker network` - 网络管理
- `docker volume` - 卷管理

### 系统管理
- `docker system df/prune` - 磁盘使用/清理

## 安装方式

```bash
# 使用 ClawHub 安装
clawhub install docker-essentials
```

## 推荐安装评估

| 场景 | 推荐 | 说明 |
|------|------|------|
| 本地开发 | ✅ 推荐 | 日常容器操作必备 |
| ECS/服务器 | ✅ 推荐 | 服务器运维必备技能 |

### 本地部署
- 开发环境容器管理
- 本地多服务编排
- 快速环境搭建

### ECS 部署
- 生产容器运维
- 镜像构建与推送
- 服务编排管理
