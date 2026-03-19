# Playwright (Automation + MCP + Scraper)

> 浏览器自动化、Playwright 测试编写、MCP 驱动浏览器控制和结构化数据提取

## 📋 基本信息

| 项目 | 内容 |
|------|------|
| **技能名称** | playwright |
| **版本** | 1.0.0+ |
| **作者** | ivangdavila |
| **评分** | ⭐ 3.0 |

## 🎯 技能描述

Playwright 技能提供完整的浏览器自动化解决方案，支持真实浏览器任务：JS 渲染页面、多步表单、截图/PDF、UI 调试、Playwright 测试编写、MCP 驱动的浏览器控制和结构化数据提取。

## 🛠️ 功能列表

### 1. MCP 浏览器控制
- `browser_navigate` - 打开页面
- `browser_click` - 点击交互
- `browser_press` - 键盘操作
- `browser_type` - 文本输入
- `browser_select_option` - 下拉选择
- `browser_snapshot` - 页面快照
- `browser_evaluate` - JavaScript 执行
- `browser_choose_file` - 文件上传

### 2. 浏览器结果捕获
- 截图 (PNG/JPEG)
- PDF 生成
- 文件下载
- Trace 录制

### 3. 测试编写
- 测试生成 (`codegen`)
- 测试运行
- 调试模式
- Trace 查看

### 4. 爬虫功能
- 渲染页面提取
- 分页处理
- 礼貌限速
- 反爬虫应对

## 📦 安装方式

```bash
# 使用 ClawHub 安装
clawhub install playwright

# 安装 Playwright
npm install -D @playwright/test
npx playwright install chromium

# 或使用 MCP 模式
npx @playwright/mcp --headless
```

## 🔧 配置要求

### 快速开始 - MCP 路径
```bash
npx @playwright/mcp --headless
```

### 直接脚本路径
```javascript
const { chromium } = require('playwright');

(async () => {
  const browser = await chromium.launch({ headless: true });
  const page = await browser.newPage();
  await page.goto('https://example.com');
  await page.screenshot({ path: 'page.png', fullPage: true });
  await browser.close();
})();
```

### 浏览器选项
- `--headless` - 无头模式
- `--headed` - 有头模式 (调试)
- `--trace on` - 录制 Trace

## 📊 推荐安装评估

| 场景 | 推荐度 | 说明 |
|------|--------|------|
| **本地安装** | ⭐⭐⭐⭐⭐ | 强烈推荐，浏览器自动化必备 |
| **ECS 安装** | ⭐⭐⭐ | 一般，需要显示器环境 |

### 评分理由

- ✅ 功能全面的浏览器自动化
- ✅ 支持 MCP 工具集成
- ✅ 测试编写能力强大
- ⚠️ ECS 环境需要 xvfb 虚拟显示
- ⚠️ 需要 Playwright 依赖

## 🎯 场景选择指南

| 场景 | 推荐方案 | 原因 |
|------|----------|------|
| 静态 HTML 简单抓取 | Web Fetch | 更快更轻量 |
| JS 渲染页面 | Playwright MCP | 完整浏览器支持 |
| 多步表单 | Playwright 脚本 | 可重复执行 |
| UI 调试/测试 | Playwright --headed | 可视化调试 |
| 结构化提取 | Playwright + 等待 | DOM 状态等待 |

## 📚 参考文档

| 主题 | 文件 |
|------|------|
| 选择器策略和 frame 处理 | `selectors.md` |
| 失败分析、traces、调试 | `debugging.md` |
| 测试架构、mock、认证、断言 | `testing.md` |
| CI/CD、 retries、 artifacts | `ci-cd.md` |
| 渲染页面提取、分页 | `scraping.md` |

## 💡 最佳实践

1. **优先简单方案**: 能用静态 fetch 就不用浏览器
2. **保持认证临时**: 不需要持久化除非明确需要
3. **最小化引用**: 只加载任务所需的最少引用文件
4. **使用 trace 调试**: 失败时启用 trace 便于分析

---

*本报告由 OpenClaw 自动生成，更新时间: 2026-03-17*
