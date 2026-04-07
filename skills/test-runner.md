# Test Runner

> 多框架测试运行器指南

## 技能描述

Test Runner 提供 Vitest、Jest、pytest、XCTest、Playwright 等主流测试框架的命令行参考和最佳实践。

## 功能列表

- Vitest 运行和配置
- Jest 测试运行
- pytest 运行和覆盖率
- XCTest (iOS/macOS) 测试
- Playwright 浏览器测试
- 测试覆盖率报告
- 测试模式和建议

## 安装方式

```bash
clawhub install test-runner
```

## 推荐安装评估

| 环境 | 推荐度 | 说明 |
|------|--------|------|
| 本地开发 | ⭐⭐⭐⭐⭐ | 前端/后端开发必备 |
| CI/CD | ⭐⭐⭐⭐⭐ | 自动化测试必备 |
| ECS/服务器 | ⭐⭐⭐ | 服务器上运行测试 |

## 使用前提

- 对应框架的 CLI 工具（npm, pip, xcodebuild）
- 项目中已配置测试框架

## 注意事项

- 部分命令可能有小错误（如 `uv pip install`），使用前确认命令正确性
- Playwright 会下载浏览器，需确保网络畅通
