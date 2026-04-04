# Docker Helper

## 背景需求

Docker 使用中常见需求：生成 Dockerfile、编写 docker-compose、命令速查、调试排错、镜像优化、仓库配置。开发者需要统一入口处理这些任务。

## 目标

提供完整的 Docker 辅助功能，包括构建、编排、调试、优化。

## 设计方案

### 核心功能
- Dockerfile 生成
- docker-compose 编排
- 命令速查
- 调试排错
- 镜像优化
- 仓库配置

### 特色
- 中文支持
- 版本：2.0.0
- 标签：productivity

## 本地部署

```bash
clawhub install docker-helper
```

## 效果展示

技能提供：
- Dockerfile 模板生成
- Compose 文件编写
- 常见问题诊断
- 镜像大小优化建议
- 镜像仓库配置

## 优缺点分析

| 优点 | 缺点 |
|------|------|
| 功能全面 | 特定场景可能不适用 |
| 中文界面 | 文档可更丰富 |
| 版本活跃 | |

## 平替对比

| 技能 | 特点 |
|------|------|
| docker-essentials | 基础 Docker 操作 |
| docker-sandbox | 安全沙箱 |
| docker-manager | 完整管理 |

## 落地过程

1. 安装：`clawhub install docker-helper`
2. 使用：描述 Docker 需求，获取对应辅助

**推荐安装**：本地/ECS 均可 ⭐⭐⭐⭐⭐