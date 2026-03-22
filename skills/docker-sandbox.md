# Docker Sandbox

## 技能概述

- **技能名称**: Docker Sandbox
- **Slug**: docker-sandbox
- **版本**: 1.0.0
- **作者**: gitgoodordietrying
- **创建时间**: 2026-02-03
- **更新时间**: 2026-02-28

## 背景需求

在 AI 助手中运行不受信任的代码、探索新包或隔离工作负载存在安全风险。开发者需要一个安全的沙箱环境来执行这些操作。

## 目标

为 AI 助手创建和管理 Docker 沙箱 VM 环境，提供安全的代码执行隔离环境。

## 功能列表

1. **沙箱环境创建** - 创建隔离的 Docker 容器
2. **安全执行** - 运行不受信任的代码
3. **包探索** - 安全地探索和测试新包
4. **工作负载隔离** - 隔离 AI 助手的工作负载
5. **多代理支持** - 支持 Claude、Codex、Copilot、Gemini、Kiro
6. **网络控制** - 代理网络控制

## 安装方式

```bash
# 确保 Docker 已安装
apt-get install docker.io

# 安装技能
clawhub install docker-sandbox
```

## 推荐安装评估

- **本地开发**: ⭐⭐⭐⭐⭐ 安全测试必备
- **ECS 服务器**: ⭐⭐⭐⭐⭐ 生产环境安全测试

## 优缺点分析

### 优点
- 提供安全的隔离环境
- 支持多种 AI 代理
- 适合运行不受信任的代码

### 缺点
- 需要 Docker 知识
- 资源消耗较高

## 平替对比

| 技能 | 评分 | 特点 |
|------|------|------|
| docker-essentials | 3.721 | 更侧重基础命令 |
| docker-ctl | 3.550 | 更侧重控制操作 |
| docker-skill | 3.397 | 更通用的 Docker 技能 |

## 落地过程

1. 确保 Docker 已安装并运行
2. 安装技能: `clawhub install docker-sandbox`
3. 配置沙箱环境参数
4. 开始安全执行代码
