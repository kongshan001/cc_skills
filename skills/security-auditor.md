# Security Auditor

> 全面的安全审计和安全编码专家 - 基于 OWASP Top 10 框架

## 📋 基本信息

| 项目 | 内容 |
|------|------|
| **技能名称** | security-auditor |
| **版本** | 1.0.0 |
| **作者** | jgarrison929 |
| **许可证** | MIT |
| **评分** | ⭐ 3.0+ |

## 🎯 技能描述

Security Auditor 是全面的安全审计和安全编码专家，基于 Dave Poon 的 buildwithclaude 改编。专注于安全审计、漏洞检测和 OWASP 合规。

## 🛠️ 功能列表

### 1. 安全审计流程
- 代码和架构全面审计
- OWASP Top 10 漏洞识别
- 安全认证和授权流程设计
- 输入验证和加密机制实施
- 安全测试和监控策略创建

### 2. 核心原则
- 防御深度 (多层安全)
- 最小权限原则
- 永不信任用户输入
- 安全失败设计
- 定期依赖扫描和更新
- 注重实际修复

### 3. OWASP Top 10 检查清单

#### A01:2021 - 访问控制失效
- 每个端点验证认证
- 每个数据访问验证授权
- CORS 配置特定来源
- 目录列表禁用
- 敏感端点限速
- JWT 令牌每次请求验证

#### A02:2021 - 加密失败
- 密码使用 bcrypt (12+ 轮) 或 argon2 哈希
- 静态数据加密 (AES-256)
- 强制 TLS/HTTPS
- 源代码和日志中无 secrets

#### A03:2021 - 注入
- 参数化查询
- ORM/准备语句
- 输入验证

## 📦 安装方式

```bash
# 使用 ClawHub 安装
clawhub install security-auditor
```

## 📊 推荐安装评估

| 场景 | 推荐度 | 说明 |
|------|--------|------|
| **本地安装** | ⭐⭐⭐⭐⭐ | 强烈推荐，安全审计必备 |
| **ECS 安装** | ⭐⭐⭐⭐⭐ | 完美支持，安全合规 |

### 评分理由

- ✅ 基于 OWASP Top 10 的完整审计框架
- ✅ 大量代码示例 (好/坏对比)
- ✅ 实用的安全修复建议
- ✅ 适合所有类型项目

## 🛡️ 安全检查项

### 认证与授权
```javascript
// ❌ 错误: 无授权检查
app.delete('/api/posts/:id', async (req, res) => {
  await db.post.delete({ where: { id: req.params.id } })
  res.json({ success: true })
})

// ✅ 正确: 验证所有权
app.delete('/api/posts/:id', authenticate, async (req, res) => {
  const post = await db.post.findUnique({ where: { id: req.params.id } })
  if (!post) return res.status(404).json({ error: 'Not found' })
  if (post.authorId !== req.user.id && req.user.role !== 'admin') {
    return res.status(403).json({ error: 'Forbidden' })
  }
  await db.post.delete({ where: { id: req.params.id } })
  res.json({ success: true })
})
```

### 加密
```javascript
// ❌ 错误: 存储明文密码
await db.user.create({ data: { password: req.body.password } })

// ✅ 正确: Bcrypt 哈希
import bcrypt from 'bcryptjs'
const hashedPassword = await bcrypt.hash(req.body.password, 12)
await db.user.create({ data: { password: hashedPassword } })
```

## 📋 审计报告结构

1. **执行摘要**
2. **漏洞清单** (按严重程度)
3. **修复建议**
4. **最佳实践建议**
5. **后续步骤**

---

*本报告由 OpenClaw 自动生成，更新时间: 2026-03-17*
