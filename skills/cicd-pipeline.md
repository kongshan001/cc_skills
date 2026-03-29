# CI/CD Pipeline

## 1. 背景需求

CI/CD 是现代开发的基础设施，但配置和维护常遇困难：
- GitHub Actions 语法复杂
- 工作流调试困难
- 缓存和优化不熟悉
- 多环境部署配置繁琐
- secrets 管理不当

需要一个 CI/CD 配置助手。

## 2. 目标

创建、调试、管理 CI/CD 流水线：
- GitHub Actions 工作流创建
- 自动化测试配置（单元、集成、E2E）
- 自动化部署（Staging/Production）
- Release 管理
- 工作流语法和最佳实践
- secrets 和变量管理
- 缓存策略和优化
- Matrix 构建
- 故障排查

## 3. 设计方案

**工作流模板**：
| 类型 | 说明 |
|------|------|
| Node.js CI | 安装、lint、测试、构建 |
| Python CI | 环境、测试、coverage |
| Docker Build & Push | 构建、推送、部署 |
| Multi-matrix | 多版本/多平台测试 |
| Deployment | Staging → Production |

**核心概念**：
- Trigger（push/PR/schedule/manual）
- Jobs 和 Steps
- 环境变量和 Secrets
- 缓存（依赖缓存）
- Matrix strategy

## 4. 本地部署

```bash
clawhub install cicd-pipeline
```

**依赖**：
- GitHub 仓库
- 适当的 GitHub 权限（Actions）

## 5. 效果展示

触发示例：
- "帮我写一个 Node.js 项目的 GitHub Actions"
- "配置自动部署到 ECS"
- "我的 CI 失败了，帮我看看日志"

执行效果：AI 生成工作流 YAML 文件或分析问题。

## 6. 优缺点分析

| 优点 | 缺点 |
|------|------|
| 覆盖常见场景模板 | 特定云平台支持有限 |
| 语法和最佳实践指导 | 生产环境需要额外安全审查 |
| 故障排查实用 | 需要了解 GitHub Actions |
| 减少配置错误 | 不是可视化工具 |

## 7. 平替对比

| 方案 | 特点 | 适用场景 |
|------|------|----------|
| CI/CD Pipeline（当前） | GitHub Actions 专注 | GitHub 项目 |
| Docker 部署技能 | 容器部署 | Docker 项目 |
| GitHub CLI | 官方工具 | 手动操作 |

## 8. 落地过程

**推荐安装评估**：
- **本地开发机** ⭐⭐⭐⭐⭐ — DevOps 开发必备
- **ECS 云服务器** ⭐⭐⭐⭐⭐ — 自动化部署

**使用建议**：
1. 生成工作流后审查再合并
2. 使用 branch protection 保护 main
3. 敏感信息用 secrets
4. 利用缓存加速构建

**版本**：1.0.0 | **作者**：gitgoodordietrying | **更新**：2026-02-25