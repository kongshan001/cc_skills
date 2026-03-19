# Python Expert - Python 开发专家技能

## 1. 背景需求

Python 是当前最流行的编程语言之一，广泛应用于 Web 开发、数据科学、自动化和 AI 领域。开发者需要：

- 高质量的 Python 代码编写
- 遵循 Pythonic 编程风格
- 性能优化建议
- 最佳实践指导

## 2. 目标

Python Expert 是一个专注于 Python 开发的 Claude Code 子代理，提供专业的 Python 开发支持。

## 3. 设计方案

### 核心能力

| 能力 | 说明 |
|------|------|
| 代码编写 | 高质量 Python 代码生成 |
| 代码审查 | Python 代码专项审查 |
| 性能优化 | Python 性能分析和优化建议 |
| 错误调试 | Python 异常和错误排查 |
| 框架支持 | FastAPI, Django, Flask 等 |

### 专业领域

1. **Web 开发**：FastAPI, Django, Flask
2. **异步编程**：asyncio, aiohttp
3. **数据处理**：pandas, numpy
4. **类型安全**：typing, pydantic, mypy
5. **测试**：pytest, unittest

## 4. 本地部署

### 安装方式

```bash
/plugin install python-expert
```

### 环境要求

- Python 3.8+ 环境
- Claude Code 已安装

## 5. 效果展示

### 使用示例

```
"Write a FastAPI endpoint for user management"
"Review this Python code for performance issues"
"Debug this asyncio error"
"Add type hints to this function"
```

### 输出示例

```python
# 生成的代码示例
from fastapi import FastAPI, HTTPException
from pydantic import BaseModel, EmailStr
from typing import Optional
import asyncio

app = FastAPI()

class UserCreate(BaseModel):
    name: str
    email: EmailStr
    age: Optional[int] = None

@app.post("/users", response_model=UserCreate)
async def create_user(user: UserCreate) -> UserCreate:
    # Implementation with proper error handling
    await asyncio.sleep(0.1)  # Simulated DB operation
    return user
```

## 6. 优缺点分析

### 优点

| 优势 | 说明 |
|------|------|
| 专注 Python | 深度理解 Python 生态 |
| 类型安全 | 强调类型注解和 Pydantic |
| 异步支持 | 专业的 asyncio 编程建议 |
| 框架熟悉 | 主流框架的深入了解 |

### 缺点

| 劣势 | 说明 |
|------|------|
| 单一语言 | 只支持 Python |
| 依赖上下文 | 需要足够的代码上下文 |

## 7. 平替对比

| 工具 | 定位 | 优势 | 劣势 |
|------|------|------|------|
| Python Expert | Python 专项开发 | 深度 Python 支持 | 单一语言 |
| Claude Code | 通用编码 | 全语言支持 | 不专注 Python |
| GitHub Copilot | AI 编码辅助 | 通用能力强 | 非 Python 专项 |

## 8. 落地过程

### 使用场景

```bash
# 新项目启动
"Help me set up a FastAPI project with proper structure"

# 代码编写
"Write a data processing pipeline using asyncio"

# 代码审查
"Review this Python code for best practices"

# 性能优化
"Optimize this slow Python function"
```

### 最佳实践

- Python 项目中作为主力代理使用
- 配合类型检查工具（mypy）使用
- 遵循项目现有的代码风格

---

**推荐安装方式**：本地开发环境（Desktop/Laptop）

**资源链接**：Development Engineering 类别 - ccplugins/awesome-claude-code-plugins
