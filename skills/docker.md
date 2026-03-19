# Docker

> Docker、Dockerfile、容器构建、Compose、镜像发布、网络、卷、调试和生产容器操作

## 📋 基本信息

| 项目 | 内容 |
|------|------|
| **技能名称** | docker |
| **版本** | 1.0.0+ |
| **作者** | ivangdavila |
| **评分** | ⭐ 3.0+ |

## 🎯 技能描述

Docker 技能提供完整的 Docker 工作流指南，涵盖 Dockerfile 模式、Compose 编排、网络、卷、安全加固、调试和生产容器操作。

## 🛠️ 功能列表

### 1. 核心命令
- 镜像构建与管理
- 容器运行与监控
- 日志查看
- 调试技巧

### 2. Dockerfile 模式
- 多阶段构建
- 层缓存优化
- 最佳实践

### 3. Compose 编排
- 服务定义
- 依赖管理
- 环境配置

### 4. 网络与卷
- 自定义网络
- 卷挂载
- 数据持久化

### 5. 安全加固
- 非 root 用户
- 资源限制
- 镜像扫描

## 📦 安装方式

```bash
# 使用 ClawHub 安装
clawhub install docker

# Docker 安装
# macOS
brew install docker

# Linux
sudo apt install docker.io
sudo systemctl start docker
```

## 🔧 核心规则

### 1. 固定镜像版本
```dockerfile
# ✅ 正确
FROM python:3.11.5-slim

# ❌ 错误
FROM python:latest
```

### 2. 合并 RUN 命令
```dockerfile
# ✅ 正确 - 单层
RUN apt-get update && apt-get install -y pkg

# ❌ 错误 - 多层
RUN apt-get update
RUN apt-get install -y pkg
```

### 3. 默认非 Root
```dockerfile
# 添加非 root 用户
USER nonroot
```

### 4. 设置资源限制
```bash
# 内存限制
docker run -m 512m container-name
```

### 5. 配置日志轮转
```yaml
# docker-compose.yml
logging:
  driver: "json-file"
  options:
    max-size: "10m"
    max-file: "3"
```

## 📊 推荐安装评估

| 场景 | 推荐度 | 说明 |
|------|--------|------|
| **本地安装** | ⭐⭐⭐⭐⭐ | 强烈推荐，开发必备 |
| **ECS 安装** | ⭐⭐⭐⭐⭐ | 完美支持，容器化部署 |

### 评分理由

- ✅ 完整的 Docker 工作流指南
- ✅ 大量最佳实践和陷阱提示
- ✅ 安全加固建议
- ✅ Compose 完整支持

## ⚠️ 常见陷阱

### 镜像陷阱
- 多阶段构建: `--from=builder` 可能复制错误 stage
- `COPY` 在 `RUN` 之前会破坏缓存
- `ADD` 自动解压，除非需要否则用 `COPY`
- 构建参数在镜像历史中可见，不能用于 secrets

### 运行时陷阱
- 容器内的 `localhost` 是容器自己的 localhost
- 端口占用: 之前的容器可能还在停止中
- Exit code 137 = OOM killed, 139 = segfault

### 网络陷阱
- 容器 DNS 只在自定义网络有效
- 发布的端口默认绑定到 0.0.0.0

### Compose 陷阱
- `depends_on` 等待容器启动，不等待服务就绪
- `.env` 文件必须在 `docker-compose.yml` 旁边
- 卷挂载会覆盖容器文件

### 卷陷阱
- 匿名卷会悄悄积累
- 绑定挂载有权限问题
- 停止的容器数据持续到容器被删除

## 💡 资源泄漏处理

```bash
# 清理 dangling 镜像
docker image prune

# 清理构建缓存
docker builder prune

# 清理停止的容器
docker container prune

# 清理网络
docker network prune

# 完整清理
docker system prune --volumes
```

---

*本报告由 OpenClaw 自动生成，更新时间: 2026-03-17*
