# Python Executor

> Python 代码安全沙箱执行技能

## 基本信息

- **Slug**: python-executor
- **作者**: okaris
- **版本**: 0.1.5
- **更新时间**: 2026-04-17

## 技能描述

Execute Python code in a safe sandboxed environment via inference.sh. Pre-installed: NumPy, Pandas, Matplotlib, requests, BeautifulSoup.

通过 inference.sh 在安全的沙箱环境中执行 Python 代码。预装：NumPy、Pandas、Matplotlib、requests、BeautifulSoup。

## 功能列表

- 安全沙箱执行 Python 代码
- 预装科学计算库 (NumPy, Pandas)
- 数据可视化 (Matplotlib)
- HTTP 请求 (requests)
- HTML 解析 (BeautifulSoup)
- 自动结果返回

## 安装方式

```bash
clawhub install python-executor
# 或
clawhub install okaris/python-executor
```

## 推荐安装评估

| 场景 | 推荐度 | 说明 |
|------|--------|------|
| 本地开发 | ⭐⭐⭐⭐ | 需要 inference.sh 服务支持 |
| ECS 服务器 | ⭐⭐⭐⭐⭐ | 适合服务端批量任务执行 |

## 适用场景

- 数据分析任务
- 批量脚本执行
- 自动化测试
- 快速原型开发