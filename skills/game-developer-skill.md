# Game Developer Skill

## 技能描述

Game Developer Skill 是由 cryptorabea 开发的游戏开发技能，适用于构建游戏系统、实现 Unity/Unreal 特性或优化游戏性能。提供 Unity、Unreal、游戏模式、ECS、物理、网络等方面的专家指导。

## 功能列表

### 引擎开发
- Unity C# 开发 (MonoBehaviour, Scriptable Objects)
- Unreal C++ 开发 (Blueprints, Actor components)
- ECS 架构模式
- 跨平台优化

### 游戏系统
- ECS (Entity Component System)
- 物理系统优化
- AI 实现
- 网络同步

### 性能优化
- 60+ FPS 目标实现
- 对象池化
- LOD 系统
- 内存管理
- GPU/CPU 优化

### 设计模式
- 状态机
- 命令模式
- 观察者模式
- 对象池

### 核心约束
- ✅ 必须实现
  - 60+ FPS 目标
  - 对象池化
  - LOD 系统
  - 性能分析
  - 异步加载
  - 状态机
  - 组件缓存
  - 增量时间移动

- ❌ 避免做法
  - Update() 中 Instantiate/Destroy
  - 跳过性能测试
  - 字符串比较标签
  - Update 中内存分配
  - Find 方法滥用

## 安装方式

```bash
# 使用 ClawHub 安装
clawhub install game-developer-skill
```

## 推荐安装评估

| 场景 | 推荐 | 说明 |
|------|------|------|
| 本地开发 | ✅ 推荐 | 游戏客户端开发必备 |
| ECS/服务器 | ❌ 不推荐 | 服务端逻辑无需此技能 |

### 本地部署
- Unity/Unreal 项目开发
- 游戏原型制作
- 性能优化调试

### ECS 部署
- 不适用（客户端技能）
- 游戏服务器开发可考虑其他技能
