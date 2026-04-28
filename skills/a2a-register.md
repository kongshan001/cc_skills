# A2A Register — OpenClaw 实例注册管理

## 背景需求

A2A 协议下，OpenClaw 实例需要注册到 RAD Gateway 才能被发现和调用。

## 目标

将当前 OpenClaw 实例注册为 A2A Agent，支持被发现和远程调用。

## 设计方案

- 注册实例到 RAD Gateway
- 管理实例元数据
- 支持注销

## 本地部署

```bash
npm i -g clawhub
clawhub install a2a-register
```

## 效果展示

- 注册状态确认
- 实例信息展示
- 注销功能

## 优缺点分析

**优点**：
- 简化注册流程
- 标准化管理

**缺点**：
- 依赖 RAD Gateway

## 落地过程

1. 安装 skill：`clawhub install a2a-register`
2. 运行注册命令
3. 验证注册状态