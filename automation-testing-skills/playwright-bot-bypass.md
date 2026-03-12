# Playwright Bot Bypass - 机器人检测绕过工具

> 使用 rebrowser-playwright 和 undetected-chromedriver 绕过网站检测

## 1. Skill 背景需求

在使用 Playwright 进行网页自动化时，许多网站会检测并阻止机器人访问。标准 Playwright 会暴露 `navigator.webdriver = true`，使用户无法进行 Google 搜索、Twitter 抓取等操作。

## 2. 目标

- 绕过 bot.sannysoft.com 等检测工具
- 实现 Google 搜索无验证码
- 支持 Twitter/X 免登录抓取
- 提供真实 GPU 指纹

## 3. 设计方案

### 技术方案

| 方案 | 环境 | 效果 |
|------|------|------|
| rebrowser-playwright | Node.js | ✅ 通过检测 + Google 可用 |
| undetected-chromedriver | Python | ✅ 通过检测 + Google 可用 |
| playwright-stealth | Python | ✅ 通过检测 + ❌ Google 不可用 |

### 核心修改

```javascript
// 移除 WebDriver 属性
await context.addInitScript(() => {
  delete Object.getPrototypeOf(navigator).webdriver;
});
```

### 检测对比

| 检测点 | 标准 Playwright | 本方案 |
|--------|----------------|--------|
| WebDriver | navigator.webdriver = true | 已移除 |
| WebGL Renderer | SwiftShader (软件) | 真实 GPU |
| User Agent | HeadlessChrome | 正常 Chrome |

## 4. 本地部署

### Node.js (rebrowser-playwright)

```bash
npm install rebrowser-playwright

# 使用
import { chromium } from 'rebrowser-playwright';

const browser = await chromium.launch({
  headless: false,
  channel: 'chrome'
});

const context = await browser.newContext();
await context.addInitScript(() => {
  delete Object.getPrototypeOf(navigator).webdriver;
});

const page = await context.newPage();
await page.goto('https://google.com');
```

### Python (undetected-chromedriver)

```bash
pip install undetected-chromedriver

# 使用
import undetected_chromedriver as uc

driver = uc.Chrome(version_main=133)
driver.get('https://google.com')
```

## 5. 效果展示

### 测试结果

| 环境 | bot.sannysoft.com | Google 搜索 | Twitter 抓取 |
|------|-------------------|-------------|--------------|
| 标准 Playwright | ❌ 检测到 | ❌ 验证码 | ❌ 阻止 |
| rebrowser-playwright | ✅ 通过 | ✅ 可用 | ✅ 可用 |
| playwright-stealth | ✅ 通过 | ❌ 验证码 | ❌ 阻止 |
| undetected-chromedriver | ✅ 通过 | ✅ 可用 | ✅ 可用 |

### 使用场景

- Google 搜索自动化
- Twitter/X 资料抓取
- 价格监控
- 新闻聚合
- 数据采集

## 6. 优缺点分析

### 优点

- ✅ 完整绕过检测
- ✅ 真实 GPU 指纹
- ✅ 支持 Node.js 和 Python
- ✅ 附带示例脚本

### 缺点

- ⚠️ 可能违反网站服务条款
- ⚠️ 部分网站可能检测更严格
- ⚠️ 需要维护 Chrome 版本

## 7. 平替对比

| 方案 | 绕过能力 | 易用性 | 维护成本 |
|------|---------|--------|---------|
| playwright-bot-bypass | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | 中 |
| 标准 Playwright + stealth | ⭐⭐⭐ | ⭐⭐⭐ | 低 |
| Puppeteer Extra + Stealth | ⭐⭐⭐⭐ | ⭐⭐⭐ | 中 |

## 8. 落地过程

### 实践记录

1. **安装测试**：安装 rebrowser-playwright
2. **检测测试**：运行 `bot-detection-test.mjs`，成功通过
3. **Google 测试**：搜索关键词，无需验证码
4. **Twitter 测试**：成功抓取公开账号信息

### 适用场景

- 合法的数据采集
- 自动化测试
- 搜索监控
- 价格追踪

### 道德提示

> 请确保使用本工具时遵守网站的服务条款，仅用于合法目的。

---

**状态**: ✅ 已调研  
**仓库**: https://github.com/greekr4/playwright-bot-bypass  
**评分**: ⭐⭐⭐⭐ 自动化测试必备
