# LSP Python

## 技能概述

- **Slug**: lsp-python
- **名称**: LSP Python
- **作者**: genify
- **版本**: 1.1.0
- **更新时间**: 2026-04-09

## 背景需求

Python 开发中需要代码质量检查、诊断、代码补全、悬浮提示和代码风格分析。使用 Language Server Protocol (LSP) 可以提供这些功能。

## 目标

Python code quality checking and LSP integration using pylsp. Provides code diagnostics, completion, hover tips, and style analysis.

## 功能列表

- 代码质量检查
- LSP 集成 (pylsp)
- 代码诊断
- 代码补全
- 悬浮提示
- 代码风格分析
- Python 特定优化

## 安装方式

```bash
clawhub install lsp-python
```

## 推荐安装评估

- **本地开发**: ⭐⭐⭐⭐⭐ 强烈推荐
- **ECS 服务器**: ⭐⭐ 较少使用

**理由**: IDE/编辑器集成的 LSP 功能是现代 Python 开发的标配，可以显著提升代码质量和开发效率。

## 优缺点分析

### 优点

1. 提升代码质量
2. 智能代码补全
3. 实时错误检测
4. 代码风格统一

### 缺点

1. 需要编辑器 LSP 支持
2. 可能影响编辑器性能

## 平替对比

| 技能 | 特点 |
|------|------|
| python-executor | 更侧重代码执行 |
| python-code-test | 更侧重测试生成 |

## 落地过程

1. 执行 `clawhub install lsp-python`
2. 在支持的编辑器中启用 LSP
3. 开始享受智能编码体验
