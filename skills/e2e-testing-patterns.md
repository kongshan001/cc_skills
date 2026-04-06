# E2E Testing Patterns

> 使用 Playwright 和 Cypress 构建可靠、快速的端到端测试套件

## 基本信息

| 属性 | 值 |
|------|-----|
| **Slug** | `e2e-testing-patterns` |
| **作者** | wpank |
| **版本** | 1.0.0 |
| **更新时间** | 2026-02-26 |
| **标签** | e2e, testing, playwright, cypress, automation |

## 功能列表

### 测试策略
- 测试金字塔模型
- 关键用户旅程覆盖
- 消除 flaky 测试

### Playwright 模式
- Page Object Model
- Fixtures 测试数据
- 智能等待 (条件等待)
- 网络 mocking
- 视觉回归测试

### Cypress 模式
- Custom Commands
- Network Intercepts

### 最佳实践
- 选择器策略 (role > label > testid)
- CI/CD 集成
- 可访问性测试
- 调试技巧

## 安装方式

### OpenClaw/Moltbot/Clawbot
```bash
npx clawhub@latest install e2e-testing-patterns
```

### Playwright
```bash
npm init playwright@latest
# 或
npm install -D @playwright/test
npx playwright install --with-deps
```

### Cypress
```bash
npm install -D cypress
```

## 推荐安装评估

### 本地环境 ⭐⭐⭐⭐⭐
- 开发时运行测试
- 本地调试失败测试

### ECS 环境 ⭐⭐⭐⭐⭐
- CI/CD 自动化
- 定时测试任务

## 核心原则

| 原则 | 说明 |
|------|------|
| 测试行为，非实现 | 断言用户可见结果 |
| 独立测试 | 可并行、可调试 |
| 确定性等待 | 等待条件，非固定时间 |
| 稳定选择器 | 使用 data-testid/role |

## 选择器优先级

| 优先级 | 类型 | 示例 |
|--------|------|------|
| 1 | Role + name | `getByRole("button", { name: "Submit" })` |
| 2 | Label | `getByLabel("Email")` |
| 3 | data-testid | `getByTestId("checkout-form")` |
| ❌ | CSS classes | `.btn-primary` |
| ❌ | DOM 结构 | `div > form > input:nth-child(2)` |

## Playwright 配置示例

```typescript
// playwright.config.ts
export default defineConfig({
  testDir: "./e2e",
  timeout: 30000,
  fullyParallel: true,
  retries: process.env.CI ? 2 : 0,
  use: {
    baseURL: "http://localhost:3000",
    trace: "on-first-retry",
    screenshot: "only-on-failure",
  },
  projects: [
    { name: "chromium", use: { ...devices["Desktop Chrome"] } },
    { name: "firefox", use: { ...devices["Desktop Firefox"] } },
  ],
});
```

## CI/CD 集成示例

```yaml
# GitHub Actions
name: E2E Tests
on: [push, pull_request]
jobs:
  e2e:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - run: npm ci
      - run: npx playwright install --with-deps
      - run: npm run build
      - run: npm run start & npx wait-on http://localhost:3000
      - run: npx playwright test
```

## 优缺点分析

### ✅ 优点
- 完整的测试模式
- CI/CD 集成示例
- 消除 flaky 测试指南

### ⚠️ 局限
- 需要项目基础
- 学习曲线

## 替代方案

| 方案 | 特点 |
|------|------|
| Selenium | 更老牌，浏览器支持广 |
| Puppeteer | 轻量，仅 Chrome |
| Cypress | 更易上手，生态完整 |