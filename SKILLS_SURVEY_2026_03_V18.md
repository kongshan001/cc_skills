# Claude Code Skills 调研报告 - 2026年3月 (第十八轮更新)

**调研日期**: 2026-03-04  
**技能来源**: GitHub 热门仓库 + ClawHub 实时搜索 + Antigravity Awesome Skills (970+ Skills)  
**目标仓库**: https://github.com/kongshan001/cc_skills  
**状态**: ✅ 调研完成 (持续更新)

---

## 📊 调研概要

本次调研聚焦 Claude Code 热门 Skills，覆盖以下方向：
1. 游戏客户端开发 (Unity/Godot/Unreal)
2. Python 开发 (FastAPI/异步/测试)
3. 游戏客户端自动化测试 (移动端/UI 自动化)
4. 开发者工具 (浏览器自动化/GitHub 自动化/Docker)

### 数据来源

| 来源 | Skills 数量 | 说明 |
|------|-------------|------|
| Antigravity Awesome Skills | 970+ | 10+ AI 助手平台支持 |
| ClawHub Registry | 实时 | 最新热门 Skills |
| 官方 Claude Code | 50+ | 官方 Skills |

---

## 🎮 一、游戏客户端开发 Skills

### 1.1 核心 Skills 概览

| Skill 名称 | 来源 | 核心能力 | 评分/星标 |
|------------|------|---------|----------|
| game-development | antigravity | 游戏开发编排器 | 18.5K⭐ |
| openclaw-godot-skill | ClawHub | Godot 场景管理、节点操作 | **3.497** 🆕 |
| godot-dev-guide | ClawHub | Godot 4 开发指南 | **3.442** 🆕 |
| unity-developer | antigravity | Unity 6 LTS 专家 | 高 |
| unity | ClawHub | Unity 开发 | **3.030** 🆕 |
| openclaw-unreal-skill | ClawHub | Unreal 技能 | **3.376** 🆕 |
| godot-gdscript-patterns | antigravity | Godot 4 GDScript | 高 |
| godot-4-migration | antigravity | Godot 3→4 迁移 | 高 |
| unity-ecs-patterns | antigravity | Unity ECS 模式 | 高 |
| unreal-engine-cpp-pro | antigravity | UE5 C++ 开发 | 高 |
| bevy-ecs-expert | antigravity | Bevy ECS (Rust) | 中 |
| game-audio | antigravity | 游戏音频 | 中 |
| game-art | antigravity | 游戏美术管线 | 中 |
| 2d-games | antigravity | 2D 游戏开发 | 中 |
| 3d-games | antigravity | 3D 游戏开发 | 中 |
| multiplayer | antigravity | 多人游戏开发 | 中 |
| mobile-games | antigravity | 移动端游戏 | 中 |
| pc-games | antigravity | PC/主机游戏 | 中 |
| web-games | antigravity | Web 游戏 | 中 |
| vr-ar | antigravity | VR/AR 开发 | 中 |
| shader-programming-glsl | antigravity | GLSL 着色器 | 中 |

### 1.2 完整游戏开发 Skills 列表

#### Unity 相关

| Skill ID | 描述 |
|----------|------|
| unity-developer | Build Unity games with optimized C# scripts, efficient rendering |
| unity-ecs-patterns | Master Unity ECS with DOTS, Jobs, and Burst Compiler |
| unity-ai-workflow | Unity 6.2+ AI 开发工作流 (2026 新增) |

#### Godot 相关

| Skill ID | 描述 |
|----------|------|
| godot-gdscript-patterns | Godot 4 GDScript 模式 |
| godot-4-migration | Godot 3→4 迁移指南 |
| openclaw-godot-skill | Godot 场景管理、节点操作 |
| godot-dev-guide | Godot 4 开发指南 |

#### Unreal 相关

| Skill ID | 描述 |
|----------|------|
| unreal-engine-cpp-pro | Unreal Engine 5.x C++ 开发 |
| openclaw-unreal-skill | Unreal Engine 开发技能 |

