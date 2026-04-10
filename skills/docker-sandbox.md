# Docker Sandbox

> 技能Slug: docker-sandbox  
> 版本: 1.0.0  
> 作者: gitgoodordietrying  
> 更新时间: 2026-02-28

## 技能描述

Create and manage Docker sandboxed VM environments for safe agent execution. Use when running untrusted code, exploring packages, or isolating agent workloads. Supports Claude, Codex, Copilot, Gemini, and Kiro agents with network proxy controls.

创建和管理 Docker 沙箱 VM 环境，用于安全执行不信任的代码、探索软件包或隔离 agent 工作负载。支持多种 AI 代理并提供网络代理控制。

## 功能列表

- 沙箱 VM 环境创建
- 不信任代码安全运行
- 软件包探索隔离
- 多代理支持 (Claude, Codex, Copilot, Gemini, Kiro)
- 网络代理控制

## 安装方式

```bash
# 使用 clawhub 安装
clawhub install docker-sandbox

# 或使用 npx
npx clawhub@latest install docker-sandbox
```

## 推荐安装评估

### 本地开发环境 ⚠️ 谨慎使用

- 需要 Docker 运行权限
- 适合测试不信任的代码
- 建议配合网络控制使用

### ECS/服务器 ✅ 推荐

- 生产环境安全测试
- 隔离不信任的 workloads
- 多租户场景

## 适用场景

1. 运行第三方/不信任的代码
2. 探索新软件包的安全性
3. 隔离 AI agent 的工作负载
4. 多代理并发测试环境

## 安全考虑

- 建议配置网络隔离
- 限制资源使用 (CPU/内存)
- 定期清理沙箱环境
- 监控异常行为

## 替代技能对比

| 技能 | 特点 | 适用场景 |
|------|------|----------|
| docker-sandbox | 沙箱安全隔离 | 安全测试 |
| docker-essentials | 基础命令 | 日常开发 |

## 落地建议

1. 配置资源限制防止资源耗尽
2. 设置网络策略隔离
3. 定期审计沙箱日志