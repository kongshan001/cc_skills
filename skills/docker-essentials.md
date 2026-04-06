# Docker Essentials

> Docker 容器管理、镜像操作和调试必备命令

## 基本信息

| 属性 | 值 |
|------|-----|
| **Slug** | `docker-essentials` |
| **作者** | arnarsson |
| **版本** | 1.0.0 |
| **更新时间** | 2026-02-26 |
| **标签** | docker, container, devops |

## 功能列表

### 容器生命周期
- 运行容器 (前台/后台)
- 端口映射、环境变量挂载
- 卷挂载
- 容器启动/停止/重启/删除

### 容器检查与调试
- 查看日志 (实时/尾部)
- 在容器中执行命令
- 容器详情检查 (JSON 路径查询)
- 容器资源监控

### 镜像管理
- 构建镜像 (Dockerfile)
- 拉取/推送镜像
- 镜像标签管理
- 清理未使用镜像

### Docker Compose
- 服务启动/停止
- 日志查看
- 服务扩缩容

### 网络与卷
- 网络创建/连接/检查
- 卷创建/管理

## 安装方式

### 本地安装
```bash
# 安装 Docker (Linux)
curl -fsSL https://get.docker.com | sh

# 启动 Docker
sudo systemctl start docker
sudo systemctl enable docker
```

### 验证安装
```bash
docker --version
docker ps
```

## 推荐安装评估

### 本地环境 ⭐⭐⭐⭐⭐
- 开发/测试环境必备
- 学习 Docker 基础
- 小型项目容器化

### ECS 环境 ⭐⭐⭐⭐⭐
- 生产环境部署
- 微服务架构
- 自动化 CI/CD

## 常用工作流

### 开发容器
```bash
docker run -it --rm \
  -v $(pwd):/app \
  -w /app \
  -p 3000:3000 \
  node:18 npm run dev
```

### 数据库容器
```bash
docker run -d \
  --name postgres \
  -e POSTGRES_PASSWORD=secret \
  -e POSTGRES_DB=mydb \
  -v postgres-data:/var/lib/postgresql/data \
  -p 5432:5432 postgres:15
```

### 多阶段构建
```dockerfile
FROM node:18 AS builder
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build

FROM nginx:alpine
COPY --from=builder /app/dist /usr/share/nginx/html
```

## 优缺点分析

### ✅ 优点
- 覆盖常用操作
- 包含最佳实践
- 多阶段构建示例

### ⚠️ 局限
- 需要 Docker 基础
- 文档较基础

## 替代方案

| 方案 | 特点 |
|------|------|
| Docker 官方文档 | 更全面 |
| Docker Compose 文件模板 | 更结构化 |
| Portainer UI | 可视化管理 |