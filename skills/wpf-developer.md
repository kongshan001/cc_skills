# WPF Developer 技能调研报告

## 1. 背景需求

WPF (Windows Presentation Foundation) 是 Windows 桌面应用开发的重要框架。企业级桌面应用仍广泛使用 WPF，需要专业的开发指导。

## 2. 目标

为 Claude Code 提供 WPF 桌面应用开发能力：
- XAML 界面设计
- MVVM 架构
- 数据绑定
- 自定义控件

## 3. 设计方案

### 核心能力
- **XAML 设计**: 响应式界面布局
- **MVVM 模式**: Model-View-ViewModel 架构
- **数据绑定**: 双向绑定和转换器
- **自定义控件**: 复杂 UI 组件开发

### 技术栈
- .NET 8+
- WPF
- MVVM Toolkit
- CommunityToolkit

## 4. 本地部署

```bash
# 安装 WPF Developer 技能
clawhub install wpf-developer
```

### 推荐安装评估
| 环境 | 推荐度 | 说明 |
|------|--------|------|
| 本地 | ⭐⭐⭐⭐⭐ | 桌面开发必需 |
| ECS | ⭐⭐ | 不适合桌面 UI |

## 5. 效果展示

典型应用场景：
- 企业管理软件
- 数据可视化工具
- 系统监控面板
- 配置管理工具

## 6. 优缺点分析

### 优点
- 专注 Windows 桌面开发
- MVVM 最佳实践
- 丰富的 UI 组件

### 缺点
- 仅限 Windows 平台
- 桌面应用市场萎缩

## 7. 平替对比

| 技能 | 特点 |
|------|------|
| wpf-developer | Windows 桌面 WPF |
| csharp-developer | 通用 .NET 开发 |

## 8. 落地过程

1. 执行 `clawhub install wpf-developer`
2. 创建 WPF 项目
3. 设计 XAML 界面
4. 实现 MVVM 逻辑

---
*调研时间: 2026-03-25*
*来源: ClawHub*
