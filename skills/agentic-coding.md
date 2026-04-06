# Agentic Coding

> 通过验收合约、微分diff、红绿循环和确定性交接点交付生产代码

## 基本信息

| 属性 | 值 |
|------|-----|
| **Slug** | `agentic-coding` |
| **作者** | ivangdavila |
| **版本** | 1.0.0 |
| **更新时间** | 2026-02-27 |
| **标签** | coding, workflow, contract, production |

## 功能列表

### PACT 协议
- **P**roblem framing - 问题定义
- **A**cceptance design - 验收设计
- **C**hange set - 变更集
- **T**race and test - 追踪测试

### 核心规则
- 编写代码前先锁定合约
- 保持 diff 精确
- 先证明失败再证明修复
- 交付交接级别的输出
- 升级时有结构化后备方案

### 记忆系统
- `~/agentic-coding/memory.md` - 持久化偏好
- `~/agentic-coding/contracts.md` - 任务合约
- `~/agentic-coding/evidence.md` - 测试证据
- `~/agentic-coding/handoffs.md` - 交付笔记

## 安装方式

### 初始化
```bash
# 创建工作目录
mkdir -p ~/agentic-coding
```

### 使用流程
1. 阅读 setup.md 获取设置指导
2. 创建 memory.md 配置文件
3. 使用 prompt-contracts.md 创建任务合约
4. 按 PACT 循环执行任务

## 推荐安装评估

### 本地环境 ⭐⭐⭐⭐⭐
- 适合个人开发工作流
- 适合代码质量要求高的项目

### ECS 环境 ⭐⭐⭐
- 需要持久化存储
- 团队协作场景更佳

## 适用场景

- 生产功能开发
- 高风险重构
- 可重现失败的 bug 修复
- iOS/macOS 发布分支热修复

## 核心原则

| 原则 | 说明 |
|------|------|
| 合约先行 | 无合约，不写代码 |
| 最小 diff | 一个目标对应一个变更集 |
| 证据驱动 | 先证失败，再证修复 |
| 交接级别 | 输出清晰、可回滚 |

## 优缺点分析

### ✅ 优点
- 结构化开发流程
- 质量门禁明确
- 可追溯的交付物

### ⚠️ 局限
- 需要纪律性
- 学习曲线较陡

## 相关技能

- `agentic-engineering` - 多代理协作
- `vibe-coding` - 快速原型
- `coding` - 通用编码支持