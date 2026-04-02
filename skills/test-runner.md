# Test Runner - 测试运行器

## 基本信息

| 项目 | 内容 |
|------|------|
| **名称** | Test Runner |
| **Slug** | test-runner |
| **版本** | 1.0.0 |
| **作者** | cmanfre7 |
| **创建时间** | 2026-01-28 |
| **更新时间** | 2026-02-26 |

## 技能描述

Write, run, and manage unit, integration, and E2E tests across TypeScript, Python, and Swift using recommended frameworks.

测试运行器，支持为 TypeScript、Python 和 Swift 编写、运行和管理单元测试、集成测试和 E2E 测试。

## 功能列表

- 单元测试 (Unit Testing)
- 集成测试 (Integration Testing)
- E2E 测试 (End-to-End Testing)
- TypeScript 测试支持
- Python 测试支持
- Swift 测试支持

## 安装方式

```bash
# 使用 ClawHub 安装
npx clawhub@latest install test-runner

# 或全局安装 ClawHub 后安装
npm i -g clawhub
clawhub install test-runner
```

## 推荐安装评估

### 本地安装 ⭐⭐⭐⭐⭐
- 适合场景：本地开发环境、快速反馈循环
- 优势：即时测试反馈、支持 TDD
- 要求：Node.js / Python / Swift 环境

### ECS 安装 ⭐⭐⭐⭐
- 适合场景：CI/CD 流水线、自动化测试
- 优势：可集成到持续集成流程
- 要求：ECS 需配置对应语言环境

## 优缺点分析

### 优点
- 多语言支持
- 覆盖多种测试类型
- 适合主流测试框架

### 缺点
- 需要配置各语言测试环境
- 某些框架可能有依赖冲突

## 平替对比

| 技能 | 对比 |
|------|------|
| code | Code 包含完整流程，test-runner 专注测试 |
| database-operations | 专注数据库，test-runner 专注测试 |

## 落地过程

1. 准备测试环境 (Node.js/Python/Swift)
2. 安装 ClawHub: `npm i -g clawhub`
3. 安装技能: `clawhub install test-runner`
4. 根据 SKILL.md 配置测试框架
5. 开始编写和运行测试