# Kubernetes

## 技能描述

Avoid common Kubernetes mistakes — resource limits, probe configuration, selector mismatches, and RBAC pitfalls.

**所有者**: ivangdavila  
**创建时间**: 2026-02-10  
**最新版本**: 1.0.0  
**ClawHub Slug**: `k8s`

## 功能列表

- Kubernetes 最佳实践指导
- 资源限制配置
- 健康检查探针配置
- Selector 匹配检查
- RBAC 配置审计
- 常见错误避免
- YAML 配置验证

## 安装方式

```bash
clawhub install k8s
```

或指定版本：

```bash
clawhub install k8s --version 1.0.0
```

## 推荐安装评估

### 本地环境
- ✅ **推荐** - 适合学习和开发
- 需要 kubectl 和 kubeconfig 配置
- 可配合 minikube 或 kind 使用
- 适合 DevOps 工程师

### ECS/云服务器
- ✅ **强烈推荐** - 生产环境 K8s 管理必备
- 避免生产环境常见错误
- 需要集群访问权限
- 建议配合 kubectl 技能使用

## 使用场景

1. K8s 配置审查
2. 生产环境部署前检查
3. 资源配置优化
4. 安全配置审计
5. 故障排查指导
6. 学习 K8s 最佳实践

## 常见问题检查

- 资源限制缺失或不当
- 探针配置错误
- Label selector 不匹配
- RBAC 权限过大
- ConfigMap/Secret 引用错误
- Pod 安全策略违规

## 相关技能

- kubectl - Kubectl 命令工具
- docker-compose - 容器编排
- docker-essentials - Docker 基础

## 来源

- **ClawHub**: https://clawhub.com/skills/k8s
- **搜索分数**: 1.026（Kubernetes 类别）
