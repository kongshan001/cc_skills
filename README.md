# Claude Code Skills 调研报告

> 基于 ClawHub 热门技能的完整调研

## 调研说明

本调研报告分析了 ClawHub 平台 Top 20 热门技能，为每个技能生成详细分析报告，包含功能描述、使用场景、安装方式和部署评估。

## 技能列表

| 技能名称 | 描述 | 版本 | 适用场景 | GitHub 仓库 |
|---------|------|------|----------|------------|
| [cli-developer](./skills/cli-developer.md) | CLI 工具开发技能 | 0.1.0 | 命令行工具开发 | - |
| [mcp-adapter](./skills/mcp-adapter.md) | Model Context Protocol 适配器 | 0.1.0 | MCP 服务器集成 | - |
| [tools-ui](./skills/tools-ui.md) | 工具生命周期 UI 组件 | 0.1.5 | React 工具界面开发 | - |
| [wechat-toolkit](./skills/wechat-toolkit.md) | 微信公众号工具包 | 1.0.3 | 公众号内容管理 | - |
| [ydc-ai-sdk-integration](./skills/ydc-ai-sdk-integration.md) | You.com + Vercel AI SDK 集成 | 1.0.0 | AI SDK 集成开发 | - |
| [meow-finder](./skills/meow-finder.md) | AI 工具发现 CLI | 1.0.0 | AI 工具查找 | - |
| [webmcp](./skills/webmcp.md) | 网页 MCP 自动化 | 1.0.0 | 网页自动化 | - |
| [web-mcp](./skills/web-mcp.md) | Next.js/React WebMCP 实现 | 1.0.0 | 前端 MCP 实现 | - |
| [tool-call-retry](./skills/tool-call-retry.md) | 工具调用自动重试 | 1.0.1 | 错误处理与重试 | - |
| [gizmolab-tools](./skills/gizmolab-tools.md) | 区块链开发者工具 | 1.0.0 | Web3 开发 | - |
| [devtopia](./skills/devtopia.md) | AI 工具管理与编排 | 1.0.1 | AI 工具生态 | - |
| [social-auto-tool-builder](./skills/social-auto-tool-builder.md) | 社交媒体自动化工具构建 | 1.1.0 | 社交媒体自动化 | - |
| [tool-master](./skills/tool-master.md) | 工具使用大师 | 0.1.1 | 工具查找系统 | - |
| [tooldyn](./skills/tooldyn.md) | 意图驱动的工具选择 | 1.0.0 | 智能工具推荐 | - |
| [openclaw-cursor-agent](./skills/openclaw-cursor-agent.md) | Cursor CLI 编码任务管理 | 1.0.0 | 长期编码任务 | - |
| [ai-dev-runtime](./skills/ai-dev-runtime.md) | AI 开发运行时工具 | 0.5.0 | 开发工具集 | - |
| [dev](./skills/dev.md) | 全栈网页开发助手 | 1.0.0 | Web 开发 | - |
| [webperf](./skills/webperf.md) | Web 性能测量与调试 | 0.1.0 | 性能优化 | - |
| [nexsolve-ai](./skills/nexsolve-ai.md) | 需求广场 AI 开发者平台 | 1.0.2 | 需求连接平台 | - |
| [mcp-review](./skills/mcp-review.md) | MCP Server 工具实现审查 | 1.0.0 | 工具设计审查 | - |

## 调研统计

- **总技能数量:** 20 个
- **更新时间:** 2026-04-08
- **涵盖领域:**
  - 开发工具 (8个)
  - AI 工具 (6个) 
  - 前端工具 (3个)
  - 区块链工具 (1个)
  - 社交媒体工具 (1个)
  - 性能工具 (1个)

## 部署建议

### 本地开发推荐
✅ **强推荐:** cli-developer, meow-finder, tool-master, tooldyn, webperf
✅ **推荐:** mcp-adapter, tool-call-retry, gizmolab-tools, devtopia, ai-dev-runtime, dev, mcp-review

### ECS 服务器推荐
✅ **强推荐:** mcp-adapter, wechat-toolkit, ydc-ai-sdk-integration, social-auto-tool-builder, openclaw-cursor-agent
✅ **推荐:** tools-ui, devtopia, ai-dev-runtime, dev, webperf

## 部署注意事项

1. **外部依赖:** 部分技能需要外部 API 或服务支持
2. **环境要求:** 前端相关技能需要 JavaScript 环境
3. **网络访问:** 某些技能需要网络连接到特定服务
4. **权限配置:** 社交媒体相关工具需要相应平台 API 权限

## 后续维护

建议定期更新技能调研：
- 监控技能版本更新
- 关注新增热门技能
- 跟踪领域发展趋势
- 更新部署建议

---

*生成时间: 2026-04-08*
*调研工具: ClawHub CLI*
*数据源: https://clawhub.com*