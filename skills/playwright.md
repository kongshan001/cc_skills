# Playwright (Automation + MCP + Scraper)

## 技能描述

Playwright 是由 ivangdavila 开发的浏览器自动化技能，提供通过 Playwright MCP 进行网站导航、元素点击、表单填写、截图、数据提取和调试真实浏览器工作流程的能力。

## 功能列表

### 核心功能
- **浏览器导航**: 使用 browser_navigate 打开页面
- **元素交互**: browser_click, browser_press, browser_type, browser_select_option
- **数据提取**: browser_snapshot, browser_evaluate 用于检查和提取
- **文件操作**: browser_choose_file 处理文件上传
- **证据捕获**: screenshot, PDF, trace, download 捕获

### 测试功能
- `npx playwright test` - 运行测试套件
- `npx playwright test --headed` - 有头模式运行
- `npx playwright test --trace on` - 启用跟踪
- `npx playwright codegen` - Bootstrap 选择器和流程

### MCP 路径
- `npx @playwright/mcp --headless` - MCP 浏览器控制

## 安装方式

```bash
# 使用 ClawHub 安装
clawhub install playwright
```

## 推荐安装评估

| 场景 | 推荐 | 说明 |
|------|------|------|
| 本地开发 | ✅ 推荐 | 适合本地 E2E 测试、调试、截图 |
| ECS/服务器 | ⚠️ 谨慎 | 需要图形环境(Xvfb)，资源消耗较高 |

### 本地部署优势
- 完整的浏览器环境支持
- 适合开发调试
- 快速反馈循环

### ECS 部署注意事项
- 需要安装 xvfb 和浏览器依赖
- 内存和 CPU 需求较高
- 建议使用 Docker 容器化部署
