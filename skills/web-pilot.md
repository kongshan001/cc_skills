# Web Pilot - 网页导航技能

## 基本信息

| 项目 | 内容 |
|------|------|
| **名称** | Web Pilot |
| **Slug** | web-pilot |
| **版本** | 1.0.0 |
| **作者** | liranudi |
| **创建时间** | 2026-02-17 |
| **更新时间** | 2026-04-02 |

## 技能描述

Search the web and read page contents without API keys. Use when you need to search via DuckDuckGo/Brave/Google (multi-page), extract readable text from URLs...

网页导航技能，无需 API 密钥即可搜索网页并读取页面内容。支持 DuckDuckGo/Brave/Google 搜索。

## 功能列表

- 网页搜索 (DuckDuckGo/Brave/Google)
- 网页内容提取
- 多页面搜索
- 无需 API 密钥

## 安装方式

```bash
# 使用 ClawHub 安装
npx clawhub@latest install web-pilot

# 或全局安装 ClawHub 后安装
npm i -g clawhub
clawhub install web-pilot
```

## 推荐安装评估

### 本地安装 ⭐⭐⭐⭐
- 适合场景：本地研究、信息收集
- 优势：无需 API 成本、灵活搜索
- 要求：网络访问

### ECS 安装 ⭐⭐⭐⭐⭐
- 适合场景：服务器端数据抓取、研究自动化
- 优势：可定时任务、批量处理
- 要求：ECS 有网络访问

## 优缺点分析

### 优点
- 无需 API 密钥
- 多搜索引擎支持
- 免费使用

### 缺点
- 可能受搜索引擎限制
- 稳定性依赖第三方服务

## 平替对比

| 技能 | 对比 |
|------|------|
| web_search | 需要 Brave API，web-pilot 无需密钥 |

## 落地过程

1. 安装 ClawHub: `npm i -g clawhub`
2. 安装技能: `clawhub install web-pilot`
3. 根据 SKILL.md 配置搜索引擎
4. 开始搜索和抓取任务