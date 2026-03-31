# E2E Testing Patterns - 端到端测试模式

## 技能描述
使用Playwright和Cypress构建可靠、快速E2E测试套件的专家技能。涵盖关键用户旅程覆盖、脆弱测试消除和CI/CD集成，专注于浏览器测试的最佳实践和稳定测试策略。

## 功能列表
- **测试金字塔**: E2E测试定位和边界定义
- **测试策略**: 关键用户旅程覆盖、测试选择标准
- **Playwright模式**: 配置设置、页面对象模型、智能等待
- **Cypress模式**: 自定义命令、网络拦截、测试组织
- **选择器策略**: 稳定的角色、标签、文本和testid选择器
- **回归测试**: 测试行为而非实现、独立测试、确定等待
- **视觉回归测试**: 截图比较、UI状态验证
- **无障碍测试**: 可访问性验证和合规检查
- **CI/CD集成**: 并行执行、性能优化、失败处理

## 测试金字塔
```
        /\
       /E2E\         ← FEW: 仅关键路径（本技能）
      /─────\
     /Integr\        ← MORE: 组件交互、API合同
    /────────\
   /Unit Tests\      ← MANY: 快速、隔离、覆盖边缘情况
  /────────────\
```

### E2E测试适用范围
| E2E测试 ✓ | 不适合E2E测试 ✗ |
|----------|-----------------|
| 关键用户旅程（登录→仪表板→操作→登出） | 单元级逻辑（使用单元测试） |
| 多步流程（结账、入职向导） | API合同（使用集成测试） |
| 跨浏览器兼容性 | 边缘情况（太慢，使用单元测试） |
| 真实API集成 | 内部实现细节 |
| 认证流程 | 组件视觉状态（使用Storybook） |

## 核心原则
| 原则 | 原因 | 方法 |
|------|------|------|
| **测试行为，而非实现** | 适应重构 | 断言用户可见结果，而非DOM结构 |
| **独立测试** | 可并行、可调试 | 每个测试创建自己的数据，清理后 |
| **确定性等待** | 避免脆弱性 | 等待条件，而非固定超时 |
| **稳定选择器** | 适应UI变化 | 使用data-testid、角色、标签，永不使用CSS类 |
| **快速反馈** | 开发者运行 | 模拟外部服务，并行化，分片 |

## Playwright模式
```typescript
// 配置
import { defineConfig, devices } from "@playwright/test";

export default defineConfig({
  testDir: "./e2e",
  timeout: 30000,
  expect: { timeout: 5000 },
  fullyParallel: true,
  forbidOnly: !!process.env.CI,
  retries: process.env.CI ? 2 : 0,
  workers: process.env.CI ? 1 : undefined,
  projects: [
    { name: "chromium", use: { ...devices["Desktop Chrome"] } },
    { name: "firefox", use: { ...devices["Desktop Firefox"] } },
    { name: "webkit", use: { ...devices["Desktop Safari"] } },
    { name: "mobile", use: { ...devices["iPhone 13"] } },
  ],
});

// 页面对象模型
export class LoginPage {
  constructor(page: Page) {
    this.page = page;
    this.emailInput = page.getByLabel("Email");
    this.passwordInput = page.getByLabel("Password");
    this.loginButton = page.getByRole("button", { name: "Login" });
  }

  async login(email: string, password: string) {
    await this.emailInput.fill(email);
    await this.passwordInput.fill(password);
    await this.loginButton.click();
  }
}
```

## 智能等待
```typescript
// ❌ 脆弱：固定超时
await page.waitForTimeout(3000);

// ✅ 稳定：等待条件
await page.waitForLoadState("networkidle");
await page.waitForURL("/dashboard");

// ✅ 最佳：自动等待断言
await expect(page.getByText("Welcome")).toBeVisible();
await expect(page.getByRole("button", { name: "Submit" })).toBeEnabled();

// 等待API响应
const responsePromise = page.waitForResponse(
  (r) => r.url().includes("/api/users") && r.status() === 200
);
await page.getByRole("button", { name: "Load" }).click();
await responsePromise;
```

## 选择器策略
| 优先级 | 选择器类型 | 示例 | 原因 |
|--------|------------|------|------|
| 1 | **角色 + 名称** | `getByRole("button", { name: "Submit" })` | 可访问、面向用户 |
| 2 | **标签** | `getByLabel("Email address")` | 可访问、语义化 |
| 3 | **data-testid** | `getByTestId("checkout-form")` | 稳定、明确用于测试 |
| 4 | **文本内容** | `getByText("Welcome back")` | 面向用户 |
| ❌ | CSS类 | `.btn-primary` | 样式变化会破坏 |
| ❌ | DOM结构 | `div > form > input:nth-child(2)` | 任何重构都会破坏 |

## CI/CD集成
```yaml
# GitHub Actions示例
name: E2E Tests
on: [push, pull_request]

jobs:
  e2e:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-node@v4
      - run: npm ci
      - run: npx playwright install --with-deps
      - run: npm run build
      - run: npm run start & npx wait-on http://localhost:3000
      - run: npx playwright test
      - uses: actions/upload-artifact@v4
        if: failure()
        with:
          name: playwright-report
          path: playwright-report/
```

## 使用场景
- Web应用的端到端自动化测试
- 修复脆弱测试
- CI/CD测试流水线设置
- 关键用户流程测试
- 测试框架构建

## 安装方式
```bash
# 安装
npx clawhub@latest install e2e-testing-patterns

# 运行测试
npx playwright test
npx playwright test --headed
npx playwright test --trace on
```

## 推荐安装评估

### 本地部署
**适用场景**:
- 个人开发者、小型团队
- 本地开发环境
- 学习E2E测试
- 个人项目测试

**优势**:
- 快速迭代和调试
- 完全本地化，无网络依赖
- 学习成本较低
- 即时反馈

**ECS部署**
**适用场景**:
- 大型开发团队
- 多项目并行测试
- 企业级测试流水线
- CI/CD集成需求

**优势**:
- 弹性计算资源
- 统一测试环境
- 并行执行能力
- 性能监控
- 测试报告和分析

**选择建议**: 个人学习和小项目推荐本地部署，企业级项目和大规模测试选择ECS部署。