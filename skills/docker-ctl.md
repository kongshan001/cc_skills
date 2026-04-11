# Docker Ctl

## 技能概述

**Slug**: `docker-ctl`  
**作者**: xejrax  
**版本**: 1.0.0  
**更新日期**: 2026-02-28

## 背景需求

Inspect containers, logs, and images via podman.

## 功能列表

1. 容器检查
2. 日志查看
3. 镜像管理（通过 Podman）

## 安装方式

```bash
clawhub install docker-ctl
```

## 推荐安装评估

| 场景 | 推荐程度 | 说明 |
|------|----------|------|
| 本地开发 | ⭐⭐⭐⭐ | 需 Podman 环境 |
| ECS 服务器 | ⭐⭐⭐⭐ | 容器管理能力 |

## 优缺点分析

**优点**:
- 支持 Podman（无守护进程）
- 轻量级

**缺点**:
- 需要 Podman 而非 Docker