# Docker Sandbox

> Docker 沙箱环境创建和管理

## 技能描述

Docker Sandbox 提供安全的容器化代码执行环境，用于隔离运行不受信任的代码。支持工作区挂载、网络策略配置等。

## 功能列表

- 创建隔离的 Docker 沙箱
- 工作区挂载（virtiofs）
- Docker socket 暴露配置
- 网络策略配置
- 代理环境变量设置
- 沙箱快照和模板管理
- 持久化配置

## 安装方式

```bash
clawhub install docker-sandbox
```

## 推荐安装评估

| 环境 | 推荐度 | 说明 |
|------|--------|------|
| 本地开发 | ⭐⭐⭐⭐ | 需要安全隔离时使用 |
| ECS/服务器 | ⭐⭐⭐⭐ | 运行不受信任代码时使用 |

## 安全注意事项

⚠️ **重要安全警告：**

- 挂载主机路径和暴露 Docker socket (`/run/docker.sock`) 会削弱隔离效果
- 避免挂载敏感主机路径
- 不需要时不暴露 Docker socket
- 如需更强隔离，考虑使用独立 VM

## 使用前提

- Docker CLI
- 理解容器安全机制
