# Claude Skills - 167 个生产级技能集合

> 覆盖 Cloudflare/React/Tailwind/AI 的即插即用技能市场

## 1. Skill 背景需求

Claude Code 的能力受限于内置技能，面对新技术栈时往往需要大量调试才能正确配置。claude-skills 提供了 167 个经过生产验证的技能，每个技能都经过测试并记录了常见错误解决方案。

## 2. 目标

- 提供 167 个开箱即用的技能，覆盖前端、云、AI、数据库等
- 减少配置错误，每个技能记录了 12+ 个常见问题解决方案
- 降低 Token 消耗，通过技能复用减少上下文膨胀

## 3. 设计方案

### 技能分类

| 类别 | 数量 | 示例 |
|------|------|------|
| tooling | 28 | turborepo, plan-interview |
| frontend | 25 | nuxt-v4, tailwind-v4-shadcn |
| cloudflare | 21 | cloudflare-d1, workers-ai |
| ai | 20 | openai-agents, ai-sdk-core |
| api | 16 | graphql-implementation |
| web | 10 | hono-routing |
| mobile | 7 | react-native-skills |
| database | 6 | drizzle-orm-d1 |
| security | 6 | csrf-protection |
| testing | 4 | vitest-testing |

### 技能结构

```
skill-name/
├── SKILL.md              # 核心知识
├── .claude-plugin/
│   └── plugin.json       # 元数据
├── templates/            # 可复制模板
├── scripts/             # 自动化脚本
└── references/          # 扩展文档
```

## 4. 本地部署

### 添加市场

```bash
/plugin marketplace add https://github.com/secondsky/claude-skills
```

### 安装单个技能

```bash
/plugin install cloudflare-d1@claude-skills
/plugin install tailwind-v4-shadcn@claude-skills
/plugin install ai-sdk-core@claude-skills
```

### 克隆安装

```bash
git clone https://github.com/secondsky/claude-skills.git
cd claude-skills
./scripts/install-all.sh  # 安装全部167个
```

## 5. 效果展示

### 实际案例：Cloudflare D1 设置

```
用户: "Set up a Cloudflare Worker with D1 database"

Claude: [检查 skills]
→ 发现 cloudflare-d1 skill
→ 提示: "These prevent 12 documented errors. Use them?"
→ 用户确认后
→ 自动配置: Worker + D1 + 绑定 + 迁移
→ 耗时: 15分钟 (传统方式 2-4小时)
```

### 效率对比

| 指标 | 传统方式 | 使用 Skills |
|------|---------|-------------|
| Token 消耗 | 12,000-15,000 | 4,000-5,000 |
| 错误数 | 2-4 个 | 0 |
| 配置时间 | 2-4 小时 | 15-45 分钟 |

## 6. 优缺点分析

### 优点

- ✅ 167 个技能，覆盖面极广
- ✅ 每个技能经过生产验证
- ✅ 记录了 400+ 常见错误解决方案
- ✅ 减少约 65% Token 消耗
- ✅ 即插即用，按需安装

### 缺点

- ⚠️ Token 限制：15,000 字符限制，一次只能看到部分技能
- ⚠️ 偶有新版本兼容问题
- ⚠️ 部分技能需要手动配置

## 7. 平替对比

| 方案 | 技能数 | 错误预防 | 部署难度 |
|------|--------|---------|---------|
| claude-skills | 167 | 400+ | 低 |
| developer-kit | 11插件 | 100+ | 中 |
| 手动配置 | 0 | 0 | 高 |

## 8. 落地过程

### 实践记录

1. **首次安装**：添加市场，安装 cloudflare-d1 和 tailwind-v4
2. **Nuxt 项目**：使用 `/nuxt-v4` 创建项目，自动配置成功
3. **测试集成**：安装 `vitest-testing`，生成测试模板
4. **AI 集成**：安装 `ai-sdk-core`，快速接入 OpenAI

### 适用场景

- 现代 Web 开发（React/Next.js/Nuxt）
- Cloudflare 生态
- AI 应用开发
- 需要快速原型验证的项目

---

**状态**: ✅ 已调研  
**仓库**: https://github.com/secondsky/claude-skills  
**评分**: ⭐⭐⭐⭐⭐ 技能最全，生产验证
