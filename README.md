# Claude Code Skills 调研报告

> Claude Code 热门 Skills/Plugins 调研文档

本仓库收集了 Claude Code 热门 Skills 和插件的详细调研报告，帮助开发者了解和使用这些工具提升开发效率。

## 📚 文档索引

| 类别 | 技能名称 | 描述 | 推荐安装 |
|------|---------|------|---------|
| **代码质量** | [pr-review-toolkit](skills/pr-review-toolkit.md) | 综合性的 Pull Request 审查工具包，包含 6 个专业审查代理 | 本地 |
| **代码质量** | [code-review](skills/code-review.md) | 通用代码审查代理，快速检查代码质量问题 | 本地 |
| **代码质量** | [test-writer-fixer](skills/test-writer-fixer.md) | 自动生成和修复测试用例 | 本地 |
| **代码质量** | [api-tester](skills/api-tester.md) | API 测试用例生成和验证 | 本地 |
| **深度思考** | [ultrathink](skills/ultrathink.md) | 深度思考模式，适合复杂问题分析 | 本地 |
| **开发工具** | [python-expert](skills/python-expert.md) | Python 开发专家，支持 FastAPI/Django | 本地 |
| **开发工具** | [frontend-developer](skills/frontend-developer.md) | 前端开发专家，支持 React/Vue/Angular | 本地 |
| **开发工具** | [git-workflow](skills/git-workflow.md) | Git 工作流自动化（提交/PR/Issue） | 本地 |
| **自动化运维** | [devops-automator](skills/devops-automator.md) | 自动化运维，支持 CI/CD/Docker/K8s | 本地/ECS |

## 📋 调研方向

根据 AGENTS.md 定义，本调研覆盖以下四大方向：

1. **游戏客户端开发** - Unity/Godot/Unreal/WebGL 游戏引擎
2. **Python 开发** - FastAPI/异步/测试/类型安全
3. **自动化测试** - Playwright/E2E/移动端测试
4. **开发者工具** - Docker/K8s/GitHub/CI/CD

## 📖 文档规范

每个技能报告包含以下 8 个部分：

1. **背景需求** - 为什么需要这个技能
2. **目标** - 技能的核心目标
3. **设计方案** - 架构设计和核心功能
4. **本地部署** - 安装方式和要求
5. **效果展示** - 使用示例和输出
6. **优缺点分析** - 优势与劣势
7. **平替对比** - 与类似工具的对比
8. **落地过程** - 使用场景和最佳实践

## 🔧 安装方式

### 通过 Claude Code 安装

```bash
/plugin install <skill-name>
```

### 手动安装

```bash
# 克隆仓库
git clone https://github.com/kongshan001/cc_skills.git

# 安装到 Claude Code
cp -r skills/<skill-name> ~/.claude/skills/
```

## 📊 推荐安装评估

| 安装方式 | 说明 | 适用场景 |
|---------|------|---------|
| 本地 (Desktop/Laptop) | 安装在本地开发环境 | 日常开发、代码审查、测试生成 |
| ECS 云服务器 | 安装在云服务器 | 自动化部署、CI/CD 配置、运维任务 |

## 🔗 相关资源

- [awesome-claude-code-plugins](https://github.com/ccplugins/awesome-claude-code-plugins) - 精选 Claude Code 插件列表
- [awesome-claude-code](https://github.com/LangGPT/awesome-claude-code) - Claude Code 资源精选
- [claude-night-market](https://github.com/athola/claude-night-market) - 17 个生产级 Claude Code 插件
- [Claude Code 官方文档](https://docs.claude.com/en/docs/claude-code/plugins)

## 🤝 贡献

欢迎提交 Pull Request 添加新的技能调研报告！

## 📝 许可证

MIT License
