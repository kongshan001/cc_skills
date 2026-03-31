# kubectl - Kubernetes技能

## 技能描述
通过`kubectl`命令行工具执行和管理的Kubernetes集群专业技能。支持资源查询、应用部署、容器调试、配置管理和集群健康监控，为Kubernetes运维提供全面支持。

## 功能列表
- **资源查询**: Pods、Deployments、Services、Nodes等列表和详细信息获取
- **部署与更新**: 创建、应用、补丁和更新Kubernetes资源
- **调试与故障排除**: 日志查看、容器命令执行、事件检查
- **配置管理**: kubeconfig更新、上下文切换、命名空间管理
- **健康监控**: 资源使用、滚动状态、事件、Pod条件检查
- **操作执行**: 部署扩展、节点维护、污点和标签管理

## 必备条件
1. **kubectl二进制文件**: 安装并在PATH上可用（v1.20+）
2. **kubeconfig文件**: 已配置集群凭证（默认：`~/.kube/config`）
3. **活跃连接**: 与Kubernetes集群的活跃连接

## 快速设置
### 安装kubectl
**macOS:**
```bash
brew install kubernetes-cli
```

**Linux:**
```bash
apt-get install -y kubectl  # Ubuntu/Debian
yum install -y kubectl      # RHEL/CentOS
```

**验证安装:**
```bash
kubectl version --client
kubectl cluster-info  # 测试连接
```

## 基本命令
### 资源查询
```bash
kubectl get pods                    # 列出当前命名空间的所有pods
kubectl get pods -A                 # 所有命名空间
kubectl get pods -o wide            # 更多列信息
kubectl get nodes                   # 列出节点
kubectl describe pod POD_NAME        # 详细信息和事件
```

### 日志查看
```bash
kubectl logs POD_NAME                # 获取日志
kubectl logs -f POD_NAME             # 跟踪日志（tail -f）
kubectl logs POD_NAME -c CONTAINER   # 特定容器
kubectl logs POD_NAME --previous     # 之前的容器日志
```

### 命令执行
```bash
kubectl exec -it POD_NAME -- /bin/bash   # 交互式shell
kubectl exec POD_NAME -- COMMAND         # 运行单个命令
```

### 应用部署
```bash
kubectl apply -f deployment.yaml         # 应用配置
kubectl create -f deployment.yaml        # 创建资源
kubectl apply -f deployment.yaml --dry-run=client  # 测试
```

## 常见模式
### Pod调试
```bash
# 1. 识别问题
kubectl describe pod POD_NAME

# 2. 检查日志
kubectl logs POD_NAME
kubectl logs POD_NAME --previous

# 3. 执行调试命令
kubectl exec -it POD_NAME -- /bin/bash

# 4. 检查事件
kubectl get events --sort-by='.lastTimestamp'
```

### 部署新版本
```bash
# 1. 更新镜像
kubectl set image deployment/MY_APP my-app=my-app:v2

# 2. 监控滚动
kubectl rollout status deployment/MY_APP -w

# 3. 验证
kubectl get pods -l app=my-app

# 4. 回滚（如需要）
kubectl rollout undo deployment/MY_APP
```

### 节点维护准备
```bash
# 1. 驱逐节点（驱逐所有pods）
kubectl drain NODE_NAME --ignore-daemonsets

# 2. 执行维护
# ...

# 3. 重新上线
kubectl uncordon NODE_NAME
```

## 输出格式
`--output`（`-o`）标志支持多种格式：
- `table` - 默认表格格式
- `wide` - 扩展表格格式
- `json` - JSON格式（与`jq`配合使用）
- `yaml` - YAML格式
- `jsonpath` - JSONPath表达式
- `custom-columns` - 自定义输出列
- `name` - 仅资源名称

**示例:**
```bash
kubectl get pods -o json | jq '.items[0].metadata.name'
kubectl get pods -o jsonpath='{.items[*].metadata.name}'
kubectl get pods -o custom-columns=NAME:.metadata.name,STATUS:.status.phase
```

## 全局标志
所有命令都支持的标志：
```bash
-n, --namespace=<ns>           # 在特定命名空间操作
-A, --all-namespaces           # 跨所有命名空间操作
--context=<context>            # 使用特定kubeconfig上下文
-o, --output=<format>          # 输出格式（json, yaml, table, etc.）
--dry-run=<mode>               # 干运行模式（none, client, server）
-l, --selector=<labels>        # 按标签过滤
--field-selector=<selector>    # 按字段过滤
-v, --v=<int>                  # 详细程度级别（0-9）
```

## 干运行模式
- `--dry-run=client` - 快速客户端验证（安全测试命令）
- `--dry-run=server` - 服务器端验证（更准确）
- `--dry-run=none` - 真实执行（默认）

**总是先测试:**
```bash
kubectl apply -f manifest.yaml --dry-run=client
```

## 调试技巧
1. **使用标签选择器进行批量操作:**
   ```bash
   kubectl delete pods -l app=myapp
   kubectl get pods -l env=prod,tier=backend
   ```

2. **实时监控资源:**
   ```bash
   kubectl get pods -w  # 监控变化
   ```

3. **使用`-A`查看所有命名空间:**
   ```bash
   kubectl get pods -A  # 查看所有pods
   ```

4. **保存输出供后续比较:**
   ```bash
   kubectl get deployment my-app -o yaml > deployment-backup.yaml
   ```

5. **删除前检查:**
   ```bash
   kubectl delete pod POD_NAME --dry-run=client
   ```

## 推荐安装评估

### 本地部署
**适用场景**:
- 个人开发者、小型团队
- 本地开发环境
- 学习Kubernetes
- 个人项目部署

**优势**:
- 完全本地化，无网络依赖
- 开发环境配置简单
- 快速启动和使用
- 学习成本低
- 即时反馈

**ECS部署**
**适用场景**:
- 大型开发团队
- 企业级Kubernetes管理
- 生产环境集群
- 多团队协作

**优势**:
- 统一集群管理
- 企业级安全策略
- 监控和日志管理
- 高可用性配置
- 自动化运维
- 团队权限管理

**选择建议**: 个人学习和开发推荐本地部署，生产环境和企业级管理选择ECS部署。