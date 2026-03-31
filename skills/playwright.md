# Playwright - 浏览器自动化技能

## 技能描述
通过Playwright MCP实现浏览器自动化技能。支持导航网站、点击元素、填写表单、截图、提取数据和调试真实浏览器工作流。适用于需要真实浏览器而非静态fetch的任务，包括Playwright测试、脚本编写和JS渲染页面处理。

## 功能列表
- **MCP浏览器控制**: browser_navigate、browser_click、browser_press
- **表单交互**: browser_type、browser_select_option、browser_choose_file
- **页面检查**: browser_snapshot、browser_evaluate、DOM状态查看
- **内容捕获**: screenshot、PDF生成、trace查看、下载功能
- **自动化脚本**: 直接Playwright API编写测试和脚本
- **测试架构**: 测试套件设计、断言编写、CI/CD集成
- **调试工具**: headed模式、trace、console和网络检查
- **选择器策略**: 稳定的角色、标签、文本和testid选择器

## 使用场景
- **真实浏览器任务**: JS渲染页面、多步表单、截图/PDF/下载
- **Playwright测试**: 测试作者、调试、重现、截图
- **MCP控制**: 现有浏览器工具、无代码浏览器控制
- **页面提取**: 渲染页面提取、结构化数据获取

## 架构选择
| 情况 | 最佳路径 | 原因 |
|------|----------|------|
| 静态HTML足够 | 廉价fetch路径 | 更快、更便宜、更少脆弱 |
| 选择器原型需求 | codegen或headed探索 | 比猜测选择器更快 |
| 本地应用或E2E套件 | @playwright/test | 最适合重复测试 |
| 一次性浏览器自动化 | 直接Playwright API | 简单、明确、易调试 |
| 现有工具依赖 | Playwright MCP | 最快路径 |
| CI失败或漂移 | 调试模式和traces | 跟踪和工件更重要 |

## 快速开始
```bash
# MCP浏览器路径
npx @playwright/mcp --headless

# 现有测试套件
npx playwright test
npx playwright test --headed
npx playwright test --trace on

# 选择器生成
npx playwright codegen https://example.com

# 直接脚本
const { chromium } = require('playwright');
(async () => {
  const browser = await chromium.launch({ headless: true });
  const page = await browser.newPage();
  await page.goto('https://example.com');
  await page.screenshot({ path: 'page.png', fullPage: true });
  await browser.close();
})();
```

## 核心规则
1. **测试用户可见行为**: 测试真实浏览器边界，不花费在单元或API测试能覆盖的细节
2. **隔离运行**: 测试和脚本独立，重试、并行和重播不继承隐藏状态
3. **行动前侦察**: 先打开、等待和检查渲染状态，锁定选择器和断言
4. **弹性定位器**: 使用角色、标签、文本、alt文本、标题或testid优先于CSS或XPath
5. **等待行动性**: 让Playwright的动作检查为您工作，然后到达睡眠或强制操作

## 推荐安装评估

### 本地部署
**适用场景**:
- 个人开发者、小型团队
- 本地开发环境
- 个人项目测试
- 学习浏览器自动化

**优势**:
- 即时反馈，低延迟
- 完全本地化，无网络依赖
- 开发环境配置简单
- 快速迭代和调试
- 学习成本低

**ECS部署**
**适用场景**:
- 大型开发团队
- CI/CD测试流水线
- 多项目并行测试
- 企业级自动化测试

**优势**:
- 弹性扩展资源
- 统一测试环境
- 团队协作功能
- 集成CI/CD流程
- 性能监控
- 测试报告和统计

**选择建议**: 个人开发和本地测试推荐本地部署，团队协作和企业级测试选择ECS部署。