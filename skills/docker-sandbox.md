# Docker Sandbox

## 技能描述

Create and manage Docker sandboxed VM environments for safe agent execution. Use when running untrusted code, exploring packages, or isolating agent workloads. Supports Claude, Codex, Copilot, Gemini, and Kiro agents with network proxy controls.

**所有者**: gitgoodordietrying  
**创建时间**: 2026-02-03  
**最新版本**: 1.0.0  
**ClawHub Slug**: `docker-sandbox`

## 功能列表

- 创建隔离的 Docker 沙箱环境
- 支持多种 AI 代理（Claude, Codex, Copilot, Gemini, Kiro）
- 运行不受信任代码的安全环境
- 包管理和探索
- 网络代理控制
- 工作负载隔离

## 安装方式

```bash
clawhub install docker-sandbox
```

或指定版本：

```bash
clawhub install docker-sandbox --version 1.0.0
```

## 推荐安装评估

### 本地环境
- ⚠️ **谨慎使用** - 需要 Docker 和较高系统资源
- 适合需要安全执行外部代码的场景
- 建议至少 8GB 内存

### ECS/云服务器
- ✅ **强烈推荐** - 生产环境安全隔离的最佳选择
- 适合运行不受信任的 AI 代理
- 需要配置网络代理规则
- 推荐至少 4 核 CPU + 8GB 内存

## 使用场景

1. 安全执行外部 AI 代理代码
2. 测试和探索新包
3. 隔离不同工作负载
4. 多租户环境隔离
5. CI/CD 流水线中的安全执行

## 安全特性

- 完全隔离的虚拟机环境
- 网络代理控制
- 资源限制
- 自动清理机制

## 相关技能

- docker-essentials - Docker 基础
- docker-compose - 多容器编排
- docker-diag - Docker 诊断

## 来源

- **ClawHub**: https://clawhub.com/skills/docker-sandbox
- **搜索分数**: 3.563（Docker 类别第二高分）
