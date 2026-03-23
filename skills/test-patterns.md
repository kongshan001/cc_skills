# Test Patterns

## 技能描述

Test Patterns 是由 gitgoodordietrying 开发的测试技能，涵盖跨语言的单元测试、集成测试、E2E 测试、mocking、覆盖率测量和 TDD 工作流程。

## 功能列表

### Node.js (Jest / Vitest)
- 单元测试编写
- 异步测试
- Mocking (模块、fetch、spy)
- 覆盖率测量
- TDD 工作流

### Python (pytest)
- 单元测试 (pytest)
- 参数化测试 (@pytest.mark.parametrize)
- Fixtures (tmp_path, mock)
- Mocking (unittest.mock)
- 覆盖率 (pytest-cov)

### Go
- 单元测试
- 表驱动测试
- 覆盖率
- 竞态检测 (-race)
- Benchmark

### Rust
- 单元测试
- 集成测试
- 覆盖率 (cargo-tarpaulin)
- 错误处理测试

### Bash
- 简单测试运行器
- assert_eq/assert_exit_code/assert_contains

### 集成测试
- API 集成测试
- 数据库集成测试
- 服务启动/停止

### TDD 工作流
- Red-Green-Refactor 循环
- 监视模式 (jest --watch, ptw)

### 调试失败的测试
- 共享状态问题
- 异步操作问题
- 覆盖率分析
- 单测试运行

## 安装方式

```bash
# 使用 ClawHub 安装
clawhub install test-patterns
```

## 推荐安装评估

| 场景 | 推荐 | 说明 |
|------|------|------|
| 本地开发 | ✅ 推荐 | 测试驱动开发必备 |
| ECS/服务器 | ✅ 推荐 | CI/CD 流程测试必备 |

### 本地部署
- 项目测试套件搭建
- TDD 开发流程
- 测试调试

### ECS 部署
- CI/CD 自动化测试
- 代码质量把控
- 覆盖率门禁
