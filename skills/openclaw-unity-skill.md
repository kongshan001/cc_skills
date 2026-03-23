# OpenClaw Unity Skill

## 技能描述

OpenClaw Unity Skill 是由 tomleelive 开发的 Unity 编辑器控制技能，提供约 100 个内置工具，支持在 Editor 和 Play 模式下控制 Unity 编辑器。

## 功能列表

### 连接模式
1. **OpenClaw Gateway (远程)**: Telegram、Discord 等
2. **MCP Bridge (本地)**: Claude Code、Cursor 等本地 AI 工具

### 核心工具分类 (~100 工具)

#### 控制台 (3)
- console.getLogs
- console.getErrors
- console.clear

#### 场景 (7)
- scene.list/getActive/getData
- scene.load/open/save

#### GameObject (8)
- gameobject.find/getAll/create/destroy
- gameobject.getData/setActive/setParent

#### 变换 (6)
- transform.getPosition/Rotation/Scale
- transform.setPosition/Rotation/Scale

#### 组件 (5)
- component.add/remove/get/set/list

#### 脚本 (3)
- script.execute/read/list

#### 调试 (3)
- debug.log/screenshot/hierarchy

#### 编辑器 (9)
- editor.refresh/recompile/domainReload
- editor.getState/play/stop/pause

#### 输入模拟 (10)
- input.keyPress/keyDown/keyUp
- input.type/mouseMove/mouseClick
- input.mouseDrag/scroll/clickUI

#### 材质 (5)
- material.create/assign/modify/getInfo/list

#### 预制件 (5)
- prefab.create/instantiate/open/close/save

#### 资源 (7)
- asset.find/copy/move/delete/refresh

#### 包管理 (4)
- package.add/remove/list/search

#### 测试运行器 (3)
- test.run/list/getResults

### 常用工作流
- 场景检查
- 查找/修改对象
- UI 测试
- Play 模式控制
- 材质创建
- 预制件工作流
- 资源管理
- 包管理
- 测试运行

## 安装方式

```bash
# 使用 ClawHub 安装
clawhub install openclaw-unity-skill

# MCP Bridge 启动
# Window → OpenClaw Plugin → MCP Bridge → Start
# 默认端口: 27182
```

## 推荐安装评估

| 场景 | 推荐 | 说明 |
|------|------|------|
| 本地开发 | ✅ 推荐 | Unity 项目开发测试必备 |
| ECS/服务器 | ❌ 不推荐 | 需要 Unity Editor 环境 |

### 本地部署
- Unity 游戏开发
- UI 自动化测试
- 资源批量处理
- 场景编辑自动化

### ECS 部署
- 不适用（需要 Unity Editor）
- CI/CD 可使用 Unity Build Runner
