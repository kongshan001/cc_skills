# Kubernetes (K8s)

## 技能描述

K8s 是由 ivangdavila 开发的 Kubernetes 技能，帮助避免常见的 Kubernetes 错误，包括资源限制、探测配置、选择器不匹配和 RBAC 陷阱。

## 功能列表

### 资源管理
- requests/limits 正确配置
- 资源配额理解
- 调度策略

### 探测配置
- readinessProbe - 控制流量
- livenessProbe - 重启容器
- startupProbe - 慢启动处理
- 常见探测陷阱避免

### 标签与选择器
- Service selector 匹配
- Deployment selector 不可变性
- matchExpressions 复杂选择

### 配置管理
- ConfigMap 更新策略
- Secrets 安全处理
- 环境变量配置

### 网络
- ClusterIP/NodePort/LoadBalancer
- Ingress 与 Ingress Controller
- 服务发现

### 持久存储
- PVC/PV 绑定
- storageClass 配置
- 访问模式 (ReadWriteOnce/Many)

### 调试
- `kubectl describe pod` - 查看事件
- `kubectl logs` - 日志查看
- `kubectl exec` - 容器内调试
- `kubectl get events` - 集群事件

### RBAC
- ServiceAccount 配置
- Role/ClusterRole 区别
- 权限检查

## 安装方式

```bash
# 使用 ClawHub 安装
clawhub install k8s

# 依赖
kubectl CLI 配置
```

## 推荐安装评估

| 场景 | 推荐 | 说明 |
|------|------|------|
| 本地开发 | ⚠️ 需K8s | 需要本地K8s集群(Minikube/Kind) |
| ECS/服务器 | ✅ 推荐 | 云原生服务运维必备 |

### 本地部署
- Minikube 集群
- Kind 本地测试
- K3s 轻量方案

### ECS 部署
- 云厂商EKS/GKE/ACK
- 生产集群管理
- CI/CD 集成
