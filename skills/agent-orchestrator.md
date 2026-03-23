# Agent Orchestrator

## 技能描述

Agent Orchestrator 是由 aatmaan1 开发的代理编排技能，通过将复杂任务分解为子任务、生成自主子代理并整合其工作来编排复杂任务。

## 功能列表

### 核心工作流程

#### 1. 任务分解
- 分析宏任务并分解为独立、可并行的子任务
- 识别依赖关系
- 创建依赖图

#### 2. 代理生成
- `python3 scripts/create_agent.py <agent-name> --workspace <path>`
- 生成目录结构:
  - SKILL.md - 代理技能文件
  - inbox/ - 接收输入文件
  - outbox/ - 交付完成工作
  - workspace/ - 代理工作区
  - status.json - 状态跟踪

#### 3. 代理分发
- 写入任务指令到 inbox/instructions.md
- 复制输入文件到 inbox/
- 使用 Task 工具生成代理

#### 4. 监控 (基于检查点)
- 检查 status.json 状态
- 状态: pending → running → completed | failed

#### 5. 整合
- 收集每个代理 outbox/ 中的输出
- 根据成功标准验证交付物
- 合并/集成输出
- 解决冲突

#### 6. 解散与总结
- 归档代理工作区
- 生成最终总结

### 通信协议
- inbox/ - 代理只读，由编排器写入
- outbox/ - 代理只写，由编排器读取
- status.json - 状态更新

### 预建代理模板
- Research Agent - 网络搜索、数据收集
- Code Agent - 实现、测试
- Analysis Agent - 数据处理、模式发现
- Writer Agent - 内容创建、文档
- Review Agent - 质量保证、编辑
- Integration Agent - 输出合并、冲突解决

## 安装方式

```bash
# 使用 ClawHub 安装
clawhub install agent-orchestrator
```

## 推荐安装评估

| 场景 | 推荐 | 说明 |
|------|------|------|
| 本地开发 | ✅ 推荐 | 复杂项目多代理协作 |
| ECS/服务器 | ⚠️ 需配置 | 需要代理运行环境 |

### 本地部署
- 大型代码库分析
- 市场调研报告
- 多模块项目开发
- 代码审查工作流

### ECS 部署
- 需要 Python 3
- 需要 Task 工具支持
- 适合自动化 CI/CD 流程
