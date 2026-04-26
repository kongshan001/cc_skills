# Friendly Python

> 友好 Python - Pythonic 代码实践指南

## 基础信息

| 项目 | 值 |
|------|-----|
| **Slug** | friendly-python |
| **作者** | psiace |
| **版本** | 1.0.0 |
| **更新时间** | 2026-03-20 |
| **评分** | ⭐ 3.348 |

## 1. 背景需求

Python 以其简洁和 Pythonic 著称，但写出高质量、可维护的 Python 代码需要遵循一定的规范和最佳实践。缺乏指导会导致代码风格不一致、可读性差、难以维护。

## 2. 目标

提供 Python 代码编写、重构和评审的实践指导：
- Pythonic 编码风格
- 代码可读性和可维护性
- 最佳实践推荐
- 常见反模式警示

## 3. 设计方案

### 核心功能模块
- **代码风格**: PEP 8 规范、命名约定
- **Pythonic 模式**: 列表推导、生成器、上下文管理器
- **重构建议**: 识别代码 smells，提供优化方案
- **代码评审**: 检查代码问题，提供改进建议

### 技术架构
- 集成 PEP 8 规范
- 基于常见 Python 最佳实践
- 提供代码示例和对比

## 4. 本地部署

```bash
# 安装技能
clawhub install friendly-python

# 验证安装
clawhub list | grep python
```

### 环境要求
- Python 3.8+
- 无特殊依赖，纯指导性质

## 5. 效果展示

```
用户: 帮我重构这段代码
原代码:
result = []
for item in items:
    if item.active:
        result.append(item.name)

助手: 建议使用列表推导式:
result = [item.name for item in items if item.active]

更 Pythonic, 更简洁, 更易读
```

## 6. 优缺点分析

### 优点
- ✅ 专注于代码质量提升
- ✅ 提供实用的重构建议
- ✅ 适合 Python 学习者

### 缺点
- ⚠️ 纯指导性质，无实际执行能力
- ⚠️ 评分相对较低（3.348）
- ⚠️ 需要用户自行实践

## 7. 平替对比

| 技能 | 评分 | 特点 |
|------|------|------|
| friendly-python | 3.348 | 代码风格指导 |
| python-support | 3.306 | 语言支持 |
| python-cookbook | 3.283 | 食谱大全 |
| python | 3.230 | 编码规范 |

**推荐**: 代码风格选 **friendly-python**，语言支持选 **python-support**

## 8. 落地过程

### 第一阶段：安装配置 (2分钟)
1. 安装技能: `clawhub install friendly-python`

### 第二阶段：日常使用 (持续)
- 代码编写时参考
- 代码重构时咨询
- 代码评审时使用

### 推荐安装评估

| 场景 | 推荐 | 理由 |
|------|------|------|
| **本地开发** | ⭐⭐⭐⭐⭐ | 提升代码质量 |
| **ECS 服务器** | ⭐⭐⭐ | 无实际执行需求 |
| **Python 学习** | ⭐⭐⭐⭐⭐ | 最佳学习资源 |

**综合推荐**: ✅ 推荐安装，特别适合 Python 初学者和注重代码质量的开发者。