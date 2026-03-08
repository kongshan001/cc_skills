# Claude Code Skills 实践指南

> 记录每个 Skill 的落地实践过程

## 📁 项目结构

```
cc_skills/
├── README.md                    # 主文档（本文件）
├── docs/
│   ├── surveys/                 # 调研报告
│   │   ├── weekly/              # 周报 (WEEK20-80)
│   │   └── archives/            # 历史版本
│   └── supplements/             # 补充报告
│       └── weekly/              # 周补充报告
├── game-dev-skills/             # 游戏开发 Skills
├── python-dev-skills/           # Python 开发 Skills
├── automation-testing-skills/   # 自动化测试 Skills
├── developer-tools-skills/      # 开发者工具 Skills
└── ...                          # 更多 Skills 目录
```

## 📚 Skills 列表

### 🎮 游戏开发

| Skill 名称 | 描述 | 状态 |
|-----------|------|------|
| [game-dev-skills](./game-dev-skills/README.md) | 游戏客户端开发 Skills，覆盖 Unity/Godot/Unreal 主流引擎，ECS/DOTS 架构，Unity AI Workflow 2026 | ✅ 已调研 |
| [claude-code-game-studios](./claude-code-game-studios.md) | Claude Code Game Studios 完整工作室架构，48 agents + 36 skills，Godot/Unity/Unreal 多引擎支持 | 🆕 新增 |

### 🐍 Python 开发

| Skill 名称 | 描述 | 状态 |
|-----------|------|------|
| [python-dev-skills](./python-dev-skills/README.md) | Python 开发 Skills，Python 3.12+ 现代工具链，FastAPI/异步/测试/性能优化 | ✅ 已调研 |
| [python-type-safety](./python-type-safety/README.md) | Python 类型安全最佳实践，10 个核心模式，mypy/pyright 严格检查 | ✅ 已调研 |
| [ricko12vpl-python-skills](./ricko12vpl-python-skills.md) | Ricko12vPL Python Skills 专业技能包，8 个 Skills，Python/软件工程/机器学习/量化金融 | 🆕 新增 |

### 🧪 自动化测试

| Skill 名称 | 描述 | 状态 |
|-----------|------|------|
| [automation-testing-skills](./automation-testing-skills/README.md) | 自动化测试 Skills，AI 驱动测试、Playwright/Cypress E2E、pytest、TDD | ✅ 已调研 |

### 🛠️ 开发者工具

| Skill 名称 | 描述 | 状态 |
|-----------|------|------|
| [skill-creator](./skill-creator/README.md) | Anthropic AgentSkills 创建工具，用于设计、构建和封装自定义技能包 | ✅ 已同步 |
| [skills](./skills/README.md) | OpenAI Codex Skills 官方技能系统调研，30+ 精选技能 | ✅ 已调研 |
| [developer-tools-skills](./developer-tools-skills/README.md) | 开发者工具 Skills，浏览器自动化、GitHub/GitLab 自动化、CI/CD 流水线 | ✅ 已调研 |
| [compound-engineering](./compound-engineering/README.md) | 复合工程插件，9,782⭐，29 agents·22 commands·20 skills，完整 Plan→Work→Review→Compound 工作流 | ✅ 已调研 |
| [superpowers](./superpowers/README.md) | Agentic Skills 完整工程工作流框架，68k⭐ | ✅ 已调研 |
| [agentsys](./agentsys/README.md) | 14 插件·43 agents·30 skills 模块化编排系统，任务到生产完整自动化 | ✅ 已调研 |
| [get-shit-done](./get-shit-done/README.md) | 轻量级 Spec 驱动开发系统，解决 Context Rot，Wave 并行执行 | ✅ 已调研 |
| [everything-claude-code](./everything-claude-code/README.md) | 50K⭐ AI Agent 性能优化系统，13 agents, 56 skills, Anthropic Hackathon Winner | ✅ 已调研 |
| [antigravity-awesome-skills](./antigravity-awesome-skills/README.md) | 968+ 通用 Agentic Skills 集合，10+ AI 助手平台支持，12 大类分类 | ✅ 已调研 |
| [fullstack-dev-skills](./fullstack-dev-skills/README.md) | 66+ Skills 全栈开发框架，9 个工作流命令，覆盖 12 个技术类别 | ✅ 已调研 |
| [cc_devops_skills](./cc_devops_skills/README.md) | 31 个 DevOps 工程技能，覆盖 IaC、CI/CD、容器编排、可观测性 | ✅ 已调研 |

### 🧠 AI/记忆/规划

| Skill 名称 | 描述 | 状态 |
|-----------|------|------|
| [claude-mem](./claude-mem/README.md) | 智能记忆系统，自动捕获会话内容并生成 AI 摘要 | ✅ 已调研 |
| [episodic-memory](./episodic-memory/README.md) | 跨会话语义搜索，记住之前的讨论、决策和模式 | ✅ 已调研 |
| [planning-with-files](./planning-with-files/README.md) | Manus 风格持久化 Markdown 规划系统，15k⭐ | ✅ 已调研 |
| [deep-research](./deep-research/README.md) | Gemini 深度研究技能，自主多步骤市场分析 | ✅ 已调研 |

### 🎨 UI/UX/部署

| Skill 名称 | 描述 | 状态 |
|-----------|------|------|
| [ui-ux-pro-max](./ui-ux-pro-max/README.md) | AI UI/UX 设计智能助手，67+设计风格，36k⭐ | ✅ 已调研 |
| [pinme](./pinme/README.md) | 零配置前端部署工具，一键部署到 IPFS，2939⭐ | ✅ 已调研 |

### 🔒 安全/科研/其他

| Skill 名称 | 描述 | 状态 |
|-----------|------|------|
| [trailofbits-security](./trailofbits-security/README.md) | Trail of Bits 安全技能集，20+安全插件 | ✅ 已调研 |
| [claude-scientific-skills](./claude-scientific-skills/README.md) | 148+ 科学研究 Skills，250+ 数据库，跨生物信息、药物发现等领域 | ✅ 已调研 |
| [book-factory](./book-factory/README.md) | 非小说类书籍创作流水线，6 个 Skills 覆盖概念开发、市场验证等 | ✅ 已调研 |

## 📝 文档规范

每个 Skill 文档包含：

1. **Skill 背景需求** - 为什么需要这个 Skill
2. **目标** - Skill 要解决什么问题
3. **设计方案** - Skill 的技术架构
4. **本地部署** - Win/Mac/Linux 部署指南
5. **效果展示** - 实际使用效果
6. **优缺点分析** - Skill 的优势与不足
7. **平替对比** - 类似 Skill 对比
8. **落地过程** - 实践验证的完整记录

## 🔧 如何贡献

1. 在根目录下创建 Skill 文件夹
2. 按照上述规范编写 `README.md`
3. 在项目根目录 `README.md` 中添加链接
4. 提交 PR

---

*让 AI 助手真正记住你*
