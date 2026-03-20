# ClawHub 热门技能调研报告

> 本仓库包含 ClawHub 平台上热门技能的详细调研报告，涵盖 Docker、Python、Kubernetes、数据库、游戏开发、测试等多个领域。

## 📊 调研概览

- **调研时间**: 2026-03-20
- **技能数量**: 20 个热门技能
- **数据来源**: ClawHub (https://clawhub.com)
- **调研方法**: 使用 `clawhub search` 和 `clawhub inspect` 获取技能信息

## 📑 技能索引

### 🐳 Docker & 容器

| 技能名称 | 描述 | 搜索分数 | 推荐度 | 报告链接 |
|---------|------|---------|--------|---------|
| **docker-essentials** | Docker 容器管理基础命令和工作流 | 3.719 | ⭐⭐⭐⭐⭐ | [查看报告](./skills/docker-essentials.md) |
| **docker-sandbox** | 创建和管理 Docker 沙箱环境，安全执行代理代码 | 3.563 | ⭐⭐⭐⭐⭐ | [查看报告](./skills/docker-sandbox.md) |
| **docker-compose** | 定义多容器应用，依赖处理和网络管理 | 3.547 | ⭐⭐⭐⭐⭐ | [查看报告](./skills/docker-compose.md) |

### 🐍 Python 开发

| 技能名称 | 描述 | 搜索分数 | 推荐度 | 报告链接 |
|---------|------|---------|--------|---------|
| **python-dataviz** | 专业数据可视化（matplotlib, seaborn, plotly） | 3.488 | ⭐⭐⭐⭐⭐ | [查看报告](./skills/python-dataviz.md) |
| **python-script-generator** | Python 脚本和应用模板生成器 | 3.409 | ⭐⭐⭐⭐⭐ | [查看报告](./skills/python-script-generator.md) |

### 🧪 测试 & 自动化

| 技能名称 | 描述 | 搜索分数 | 推荐度 | 报告链接 |
|---------|------|---------|--------|---------|
| **api-test-automation** | REST/GraphQL API 测试自动化工具 | 2.968 | ⭐⭐⭐⭐⭐ | [查看报告](./skills/api-test-automation.md) |
| **test-runner** | 单元、集成和 E2E 测试运行器 | 1.242 | ⭐⭐⭐⭐⭐ | [查看报告](./skills/test-runner.md) |

### 🐙 GitHub & 版本控制

| 技能名称 | 描述 | 搜索分数 | 推荐度 | 报告链接 |
|---------|------|---------|--------|---------|
| **github** | GitHub CLI (gh) 集成，管理 Issues/PRs/CI | 2.833 | ⭐⭐⭐⭐⭐ | [查看报告](./skills/github.md) |
| **openclaw-github-assistant** | OpenClaw GitHub 仓库管理助手 | 2.631 | ⭐⭐⭐⭐ | [查看报告](./skills/openclaw-github-assistant.md) |

### 🌐 Web 开发

| 技能名称 | 描述 | 搜索分数 | 推荐度 | 报告链接 |
|---------|------|---------|--------|---------|
| **web** | HTML/CSS/JavaScript 网站构建和部署 | 2.229 | ⭐⭐⭐⭐⭐ | [查看报告](./skills/web-development.md) |

### ☸️ Kubernetes

| 技能名称 | 描述 | 搜索分数 | 推荐度 | 报告链接 |
|---------|------|---------|--------|---------|
| **kubernetes** | K8s 最佳实践，避免常见错误 | 1.026 | ⭐⭐⭐⭐⭐ | [查看报告](./skills/kubernetes.md) |
| **kubectl** | Kubernetes 集群管理和命令工具 | 1.085 | ⭐⭐⭐⭐⭐ | [查看报告](./skills/kubectl.md) |

### 🗄️ 数据库

| 技能名称 | 描述 | 搜索分数 | 推荐度 | 报告链接 |
|---------|------|---------|--------|---------|
| **sql-toolkit** | SQL 查询、设计、迁移和优化工具 | 1.163 | ⭐⭐⭐⭐⭐ | [查看报告](./skills/sql-toolkit.md) |
| **database-operations** | 数据库操作和性能优化 | 1.112 | ⭐⭐⭐⭐⭐ | [查看报告](./skills/database-operations.md) |
| **mysql** | MySQL 查询编写和优化 | 1.010 | ⭐⭐⭐⭐ | [查看报告](./skills/mysql.md) |
| **postgresql** | PostgreSQL 查询和 Schema 设计 | 0.983 | ⭐⭐⭐⭐ | [查看报告](./skills/postgresql.md) |

### 🎮 游戏开发

| 技能名称 | 描述 | 搜索分数 | 推荐度 | 报告链接 |
|---------|------|---------|--------|---------|
| **godot-dev-guide** | Godot 4.x 完整开发指南 | 1.044 | ⭐⭐⭐⭐⭐ | [查看报告](./skills/godot-dev-guide.md) |
| **game-cog** | AI 驱动的游戏设计推理工具 | 1.036 | ⭐⭐⭐⭐ | [查看报告](./skills/game-cog.md) |
| **unity** | Unity 常见错误避免和优化 | 0.979 | ⭐⭐⭐⭐ | [查看报告](./skills/unity.md) |
| **blender** | Blender 3D 建模和导出最佳实践 | 0.957 | ⭐⭐⭐⭐ | [查看报告](./skills/blender.md) |

## 📝 报告格式

每个技能报告包含以下内容：

1. **技能描述** - 技能的基本介绍和用途
2. **功能列表** - 技能提供的主要功能
3. **安装方式** - 如何安装和使用该技能
4. **推荐安装评估**
   - 本地环境适用性
   - ECS/云服务器适用性
5. **使用场景** - 典型的应用场景
6. **相关技能** - 相关的其他技能推荐
7. **来源** - ClawHub 链接和搜索分数

## 🚀 快速开始

### 安装 ClawHub CLI

```bash
npm install -g clawhub
```

### 安装技能

```bash
# 安装任意技能
clawhub install <skill-slug>

# 例如安装 docker-essentials
clawhub install docker-essentials
```

### 查看技能详情

```bash
clawhub inspect <skill-slug>
```

## 📊 推荐度说明

- ⭐⭐⭐⭐⭐ **强烈推荐** - 必备技能，适用于大多数场景
- ⭐⭐⭐⭐ **推荐** - 常用技能，特定场景下很有价值
- ⭐⭐⭐ **可选** - 根据需求选择安装

## 🔗 相关链接

- **ClawHub 官网**: https://clawhub.com
- **ClawHub 技能市场**: https://clawhub.com/skills
- **OpenClaw 文档**: https://docs.openclaw.ai
- **GitHub 仓库**: https://github.com/kongshan001/cc_skills

## 📄 License

MIT License

---

**最后更新**: 2026-03-20  
**维护者**: OpenClaw Agent
