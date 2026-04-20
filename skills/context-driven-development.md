# Context Driven Development

> 让项目上下文成为与代码同等的核心资产

## 技能描述

将项目上下文作为与代码同等重要的资产进行管理。通过结构化上下文文档（product.md、tech-stack.md、workflow.md）实现一致的 AI 交互和团队协作。对于使用 AI 辅助开发的项目来说是必备技能。

## 核心功能

1. **结构化上下文文档** - product.md（产品需求）、tech-stack.md（技术栈）、workflow.md（工作流）
2. **AI 交互一致性** - 让 AI 每次都能获取项目上下文
3. **团队协作对齐** - 统一团队成员对项目的理解
4. **上下文版本管理** - 追踪上下文的演进历史

## 安装方式

```bash
clawhub install context-driven-development
# 或指定目录
clawhub install context-driven-development --dir ./my-skills
```

## 推荐安装评估

| 场景 | 推荐度 | 说明 |
|------|--------|------|
| 本地开发 | ⭐⭐⭐⭐⭐ | 强烈推荐，任何 AI 开发项目都应使用 |
| ECS/服务器 | ⭐⭐⭐⭐ | 适合团队共享项目上下文 |
| 个人项目 | ⭐⭐⭐⭐⭐ | 必备技能 |

### 适用人群

- 使用 Claude Code / OpenCode 进行 AI 辅助开发的开发者
- 需要团队协作的项目成员
- 希望规范项目文档的团队

## 使用示例

安装后，在项目中创建以下文件：
- `context/product.md` - 产品需求和目标
- `context/tech-stack.md` - 技术栈说明
- `context/workflow.md` - 开发工作流规范