# ClawHub 热门技能调研报告

> Claude Code 热门 Skills 调研成果

## 索引表格

| 类别 | 技能名称 | Slug | 评分 | 版本 | 推荐安装 |
|------|----------|------|------|------|----------|
| GitHub | OpenClaw GitHub Assistant | openclaw-github-assistant | 3.676 | 2.0.1 | 本地/ECS |
| GitHub | GitHub CLI | github-cli | 3.596 | 1.0.0 | 本地 |
| GitHub | GitHub Ops | github-ops | 3.530 | 1.0.0 | 本地/ECS |
| Docker | Docker Essentials | docker-essentials | 3.721 | 1.0.0 | 本地/ECS |
| Docker | Docker Sandbox | docker-sandbox | 3.565 | 1.0.0 | 本地/ECS |
| Docker | Docker Compose | docker-compose | 3.550 | 1.0.0 | 本地/ECS |
| DevOps | DevOps | devops | 3.713 | 1.0.0 | ECS |
| DevOps | Senior DevOps | senior-devops | 3.554 | 2.1.1 | ECS |
| DevOps | Azure DevOps | azure-devops | 3.482 | 1.0.0 | ECS |
| Python | Python Dataviz | python-dataviz | 3.492 | 1.0.0 | 本地 |
| Python | LSP Python | lsp-python | 3.424 | 1.1.0 | 本地 |
| Web | Web Pilot | web-pilot | 3.517 | 1.0.0 | 本地/ECS |
| Web | Web Development | web | 3.510 | 1.0.0 | 本地/ECS |

## 技能分类

### GitHub 工具
- [OpenClaw GitHub Assistant](./skills/openclaw-github-assistant.md) - GitHub 仓库管理和自动化
- [GitHub CLI](./skills/github-cli.md) - GitHub CLI 全命令参考
- [GitHub Ops](./skills/github-ops.md) - 自动化仓库操作和 Release 管理

### Docker 容器
- [Docker Essentials](./skills/docker-essentials.md) - Docker 核心命令和工作流
- [Docker Sandbox](./skills/docker-sandbox.md) - 安全沙箱环境
- [Docker Compose](./skills/docker-compose.md) - 多容器应用编排

### DevOps 工具
- [DevOps](./skills/devops.md) - 部署自动化和 CI/CD
- [Senior DevOps](./skills/senior-devops.md) - 高级 DevOps 多云支持
- [Azure DevOps](./skills/azure-devops.md) - Azure 平台 DevOps

### Python 开发
- [Python Dataviz](./skills/python-dataviz.md) - 数据可视化
- [LSP Python](./skills/lsp-python.md) - Python 代码质量检查

### Web 开发
- [Web Pilot](./skills/web-pilot.md) - 网页搜索和内容抓取
- [Web Development](./skills/web.md) - Web 开发最佳实践

## 安装方式

```bash
# 安装所有技能
for skill in openclaw-github-assistant github-cli github-ops docker-essentials docker-sandbox docker-compose devops senior-devops azure-devops python-dataviz lsp-python web-pilot web; do
    clawhub install $skill
done
```

## 推荐安装评估说明

- ⭐⭐⭐⭐⭐ 本地/ECS 必备 - 强烈推荐安装
- ⭐⭐⭐⭐ 适合安装 - 推荐根据需求安装
- ⭐⭐⭐ 可选安装 - 有特定需求时安装

## 贡献

欢迎提交 Issue 和 PR 来完善这个技能列表。

## 许可证

MIT
