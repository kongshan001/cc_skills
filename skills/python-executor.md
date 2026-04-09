# Python Executor

## 技能概述

- **Slug**: python-executor
- **名称**: Python Executor
- **作者**: okaris
- **版本**: 0.1.5
- **更新时间**: 2026-04-09

## 背景需求

在开发过程中，经常需要执行 Python 代码进行快速验证、数据分析或原型开发。需要一个安全的方式来执行 Python 代码。

## 目标

Execute Python code in a safe sandboxed environment via inference.sh. Pre-installed: NumPy, Pandas, Matplotlib, requests, BeautifulSoup, SciPy, Seaborn, Plotly, Pillow.

## 功能列表

- 安全沙箱环境执行 Python 代码
- 预装常用库 (NumPy, Pandas, Matplotlib, requests, BeautifulSoup 等)
- 无需本地 Python 环境
- 快速原型开发
- 数据分析支持

## 安装方式

```bash
clawhub install python-executor
```

## 推荐安装评估

- **本地开发**: ⭐⭐⭐⭐ 推荐
- **ECS 服务器**: ⭐⭐⭐⭐ 推荐

**理由**: 适合需要快速执行 Python 代码但不想配置本地环境的场景。预装的科学计算库使其特别适合数据分析任务。

## 优缺点分析

### 优点

1. 无需配置本地 Python 环境
2. 预装常用库
3. 安全沙箱执行
4. 适合快速原型开发

### 缺点

1. 依赖外部服务 (inference.sh)
2. 网络要求
3. 资源可能受限

## 平替对比

| 技能 | 特点 |
|------|------|
| lsp-python | 更侧重代码质量检查 |
| python-code-test | 更侧重测试生成 |

## 落地过程

1. 执行 `clawhub install python-executor`
2. 激活技能后即可执行 Python 代码
3. 适合快速验证想法和数据分析
