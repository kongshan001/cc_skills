# Code Review - 通用代码审查技能

## 1. 背景需求

代码审查是软件质量保证的关键环节，但人工审查耗时且容易遗漏问题。开发者需要：

- 在提交代码前自动检查质量问题
- 识别潜在的 bug 和安全漏洞
- 确保代码符合项目规范
- 减少代码审查的时间和精力成本

## 2. 目标

Code Review 是一个通用的代码审查代理，专注于在代码提交或创建 PR 前进行全面的质量检查。

## 3. 设计方案

### 核心功能

| 功能 | 说明 |
|------|------|
| CLAUDE.md 合规检查 | 验证代码是否符合项目规范 |
| 风格违规检测 | 检查代码风格一致性 |
| Bug 检测 | 识别常见的编程错误 |
| 代码质量问题 | 发现代码异味和可改进点 |

### 分析维度

1. **代码风格**：缩进、命名、格式
2. **逻辑错误**：空指针、数组越界、资源泄漏
3. **安全漏洞**：SQL 注入、XSS、硬编码密码
4. **性能问题**：N+1 查询、重复计算
5. **最佳实践**：异常处理、资源管理

## 4. 本地部署

### 安装方式

```bash
/plugin install code-review
```

### 环境要求

- Claude Code 已安装
- 项目包含 CLAUDE.md（推荐）

## 5. 效果展示

### 使用示例

```
"Review my recent changes"
"Check if everything looks good"
"Review this code before I commit"
```

### 输出示例

```
📊 Code Review Results:

Critical Issues (2):
  - [bug] Potential null pointer at userService.ts:45
  - [security] Hardcoded API key at config.js:12

Warnings (5):
  - [style] Inconsistent naming: use camelCase
  - [perf] N+1 query detected at repository.ts:78
  - ...

Code Quality Score: 78/100
```

## 6. 优缺点分析

### 优点

| 优势 | 说明 |
|------|------|
| 轻量级 | 安装简单，使用方便 |
| 快速反馈 | 几乎即时返回审查结果 |
| 全面检查 | 多维度代码质量分析 |
| 无缝集成 | 融入 Claude Code 工作流 |

### 缺点

| 劣势 | 说明 |
|------|------|
| 依赖项目规范 | 需要 CLAUDE.md 才能发挥最大效果 |
| 深度有限 | 适合快速检查，不适合深入分析 |
| 误报可能 | 复杂上下文中可能有误报 |

## 7. 平替对比

| 工具 | 定位 | 优势 | 劣势 |
|------|------|------|------|
| Code Review | 快速代码审查 | 轻量、即时 | 深度有限 |
| PR Review Toolkit | 综合性PR审查 | 多代理、更全面 | 较重 |
| SonarQube | 静态分析 | 企业级、深度 | 需部署 |
| DeepCode | AI 审查 | 实时、精准 | 需付费 |

## 8. 落地过程

### 工作流集成

```bash
# 开发完成后立即使用
"Review my recent changes"

# 提交前检查
"Check if everything looks good before I commit"

# PR 创建前
"Review this code before I create a PR"
```

### 最佳实践

- 每次代码编写后使用
- 与 PR Review Toolkit 配合使用
- 重视 Critical 问题，酌情处理 Warning

---

**推荐安装方式**：本地开发环境（Desktop/Laptop）

**资源链接**：Code Quality Testing 类别 - ccplugins/awesome-claude-code-plugins
