# 图灵罐游戏日志阅读器 (play-game-solana-turing-pot-log-reader)

## 背景需求

The Turing Pot 是一个链上 AI 游戏平台，玩家需要查询历史游戏记录、观看实时日志，但缺乏友好 的查询接口。

## 目标

提供与 Big Log（永久 AI 日志系统）的交互接口，支持查询历史存档、订阅实时日志、发送链上打赏。

## 设计方案

- **核心功能**:
  - 查询历史游戏轮次存档
  - 订阅实时日志流
  - 发送链上小费给 Big Log
- **触发方式**: 关键词触发

## 本地部署

```bash
clawhub install play-game-solana-turing-pot-log-reader
```

## 效果展示

- 历史记录查询
- 实时日志流
- 链上交互

## 优缺点分析

✅ 优点:
- 链上数据透明
- 实时性好
- 支持打赏机制

❌ 缺点:
- 依赖 Solana 链
- 需加密钱包

## 落地过程

1. 触发技能
2. 查询历史或订阅实时
3. 可选发送打赏

---

- **技能Slug**: play-game-solana-turing-pot-log-reader
- **作者**: joelstrawn
- **最新版本**: 1.0.0
- **推荐安装方式**: ECS (链上交互场景)