#### 其他游戏引擎

| Skill ID | 描述 |
|----------|------|
| bevy-ecs-expert | Bevy ECS (Rust 游戏引擎) |

### 1.3 游戏开发核心原则

```markdown
### 1. 游戏循环 (Game Loop)
```
INPUT → UPDATE (固定时间步 50Hz) → RENDER (插值)
```

### 2. 模式选择矩阵
| 模式 | 使用场景 | 示例 |
|------|---------|------|
| **状态机** | 3-5 个离散状态 | 玩家: Idle→Walk→Jump |
| **对象池** | 频繁生成/销毁 | 子弹、粒子 |
| **ECS** | 数千相似实体 | RTS 单位 |
| **行为树** | 复杂 AI 决策 | 敌人 AI |

### 3. 性能预算 (60 FPS = 16.67ms)
| 系统 | 预算 |
|------|------|
| 输入 | 1ms |
| 物理 | 3ms |
| AI | 2ms |
| 游戏逻辑 | 4ms |
| 渲染 | 5ms |
```

### 1.4 Unity AI Workflow (2026 新增)

**项目地址**: [David-GD13/unity-ai-workflow](https://github.com/David-GD13/unity-ai-workflow)

```markdown
### Dev Modes (三种开发模式)
| 模式 | 角色 | 适用场景 |
|------|------|---------|
| Assistant | 你构建，AI 辅助文档和解释 | 学习、创意控制 |
| Mix (默认) | 协作模式，AI 建议，你确认 | 大多数项目 |
| Automatic | AI 构建，短的 onboarding Q&A | 快速原型、游戏 jam |

### 核心哲学: Game Feel 不是可选的
- 每项功能使用 /implement-feature 完整构建
- AI 在写代码前询问 VFX、SFX、相机反馈和触觉
- 迭代打磨，不是单独阶段

### 技术架构
- TCREI Prompting: Task-Context-References-Evaluate-Iterate 方法论
- 验证系统: 每个 AI 推荐标记 [VERIFIED]/[SYNTHESIZED]/[UNVERIFIED]
```

### 1.5 游戏开发 Skills 推荐安装

```bash
# 核心 Skills
clawhub install game-development
clawhub install openclaw-godot-skill
clawhub install godot-dev-guide
clawhub install unity-developer
clawhub install unity
clawhub install openclaw-unreal-skill

# 使用 Antigravity
npx antigravity-awesome-skills --claude
>> /godot-gdscript-patterns
>> /unity-developer
>> /unreal-engine-cpp-pro
```

---

## 🐍 二、Python 开发 Skills

### 2.1 核心 Skills 概览

| Skill 名称 | 来源 | 核心能力 | 评分 |
|------------|------|---------|------|
| python-executor | ClawHub | 安全沙箱执行 Python | 3.480 |
| python-dataviz | ClawHub | 数据可视化 | 3.428 |
| fastapi | ClawHub | FastAPI | 3.523 |
| lsp-python | ClawHub | LSP Python | 3.289 |
| python-script-generator | ClawHub | 脚本生成 | 3.220 |
| python-pro | antigravity | Python 3.12+ 全栈 | 高 |
| python-patterns | antigravity | Python 设计模式 | 高 |
| python-fastapi-development | antigravity | FastAPI 开发 | 高 |
| python-development-python-scaffold | antigravity | 项目脚手架 | 高 |
| python-performance-optimization | antigravity | 性能优化 | 高 |
| python-testing-patterns | antigravity | pytest 测试策略 | 高 |
| async-python-patterns | antigravity | asyncio 异步编程 | 高 |
| python-packaging | antigravity | 包发布 | 高 |
| django-pro | antigravity | Django 5.x | 高 |
| fastapi-pro | antigravity | FastAPI Pro | 高 |
| temporal-python-pro | antigravity | Temporal 工作流 | 高 |
| temporal-python-testing | antigravity | Temporal 测试 | 高 |

### 2.2 Python Skills 详细分类

#### Web 框架

| Skill ID | 描述 |
|----------|------|
| fastapi-pro | High-performance async APIs with FastAPI, SQLAlchemy 2.0 |
| fastapi | RESTful API 开发 (ClawHub) |
| fastapi-router-py | FastAPI routers with CRUD operations |
| fastapi-templates | Production-ready FastAPI 项目模板 |
| django-pro | Django 5.x with async views, DRF, Celery |
| python-fastapi-development | FastAPI 后端开发工作流 |

#### 异步编程

| Skill ID | 描述 |
|----------|------|
| async-python-patterns | Python asyncio, concurrent programming |
| temporal-python-pro | Temporal workflow orchestration |
| temporal-python-testing | Temporal workflows 测试 |

#### 测试

| Skill ID | 描述 |
|----------|------|
| python-testing-patterns | pytest, fixtures, mocking |
| temporal-python-testing | Temporal 测试模式 |

#### 性能与优化

| Skill ID | 描述 |
|----------|------|
| python-performance-optimization | cProfile, memory profiler 性能分析 |
| python-pro | Python 3.12+ 现代特性 |

#### 项目结构

| Skill ID | 描述 |
|----------|------|
| python-development-python-scaffold | 项目脚手架 |
| python-packaging | PyPI 包发布 |
| python-patterns | 开发原则和决策 |

### 2.3 Python Executor 详解 (评分: 3.480)

**来源**: ClawHub

```markdown
### 核心能力
- 安全沙箱执行
- 依赖预装: NumPy, Pandas, Matplotlib, requests, BeautifulSoup
- 数据处理和分析
- 可视化图表生成
- 文件 I/O 操作

### 适用场景
- 数据分析原型
- 快速脚本验证
- 自动化任务执行
```

### 2.4 FastAPI Skill 详解 (评分: 3.523)

**来源**: ClawHub

```markdown
### 核心能力
- RESTful API 设计
- Pydantic 数据验证
- 依赖注入
- 自动文档生成 (Swagger/ReDoc)
- 异步支持

### 适用场景
- 微服务开发
- REST API 构建
- Web 后端开发
```

### 2.5 Async Python Patterns 详解

```python
### asyncio 示例
import asyncio

async def fetch_data(url: str) -> dict:
    await asyncio.sleep(0.1)
    return {"url": url, "data": "result"}

async def fetch_all(urls: list) -> list:
    tasks = [fetch_data(url) for url in urls]
    return await asyncio.gather(*tasks)

asyncio.run(fetch_all(["url1", "url2"]))
```

### 2.6 Python 开发 Skills 推荐安装

```bash
# 核心 Skills
clawhub install python-executor
clawhub install python-dataviz
clawhub install fastapi
clawhub install python-script-generator
clawhub install lsp-python

# 使用 Antigravity
>> /python-pro
>> /python-fastapi-development
>> /async-python-patterns
>> /python-testing-patterns
```

---

## 🧪 三、自动化测试 Skills

### 3.1 核心 Skills 概览

| Skill 名称 | 来源 | 核心能力 | 评分 |
|------------|------|---------|------|
| test-runner | ClawHub | 测试运行器 | 3.639 |
| test-master | ClawHub | 测试大师 | 3.576 |
| test-patterns | ClawHub | 测试模式 | 3.548 |
| test-specialist | ClawHub | 测试专家 | 3.467 |
| test-sentinel | ClawHub | 测试哨兵 | 3.347 |
| test-case-generator | ClawHub | 测试用例生成 | 3.336 |
| playwright | ClawHub | 浏览器自动化 | 3.538 |
| playwright-mcp | ClawHub | Playwright MCP | 3.581 |
| playwright-scraper-skill | ClawHub | 网页抓取 | 3.584 |
| e2e-testing | antigravity | E2E 测试 | 高 |
| e2e-testing-patterns | antigravity | E2E 测试模式 | 高 |
| browser-automation | antigravity | 浏览器自动化 | 高 |
| testing-patterns | antigravity | Jest 测试模式 | 高 |
| test-driven-development | antigravity | TDD | 高 |
| test-automator | antigravity | AI 驱动测试自动化 | 高 |
| testing-qa | antigravity | 综合 QA 工作流 | 高 |

### 3.2 完整测试 Skills 列表

#### 测试运行器

| Skill ID | 描述 |
|----------|------|
| test-runner | 多框架测试运行器 |
| test-master | 测试策略规划 |
| test-patterns | 测试设计模式 |
| test-specialist | 测试专家 |
| test-sentinel | 测试监控 |
| test-case-generator | 测试用例生成 |

#### 浏览器自动化

| Skill ID | 评分 |
|----------|------|
| playwright-scraper-skill | 3.584 |
| playwright-mcp | 3.581 |
| playwright | 3.538 |
| playwright-browser-automation | 3.509 |

#### E2E 测试

| Skill ID | 描述 |
|----------|------|
| e2e-testing | Playwright E2E 测试工作流 |
| e2e-testing-patterns | Playwright/Cypress 测试模式 |
| browser-automation | 浏览器自动化 |

#### 移动端测试

| Skill ID | 评分 |
|----------|------|
| mobile-appium-test | 3.189 |
| android-remote-control | 3.304 |
| ios-simulator | 3.456 |
| android-studio | 3.209 |

#### TDD 和 QA

| Skill ID | 描述 |
|----------|------|
| test-driven-development | TDD 开发流程 |
| tdd-orchestrator | TDD 编排器 |
| tdd-workflow | TDD 工作流 |
| testing-qa | 综合 QA 工作流 |
| test-fixing | 测试修复 |

### 3.3 Test Runner 详解 (评分: 3.639)

**来源**: ClawHub

```markdown
### 核心能力
- 多框架支持 (pytest, Jest, Mocha)
- 并行执行
- 测试选择和过滤
- JUnit XML 报告
- HTML 报告
- CI/CD 集成

### 适用场景
- 单元测试运行
- 集成测试管理
- CI/CD 流水线集成
```

### 3.4 Playwright Skills 专题

```markdown
### 核心能力
- 浏览器自动化
- 表单填写和提交
- 页面截图
- 数据提取
- E2E 测试
- 视觉回归测试
- MCP 协议集成

### 适用场景
- 网页自动化
- 数据抓取
- E2E 测试
- 视觉回归测试
```

### 3.5 移动端自动化测试

```markdown
### Appium 测试
- Android/iOS 原生应用测试
- 混合应用测试
- 自动化测试脚本

### 设备控制
- android-remote-control: Android 远程控制
- ios-simulator: iOS 模拟器管理

### 特定场景
- 触控响应延迟测试
- 陀螺仪/重力感应测试
- 内存/电量消耗测试
```

### 3.6 自动化测试 Skills 推荐安装

```bash
# 测试运行器
clawhub install test-runner
clawhub install test-master
clawhub install test-patterns

# Playwright
clawhub install playwright
clawhub install playwright-mcp
clawhub install playwright-scraper-skill

# 移动端测试
clawhub install mobile-appium-test
clawhub install android-remote-control
clawhub install ios-simulator

# 使用 Antigravity
>> /e2e-testing-patterns
>> /test-driven-development
>> /test-automator
```

---

## 🛠️ 四、开发者工具 Skills

### 4.1 GitHub 专题

| Skill | 评分 | 说明 |
|-------|------|------|
| github | 3.790 | GitHub 基础操作 |
| openclaw-github-assistant | 3.615 🆕 | OpenClaw GitHub 助手 |
| github-cli | 3.501 | GitHub CLI |
| github-trending-cn | 3.458 | GitHub 中文趋势 |
| github-ops | 3.345 | GitHub 运维 |
| github-actions-generator | 3.238 | Actions 生成器 |
| code-review | 3.620 | 代码审查 |
| receiving-code-review | 3.570 | 接收代码审查 |
| requesting-code-review | 3.554 | 请求代码审查 |

### 4.2 Docker 专题

| Skill | 评分 | 说明 |
|-------|------|------|
| docker-essentials | 3.694 | Docker 基础 |
| docker | 3.577 | Docker 完整版 |
| docker-sandbox | 3.548 | Docker 沙箱 |
| docker-ctl | 3.531 🆕 | Docker 控制 |
| docker-compose | 3.511 | Docker Compose |
| docker-diag | 3.474 🆕 | Docker 诊断 |

### 4.3 浏览器自动化专题

| Skill | 评分 |
|-------|------|
| agent-browser | 3.772 |
| browser-automation | 3.700 |
| browser-use | 3.653 |
| fast-browser-use | 3.619 |
| stagehand-browser-cli | 3.597 |

### 4.4 安全审计 Skills

| Skill | 评分 |
|-------|------|
| security-auditor | 3.556 |
| clawdbot-security-check | 3.514 |
| security-audit-toolkit | 3.513 |
| clawdbot-security-suite | 3.452 |

### 4.5 API 开发 Skills

| Skill | 评分 |
|-------|------|
| api-gateway | 3.684 |
| secure-api-calls | 3.459 |
| fastapi | 3.523 |

### 4.6 CI/CD 专题

| Skill | 描述 |
|----------|------|
| github-workflow-automation | GitHub Actions 自动化 |
| cicd-automation-workflow-automate | CI/CD 流水线自动化 |
| changelog-automation | Changelog 自动生成 |
| circleci-automation | CircleCI 自动化 |
| bitbucket-automation | Bitbucket 自动化 |

### 4.7 开发者工具 Skills 推荐安装

```bash
# GitHub
clawhub install github
clawhub install github-cli
clawhub install code-review

# Docker
clawhub install docker-essentials
clawhub install docker-compose
clawhub install docker-ctl

# 浏览器自动化
clawhub install browser-automation
clawhub install browser-use

# 安全
clawhub install security-auditor

# 使用 Antigravity
>> /github-workflow-automation
>> /cicd-automation-workflow-automate
```

---

## 📈 Skills 评分排行榜 (Top 30)

| 排名 | Skill | 类别 | 评分 | 趋势 |
|------|-------|------|------|------|
| 1 | github | DevOps | 3.790 | - |
| 2 | agent-browser | Browser | 3.772 | - |
| 3 | browser-automation | Browser | 3.700 | 🆕 |
| 4 | automation-workflows | Automation | 3.699 | - |
| 5 | docker-essentials | DevOps | 3.694 | - |
| 6 | api-gateway | API | 3.684 | - |
| 7 | browser-use | Browser | 3.653 | 🆕 |
| 8 | test-runner | Testing | 3.639 | 🆕 |
| 9 | fast-browser-use | Browser | 3.619 | 🆕 |
| 10 | code-review | DevOps | 3.620 | 🆕 |
| 11 | openclaw-github-assistant | DevOps | 3.615 | 🆕 |
| 12 | playwright-scraper-skill | Automation | 3.584 | - |
| 13 | playwright-mcp | Automation | 3.581 | - |
| 14 | docker | DevOps | 3.577 | - |
| 15 | test-master | Testing | 3.576 | 🆕 |
| 16 | receiving-code-review | DevOps | 3.570 | 🆕 |
| 17 | docker-sandbox | DevOps | 3.548 | - |
| 18 | test-patterns | Testing | 3.548 | 🆕 |
| 19 | playwright | Automation | 3.538 | - |
| 20 | docker-ctl | DevOps | 3.531 | 🆕 |
| 21 | docker-compose | DevOps | 3.511 | - |
| 22 | playwright-browser-automation | Automation | 3.509 | - |
| 23 | docker-essentials-1-0-0 | DevOps | 3.498 | 🆕 |
| 24 | openclaw-godot-skill | Game | 3.497 | 🆕 |
| 25 | security-auditor | Security | 3.556 | 🆕 |
| 26 | godot-dev-guide | Game | 3.442 | 🆕 |
| 27 | docker-diag | DevOps | 3.474 | 🆕 |
| 28 | stagehand-browser-cli | Browser | 3.597 | 🆕 |
| 29 | requesting-code-review | DevOps | 3.554 | 🆕 |
| 30 | test-specialist | Testing | 3.467 | 🆕 |

---

## 📦 安装指南

### ClawHub 安装

```bash
# 搜索 Skills
clawhub search <keyword>

# 安装 Skills
clawhub install <skill-id>

# 示例
clawhub install python-executor
clawhub install test-runner
clawhub install playwright
```

### Antigravity 安装

```bash
# 安装所有 Skills
npx antigravity-awesome-skills --claude

# 使用特定 Skill
>> /python-pro 帮助我设计一个 FastAPI 项目
>> /game-development 创建一个 Unity 项目
>> /test-driven-development 使用 TDD 开发这个功能
```

---

## 🔗 资源链接

- [Antigravity Awesome Skills](https://github.com/sickn33/antigravity-awesome-skills)
- [ClawHub Registry](https://clawhub.com)
- [Claude Code 官方](https://github.com/anthropics/claude-code)
- [CC Skills 仓库](https://github.com/kongshan001/cc_skills)
- [Unity AI Workflow](https://github.com/David-GD13/unity-ai-workflow)

---

## 📝 附录：完整 Skills 索引

### 游戏开发 Skills 完整列表

| Category | Skill ID | Source |
|----------|----------|--------|
| Orchestrator | game-development | antigravity |
| Unity | unity-developer | antigravity |
| Unity | unity-ecs-patterns | antigravity |
| Unity | unity-ai-workflow | github |
| Godot | godot-gdscript-patterns | antigravity |
| Godot | godot-4-migration | antigravity |
| Godot | openclaw-godot-skill | ClawHub |
| Godot | godot-dev-guide | ClawHub |
| Unreal | unreal-engine-cpp-pro | antigravity |
| Unreal | openclaw-unreal-skill | ClawHub |
| Rust | bevy-ecs-expert | antigravity |
| 2D | 2d-games | antigravity |
| 3D | 3d-games | antigravity |
| Multiplayer | multiplayer | antigravity |
| Mobile | mobile-games | antigravity |
| PC | pc-games | antigravity |
| Web | web-games | antigravity |
| VR/AR | vr-ar | antigravity |
| Audio | game-audio | antigravity |
| Art | game-art | antigravity |
| Shaders | shader-programming-glsl | antigravity |

### Python Skills 完整列表

| Category | Skill ID | Source |
|----------|----------|--------|
| Core | python-pro | antigravity |
| Core | python-patterns | antigravity |
| Web | fastapi | ClawHub |
| Web | fastapi-pro | antigravity |
| Web | django-pro | antigravity |
| Async | async-python-patterns | antigravity |
| Testing | python-testing-patterns | antigravity |
| Perf | python-performance-optimization | antigravity |
| Scaffold | python-development-python-scaffold | antigravity |
| Package | python-packaging | antigravity |
| Temporal | temporal-python-pro | antigravity |
| Temporal | temporal-python-testing | antigravity |
| Executor | python-executor | ClawHub |
| Script | python-script-generator | ClawHub |

---

**文档版本**: 2026.03.04.18  
**本轮更新**: 
- 新增游戏开发 Skills 完整索引 (20+ Skills)
- 新增 Python Skills 详细分类 (14+ Skills)
- 新增测试 Skills 完整列表 (20+ Skills)
- 新增开发者工具 Skills (CI/CD, API, 安全)
- 更新 Skills 评分排行榜 Top 30
- 增加完整 Skills 索引附录

**调研完成**: ✅
