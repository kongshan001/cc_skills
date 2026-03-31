# Game Engine Skill - Web游戏引擎开发

## 技能描述
使用HTML5 Canvas、WebGL和JavaScript构建基于Web的游戏引擎和游戏的专家技能。包括启动模板、参考文档和分步工作流程，用于2D和3D游戏开发，支持Phaser、Three.js、Babylon.js和A-Frame等框架。

## 功能列表
- **游戏循环实现**: requestAnimationFrame优化渲染
- **渲染系统**: Canvas 2D、WebGL 3D、SVG矢量图形、CSS DOM元素
- **物理与碰撞检测**: 2D碰撞检测(AABB、圆形、SAT)、3D碰撞检测、速度加速度、重力
- **控制系统**: 键盘输入、鼠标控制、触摸支持、手柄API
- **音频系统**: Web Audio API、HTML5音频
- **游戏类型支持**: 2D平台游戏、Breakout风格游戏、迷宫游戏、3D体验
- **地图系统**: 瓦片地图、精灵表、动画系统
- **发布功能**: Web游戏发布、平台集成、分发策略
- **性能优化**: 代码压缩、资源优化、跨浏览器测试
- **多人游戏**: WebRTC、WebSockets多人实现

## 核心概念
### 游戏循环
```
1. 处理输入 - 读取键盘、鼠标、触摸或手柄输入
2. 更新状态 - 更新游戏对象位置、物理、AI和逻辑
3. 渲染 - 将当前游戏状态绘制到屏幕
```

### 渲染方式
- **Canvas 2D**: 2D游戏、精灵渲染、瓦片地图
- **WebGL**: 硬件加速3D和高级2D渲染
- **SVG**: 矢量图形元素
- **CSS**: DOM-based游戏元素和过渡

### 项目模板
- paddle-game-template.md - 纯JavaScript的2D Breakout风格游戏
- 2d-maze-game.md - 设备方向控制的迷宫游戏
- 2d-platform-game.md - 使用Phaser框架的平台游戏
- simple-2d-engine.md - 带碰撞的简单2D平台游戏引擎

## 安装方式
```bash
# 基础依赖
npm install
# 或
yarn install

# 开发服务器（如果需要）
npm run dev
# 或
yarn dev

# 构建生产版本
npm run build
# 或
yarn build
```

**前置要求**:
- 基础HTML、CSS、JavaScript知识
- 支持Canvas/WebGL的现代浏览器
- 文本编辑器或IDE
- 可选：Node.js用于构建工具和本地开发服务器

## 推荐安装评估

### 本地部署
**适用场景**:
- 独立开发者、小型游戏工作室
- Web游戏原型开发
- 学习游戏开发概念
- 个人项目开发

**优势**:
- 零部署成本，本地开发
- 快速迭代和调试
- 完全控制开发环境
- 学习曲线平缓
- 即时反馈

**ECS部署**
**适用场景**:
- 专业游戏开发团队
- 多人协作项目
- 大型Web游戏开发
- 企业级项目管理

**优势**:
- 统一的开发环境
- 团队协作功能
- 代码管理和版本控制
- CI/CD集成
- 性能监控和优化
- 自动化测试

**选择建议**: 个人学习和小型项目推荐本地部署，专业团队和商业项目选择ECS部署。