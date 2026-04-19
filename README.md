# ClawHub 热门技能调研报告

> 自动化调研 ClawHub 热门技能并生成独立调研文档

## 技能索引

| 技能名称 | 描述 | 本地开发 | ECS/服务器 | 文档 |
|----------|------|:--------:|:----------:|------|
| docker-essentials | Docker  Essentials - Docker 容器管理核心命令和工作流程 | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | [查看](./skills/docker-essentials.md) |
| python-executor | Python Executor - 安全沙箱环境执行 Python 代码 | ⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | [查看](./skills/python-executor.md) |
| github-cli | GitHub CLI - 全面的 gh CLI 参考 | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | [查看](./skills/github-cli.md) |
| k8s-debug | K8s Debug - Kubernetes Pod 故障诊断 | ⭐⭐ | ⭐⭐⭐⭐⭐ | [查看](./skills/k8s-debug.md) |
| kubernetes-devops | Kubernetes DevOps - K8s 资源清单生成 | ⭐⭐⭐ | ⭐⭐⭐⭐⭐ | [查看](./skills/kubernetes-devops.md) |
| openclaw-github-assistant | OpenClaw GitHub Assistant - GitHub 仓库管理 | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | [查看](./skills/openclaw-github-assistant.md) |
| test-runner | Test Runner - 单元/集成/E2E 测试 | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | [查看](./skills/test-runner.md) |
| docker-compose | Docker Compose - 多容器应用定义 | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | [查看](./skills/docker-compose.md) |

## 调研方法

使用 `clawhub search` 命令搜索热门方向：

- Docker 相关: docker-essentials, docker-compose, docker-sandbox
- Python 开发: python-executor, python-script-generator
- Kubernetes: k8s-debug, kubernetes-devops
- GitHub: github-cli, openclaw-github-assistant
- 测试: test-runner, test-master

## 安装方式

```bash
# 安装单个技能
clawhub install <skill-name>

# 查看所有可用技能
clawhub list
```

## 更新日志

- 2026-04-19: 初始化调研，生成 8 个热门技能报告