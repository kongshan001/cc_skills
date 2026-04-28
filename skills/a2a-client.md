# A2A Client — A2A 代理发现与任务发送

## 背景需求

在多 Agent 系统中，需要发现可用的 A2A Agent 并向其发送任务请求。

## 目标

通过 RAD Gateway 发现和调用其他 A2A Agent。

## 设计方案

- 发现可用 Agent
- 发送任务请求
- 接收执行结果

## 本地部署

```bash
npm i -g clawhub
clawhub install a2a-client
```

## 效果展示

- Agent 列表查询
- 任务发送

## 优缺点分析

**优点**：
- 标准化 A2A 调用

**缺点**：
- 需要 Gateway 支持