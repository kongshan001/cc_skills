# Test Patterns

> 多语言测试模式和最佳实践

## 技能描述

Test Patterns 提供 Node.js、Python、Go、Rust、Bash 等语言的测试模式和最佳实践指南，包括单元测试、集成测试、模拟和覆盖率。

## 功能列表

- Node.js 测试（Jest, Mocha）
- Python 测试（pytest）
- Go 测试
- Rust 测试
- Bash 脚本测试
- 测试模拟（Mocking）
- 测试覆盖率配置
- 临时数据库设置

## 安装方式

```bash
clawhub install test-patterns
```

## 推荐安装评估

| 环境 | 推荐度 | 说明 |
|------|--------|------|
| 本地开发 | ⭐⭐⭐⭐⭐ | 开发必备 |
| CI/CD | ⭐⭐⭐⭐⭐ | 自动化测试必备 |
| ECS/服务器 | ⭐⭐⭐ | 服务器端测试 |

## 使用前提

- 对应语言的运行时（node, python3, go, cargo, bash）
- 已配置测试框架

## 注意事项

- 运行测试会执行仓库代码，可能包含网络调用或数据库交互
- 建议在隔离环境运行测试
- 安装依赖会拉取第三方代码
