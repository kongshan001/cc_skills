# Playwright Browser Automation

## 1. 背景需求

浏览器自动化是 AI 代理的重要能力，用于：
- 网页数据采集和爬虫
- 表单自动填写和提交
- 页面截图和 PDF 生成
- 复杂交互流程自动化

相比 MCP 方案，直接使用 Playwright API 更可靠。

## 2. 目标

提供完整的 Playwright 浏览器自动化能力：
- 页面导航和交互
- 元素定位和操作
- 数据提取（文本、结构化数据）
- 截图和 PDF 生成
- 视频录制复杂流程
- 跨浏览器支持（Chromium/Firefox/WebKit）

## 3. 设计方案

**核心能力**：
- 智能元素定位（CSS/XPath/ARIA/text）
- 等待策略（条件等待、软等待）
- 网络拦截和模拟
- 下载和文件处理
- 浏览器上下文隔离
- 无头和有头模式切换

**超越 MCP 的优势**：
- 完整的异步控制
- 更可靠的操作保证
- 灵活的配置选项

## 4. 本地部署

```bash
clawhub install playwright-browser-automation
```

**依赖**：
- Node.js 18+
- Playwright

**验证**：
```bash
npx playwright install chromium
npx playwright --version
```

## 5. 效果展示

触发示例：
- "帮我爬取这个网站的产品列表"
- "自动填写并提交这个表单"
- "截取这个页面的全屏截图"

执行效果：AI 生成并执行 Playwright 脚本，返回数据或截图。

## 6. 优缺点分析

| 优点 | 缺点 |
|------|------|
| 比 MCP 更可靠 | 需要编程知识 |
| 完整浏览器控制 | 需要维护脚本 |
| 支持截图/视频/PDF | 反爬检测需要额外处理 |
| 多浏览器支持 | 资源消耗较高 |

## 7. 平替对比

| 方案 | 特点 | 适用场景 |
|------|------|----------|
| Playwright Browser Automation（当前） | API 级，完整控制 | 复杂自动化 |
| Playwright Skill | 基础封装 | 简单操作 |
| Computer Use Skill | 远程代理 | 自然语言控制 |
| Web Scraper MCP | 即插即用 | 简单爬虫 |

## 8. 落地过程

**推荐安装评估**：
- **本地开发机** ⭐⭐⭐⭐⭐ — 数据采集必备
- **ECS 云服务器** ⭐⭐⭐⭐ — 自动化任务

**使用建议**：
1. 从简单任务开始（截图、导航）
2. 善用等待策略避免 flaky
3. 使用浏览器上下文隔离会话

**版本**：2.0.0 | **作者**：spiceman161 | **更新**：2026-03-29