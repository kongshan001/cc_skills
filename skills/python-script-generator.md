# Python Script Generator

## 背景需求

Python 开发者经常需要快速生成项目模板（CLI 工具、Flask/FastAPI Web 应用、爬虫等），手动创建项目结构耗时且容易出错。

## 目标

一键生成专业 Python 脚本和应用模板，提升开发效率。

## 设计方案

### 支持模板类型
- CLI 工具
- Flask API
- FastAPI
- Django Command
- Scraper（爬虫）
- 完整项目代码

### 触发词
- python generator, cli, script generation

## 本地部署

```bash
clawhub install python-script-generator
```

## 效果展示

技能提供：
- 多种项目模板一键生成
- 完整项目结构（requirements.txt, setup.py）
- 最佳实践代码规范
- 中文支持

## 优缺点分析

| 优点 | 缺点 |
|------|------|
| 模板丰富 | 某些模板可能不适用于生产环境 |
| 中文界面友好 | 更新频率一般 |
| 一键生成完整代码 | |

## 平替对比

| 技能 | 特点 |
|------|------|
| python-code-guide-skill | PEP8 代码规范 |
| skill-python-env | Python 环境管理 |
| python-code-test | 测试相关 |

## 落地过程

1. 安装：`clawhub install python-script-generator`
2. 使用：描述需求，自动生成对应模板代码

**推荐安装**：本地开发环境 ⭐⭐⭐⭐☆