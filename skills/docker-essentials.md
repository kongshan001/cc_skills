# Docker Essentials

> Docker 必备技能 - 容器管理和调试的全面指南

## 基础信息

| 项目 | 值 |
|------|-----|
| **Slug** | docker-essentials |
| **作者** | arnarsson |
| **版本** | 1.0.0 |
| **更新时间** | 2026-02-26 |
| **评分** | ⭐ 3.744 |

## 1. 背景需求

容器化已成为现代应用部署的标准方式。在 OpenClaw 中进行开发、调试时，经常需要与 Docker 进行交互，如管理镜像、容器、调试运行中的容器等。缺乏 Docker 集成技能会导致开发效率降低。

## 2. 目标

提供完整的 Docker 命令和工作流支持：
- 容器生命周期管理
- 镜像操作
- 容器调试
- 网络和卷管理

## 3. 设计方案

### 核心功能模块
- **容器管理**: 启动、停止、重启、删除容器
- **镜像操作**: 拉取、构建、推送、列出镜像
- **日志和调试**: 查看容器日志、进入容器内部
- **网络管理**: 创建和管理 Docker 网络
- **卷管理**: 数据持久化和共享

### 技术架构
- 直接调用 Docker Engine API
- 支持 Docker Compose 集成
- 提供常用命令模板

## 4. 本地部署

```bash
# 安装技能
clawhub install docker-essentials

# 验证安装
clawhub list | grep docker
```

### 环境要求
- Docker Engine 20.10+
- 本地或远程 Docker Daemon
- 网络访问 Docker Hub（可选）

## 5. 效果展示

```
用户: 列出运行中的容器
助手: [调用 Docker API]
CONTAINER ID  IMAGE          STATUS      PORTS
abc123        nginx:latest   Up 2 hours  0.0.0.0:80->80/tcp
def456        redis:alpine   Up 5 mins   0.0.0.0:6379->6379/tcp

用户: 查看 nginx 日志
助手: 2026/04/26 10:00:00 [notice] 1#1: start worker process
2026/04/26 10:00:01 [notice] 1#1: signal 29 received
```

## 6. 优缺点分析

### 优点
- ✅ 覆盖常用 Docker 操作
- ✅ 评分最高（3.744）的 Docker 相关技能
- ✅ 轻量级，无需额外依赖

### 缺点
- ⚠️ 需要 Docker socket 访问权限
- ⚠️ 1.0.0 版本相对基础
- ⚠️ 不支持 Windows 容器

## 7. 平替对比

| 技能 | 评分 | 特点 |
|------|------|------|
| docker-essentials | 3.744 | 基础功能全面 |
| docker-compose | 3.585 | 多容器编排 |
| docker-sandbox | 3.585 | 沙箱环境 |
| docker-ctl | 3.569 | 控制类技能 |

**推荐**: 基础需求选 **docker-essentials**，多容器编排选 **docker-compose**

## 8. 落地过程

### 第一阶段：安装配置 (5分钟)
1. 安装技能: `clawhub install docker-essentials`
2. 确保 Docker daemon 运行
3. 验证 Docker 访问权限

### 第二阶段：日常使用 (持续)
- 容器日常管理
- 镜像拉取和构建
- 调试运行中的容器

### 推荐安装评估

| 场景 | 推荐 | 理由 |
|------|------|------|
| **本地开发** | ⭐⭐⭐⭐⭐ | 完美支持开发环境 |
| **ECS 服务器** | ⭐⭐⭐⭐⭐ | 容器管理必备 |
| **Docker 开发** | ⭐⭐⭐⭐⭐ | 核心技能 |

**综合推荐**: ✅ 强烈推荐，所有 Docker 相关工作都需要此技能。