# Python Executor

> 技能Slug: python-executor  
> 版本: 0.1.5  
> 作者: okaris  
> 更新时间: 2026-04-10

## 技能描述

Execute Python code in a safe sandboxed environment via inference.sh. Pre-installed: NumPy, Pandas, Matplotlib, requests, BeautifulSoup.

在安全的沙箱环境中执行 Python 代码。预装常用数据科学库。

## 功能列表

- Python 代码安全执行
- 沙箱环境隔离
- 预装库：NumPy, Pandas, Matplotlib, requests, BeautifulSoup
- 输出捕获与返回

## 安装方式

```bash
# 使用 clawhub 安装
clawhub install python-executor

# 或使用 npx
npx clawhub@latest install python-executor
```

## 推荐安装评估

### 本地开发环境 ✅ 推荐

- 适合快速原型开发
- 数据分析脚本执行
- 需要 Python 环境

### ECS/服务器 ✅ 推荐

- 服务端脚本执行
- 自动化任务处理

## 适用场景

1. 数据分析脚本运行
2. 快速原型验证
3. 自动化任务
4. API 调用测试

## 替代技能对比

| 技能 | 特点 | 适用场景 |
|------|------|----------|
| python-executor | 沙箱安全执行 | 数据分析/原型 |
| python-script-generator | 脚本生成 | 项目初始化 |