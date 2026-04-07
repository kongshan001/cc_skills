# GitHub Actions Generator

> GitHub Actions 工作流生成工具

## 技能描述

GitHub Actions Generator 用于自动生成 GitHub Actions CI/CD 工作流配置。

## 功能列表

- CI 工作流生成
- Deploy 工作流生成
- Node.js 工作流配置

## 安装方式

```bash
clawhub install github-actions-generator
```

## 推荐安装评估

| 环境 | 推荐度 | 说明 |
|------|--------|------|
| 本地开发 | ⭐⭐⭐ | 快速生成工作流 |
| CI/CD | ⭐⭐⭐ | 初始配置 |

## 注意事项

⚠️ 当前版本功能有限：
- 仅支持生成 Node.js 的 CI 和 Deploy 工作流
- Docker/Release/Dependabot 功能未完全实现
- 使用前请验证生成的 workflow 文件
- 建议在测试仓库先试用

## 使用前提

- GitHub 仓库
- GitHub Token（用于某些操作）
