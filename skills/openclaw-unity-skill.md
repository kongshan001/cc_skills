# Unity Plugin Skill - Unity Editor控制技能

## 技能描述
通过OpenClaw Unity插件控制Unity Editor的全能技能。提供~100个内置工具，支持场景管理、GameObject/组件操作、调试、输入模拟和Play模式控制。支持Unity开发任务，包括场景检查、对象创建、截图、游戏测试和编辑器控制。

## 功能列表
- **场景管理**: 活动场景获取、场景数据读取、场景加载/打开/保存
- **GameObject操作**: 对象查找、获取所有对象、创建对象、销毁对象
- **组件管理**: 组件获取/设置、组件添加/移除、组件列表
- **变换操作**: 位置/旋转/缩放获取和设置
- **调试功能**: 层级查看、截图、控制台日志获取
- **输入模拟**: UI点击、文本输入、按键按下、鼠标操作
- **编辑器控制**: 状态获取、播放/停止、刷新、窗口聚焦
- **材质系统**: 材质创建、分配、修改、信息获取
- **预制体管理**: 预制体创建、实例化、打开、保存
- **资源管理**: 资源查找、复制、移动、删除
- **包管理**: 包安装、卸载、列表、搜索
- **测试运行器**: 测试执行、列表、结果获取
- **批执行**: 多工具并行执行（10-100倍性能提升）
- **MCP桥接**: 支持Claude Code/Cursor集成

## 连接模式
### 1. OpenClaw Gateway（远程）
- 用于Telegram、Discord和其他OpenClaw频道
- Unity打开时自动连接
- 配置位置：Window → OpenClaw Plugin → Settings

### 2. MCP Bridge（本地）
- 用于Claude Code、Cursor和本地AI工具
- 启动：Window → OpenClaw Plugin → MCP Bridge → Start
- 默认端口：27182

## 安装方式
```bash
# 第一次设置（如果未安装扩展）
./scripts/install-extension.sh

# 重启网关
openclaw gateway restart

# MCP桥接设置
claude mcp add unity -- node <path>/MCP~/index.js
```

## 常用工作流
```bash
# 场景检查
unity_execute: debug.hierarchy {depth: 2}
unity_execute: scene.getActive

# 对象查找与修改
unity_execute: gameobject.find {name: "Player"}
unity_execute: component.get {name: "Player", componentType: "Transform"}
unity_execute: transform.setPosition {name: "Player", x: 0, y: 5, z: 0}

# UI测试
unity_execute: input.clickUI {name: "PlayButton"}
unity_execute: input.type {text: "TestUser", elementName: "UsernameInput"}

# Play模式控制
unity_execute: editor.play
unity_execute: editor.stop
unity_execute: editor.pause
unity_execute: editor.unpause
```

## 推荐安装评估

### 本地部署
**适用场景**:
- 个人开发者、小型团队
- 需要快速迭代和调试
- 单机开发环境
- 学习Unity开发

**优势**:
- 即时响应，低延迟
- 本地数据安全
- 开发环境配置简单
- 离线工作能力强
- 成本低廉

**ECS部署**
**适用场景**:
- 大型游戏开发团队
- 多人协作开发
- 远程团队协作
- 企业级项目管理
- 云端开发环境

**优势**:
- 远程访问，随时随地开发
- 资源集中管理
- 统一的开发环境
- 团队协作功能完善
- 高可用性和备份
- 集成CI/CD流程

**选择建议**: 个人开发和小团队推荐本地部署，大型团队和远程协作选择ECS部署。