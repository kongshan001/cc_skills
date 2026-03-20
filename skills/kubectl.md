# kubectl

## 技能描述

Execute and manage Kubernetes clusters via kubectl commands. Query resources, deploy applications, debug containers, manage configurations, and monitor cluster health. Use when working with Kubernetes clusters, containers, deployments, or pod diagnostics.

**所有者**: ddevaal  
**创建时间**: 2026-01-24  
**最新版本**: 1.0.0  
**ClawHub Slug**: `kubectl`

## 功能列表

- Kubernetes 集群管理
- 资源查询
- 应用部署
- 容器调试
- 配置管理
- 集群健康监控
- Pod 诊断
- 日志查看

## 安装方式

```bash
clawhub install kubectl
```

或指定版本：

```bash
clawhub install kubectl --version 1.0.0
```

## 依赖要求

```bash
# 安装 kubectl
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
chmod +x kubectl
sudo mv kubectl /usr/local/bin/
```

## 推荐安装评估

### 本地环境
- ✅ **推荐** - K8s 开发和管理必备
- 适合 DevOps 工程师
- 需要 kubeconfig 配置
- 资源占用低

### ECS/云服务器
- ✅ **强烈推荐** - 生产环境 K8s 管理必备
- 适合集群运维
- 需要集群访问权限
- 建议配合 k8s 技能使用

## 使用场景

1. 集群资源管理
2. 应用部署和更新
3. Pod 问题排查
4. 日志查看和分析
5. 配置管理
6. 集群监控
7. 服务调试

## 常用命令

```bash
kubectl get pods -n namespace
kubectl describe pod <pod-name>
kubectl logs <pod-name> -f
kubectl apply -f deployment.yaml
kubectl exec -it <pod-name> -- /bin/bash
```

## 相关技能

- kubernetes - K8s 最佳实践
- docker-compose - 容器编排
- docker-essentials - Docker 基础

## 来源

- **ClawHub**: https://clawhub.com/skills/kubectl
- **搜索分数**: 1.085（Kubernetes 类别高分）
