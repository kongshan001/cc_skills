# DevOps - DevOps自动化技能

## 技能描述
现代DevOps自动化工具包，专注于部署自动化、基础设施管理和可靠的CI/CD流水线构建。提供全面的DevOps最佳实践和工作流程。

## 功能列表
- **CI/CD流水线**: 自动化测试、部署流水线、发布自动化
- **部署策略**: 蓝绿部署、金丝雀部署、滚动更新、回滚计划
- **基础设施即代码**: Terraform、Ansible、CloudFormation版本控制
- **容器管理**: Docker、Kubernetes、容器注册表设置
- **监控与告警**: Prometheus、Grafana、告警规则、日志聚合
- **备份与恢复**: 数据库备份、卷快照、灾难恢复脚本

## CI/CD流水线规则
### 快速失败原则
```yaml
# 流水线配置示例
stages:
  - test
  - build
  - deploy

# 测试阶段 - 先快速验证
test:
  stage: test
  script:
    - npm run lint
    - npm run test
    - npm run build
  allow_failure: false
```

### 依赖缓存
```yaml
# Node.js缓存
- uses: actions/setup-node@v4
  with:
    node-version: 20
    cache: npm

# 通用缓存
- uses: actions/cache@v4
  with:
    path: |
      ~/.cache/pip
      ~/.cargo/registry
      node_modules
    key: ${{ runner.os }}-deps-${{ hashFiles('**/package-lock.json') }}
```

### 版本固定
```yaml
# 固定版本提供安全
- uses: actions/checkout@b4ffde...  # SHA而非tag
- uses: docker/setup-buildx-action@v3
```

## 部署策略
### 蓝绿部署
```yaml
# 蓝绿部署策略
stages:
  - deploy_green
  - switch_traffic
  - deploy_blue
```

### 金丝雀部署
```yaml
# 渐进式流量分配
canary:
  percentage: 10
  weight: 1
```

## 容器管理
### 一进程一容器
```dockerfile
# 最佳实践：单进程
FROM node:18
WORKDIR /app
COPY package*.json ./
RUN npm ci
COPY . .
CMD ["node", "app.js"]
```

### 健康检查
```yaml
# Kubernetes健康检查
livenessProbe:
  httpGet:
    path: /health
    port: 3000
  initialDelaySeconds: 30
  periodSeconds: 10

readinessProbe:
  httpGet:
    path: /ready
    port: 3000
  initialDelaySeconds: 5
  periodSeconds: 5
```

## 基础设施即代码
### Terraform示例
```hcl
# 主要配置文件
provider "aws" {
  region = "us-west-2"
}

resource "aws_ecs_cluster" "app" {
  name = "app-cluster"
}

resource "aws_ecs_service" "app" {
  name          = "app-service"
  cluster      = aws_ecs_cluster.app.id
  desired_count = 3
}
```

### Ansible示例
```yaml
# Playbook示例
- name: Deploy application
  hosts: webservers
  tasks:
    - name: Install dependencies
      apt:
        name: nginx
        state: present
    
    - name: Deploy application
      copy:
        src: /app
        dest: /var/www/app
```

## 监控与告警
### 四个黄金信号
1. **延迟** (Latency) - 请求处理时间
2. **流量** (Traffic) - 请求数量
3. **错误** (Errors) - 错误率
4. **饱和度** (Saturation) - 资源使用率

### 告警原则
- **告警症状，而非原因** - "用户看到错误"而非"CPU高"
- **每个告警都可操作** - 如果无法做任何事情，就是噪音
- **每个服务设置仪表板** - 一眼看出健康状况
- **结构化日志** - 便于机器解析和查询

## 安全最佳实践
### 密钥管理
```bash
# 环境变量而非硬编码
# 使用vault或sealed secrets
# 定期轮换密钥
# 不同环境不同密钥
```

### 网络安全
```yaml
# 内部服务不需要公网IP
# 私有子网，仅暴露负载均衡器
# TLS everywhere，包括内部流量
# 默认拒绝防火墙策略
```

## 常见错误
### 避免的错误
- **SSH到生产环境修复** - 所有变更通过自动化
- **没有staging环境** - "在我的机器上能运行"
- **忽略脆弱测试** - 破坏对CI的信任
- **部署中的手动步骤** - 如果不自动化，最终会做错
- **仅监控happy路径** - 检查错误率和边缘情况

### 调试流水线
```bash
# 重新运行失败作业
gh run rerun <run-id>

# 使用SSH调试
tmate

# 验证配置
terraform plan
docker-compose config

# 检查缓存
docker system df
```

## 使用场景
- CI/CD流水线设置
- 基础设施即代码
- 容器化部署
- 监控和告警系统
- 自动化运维
- 安全最佳实践
- 团队协作和流程优化

## 安装方式
```bash
# 核心工具安装
pip install ansible
terraform init
docker-compose up -d
kubectl apply -f manifests/

# 常用命令
terraform plan
ansible-playbook playbook.yml
docker build -t myapp .
kubectl get pods
```

## 推荐安装评估

### 本地部署
**适用场景**:
- 个人开发者、小型团队
- 学习DevOps概念
- 个人项目部署
- 本地开发环境

**优势**:
- 完全本地化，无网络依赖
- 开发环境配置简单
- 快速启动和使用
- 学习成本低
- 即时反馈和调试

**ECS部署**
**适用场景**:
- 大型开发团队
- 企业级DevOps管理
- 生产环境部署
- 多团队协作

**优势**:
- 统一基础设施环境
- 企业级安全策略
- 监控和日志管理
- 高可用性和容错能力
- 自动化运维
- 团队权限管理

**选择建议**: 个人学习和开发推荐本地部署，生产环境和企业级管理选择ECS部署。