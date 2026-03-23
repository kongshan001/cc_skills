# Claude Code Skills 调研报告

> 自动化调研 ClawHub 热门 Skills 并生成文档

## 索引表格

| 技能名称 | 类别 | 描述 | 本地开发 | ECS/服务器 |
|----------|------|------|----------|------------|
| [playwright](skills/playwright.md) | 自动化测试 | 浏览器自动化、MCP、爬虫 | ✅ 推荐 | ⚠️ 需Xvfb |
| [fastapi](skills/fastapi.md) | Python开发 | 生产级 Python API 框架 | ✅ 推荐 | ✅ 推荐 |
| [docker-essentials](skills/docker-essentials.md) | 开发者工具 | Docker 容器管理命令 | ✅ 推荐 | ✅ 推荐 |
| [k8s](skills/k8s.md) | 开发者工具 | Kubernetes 集群管理 | ⚠️ 需集群 | ✅ 推荐 |
| [game-developer-skill](skills/game-developer-skill.md) | 游戏开发 | Unity/Unreal 游戏开发 | ✅ 推荐 | ❌ 不适用 |
| [agency-agents-ai-specialists](skills/agency-agents-ai-specialists.md) | AI代理 | 50+ 专业AI代理人格 | ✅ 推荐 | ⚠️ 可选 |
| [agent-orchestrator](skills/agent-orchestrator.md) | AI代理 | 多代理任务编排 | ✅ 推荐 | ⚠️ 需配置 |
| [test-patterns](skills/test-patterns.md) | 自动化测试 | 跨语言测试模式 | ✅ 推荐 | ✅ 推荐 |
| [mobile](skills/mobile.md) | 移动开发 | iOS/Android 开发最佳实践 | ✅ 推荐 | ❌ 不适用 |
| [devops](skills/devops.md) | 开发者工具 | DevOps CI/CD 和运维 | ⚠️ 可选 | ✅ 推荐 |
| [openclaw-unity-skill](skills/openclaw-unity-skill.md) | 游戏开发 | Unity 编辑器自动化控制 | ✅ 推荐 | ❌ 不适用 |

## 技能分类

### 自动化测试
- [playwright](skills/playwright.md) - 浏览器自动化测试
- [test-patterns](skills/test-patterns.md) - 单元/集成/E2E测试

### Python 开发
- [fastapi](skills/fastapi.md) - 异步API开发

### 游戏开发
- [game-developer-skill](skills/game-developer-skill.md) - Unity/Unreal游戏开发
- [openclaw-unity-skill](skills/openclaw-unity-skill.md) - Unity编辑器控制

### 开发者工具
- [docker-essentials](skills/docker-essentials.md) - Docker容器管理
- [k8s](skills/k8s.md) - Kubernetes集群管理
- [devops](skills/devops.md) - DevOps运维实践

### AI代理
- [agency-agents-ai-specialists](skills/agency-agents-ai-specialists.md) - 专业AI代理集合
- [agent-orchestrator](skills/agent-orchestrator.md) - 多代理编排

### 移动开发
- [mobile](skills/mobile.md) - 移动应用开发最佳实践

## 安装方式

```bash
# 安装单个技能
clawhub install <skill-name>

# 示例
clawhub install playwright
clawhub install fastapi
clawhub install docker-essentials
```

## 贡献

欢迎提交新的技能调研报告！请遵循以下格式：
- 每个技能独立 MD 文件
- 包含：技能描述、功能列表、安装方式、推荐安装评估
