# Friendly Python - 友好Python编程指南

## 技能描述
编写友好Python代码的实用指导技能，专注于清晰、可维护和易于扩展的Pythonic风格。包括代码重构、代码审查和API设计指导，如果项目中包含piglet技能，建议同时使用以获得更好的Python工匠模式。

## 功能列表
- **代码编写指导**: 新代码编写、重构指导、代码审查
- **API设计**: 默认值和简单入口点；隐藏内部连接
- **扩展架构**: 集中化扩展点和变更位置
- **面向对象设计**: 清晰的构造函数；避免__init__中的模式切换
- **重用与组合**: 优先使用轻量级包装器和组合
- **可移植性与Pythonic**: 避免复制其他语言模式；保持Pythonic
- **CLI argparse**: 解析与执行分离；结构化子命令
- **代码审查**: 代码质量审查清单

## 核心原则
1. **正确性优先**: 首先确保正确性和清晰边界
2. **可读性和可维护性**: 其次考虑可读性和可维护性
3. **可扩展性**: 然后考虑扩展性和演化成本
4. **性能优化**: 最后考虑性能和优化

## 决策流程
```
1. 定位相关主题
2. 应用指导和建议
3. 如果$piglet可用，建议同时使用
4. 对照[references/review-checklist.md]进行审查
```

## 主题分类
| 主题 | 指导 | 参考 |
|---|---|---|
| 原则 | 正确性第一，清晰性第二，性能第三 | [references/principles.md](references/principles.md) |
| 错误处理 | 只捕获能够处理的异常；保留上下文 | [references/error-handling.md](references/error-handling.md) |
| API设计 | 默认值和简单入口点；隐藏内部连接 | [references/api-design.md](references/api-design.md) |
| 扩展架构 | 集中化扩展点和变更位置 | [references/extension-architecture.md](references/extension-architecture.md) |
| OOP设计 | 清晰的构造函数；避免__init__中的模式切换 | [references/oop-design.md](references/oop-design.md) |
| 重用与组合 | 优先使用轻量级包装器和组合 | [references/reuse-composition.md](references/reuse-composition.md) |

## 使用场景
- Python开发者进行代码编写和重构
- API设计和CLI工具开发
- 代码审查和质量保证
- 学习Pythonic编程风格

## 最佳实践
- 优先考虑正确性和清晰性
- 避免过度优化
- 保持代码简洁明了
- 注重可维护性和扩展性
- 遵循Python社区最佳实践

## 安装方式
```bash
# 无需额外安装
# 直接在Python项目中应用指导

# 如果需要piglet辅助
clawhub install piglet
```

## 推荐安装评估

### 本地部署
**适用场景**:
- 个人Python开发者
- 小型项目和个人工具
- 学习Python编程规范
- 代码质量提升需求

**优势**:
- 即时应用指导
- 本地开发环境
- 学习过程可视化
- 快速迭代和改进
- 无额外依赖

**ECS部署**
**适用场景**:
- 大型Python项目团队
- 企业级开发团队
- 标准化代码审查流程
- 多人协作开发

**优势**:
- 统一的代码标准
- 团队协作审查
- 质量控制和保证
- 持续集成支持
- 知识库积累和共享

**选择建议**: 个人开发者和小团队推荐本地部署，大型团队和企业项目选择ECS部署。