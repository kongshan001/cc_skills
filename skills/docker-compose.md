# Docker Compose

## 技能描述

Define multi-container applications with proper dependency handling, networking, and volume management.

**所有者**: ivangdavila  
**创建时间**: 2026-02-10  
**最新版本**: 1.0.0  
**ClawHub Slug**: `docker-compose`

## 功能列表

- 多容器应用定义
- 服务依赖管理
- 网络配置
- 卷管理
- 环境变量管理
- 服务编排
- 开发环境标准化
- 生产环境部署

## 安装方式

```bash
clawhub install docker-compose
```

或指定版本：

```bash
clawhub install docker-compose --version 1.0.0
```

## 推荐安装评估

### 本地环境
- ✅ **强烈推荐** - 本地开发环境标准化必备
- 适合微服务开发
- 需要 Docker 和 Docker Compose
- 资源占用取决于服务数量

### ECS/云服务器
- ✅ **强烈推荐** - 生产环境部署常用工具
- 适合容器化应用部署
- 需要配置资源和网络
- 建议配合 Docker Swarm 或 K8s

## 使用场景

1. 本地开发环境搭建
2. 微服务编排
3. CI/CD 流水线
4. 测试环境部署
5. 生产环境部署（小型）
6. 服务依赖管理
7. 数据持久化配置

## 常用配置

```yaml
version: '3.8'
services:
  web:
    build: .
    ports:
      - "3000:3000"
    depends_on:
      - db
  db:
    image: postgres:13
    volumes:
      - db-data:/var/lib/postgresql/data
volumes:
  db-data:
```

## 相关技能

- docker-essentials - Docker 基础
- docker-sandbox - Docker 沙箱
- kubernetes - 容器编排（高级）

## 来源

- **ClawHub**: https://clawhub.com/skills/docker-compose
- **搜索分数**: 3.547（Docker 类别高分）
