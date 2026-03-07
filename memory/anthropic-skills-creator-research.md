# Anthropic Skills-Creator 技能调研文档

## 概述

Skills-Creator 是 Anthropic 提供的用于创建和管理 AgentSkills（智能体技能）的框架式技能。它为 AI 代理（如 Codex、Claude Code）提供了创建模块化、可复用技能包的指导方针和工具流程。

## 核心定位

- **本质**: 将通用 AI 代理"专业化"的能力扩展框架
- **作用**: 让 AI 获得特定领域的程序性知识、工作流程和工具集成
- **类比**: 像是给 AI 的"培训手册"或"入职指南"

## 技能包结构

```
skill-name/
├── SKILL.md (必需)
│   ├── YAML frontmatter 元数据 (必需)
│   │   ├── name: 技能名称
│   │   └── description: 触发描述
│   └── Markdown 主体说明
└── 资源包 (可选)
    ├── scripts/      - 可执行代码 (Python/Bash等)
    ├── references/   - 参考文档 (按需加载)
    └── assets/       - 输出资源 (模板、图片等)
```

## 核心原则

### 1. 简洁为王
- 上下文窗口是"公共资源"
- 默认假设 AI 已经很聪明，只需添加它不知道的内容
- 用简洁示例代替冗长解释

### 2. 设定适当的自由度

| 自由度级别 | 适用场景 | 实现方式 |
|-----------|---------|---------|
| 高自由度 | 多种方法都有效、依赖上下文 | 纯文本指令 |
| 中自由度 | 存在推荐模式、允许部分变体 | 伪代码/参数化脚本 |
| 低自由度 | 操作脆弱、必须一致性、严格顺序 | 特定脚本、少参数 |

### 3. 渐进式披露设计

三层加载系统：
1. **元数据** (name + description) - 常驻上下文 (~100词)
2. **SKILL.md 主体** - 技能触发时加载 (<5k词)
3. **资源包** - 按需加载 (无限)

## 创建流程

### Step 1: 理解技能用例
- 通过具体示例理解技能用途
- 明确"什么情况下触发此技能"

### Step 2: 规划可复用内容
分析每个示例，确定需要打包的资源：
- **Scripts**: 重复性代码（如 PDF 旋转脚本）
- **References**: 参考文档（API 文档、领域知识）
- **Assets**: 输出资源（模板、图片）

### Step 3: 初始化技能
```bash
scripts/init_skill.py <skill-name> --path <output-directory> [--resources scripts,references,assets] [--examples]
```

### Step 4: 编辑技能
- 编写 SKILL.md
- 添加工具脚本和资源文件
- 测试脚本确保可运行

### Step 5: 打包技能
```bash
scripts/package_skill.py <path/to/skill-folder>
```
- 自动验证技能格式
- 生成 .skill 压缩包分发

### Step 6: 迭代优化
基于实际使用反馈持续改进

## SKILL.md 编写规范

### Frontmatter (YAML)
```yaml
---
name: skill-name
description: 技能描述 (包含触发条件和用途)
---
```

### Body 编写
- 使用祈使句/不定式形式
- 只包含核心工作流程和选择指导
- 详细文档放入 references/

## 最佳实践

### 内容组织模式

**模式1: 高层指南 + 参考文件**
```markdown
# PDF 处理

## 快速开始
使用 pdfplumber 提取文本

## 高级功能
- 表单填写: 见 [FORMS.md](FORMS.md)
- API 参考: 见 [REFERENCE.md](REFERENCE.md)
```

**模式2: 按领域/框架分类**
```
cloud-deploy/
├── SKILL.md
└── references/
    ├── aws.md
    ├── gcp.md
    └── azure.md
```

### 避免的做法
- ❌ 添加 README.md、CHANGELOG.md 等辅助文档
- ❌ 在 SKILL.md 中放置详细参考文档
- ❌ 创建深层嵌套的引用结构

## 与 OpenClaw 的集成

OpenClaw 已内置 skill-creator 技能:
- 位置: `/usr/lib/node_modules/openclaw/skills/skill-creator/SKILL.md`
- 可用于: 创建、封装和发布自定义技能到 ClawHub

## 总结

Skills-Creator 是一个完整的技能开发框架，强调:
1. **模块化**: 技能自包含、可独立分发
2. **效率**: 渐进式加载避免上下文膨胀
3. **实用性**: 基于真实用例迭代优化
4. **可复用**: 一次创建，多次使用

适用于需要 AI 处理特定领域任务或需要固化工作流程的场景。
