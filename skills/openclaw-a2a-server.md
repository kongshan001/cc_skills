# OpenClaw A2A Server — A2A 协议入站任务监听器

## 背景需求

AI-to-AI (A2A) 通信协议需要入站任务监听器，让 OpenClaw 实例能接收来自其他 Agent 的任务请求。这是构建多 Agent 系统的基础组件。

## 目标

运行 A2A 协议服务端，让当前 OpenClaw 实例可接收来自 RAD Gateway 的远程任务。

## 设计方案

- 启动入站任务监听器
- 通过 RAD Gateway 接收任务
- 返回任务结果给调用方

## 本地部署

```bash
npm i -g clawhub
clawhub install openclaw-a2a-server
```

## 效果展示

- 任务接收状态显示
- 执行结果返回
- 日志记录

## 优缺点分析

**优点**：
- 标准 A2A 协议实现
- 支持多 Agent 协作

**缺点**：
- 需要配合 A2A Client 使用

## 平替对比

| 方案 | 特点 |
|------|------|
| openclaw-a2a-server | 入站任务服务 |
| 自定义 RPC | 需自行实现协议 |

## 落地过程

1. 安装 skill：`clawhub install openclaw-a2a-server`
2. 启动 A2A Server
3. 注册到 Gateway