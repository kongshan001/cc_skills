# Docker Compose Generator

## 1. 背景需求

现代应用通常由多个服务组成（数据库、缓存、后端、前端），手动编写 docker-compose.yml 容易出错：
- 端口映射遗漏或冲突
- 环境变量配置不完整
- 网络和卷配置复杂
- 服务依赖关系处理不当

需要一个能根据需求自动生成正确配置的生成器。

## 2. 目标

根据应用场景自动生成 docker-compose.yml 配置：
- 支持 MySQL、PostgreSQL、Redis、MongoDB、Elasticsearch 等常用服务
- 自动配置网络、卷、环境变量
- 服务依赖和启动顺序管理
- 健康检查配置
- 常用最佳实践内置

## 3. 设计方案

**生成模板**：
| 服务类型 | 默认配置 |
|----------|----------|
| MySQL | 8.0, 持久化卷, 字符集配置 |
| PostgreSQL | 15, 持久化卷, 健康检查 |
| Redis | latest, 密码可选, 持久化 |
| MongoDB | latest, 认证可选, 端口映射 |
| Elasticsearch | 单节点开发配置 |

**高级特性**：
- 多服务组合生成
- 环境变量模板化
- 开发者模式 vs 生产模式
- 端口冲突自动检测

## 4. 本地部署

```bash
clawhub install docker-compose-generator
```

**依赖**：
- Docker Compose
- Docker CLI

**验证**：
```bash
docker-compose --version
```

## 5. 效果展示

触发示例：
- "生成包含 MySQL 和 Redis 的 compose 配置"
- "帮我写一个 PostgreSQL 服务的 docker-compose"
- "我想跑一个 ELK stack，需要哪些服务"

执行效果：AI 生成完整的 docker-compose.yml，可直接使用。

## 6. 优缺点分析

| 优点 | 缺点 |
|------|------|
| 生成速度快 | 模板有限 |
| 配置正确性高 | 自定义灵活性一般 |
| 减少手动错误 | 生产环境需要加固 |
| 开箱即用 | 无版本控制支持 |

## 7. 平替对比

| 方案 | 特点 | 适用场景 |
|------|------|----------|
| Docker Compose Generator（当前） | 自动生成模板 | 快速搭建环境 |
| Docker Helper | 手动+辅助 | 需要细粒度控制 |
| 在线生成器 | 图形界面 | 偶尔使用 |

## 8. 落地过程

**推荐安装评估**：
- **本地开发机** ⭐⭐⭐⭐⭐ — 日常开发必备
- **ECS 云服务器** ⭐⭐⭐⭐ — 部署环境搭建

**使用建议**：
1. 生成后根据实际调整
2. 结合 Git 管理版本
3. 生产环境建议添加资源限制

**版本**：1.0.1 | **作者**：sunshine-del-ux | **更新**：2026-03-29 | **标签**：devops, docker, docker-compose, generator