# Python Executor

> 远程 Python 沙箱执行工具

## 技能描述

Python Executor 通过 inference.sh 服务提供远程 Python 代码执行能力，预装常用库，适合运行复杂 Python 脚本。

## 功能列表

- 远程 Python 代码执行
- 预装常用库（pandas, numpy, requests 等）
- 文件输入/输出
- API 调用和网页爬取
- 结果返回

## 安装方式

```bash
# 安装 inference.sh CLI
curl -sSL https://dist.inference.sh/install | sh

# 或使用 clawhub
clawhub install python-executor
```

## 推荐安装评估

| 环境 | 推荐度 | 说明 |
|------|--------|------|
| 本地开发 | ⭐⭐⭐⭐ | 需要远程执行时使用 |
| ECS/服务器 | ⭐⭐⭐⭐ | 服务器计算资源受限时使用 |
| 沙箱环境 | ⭐⭐⭐⭐⭐ | 需要安全隔离时使用 |

## 使用前提

- inference.sh 账户（可选登录）
- 网络连接

## 注意事项

- 代码和数据会发送到第三方服务，避免发送敏感信息
- 建议验证 SHA-256 校验和后再运行安装脚本
- 执行代码可发起网络请求，需注意数据外泄风险
