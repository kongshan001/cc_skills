# FastAPI

## 技能描述

FastAPI 是由 ivangdavila 开发的 Python Web 框架技能，帮助构建快速、生产就绪的 Python APIs，支持类型提示、验证和异步处理。

## 功能列表

### 核心功能
- **异步陷阱**: 避免混合同步/异步数据库驱动，正确使用 asyncio
- **Pydantic 验证**: 模型验证、字段约束、默认值处理
- **依赖注入**: 依赖管理、缓存、清理
- **生命周期**: startup/shutdown 处理，使用 lifespan
- **请求/响应**: 序列化、状态码、媒体类型
- **错误处理**: HTTPException、自定义异常处理器
- **后台任务**: BackgroundTasks 使用
- **安全**: OAuth2、CORS、认证依赖

### 最佳实践
- 使用 asyncpg/aiomysql 而非 psycopg2/PyMySQL
- 使用 Field(default_factory=...) 避免可变默认
- Pydantic v2 方法: model_validate(), model_dump()
- yield 依赖用于清理

## 安装方式

```bash
# 使用 ClawHub 安装
clawhub install fastapi

# 依赖安装
pip install fastapi uvicorn pydantic
```

## 推荐安装评估

| 场景 | 推荐 | 说明 |
|------|------|------|
| 本地开发 | ✅ 推荐 | 快速原型开发和测试 |
| ECS/服务器 | ✅ 推荐 | 生产部署首选异步框架 |

### 本地部署优势
- 快速启动开发服务器
- 内置热重载
- 完整的类型检查支持

### ECS 部署优势
- 高性能异步处理
- 原生支持 ASGI
- 易于容器化部署
- uvicorn/gunicorn 多worker部署
