# Skill Compiler - 技能编译器

## 技能描述

**Skill Compiler** 将 SKILL.md 文件编译为运行时工件（SKILL.struct.json 和 SKILL.toon），验证新鲜度/健康状态，准备可移植的发布就绪技能文件夹。

- **最新版本**: 0.2.0
- **作者**: shaoyanji
- **更新时间**: 2026-04-21
- **标签**: compiler, build, publish

## 功能列表

- SKILL.md 编译为结构化 JSON
- 生成 SKILL.toon 运行时工件
- 技能新鲜度验证
- 健康状态检查
- 发布就绪打包

## 安装方式

```bash
clawhub install skill-compiler
```

## 推荐安装评估

| 场景 | 推荐 | 说明 |
|------|------|------|
| 本地开发 | ✅ 适合 | 技能打包发布 |
| ECS 服务器 | ✅ 适合 | CI/CD 自动化构建 |

## 适用场景

- 技能发布打包
- 自动化构建流程
- 技能版本管理