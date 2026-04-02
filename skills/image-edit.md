# Image Edit - 图片编辑技能

## 基本信息

| 项目 | 内容 |
|------|------|
| **名称** | Image Edit |
| **Slug** | image-edit |
| **版本** | 1.0.0 |
| **作者** | ivangdavila |
| **创建时间** | 2026-02-12 |
| **更新时间** | 2026-02-26 |

## 技能描述

Edit images with AI inpainting, outpainting, background removal, upscaling, and restoration tools.

图片编辑技能，使用 AI 进行图像修复、扩展、背景去除、放大和修复。

## 功能列表

- AI 图像修复 (Inpainting)
- AI 图像扩展 (Outpainting)
- 背景去除 (Background Removal)
- 图像放大 (Upscaling)
- 图像修复 (Restoration)

## 安装方式

```bash
# 使用 ClawHub 安装
npx clawhub@latest install image-edit

# 或全局安装 ClawHub 后安装
npm i -g clawhub
clawhub install image-edit
```

## 推荐安装评估

### 本地安装 ⭐⭐⭐⭐
- 适合场景：本地图像处理、快速原型
- 优势：保护隐私、无需上传
- 要求： Node.js 环境

### ECS 安装 ⭐⭐⭐⭐⭐
- 适合场景：批量图像处理服务
- 优势：可构建图像处理 API
- 要求：ECS 实例

## 优缺点分析

### 优点
- 多种 AI 图像处理能力
- 无需专业图像处理技能
- 适合设计师和开发者

### 缺点
- 需要 AI API 支持
- 处理大图可能有延迟

## 平替对比

| 技能 | 对比 |
|------|------|
| image-generation | image-generation 专注生成，image-edit 专注编辑 |

## 落地过程

1. 安装 ClawHub: `npm i -g clawhub`
2. 安装技能: `clawhub install image-edit`
3. 配置 AI API (如 OpenAI)
4. 开始图像编辑任务