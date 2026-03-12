# Token Optimizer - Claude Code 上下文优化工具

> 审计并优化 Claude Code 的 Token 消耗，保护你的会话

## 1. Skill 背景需求

Claude Code 每次消息都会发送完整上下文（系统提示、工具定义、MCP 服务器、技能等），这些"幽灵 Token"在后台消耗你的上下文窗口，却对你的实际任务没有帮助。普通用户的设置可能浪费 38% 的上下文空间。

## 2. 目标

- 审计你的 Claude Code 配置，找出 Token 消耗来源
- 提供智能压缩功能，在自动压缩前保存关键状态
- 实时显示上下文质量评分
- 实现会话连续性，跨会话恢复状态

## 3. 设计方案

### 核心功能

| 功能 | 说明 |
|------|------|
| Smart Compaction | 自动压缩前保存决策、错误、代理状态 |
| Context Quality Scoring | 6维度质量分析，实时显示状态栏 |
| Session Continuity | 自动保存会话，新会话可恢复上下文 |

### Token 消耗分析

```
你的 200K 上下文窗口消耗来源：

固定开销 (不可避免)
├── 系统提示: ~3K tokens
└── 工具定义: ~12-17K tokens
    → 合计: ~15K (8%)

自动压缩缓冲
└── 预留空间: ~30-35K tokens (16%)

MCP 工具 (变量最大)
└── 每个延迟工具: ~15 tokens

你的配置堆栈
├── CLAUDE.md (可能过大)
├── MEMORY.md (可能重复)
├── 50+ 技能 (忘记禁用)
└── 未使用的命令

真实开销: ~43K tokens/消息 (22%)
+ 自动压缩缓冲 = 38% 不可用!
```

## 4. 本地部署

### Marketplace 安装

```bash
/plugin marketplace add alexgreensh/token-optimizer
/plugin install token-optimizer@alexgreensh-token-optimizer
```

### 手动安装

```bash
curl -fsSL https://raw.githubusercontent.com/alexgreensh/token-optimizer/main/install.sh | bash
```

### 配置 Hook（可选）

```bash
python3 ~/.claude/token-optimizer/measure.py setup-hook
```

## 5. 效果展示

### 审计输出示例

```
/token-optimizer

[Token Optimizer] Backing up config...
Dispatching 6 audit agents...

YOUR SETUP
Per-message overhead: ~43,000 tokens
Context used: 38% before your first message

QUICK WINS
• Slim CLAUDE.md + MEMORY.md: -5,200 tokens/msg
• Archive unused skills + commands: -4,800 tokens/msg
• Prune MCP + add file exclusion: -5,000 tokens/msg

Total: ~15,000 tokens/msg recovered
```

### 效率提升

| 指标 | 优化前 | 优化后 | 提升 |
|------|--------|--------|------|
| 可用 Token | 62% | 85% | +23% |
| 会话恢复 | 无 | 自动 | 100% |
| 压缩安全 | 可能丢失 | 完整保留 | ✅ |

## 6. 优缺点分析

### 优点

- ✅ 详细审计配置开销
- ✅ 智能压缩保存关键状态
- ✅ 实时质量评分
- ✅ 会话连续性保障
- ✅ 完全本地，无数据上传

### 缺点

- ⚠️ 需要 Python 环境
- ⚠️ 部分功能需要 Claude Code 1.0.33+
- ⚠️ Hook 安装略微复杂

## 7. 平替对比

| 方案 | 审计能力 | 压缩保护 | 会话连续 | 复杂度 |
|------|---------|---------|---------|-------|
| Token Optimizer | 完整 | ✅ | ✅ | 中 |
| /compact 命令 | 简单 | ❌ | ❌ | 低 |
| 手动优化 | 需手动 | ❌ | ❌ | 高 |

## 8. 落地过程

### 实践记录

1. **首次审计**：运行 `/token-optimizer`，发现 CLAUDE.md 过大
2. **优化配置**：精简 CLAUDE.md，节省 5,200 tokens/消息
3. **启用压缩保护**：设置 Smart Compaction，防止状态丢失
4. **会话测试**：关闭会话后重启，内容成功恢复

### 适用场景

- 长时间运行的项目
- 多技能配置用户
- 需要上下文优化的团队
- 复杂 MCP 服务器用户

---

**状态**: ✅ 已调研  
**仓库**: https://github.com/alexgreensh/token-optimizer  
**评分**: ⭐⭐⭐⭐⭐ 上下文优化必备
