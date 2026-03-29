# Python Script Generator

## 1. 背景需求

Python 是最流行的脚本语言之一，但从头创建项目常常耗时：
- 每次都要写重复的目录结构和配置文件
- 不同类型项目（CLI/API/Web）需要不同模板
- 新人不知道最佳实践

需要一个能根据需求一键生成完整项目代码的工具。

## 2. 目标

生成专业的 Python 脚本和应用模板：
- CLI 工具（命令行参数解析、帮助信息）
- Flask API 服务
- FastAPI REST API
- Django Management Command
- Web Scraper
- 脚本模板（logging、异常处理、配置管理）

一键生成包含完整项目结构的代码。

## 3. 设计方案

**生成器类型**：
| 类型 | 说明 |
|------|------|
| CLI 工具 | argparse/click, 入口脚本, 依赖管理 |
| Flask API | 路由、蓝图、错误处理、测试 |
| FastAPI | Pydantic 模型、依赖注入、自动文档 |
| Django Command | Management commands 模板 |
| Scraper | requests/BeautifulSoup, 异常处理 |

**输出内容**：
- 完整目录结构
- requirements.txt / pyproject.toml
- 主程序文件
- 配置管理（.env）
- 基础测试文件

## 4. 本地部署

```bash
clawhub install python-script-generator
```

**依赖**：
- Python 3.8+
- pip / uv / poetry（按需）

**验证**：
```bash
python --version
```

## 5. 效果展示

触发示例：
- "生成一个 CLI 工具，处理 CSV 文件"
- "帮我写一个 FastAPI 项目，包含用户认证"
- "创建一个爬虫，抓取某网站内容"

执行效果：AI 生成完整项目代码，可直接运行。

## 6. 优缺点分析

| 优点 | 缺点 |
|------|------|
| 快速启动新项目 | 生成代码需要审查 |
| 项目结构规范 | 复杂项目支持有限 |
| 减少重复劳动 | 不包含业务逻辑 |
| 支持多种类型 | 依赖版本可能过时 |

## 7. 平替对比

| 方案 | 特点 | 适用场景 |
|------|------|----------|
| Python Script Generator（当前） | AI 生成，灵活 | 需要定制时 |
| Cookiecutter | 固定模板 | 标准化项目 |
| 直接手写 | 无抽象 | 简单脚本 |

## 8. 落地过程

**推荐安装评估**：
- **本地开发机** ⭐⭐⭐⭐⭐ — Python 开发必备
- **ECS 云服务器** ⭐⭐⭐⭐ — 运维脚本快速生成

**使用建议**：
1. 生成后检查代码再使用
2. 补充业务逻辑
3. 添加测试覆盖

**版本**：1.0.0 | **作者**：sunshine-del-ux | **更新**：2026-03-29 | **标签**：cli, generator, python, script