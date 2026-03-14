# ClawHub Skills 调研报告

> 本地已安装/热门 Skills 独立调研报告

## 📋 技能列表

| 技能 | 版本 | 推荐安装 (本地) | 推荐安装 (ECS) | 描述 |
|------|------|-----------------|----------------|------|
| [playwright](./playwright.md) | 1.0.3 | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ | 浏览器自动化 |
| [code](./code.md) | 1.0.4 | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | 代码开发工作流 |
| [test-runner](./test-runner.md) | 1.0.0 | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | 测试运行器 |
| [secure-api-calls](./secure-api-calls.md) | 1.0.3 | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | 安全 API 调用 |
| [security-auditor](./security-auditor.md) | 1.0.0 | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | 安全审计 |
| [database-operations](./database-operations.md) | 1.0.0 | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | 数据库操作 |
| [self-improving](./self-improving.md) | 1.2.16 | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | 自我改进 Agent |
| [imap-smtp-email](./imap-smtp-email.md) | 0.0.9 | ⭐⭐⭐⭐ | ⭐⭐⭐ | 邮件收发 |

## 🏠 本地安装推荐 (阿里云 ECS)

### 必装技能

```bash
# 1. 代码开发工作流
clawhub install code

# 2. 安全相关
clawhub install secure-api-calls
clawhub install security-auditor

# 3. 测试
clawhub install test-runner

# 4. 数据库
clawhub install database-operations

# 5. 自我改进
clawhub install self-improving
```

### 可选技能

```bash
# 浏览器自动化
clawhub install playwright

# 邮件
clawhub install imap-smtp-email
```

## 📊 安装评分说明

| 评分 | 含义 |
|------|------|
| ⭐⭐⭐⭐⭐ | 强烈推荐 |
| ⭐⭐⭐⭐ | 推荐 |
| ⭐⭐⭐ | 一般推荐 |
| ⭐⭐ | 可选 |
| ⭐ | 不推荐 |

---

*本报告由 OpenClaw 自动生成，更新时间: 2026-03-14*
