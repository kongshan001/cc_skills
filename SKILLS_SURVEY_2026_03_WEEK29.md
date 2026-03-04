# Claude Code Skills 完整调研报告 - 2026年3月 (第二十九周)

**调研日期**: 2026-03-04  
**技能来源**: GitHub 热门仓库 + API 实时搜索  
**目标仓库**: https://github.com/kongshan001/cc_skills  
**状态**: ✅ 调研完成

---

## 📊 调研概要

本次调研继续聚焦 Claude Code 热门 Skills，基于 GitHub API 搜索，覆盖以下方向：

1. **游戏客户端开发** (Unity/Godot/Unreal/GameMaker/Love2D)
2. **Python 开发** (FastAPI/异步/类型安全/测试)
3. **游戏客户端自动化测试** (移动端/UI 自动化/E2E)
4. **开发者工具** (浏览器自动化/代码审查/安全评估/CI/CD)

---

## 🎮 一、游戏客户端开发 Skills

### 1.1 Claude Code Game Studios ⭐28 (2026年3月新增)

**项目地址**: [Donchitos/Claude-Code-Game-Studios](https://github.com/Donchitos/Claude-Code-Game-Studios)

Claude Code Game Studios 是目前最全面的游戏开发多代理系统，包含：

```markdown
## 核心特性
- 48 个 AI agents，专门针对游戏开发
- 36 个 workflow skills，覆盖完整游戏开发流程
- 完整的协调系统，模拟真实游戏工作室层级结构
- 支持 Unity/Unreal/Godot 多引擎

## Studio Hierarchy (三层架构)

### Tier 1 — Directors (Opus)
- creative-director: 创意总监，守护游戏愿景
- technical-director: 技术总监，技术决策
- producer: 制作人，项目管理

### Tier 2 — Department Leads (Sonnet)
- game-designer: 游戏设计师
- lead-programmer: 主程
- art-director: 美术总监
- audio-director: 音频总监
- narrative-director: 叙事总监
- qa-lead: QA 负责人
- release-manager: 发布经理
- localization-lead: 本地化负责人

### Tier 3 — Specialists (Sonnet/Haiku)
- gameplay-programmer: 玩法程序员
- engine-programmer: 引擎程序员
- ai-programmer: AI 程序员
- network-programmer: 网络程序员
- tools-programmer: 工具程序员
- ui-programmer: UI 程序员
- systems-designer: 系统设计师
- level-designer: 关卡设计师
- economy-designer: 经济系统设计师
- technical-artist: 技术美术
- sound-designer: 音效设计师
- writer: 编剧
- world-builder: 世界构建师
- ux-designer: UX 设计师
- prototyper: 原型师
- performance-analyst: 性能分析师
- devops-engineer: DevOps 工程师
- analytics-engineer: 数据分析工程师
- security-engineer: 安全工程师
- qa-tester: QA 测试员
- accessibility-specialist: 无障碍专家
- live-ops-designer: 长线运营设计师
- community-manager: 社区经理

## Slash Commands (36个)
### Reviews & Analysis
/design-review /code-review /balance-check /asset-audit
/scope-check /perf-profile /tech-debt

### Production
/sprint-plan /milestone-review /estimate /retrospective /bug-report

### Project Management
/start /project-stage-detect /reverse-document /gate-check /design-systems

### Release
/release-checklist /launch-checklist /changelog /patch-notes /hotfix

### Creative
/brainstorm /playtest-report /prototype /onboard /localize

### Team Orchestration
/team-combat /team-narrative /team-ui /team-release /team-polish
/team-audio /team-level
```

**推荐理由**: 最完整的游戏开发多代理系统，适合大型项目。

---

### 1.2 Unity AI Workflow 2026 ⭐4

**项目地址**: [David-GD13/unity-ai-workflow](https://github.com/David-GD13/unity-ai-workflow)

```markdown
## 核心哲学: Game Feel 不是可选的
- 每项功能使用 /implement-feature 完整构建
- AI 在写代码前询问 VFX、SFX、相机反馈和触觉
- 迭代打磨，不是单独阶段

## Dev Modes (三种开发模式)
| 模式 | 角色 | 适用场景 |
|------|------|---------|
| Assistant | 你构建，AI 辅助文档和解释 | 学习、创意控制 |
| Mix (默认) | 协作模式，AI 建议，你确认 | 大多数项目 |
| Automatic | AI 构建，短的 onboarding Q&A | 快速原型、game jam |

## 技术架构
- TCREI Prompting: Task-Context-References-Evaluate-Iterate 方法论
- 验证系统: [VERIFIED]/[SYNTHESIZED]/[UNVERIFIED] 标记
- 专家 Skills: UI Toolkit、ScriptableObject、Netcode、game feel、测试、调试
```

---

### 1.3 cc-plugin-unity-gamedev ⭐1

**项目地址**: [tjboudreaux/cc-plugin-unity-gamedev](https://github.com/tjboudreaux/cc-plugin-unity-gamedev)

```markdown
## 技能分类
| 类别 | 技能数量 | 包含内容 |
|-----|---------|---------|
| **工具类** | 8 | Addressables, MemoryPack, ScriptableObjects, Profiling, Package Manager, Version Control, Debugging, Asset Pipeline |
| **动画/物理** | 5 | Animation, Physics, NavMesh, Object Pooling, State Machine |
| **AI/行为** | 2 | Behavior Designer, Gameplay Ability System (GAS) |
| **音视频** | 2 | Wwise 音频, Cinemachine 相机 |
| **UI** | 2 | UGUI, Mobile Optimization |
| **测试** | 1 | Test Framework |
| **DI/异步** | 1 | VContainer, UniTask |

## 核心技能示例
// Addressables 异步加载
var handle = Addressables.LoadAssetAsync<GameObject>("Prefab");
var prefab = await handle.Task;

// GAS Ability 定义
[CreateAssetMenu(fileName = "NewAbility", menuName = "Ability/Active")]
public class GameplayAbility : AbilitySystemComponent { }

// PrimeTween 动画序列
Tween.Sequence()
    .Append(transform.TweenPosition(targetPos, 0.5f))
    .SetLoops(-1);
```

---

### 1.4 OH-Unity-GameDev-Skills ⭐6

**项目地址**: [OstrichHermit/OH-Unity-GameDev-Skills](https://github.com/OstrichHermit/OH-Unity-GameDev-Skills)

| 技能名称 | 功能描述 |
|---------|---------|
| **claude_skill_unity** | Unity 基础开发技能 |
| **doTween-unity** | DoTween 动画库集成 |
| **media-pipe-unity-skill** | MediaPipe 机器视觉集成 |
| **prime-tween-unity** | PrimeTween 高性能动画 |
| **skill-creator** | 技能创建辅助工具 |

---

### 1.5 GameMaker Skills ⭐2

**项目地址**: [leihaht/gamemaker-skills](https://github.com/leihaht/gamemaker-skills)

```markdown
## Skills 覆盖范围
- Object Creation Workflow: 完整4步流程模板
- GML Language Essentials: 变量、数据类型、操作符、控制流
- Data Structures: Structs、Arrays、ds_list、ds_map、ds_grid
- File System: JSON 处理、datafiles/ 结构、存档系统
- Event System: 执行顺序、事件类型、常见模式
- Drawing & Graphics: 精灵、表面、着色器、粒子、瓦片地图
- Collision & Movement: 检测算法、优化技术
- Performance Optimization: Draw call 减少、对象池、性能分析
- Networking: 客户端-服务器架构、包结构、延迟补偿
- Platform-Specific: 移动端、主机、HTML5、桌面特性
- Advanced Topics: Shader 编程 (GLSL ES)、光照系统、法线贴图
```

---

### 1.6 Love2D Pocket Bomber Game ⭐11

**项目地址**: [chongdashu/love2d-pocket-bomber-game](https://github.com/chongdashu/love2d-pocket-bomber-game)

展示 AI 辅助游戏开发的完整流程，使用 Lua/Love2D 框架。

---

### 1.7 Game Opus - 终极游戏开发元技能 ⭐0

**项目地址**: [nightbs8/game-opus](https://github.com/nightbs8/game-opus)

- **游戏开发技能**: 14 个
- **3D 技能**: 3 个

---

## 🐍 二、Python 开发 Skills

### 2.1 claude-arsenal ⭐9

**项目地址**: [majiayu000/claude-arsenal](https://github.com/majiayu000/claude-arsenal)

> 🚀 39+ battle-tested Claude Code skills & 9 specialized agents for professional software development.

```markdown
## 核心功能
- 39+ 经过实战测试的 Claude Code 技能
- 9 个专业化代理
- 覆盖完整的专业软件开发流程
```

---

### 2.2 fastmcp-builder ⭐5

**项目地址**: [husniadil/fastmcp-builder](https://github.com/husniadil/fastmcp-builder)

```markdown
## 核心功能
- 使用 FastMCP 构建生产级 MCP 服务器的完整技能
- 参考指南、可运行示例
- 完整实现包含 OAuth、测试和最佳实践
```

---

### 2.3 claude-skill-python ⭐0

**项目地址**: [darrenoakey/claude-skill-python](https://github.com/darrenoakey/claude-skill-python)

Claude Code skill enforcing strict Python development standards with zero-fabrication testing

---

### 2.4 test-management ⭐1

**项目地址**: [1percrnt365/test-management](https://github.com/1percrnt365/test-management)

Claude Code skill: systematic test file management strategy for any project (Python/Rust/JS/TS)

---

### 2.5 spx-claude ⭐1

**项目地址**: [outcomeengineering/spx-claude](https://github.com/outcomeengineering/spx-claude)

Claude Code plugin marketplace: testing methodology, Python workflow, and productivity skills

---

## 🧪 三、游戏客户端自动化测试 Skills

### 3.1 Playwright Skill ⭐1848 (热门第一)

**项目地址**: [lackeyjb/playwright-skill](https://github.com/lackeyjb/playwright-skill)

```markdown
## 核心功能
- 模型调用的 Playwright 自动化
- Web 应用自动化测试
- UI 验证和截图捕获
- 辅助调试 UI 行为
- Bot 检测绕过 (Patchright)

## 技术架构
用户请求 → Claude Code → Playwright Skill → 浏览器自动化
                                      ↓
                            测试结果/截图 → 返回 Claude

## 适用场景
- Web 游戏测试
- H5 游戏测试
- 前端功能验证
- UI 自动化测试
- 回归测试
```

---

### 3.2 Playwright Undetected Skill ⭐4

**项目地址**: [dalbit-mir/playwright-undetected-skill](https://github.com/dalbit-mir/playwright-undetected-skill)

```markdown
## 核心功能
- Bot 检测绕过
- Localhost 测试
- 截图捕获
- UI 交互
- Patchright 支持反检测
```

---

### 3.3 claude-skills-marketplace ⭐428

**项目地址**: [mhattingpete/claude-skills-marketplace](https://github.com/mhattingpete/claude-skills-marketplace)

```markdown
## 测试相关技能
| 技能名称 | 功能 |
|---------|------|
| test-fixing | 测试修复 |
| test-writing | 测试编写 |
| test-running | 测试运行 |
| bug-finding | Bug 查找 |
| code-review | 代码审查 |
```

---

### 3.4 fieldwork-skills ⭐12

**项目地址**: [buildoak/fieldwork-skills](https://github.com/buildoak/fieldwork-skills)

```markdown
## 核心功能
- 端到端测试
- Bug 修复
- 质量保证
```

---

### 3.5 Qa-WorkFlow ⭐2

**项目地址**: [islam-mamdouh/Qa-WorkFlow](https://github.com/islam-mamdouh/Qa-WorkFlow)

```markdown
## AI-powered QA automation framework
- Story validation (INVEST)
- IEEE 829 test plans
- Test case generation
- Bug reporting
- Figma design validation
- Jira & Figma integrations
```

---

### 3.6 casely-qa-skill ⭐2

**项目地址**: [JohnWayneeee/casely-qa-skill](https://github.com/JohnWayneeee/casely-qa-skill)

> 🚀 PDF Requirements → 47 TestRail-ready Excel test cases in 8 minutes

```markdown
## 功能
- PDF 需求文档解析
- Test Plan 生成
- Test Case 生成 (手动 + 自动)
- TestRail 导出
```

---

### 3.7 iOS Simulator Skill ⭐557

**项目地址**: [conorluddy/ios-simulator-skill](https://github.com/conorluddy/ios-simulator-skill) (Fork: NezzSigma/ios-simulator-skill ⭐1)

```markdown
## 核心功能
- 模拟器控制: 启动/停止模拟器
- 应用安装: 安装 iOS 应用
- UI 交互: 自动化 UI 测试
- 截图捕获: 状态记录
- 21 个自动化脚本用于语义导航
```

---

## 🛠️ 四、开发者工具 Skills

### 4.1 cc-switch ⭐23208 (热门第一)

**项目地址**: [farion1231/cc-switch](https://github.com/farion1231/cc-switch)

```markdown
## 核心功能
跨平台桌面 All-in-One 助手工具
- Claude Code
- Codex
- OpenCode
- Gemini CLI

支持所有主流 AI 编码工具的技能管理
```

---

### 4.2 awesome-claude-skills ⭐8141

**项目地址**: [travisvn/awesome-claude-skills](https://github.com/travisvn/awesome-claude-skills)

精选的 Claude Skills 资源列表，包含工具、工作流和自定义方法。

---

### 4.3 awesome-agent-skills ⭐2643

**项目地址**: [heilcheng/awesome-agent-skills](https://github.com/heilcheng/awesome-agent-skills)

精选的 AI 编码代理技能、工具、教程和能力列表。

---

### 4.4 pg-aiguide ⭐1579

**项目地址**: [timescale/pg-aiguide](https://github.com/timescale/pg-aiguide)

```markdown
## 核心功能
MCP server 和 Claude plugin
- PostgreSQL 技能和文档
- 帮助 AI 编码工具生成更好的 PostgreSQL 代码
```

---

### 4.5 raptor ⭐1354

**项目地址**: [gadievron/raptor](https://github.com/gadievron/raptor)

```markdown
## 核心功能
Claude Code 通用 AI 攻防安全代理
- 攻击性安全研究
- 防御性安全评估
- 对抗性思维配置
```

---

### 4.6 awesome-llm-skills ⭐962

**项目地址**: [Prat011/awesome-llm-skills](https://github.com/Prat011/awesome-llm-skills)

精选的 LLM 和 AI Agent 技能资源列表。

---

### 4.7 skillshare ⭐725

**项目地址**: [runkids/skillshare](https://github.com/runkids/skillshare)

```markdown
## 核心功能
一键同步技能到所有 AI CLI 工具
- Claude Code
- OpenClaw
- OpenCode
- 支持团队共享
```

---

### 4.8 OpenContext ⭐410

**项目地址**: [0xranx/OpenContext](https://github.com/0xranx/OpenContext)

```markdown
## 核心功能
AI 代理和个人上下文存储
- 跨代理/仓库捕获、搜索和重用项目知识
- 内置 Skills/tools
- 桌面 GUI
```

---

### 4.9 repren ⭐370

**项目地址**: [jlevy/repren](https://github.com/jlevy/repren)

```markdown
## 核心功能
强大的重命名/重构工具
- 支持 Claude Code skill
```

---

### 4.10 Skills-Manager ⭐292

**项目地址**: [jiweiyeah/Skills-Manager](https://github.com/jiweiyeah/Skills-Manager)

```markdown
## 核心功能
高性能桌面应用程序
- 管理多个 AI 编码助手的技能
- 无缝组织、同步和共享技能
- 支持 Claude Code、Codex、Opencode
- 使用 Tauri 2.0, React 19, Rust 构建
```

---

### 4.11 lovcode ⭐289

**项目地址**: [MarkShawn2020/lovcode](https://github.com/MarkShawn2020/lovcode)

```markdown
## 核心功能
AI 编码工具的桌面伴侣应用
- 浏览 Claude Code 聊天历史
- 管理配置、命令、技能等
```

---

### 4.12 agent-skills ⭐9

**项目地址**: [simota/agent-skills](https://github.com/simota/agent-skills)

> 🤖 86 specialized AI agents for software development

```markdown
## 核心功能
- bug fixing
- testing
- security
- UI/UX
- infrastructure
- Works with Claude Code, Codex CLI, Gemini CLI
```

---

### 4.13 dd-skill-test ⭐2

**项目地址**: [ryanmaclean/dd-skill-test](https://github.com/ryanmaclean/dd-skill-test)

Datadog Skills for Claude Code - Comprehensive automation in Bash, Python, and Go

---

### 4.14 claude-auto-dev ⭐2

**项目地址**: [djnsty23/claude-auto-dev](https://github.com/djnsty23/claude-auto-dev)

Autonomous development skills for Claude Code - task loops, testing, and deployment automation

---

### 4.15 research-units-pipeline-skills ⭐240

**项目地址**: [WILLOSCAR/research-units-pipeline-skills](https://github.com/WILLOSCAR/research-units-pipeline-skills)

```markdown
## 核心功能
研究管道作为语义执行单元
- 每个技能声明输入/输出
- 验收标准和护栏
- 循证方法防止空洞写作
```

---

### 4.16 superpowers-lab ⭐

**项目地址**: [obra/superpowers-lab](https://github.com/obra/superpowers-lab)

Claude Code Superpowers 实验性技能 - 新技术和工具

---

## 📈 五、技能汇总表

### 5.1 游戏开发 Skills

| 项目 | Stars | 特点 |
|------|-------|------|
| Claude Code Game Studios | 28 | 48 agents, 36 workflows, 多引擎 |
| Unity AI Workflow | 4 | Game Feel 驱动, 3 种模式 |
| cc-plugin-unity-gamedev | 1 | 21 专业技能, Unity 完整栈 |
| OH-Unity-GameDev-Skills | 6 | Python, 符合规范 |
| GameMaker Skills | 2 | GML, 2D 游戏 |
| Love2D Pocket Bomber | 11 | Lua, 完整游戏示例 |
| Game Opus | 0 | 元技能, 14+3 技能 |

### 5.2 Python 开发 Skills

| 项目 | Stars | 特点 |
|------|-------|------|
| claude-arsenal | 9 | 39+ 技能, 9 专业代理 |
| fastmcp-builder | 5 | FastMCP, 生产级 MCP |
| test-management | 1 | 测试文件管理 |
| claude-skill-python | 0 | 严格标准, 零伪造测试 |

### 5.3 自动化测试 Skills

| 项目 | Stars | 特点 |
|------|-------|------|
| Playwright Skill | 1848 | 浏览器自动化, 模型调用 |
| claude-skills-marketplace | 428 | 测试、Git、代码审查 |
| iOS Simulator Skill | 557 | iOS 模拟器, 21 脚本 |
| fieldwork-skills | 12 | 生产级测试 |
| Qa-WorkFlow | 2 | AI QA, Jira 集成 |
| Playwright Undetected | 4 | 反检测绕过 |

### 5.4 开发者工具 Skills

| 项目 | Stars | 特点 |
|------|-------|------|
| cc-switch | 23208 | All-in-One, 多 CLI 支持 |
| awesome-claude-skills | 8141 | 精选列表 |
| awesome-agent-skills | 2643 | AI 代理技能 |
| pg-aiguide | 1579 | PostgreSQL MCP |
| raptor | 1354 | 安全攻防 |
| awesome-llm-skills | 962 | LLM 技能 |
| skillshare | 725 | 跨 CLI 同步 |
| Skills-Manager | 292 | 桌面管理应用 |

---

## 🎯 六、推荐技能选择

### 6.1 游戏开发推荐

| 优先级 | 技能 | 用途 |
|--------|------|------|
| ⭐⭐⭐⭐⭐ | Claude Code Game Studios | 大型项目, 完整工作室架构 |
| ⭐⭐⭐⭐ | Unity AI Workflow | Unity 6.2+, Game Feel |
| ⭐⭐⭐⭐ | cc-plugin-unity-gamedev | Unity 专业开发 |
| ⭐⭐⭐ | OH-Unity-GameDev-Skills | Unity 快速原型 |
| ⭐⭐⭐ | GameMaker Skills | 2D 游戏开发 |

### 6.2 Python 开发推荐

| 优先级 | 技能 | 用途 |
|--------|------|------|
| ⭐⭐⭐⭐⭐ | claude-arsenal | 39+ 技能, 专业开发 |
| ⭐⭐⭐⭐ | fastmcp-builder | MCP 服务器开发 |
| ⭐⭐⭐ | test-management | 测试文件管理 |

### 6.3 测试推荐

| 优先级 | 技能 | 用途 |
|--------|------|------|
| ⭐⭐⭐⭐⭐ | Playwright Skill | Web/H5 游戏测试 |
| ⭐⭐⭐⭐ | claude-skills-marketplace | 测试工作流 |
| ⭐⭐⭐⭐ | iOS Simulator Skill | iOS 游戏测试 |
| ⭐⭐⭐ | fieldwork-skills | 生产级测试 |

### 6.4 开发者工具推荐

| 优先级 | 技能 | 用途 |
|--------|------|------|
| ⭐⭐⭐⭐⭐ | cc-switch | 跨平台工具管理 |
| ⭐⭐⭐⭐⭐ | awesome-claude-skills | 技能发现和学习 |
| ⭐⭐⭐⭐ | skillshare | 团队技能共享 |
| ⭐⭐⭐⭐ | Skills-Manager | 桌面技能管理 |

---

## 📦 七、部署指南

### 安装游戏开发技能

```bash
# Claude Code Game Studios
git clone https://github.com/Donchitos/Claude-Code-Game-Studios.git
cp -r Claude-Code-Game-Studios ~/.claude/

# Unity AI Workflow
git clone https://github.com/David-GD13/unity-ai-workflow.git
cp -r unity-ai-workflow ~/.claude/

# Unity Gamedev
git clone https://github.com/tjboudreaux/cc-plugin-unity-gamedev.git
cp -r cc-plugin-unity-gamedev ~/.claude/
```

### 安装测试技能

```bash
# Playwright
git clone https://github.com/lackeyjb/playwright-skill.git
cp -r playwright-skill ~/.claude/

# Claude Skills Marketplace
git clone https://github.com/mhattingpete/claude-skills-marketplace.git
cp -r claude-skills-marketplace/skills ~/.claude/
```

### 安装开发者工具

```bash
# cc-switch
git clone https://github.com/farion1231/cc-switch.git
# 按平台运行

# skillshare
npm install -g skillshare
skillshare sync
```

---

## ✅ 八、优缺点分析

### 优点

| 类别 | 优点 |
|------|------|
| **游戏开发** | 覆盖 Unity/Godot/GameMaker, 多代理系统成熟 |
| **Python 开发** | 类型安全、测试驱动、MCP 服务器 |
| **测试** | Playwright 生态强大, 支持反检测 |
| **开发者工具** | 跨平台支持, 技能管理工具丰富 |

### 缺点

| 类别 | 缺点 |
|------|------|
| **游戏开发** | Unreal 技能较少, 社区生态仍在早期 |
| **Python 开发** | 部分技能 Star 较低 |
| **测试** | 移动端测试技能相对较少 |
| **开发者工具** | 部分工具学习成本较高 |

---

## 🔮 九、未来趋势

### 9.1 发展趋势

| 方向 | 预测 |
|------|------|
| **游戏开发** | 多代理协作系统将更普及 |
| **测试** | AI 原生测试生成将增长 |
| **开发者工具** | 跨 CLI 工具整合将加速 |

### 9.2 值得关注

- Claude Code Game Studios - 游戏开发范式
- cc-switch - 统一工具链
- Playwright + AI - 智能测试

---

## 📎 相关资源

- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
- [awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills)
- [skills.sh](https://skills.sh)
- [Claude Code Handbook](https://nikiforovall.blog/claude-code-rules/)

---

*本报告持续更新，建议关注 GitHub 热门仓库获取最新技能信息。*
