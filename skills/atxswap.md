# ATXSwap — BSC 链上 ATX 交易工具

## 背景需求

在 BSC 链上交易 ATX 代币需要钱包管理、价格查询、Swap 执行等完整功能。

## 目标

管理 ATX 在 BSC 上的交易，包括钱包创建、价格查询、PancakeSwap V3  swaps、流动性操作等。

## 设计方案

- 钱包创建与管理
- 价格和余额查询
- PancakeSwap V3 交易
- 流动性操作 (LP positions)
- BNB/ERC20 转账

## 本地部署

```bash
npm i -g clawhub
clawhub install atxswap
```

## 推荐安装

**本地**：⚠️ 注意 - 涉及资金操作，需安全环境

## 效果展示

- 钱包仪表板
- Swap 执行结果

## 优缺点分析

**优点**：
- 一站式链上交易
- 支持 PancakeSwap V3

**缺点**：
- 合约风险