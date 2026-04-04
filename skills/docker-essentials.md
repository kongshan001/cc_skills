# Docker Essentials

## 背景需求

Docker 是容器化开发的核心工具，开发者需要快速创建、管理容器，调试容器问题，优化镜像。命令繁杂且跨平台差异大，亟需统一入口。

## 目标

提供 Docker 基本命令和工作流，覆盖容器管理、镜像操作、调试等场景。

## 设计方案

### 技能结构
- **容器管理**：run, ps, stop, rm, exec, logs
- **镜像操作**：pull, build, push, tag, rmi
- **调试**：inspect, stats, top, events

### 触发词
- docker 操作相关命令

## 本地部署

```bash
clawhub install docker-essentials
```

## 效果展示

技能提供以下能力：
- 容器生命周期管理
- 镜像构建与推送
- 日志查看与调试
- 资源监控

## 优缺点分析

| 优点 | 缺点 |
|------|------|
| 覆盖常用操作 | 不支持 Docker Compose 完整功能 |
| 作者活跃 | 缺乏 Windows 特定优化 |
| 轻量级 | |

## 平替对比

| 技能 | 特点 |
|------|------|
| docker-sandbox | 安全沙箱环境，适合运行不可信代码 |
| docker-helper | 中文支持，更丰富的高级功能 |
| docker-manager | 完整管理功能 |

## 落地过程

1. 安装：`clawhub install docker-essentials`
2. 使用示例：
   - 运行容器：`docker run -d nginx`
   - 查看日志：`docker logs <container>`
   - 交互式进入：`docker exec -it <container> sh`

**推荐安装**：本地/ECS 均可 ⭐⭐⭐⭐☆