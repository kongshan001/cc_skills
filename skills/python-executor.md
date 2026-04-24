# Python Executor

## 技能概述

- **Slug**: python-executor
- **作者**: okaris
- **版本**: 0.1.5
- **更新时间**: 2026-04-24
- **标签**: python, sandbox, executor

## 功能列表

1. 在安全的沙箱环境中执行 Python 代码
2. 预安装常用库：NumPy, Pandas, Matplotlib, requests, BeautifulSoup
3. 代码执行结果返回
4. 安全的隔离执行环境

## 安装方式

```bash
clawhub install python-executor
```

## 推荐安装评估

| 环境 | 推荐度 | 说明 |
|------|--------|------|
| 本地开发 | ⭐⭐⭐⭐⭐ | 数据分析、快速原型开发必备 |
| ECS/服务器 | ⭐⭐⭐⭐ | 适合自动化脚本执行 |

## 适用场景

- 快速数据分析和可视化
- Python 脚本测试和调试
- API 数据抓取
- 机器学习原型验证

## 优缺点分析

**优点**:
- 预装常用科学计算库
- 安全的沙箱执行环境
- 快速上手，无需环境配置

**缺点**:
- 沙箱环境可能限制某些系统调用
- 依赖 inference.sh 服务