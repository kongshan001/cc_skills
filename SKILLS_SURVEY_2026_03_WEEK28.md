# Claude Code Skills 完整调研报告（第二十八周）

**调研日期**: 2026-03-04

**技能来源**: GitHub 热门仓库 + ClawHub 实时搜索 + skills.sh 官方排行榜 + Antigravity Awesome Skills

**目标仓库**: [https://github.com/kongshan001/cc_skills](https://github.com/kongshan001/cc_skills)

---

## 📋 目录

1. [执行摘要](#执行摘要)
2. [游戏客户端开发](#游戏客户端开发)
3. [Python 开发](#python-开发)
4. [游戏客户端自动化测试](#游戏客户端自动化测试)
5. [开发者工具](#开发者工具)
6. [Skills 缺口分析](#skills-缺口分析)
7. [推荐自建 Skills](#推荐自建-skills)
8. [Top 30 Skills 排行榜](#top-30-skills-排行榜)

---

## 执行摘要

本次调研继续聚焦 Claude Code 热门 Skills，基于 GitHub 热门项目搜索、ClawHub 实时排行和 skills.sh 官方数据，覆盖以下方向：

- 游戏客户端开发 (Unity/Godot/Unreal/Love2D)
- Python 开发 (FastAPI/异步/类型安全)
- 游戏客户端自动化测试 (移动端/UI 自动化)
- 开发者工具 (浏览器自动化/GitHub 自动化/Docker)

### 核心发现

| 类别 | 覆盖程度 | 主要 Skills |
|------|---------|-------------|
| 游戏客户端开发 | ⭐⭐⭐⭐⭐ | Unity/Godot/Unreal 全覆盖 |
| Python 开发 | ⭐⭐⭐⭐⭐ | FastAPI/Async/测试全覆盖 |
| 游戏客户端测试 | ⭐⭐⭐ | Unity Test Framework/移动端测试 |
| 开发者工具 | ⭐⭐⭐⭐⭐ | GitHub/Docker/CI/CD 全覆盖 |

---

## 游戏客户端开发

### 重点 Skills

| Skill 名称 | 评分 | 核心能力 | 适用场景 |
|------------|------|----------|----------|
| game-cog | 1.132 | 游戏开发编排器，DeepResearch Bench 第一名 | 通用游戏开发 |
| game-developer-skill | 0.975 | Claude 游戏开发者 | AI 辅助开发 |
| fivem-dev | 0.958 | Fivem 开发 | GTA5 Mod 开发 |
| blender | 0.925 | Blender 3D 建模 | 3D 资产制作 |
| game-engine | 0.920 | 游戏引擎架构 | 引擎原理 |
| unity | 0.961 | Unity 最佳实践 | Unity 开发 |
| unreal-engine | 0.935 | Unreal Engine 开发 | UE 开发 |
| godot-dev-guide | 0.983 | Godot 4.x 完整开发指南 | Godot 开发 |

### Claude Code Game Studios（重点推荐）

**项目地址**: [Donchitos/Claude-Code-Game-Studios](https://github.com/Donchitos/Claude-Code-Game-Studios)

**GitHub Stars**: 28⭐ (2026年2月新增)

#### 核心特性

- **48 个 AI agents**，专门针对游戏开发
- **36 个 workflow skills**，覆盖完整游戏开发流程
- 完整的协调系统，模拟真实游戏工作室层级结构
- 支持 Unity/Unreal/Godot 多引擎

#### Agent 层级结构

**Tier 1 - 总监 (Opus)**
- creative-director (创意总监)
- technical-director (技术总监)
- producer (制作人)

**Tier 2 - 部门主管 (Sonnet)**
- game-designer (游戏设计师)
- lead-programmer (首席程序员)
- art-director (美术总监)
- audio-director (音频总监)
- qa-lead (QA 主管)

**Tier 3 - 专家 (Sonnet/Haiku)**
- gameplay-programmer (游戏玩法程序员)
- engine-programmer (引擎程序员)
- network-programmer (网络程序员)
- ui-programmer (UI 程序员)
- performance-analyst (性能分析师)

#### 多引擎支持

| 引擎 | 主代理 | 子专家 |
|------|--------|--------|
| Godot 4 | godot-specialist | GDScript, Shaders, GDExtension |
| Unity | unity-specialist | DOTS/ECS, Shaders/VFX, Addressables, UI Toolkit |
| Unreal Engine 5 | unreal-specialist | GAS, Blueprints, Replication, UMG/CommonUI |

#### Workflow Skills 分类

**Reviews & Analysis**
- `/design-review` - 设计审查
- `/code-review` - 代码审查
- `/balance-check` - 平衡性检查
- `/perf-profile` - 性能分析

**Production**
- `/sprint-plan` - 冲刺计划
- `/milestone-review` - 里程碑审查
- `/release-checklist` - 发布清单

**Creative**
- `/brainstorm` - 头脑风暴
- `/prototype` - 原型
- `/playtest-report` - 游戏测试报告

### Unity AI Workflow 2026

**项目地址**: [David-GD13/unity-ai-workflow](GitHub)

#### 🎮 Dev Modes (三种开发模式)

| 模式 | 角色 | 适用场景 |
|------|------|---------|
| Assistant | 你构建，AI 辅助文档和解释 | 学习、创意控制 |
| Mix (默认) | 协作模式，AI 建议，你确认 | 大多数项目 |
| Automatic | AI 构建，短的 onboarding Q&A | 快速原型、游戏 jam |

#### 🧃 核心哲学: Game Feel 不是可选的

- 每项功能使用 `/implement-feature` 完整构建
- AI 在写代码前询问 VFX、SFX、相机反馈和触觉
- 迭代打磨，不是单独阶段

#### 技术架构

- **TCREI Prompting**: Task-Context-References-Evaluate-Iterate 方法论
- **验证系统**: 每个 AI 推荐标记 [VERIFIED]/[SYNTHESIZED]/[UNVERIFIED]
- **Unity 6 LTS** 支持
- **URP/HDRP** 渲染管线
- **DOTS/ECS** 架构
- **Netcode** 网络同步

### 完整 Skills 列表

#### Unity

| Skill | 核心能力 | 评分 |
|-------|----------|------|
| unity-developer | Unity 6 LTS 专家，URP/HDRP，Profiler，DOTS/ECS | 0.945-1.013 |
| unity-ai-workflow-2026 | AI 驱动开发，三种模式 | 2026 新增 |
| unity-ecs-patterns | Unity DOTS/ECS 架构，性能优化 | - |
| unity-netcode | Unity Netcode 多人游戏 | - |
| unity-shader-graph | Shader Graph 可视化着色器 | - |

#### Godot

| Skill | 核心能力 | 评分 |
|-------|----------|------|
| godot-gdscript-patterns | Godot 4 GDScript 2.0 最佳实践 | - |
| godot-4-dev | Godot 4 完整开发指南 | 0.983 |
| godot-state-machine | Godot 状态机模式 | - |

#### Unreal

| Skill | 核心能力 |
|-------|----------|
| unreal-engine-cpp-pro | Unreal 5.x C++ 开发 |
| unreal-blueprint-visual | Blueprint 可视化编程 |
| unreal-slate-ui | Slate UI 框架开发 |

---

## Python 开发

### 重点 Skills

| Skill 名称 | 核心能力 | 适用场景 |
|------------|----------|----------|
| python-pro | Python 3.12+ 现代特性，uv/ruff | 通用 Python 开发 |
| python-patterns | 框架选择、类型提示、项目结构 | 架构设计 |
| python-fastapi-development | FastAPI 后端开发 | API 服务 |
| async-python-patterns | asyncio 异步编程 | 高并发 |
| python-testing-patterns | pytest 测试策略 | 质量保证 |
| python-performance-optimization | 性能分析和优化 | 性能调优 |
| temporal-python-pro | Temporal 工作流编排 | 分布式事务 |
| dbos-python | DBOS 可靠工作流 | 持久化工作流 |
| uv-global | uv 包管理器 | 快速包管理 |

### 专业 Python Skills（Claudev Pros 系列）

**项目地址**: [Ricko12vPL/claude-code-skills](https://github.com/Ricko12vPL/claude-code-skills)

**GitHub Stars**: 6⭐

#### 技能总览

| Skill | 大小 | 章节数 | 代码示例数 | 主要主题 |
|-------|------|--------|-----------|----------|
| Python Programming | 12 KB | 15 | 30+ | PEP 8, testing, async, patterns |
| Software Engineering | 28 KB | 20 | 40+ | SOLID, architecture, CI/CD |
| Machine Learning | 27 KB | 25 | 50+ | ML workflow, PyTorch, MLOps |
| Quantitative Finance | 58 KB | 18 | 60+ | Trading, backtesting, portfolio |
| Senior Quant Developer | 3 KB | 9 | 3 | Low-latency, observability |
| Senior Quant Researcher | 2.5 KB | 9 | 3 | Alpha research, validation |
| Senior Systematic Trader | 2 KB | 9 | 3 | TCA, execution, governance |
| Senior Quant Trader | 2 KB | 9 | 3 | Portfolio, attribution, KPIs |

#### Python Programming 核心内容

- ✅ PEP 8, PEP 257, PEP 484 (style, docstrings, type hints)
- ✅ 项目结构 (pyproject.toml)
- ✅ 现代特性 (dataclasses, context managers, async/await)
- ✅ 设计模式 (Singleton, Factory, Decorator, Observer)
- ✅ pytest 测试 (fixtures, parametrize, mocking)
- ✅ 异步编程 (asyncio, async context managers)

### FastAPI 专题

#### 核心特性

- **高性能**: 与 Node.js 和 Go 相当
- **自动文档**: Swagger UI/ReDoc
- **类型安全**: Pydantic 集成
- **异步支持**: async/await

#### 适用场景

- REST API 开发
- 微服务
- 实时应用 (WebSocket)
- 数据处理管道

### uv 包管理器

#### 核心优势

- 比 pip 快 **10-100 倍**
- 磁盘空间占用少
- 依赖解析优化
- 虚拟环境管理

#### 安装使用

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
uv pip install fastapi
uv venv && source .venv/bin/activate
```

### 异步编程

#### asyncio 基础

- async/await 语法
- Event loop 管理
- Task 和 Future
- 取消和超时

#### 高级模式

- 并发任务管理
- 异步生成器
- 异步上下文管理器
- 错误处理

#### 生态集成

- aiohttp: 异步 HTTP
- asyncpg: 异步 PostgreSQL
- aiomysql: 异步 MySQL

### 工作流编排

#### Temporal

- 持久化工作流
- Saga 模式
- 分布式事务
- 活动重试和超时

#### DBOS

**项目地址**: [DBOS-dev/dbos-python](https://github.com/DBOS-dev/dbos-python)

- 可靠、耐错应用构建
- 持久化工作流
- 队列支持
- 事务追踪

### skills.sh 官方 Python Skills

| 排名 | Skill | 安装量 | 核心能力 |
|------|-------|--------|----------|
| 1 | python-executor | 13.4K | Python 代码执行 |
| 2 | python-sdk | 13.2K | Python SDK |
| 3 | python-performance-optimization | 7.1K | Python 性能优化 |
| 4 | architecture-patterns | 6.7K | 架构模式 |

---

## 游戏客户端自动化测试

### 重点 Skills

| Skill 名称 | 评分 | 核心能力 | 适用场景 |
|------------|------|----------|----------|
| test-automator | - | AI 驱动测试自动化 | 智能测试生成 |
| e2e-testing-patterns | - | Playwright/Cypress E2E | 端到端测试 |
| playwright-skill | 3.538-3.584 | Playwright 浏览器自动化 | 测试/爬虫 |
| playwright-mcp | 3.581 | Playwright MCP 服务器 | 自动化服务器 |
| python-testing-patterns | - | pytest 最佳实践 | Python 测试 |
| test-driven-development | - | TDD 开发流程 | 测试先行 |
| testing-qa | - | 综合 QA 工作流 | 质量保证 |
| azure-playwright-testing-ts | - | Azure Playwright 云测试 | 大规模测试 |
| android-adb | 1.220 | Android ADB 测试 | 移动端测试 TOP 1 |
| test-runner | 1.189 | 测试运行器 | - |
| test-master | 1.158 | 测试管理 | - |

### Playwright 专题

#### 自动化能力

- 自动检测开发服务器
- 编写测试脚本到 /tmp
- 默认使用可见浏览器
- URL 参数化配置

#### 常见模式

- 页面测试 (多视口)
- 登录流程测试
- 表单填写和提交
- 链接检查
- 响应式设计测试

### Unity Test Framework

#### 测试类型

- **Edit Mode**: 纯 C# 逻辑测试，无需运行游戏
- **Play Mode**: 集成测试，运行游戏场景

#### 核心组件

- TestRunner: 测试运行器
- NUnit: 测试框架
- UnityTestAttribute: 协程测试

#### 示例测试

```csharp
[UnityTest]
public IEnumerator PlayerMove_Test()
{
    var player = new GameObject("Player");
    var mover = player.AddComponent<PlayerMover>();

    mover.Move(Vector2.right);
    yield return null;

    Assert.AreEqual(Vector2.right, mover.Velocity);
}
```

### 移动端游戏测试

#### Android ADB

**核心能力**

- ADB 命令执行
- 设备管理
- 日志查看
- 应用安装/卸载
- 屏幕截图/录制

**常用命令**

```bash
adb devices
adb shell uiautomator dump
adb install app.apk
adb logcat
```

#### 游戏特定测试

- 触控响应延迟
- 陀螺仪/重力感应
- 内存/电量消耗
- 网络切换 (WiFi → 4G)

### 网络同步测试

#### 帧同步测试

- 确定性验证: 相同输入 → 相同输出
- 断线重连测试
- 录像回放验证

#### 状态同步测试

- 状态一致性验证
- 增量同步效率
- 预测回滚测试

#### 延迟模拟

- 网络抖动 (Jitter): 0-200ms 随机延迟
- 丢包模拟: 5%-20% 丢包率
- 高延迟环境: 200-500ms RTT

### skills.sh 官方测试 Skills

| 排名 | Skill | 安装量 | 核心能力 |
|------|-------|--------|----------|
| 1 | webapp-testing | 17.7K | Web 应用测试 |
| 2 | test-driven-development | 17.2K | TDD 开发流程 |
| 3 | playwright | 15.3K | Playwright 测试 |

---

## 开发者工具

### 重点 Skills

| Skill 名称 | 评分 | 核心能力 | 适用场景 |
|------------|------|----------|----------|
| github | 3.790 | GitHub 基础操作 | PR/Issue/Workflow |
| openclaw-github-assistant | 3.615 | OpenClaw GitHub 助手 | 增强操作 |
| github-cli | 3.501 | GitHub CLI | 命令行操作 |
| docker-essentials | 3.694 | Docker 基础 | 容器化 TOP 1 |
| docker | 3.577 | Docker 完整版 | 容器管理 |
| docker-sandbox | 3.548 | Docker 沙箱 | 安全测试 |
| docker-ctl | 3.531 | Docker 控制 | 容器控制 |
| docker-compose | 3.511 | Docker Compose | 多容器编排 |
| docker-diag | 3.474 | Docker 诊断 | 问题排查 |
| git-essentials | 1.298 | Git 基础 | 版本控制 TOP 1 |
| agent-browser | 3.772 | 浏览器自动化 | 自动化 |
| automation-workflows | 3.699 | 工作流自动化 | 效率 |

### GitHub 自动化

#### 核心能力

- 仓库管理
- Issue 管理
- Pull Request 操作
- Actions 工作流

#### 典型交互

```
"Create a new issue for the bug"
"Automatically label new PRs"
"Run tests on PR and report results"
```

#### 工作流设计

- 触发条件配置
- Matrix 构建
- 依赖缓存
- Artifacts

### Docker 工具链

#### 核心能力

- Dockerfile 最佳实践
- 镜像构建优化
- 多阶段构建
- 容器网络配置
- 安全加固

### CI/CD 流水线

#### 流水线阶段

1. 源码检出
2. 依赖安装
3. 代码构建
4. 测试执行
5. 部署发布

#### 最佳实践

- 幂等性
- 快速失败
- 日志清晰
- 制品管理

### GitOps

#### 核心工具

- ArgoCD
- Flux

#### 特性

- 声明式 Kubernetes 部署
- 持续协调
- Git 作为单一真相来源

### skills.sh 官方排行榜

| 排名 | Skill | 安装量 | 所属组织 | 核心能力 |
|------|-------|--------|----------|----------|
| 1 | find-skills | 391.6K | vercel-labs | 技能发现和推荐 |
| 2 | vercel-react-best-practices | 188.1K | vercel-labs | React 最佳实践 |
| 3 | web-design-guidelines | 145.2K | vercel-labs | Web 设计指南 |
| 4 | azure-ai | 123.5K | microsoft | Azure AI 服务 |
| 5 | azure-observability | 123.3K | microsoft | Azure 监控 |

#### 关键洞察

- **Microsoft Azure** 系列 Skills 占据主导地位 - 20 个中有 17 个是 Azure 相关
- **Vercel Labs** 是最大的非企业贡献者 - find-skills 排名第一 (391.6K 安装量)
- **Web 开发** Skills 仍然最受欢迎 - React/设计指南排名靠前

---

## Skills 缺口分析

### 已有覆盖

| 方向 | 覆盖程度 |
|------|---------|
| 游戏客户端开发 | ⭐⭐⭐⭐⭐ Unity/Godot/Unreal 全覆盖 |
| Python 开发 | ⭐⭐⭐⭐⭐ FastAPI/Async/测试全覆盖 |
| 开发者工具 | ⭐⭐⭐⭐⭐ GitHub/Docker/CI/CD 全覆盖 |

### 需要补充

| 方向 | 缺口 | 建议 |
|------|------|------|
| 游戏客户端自动化测试 |专门的 Unity/Unreal 自动化测试 Skills 较少 | 可自建 Unity Test Framework + Playwright 集成 Skill |
| 帧同步测试 | 确定性测试、录像回放测试缺乏专业指导 | 可基于项目需求开发专门的测试 Skill |
| 游戏性能基准测试 | 帧率、内存、加载时间测试缺乏统一方案 | 可整合 Unity Profiler 相关工具 |

---

## 推荐自建 Skills

### 高优先级

1. **game-frame-sync-tester**: 帧同步确定性测试
2. **unity-performance-benchmark**: Unity 性能基准测试

### 中优先级

3. **godot-4-advanced**: Godot 4 高级开发技巧
4. **playwright-game-testing**: 游戏 E2E 测试
5. **unreal-automation-testing**: Unreal 自动化测试

---

## Top 30 Skills 排行榜

### 综合排名

| 排名 | Skill | 评分 | 类别 |
|------|-------|------|------|
| 1 | github | 3.790 | 开发者工具 |
| 2 | agent-browser | 3.772 | 开发者工具 |
| 3 | automation-workflows | 3.699 | 开发者工具 |
| 4 | docker-essentials | 3.694 | DevOps |
| 5 | docker | 3.577 | DevOps |
| 6 | playwright-scraper-skill | 3.584 | 测试 |
| 7 | playwright-mcp | 3.581 | 测试 |
| 8 | docker-sandbox | 3.548 | DevOps |
| 9 | playwright | 3.538 | 测试 |
| 10 | docker-ctl | 3.531 | DevOps |
| 11 | docker-compose | 3.511 | DevOps |
| 12 | docker-diag | 3.474 | DevOps |
| 13 | openclaw-github-assistant | 3.615 | 开发者工具 |
| 14 | github-cli | 3.501 | 开发者工具 |
| 15 | azure-ai | - | AI 服务 |

### 分类排名

#### 游戏开发

| 排名 | Skill | 评分 |
|------|-------|------|
| 1 | game-cog | 1.132 |
| 2 | game-developer-skill | 0.975 |
| 3 | godot-dev-guide | 0.983 |
| 4 | unity | 0.961 |
| 5 | unreal-engine | 0.935 |

#### Python 开发

| 排名 | Skill | 评分 |
|------|-------|------|
| 1 | fastapi | 1.121 |
| 2 | python | 0.986 |
| 3 | django | 0.960 |
| 4 | uv-global | 1.092 |

#### 测试

| 排名 | Skill | 评分 |
|------|-------|------|
| 1 | android-adb | 1.220 |
| 2 | test-runner | 1.189 |
| 3 | test-master | 1.158 |

#### 开发者工具

| 排名 | Skill | 评分 |
|------|-------|------|
| 1 | github | 3.790 |
| 2 | docker-essentials | 3.694 |
| 3 | git-essentials | 1.298 |

---

## 📚 参考资源

- [Antigravity Awesome Skills](https://github.com/anthropics/claude-code-skills) (968+ Skills)
- [ClawHub](https://clawhub.com) - 实时 Skills 搜索
- [skills.sh](https://skills.sh) - 官方 Skills 排行榜

---

## 📝 更新日志

- **2026-03-04**: 第二十八周调研完成，新增 Claude Code Game Studios 深度分析，skills.sh 官方排行榜数据

---

*文档更新于 2026-03-04*
