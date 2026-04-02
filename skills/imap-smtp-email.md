# imap-smtp-email - 邮件收发技能

## 基本信息

| 项目 | 内容 |
|------|------|
| **名称** | imap-smtp-email |
| **Slug** | imap-smtp-email |
| **版本** | 0.0.10 |
| **作者** | gzlicanyi |
| **创建时间** | 2026-01-29 |
| **更新时间** | 2026-03-24 |

## 技能描述

Read and send email via IMAP/SMTP. Check for new/unread messages, fetch content, search mailboxes, mark as read/unread, and send emails with attachments.

通过 IMAP/SMTP 读取和发送邮件。检查新邮件/未读邮件、获取内容、搜索邮箱、标记为已读/未读，以及发送带附件的邮件。

## 功能列表

- IMAP 邮件读取
- SMTP 邮件发送
- 检查新邮件
- 检查未读邮件
- 邮件内容获取
- 邮箱搜索
- 标记已读/未读
- 发送附件

## 安装方式

```bash
# 使用 ClawHub 安装
npx clawhub@latest install imap-smtp-email

# 或全局安装 ClawHub 后安装
npm i -g clawhub
clawhub install imap-smtp-email
```

## 推荐安装评估

### 本地安装 ⭐⭐⭐⭐
- 适合场景：本地邮件管理、自动化任务
- 优势：保护隐私、无需通过网页
- 要求：IMAP/SMTP 配置

### ECS 安装 ⭐⭐⭐⭐⭐
- 适合场景：邮件自动化、通知系统
- 优势：可定时任务、批量处理
- 要求：ECS 能访问邮件服务器

## 优缺点分析

### 优点
- 支持 IMAP 和 SMTP
- 完整邮件功能
- 适合自动化

### 缺点
- 需要邮件服务器配置
- 部分邮箱需要应用专用密码

## 平替对比

| 技能 | 对比 |
|------|------|
| 飞书消息 | 邮件 vs 飞书站内消息 |

## 落地过程

1. 安装 ClawHub: `npm i -g clawhub`
2. 安装技能: `clawhub install imap-smtp-email`
3. 配置 IMAP/SMTP 服务器
4. 开始邮件收发操作