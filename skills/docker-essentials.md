# Docker Essentials - Docker基础技能

## 技能描述
Docker容器和映像管理的核心命令和工作流程技能。专注于容器操作、映像操作和调试，提供完整的Docker使用指南。

## 功能列表
- **容器生命周期管理**: 运行、停止、启动、重启容器
- **容器管理**: 容器列表、状态监控、资源查看
- **容器检查与调试**: 日志查看、命令执行、容器检查
- **映像管理**: 构建、拉取、推送、删除映像
- **Docker Compose**: 服务启动、停止、日志、扩展
- **网络管理**: 网络创建、连接、检查
- **卷管理**: 卷创建、检查、删除、挂载
- **系统管理**: 磁盘使用、清理、信息查看

## 容器生命周期
### 运行容器
```bash
# 从映像运行容器
docker run nginx

# 后台运行
docker run -d nginx

# 指定名称运行
docker run --name my-nginx -d nginx

# 端口映射
docker run -p 8080:80 -d nginx

# 环境变量
docker run -e MY_VAR=value -d app

# 卷挂载
docker run -v /host/path:/container/path -d app

# 自动移除
docker run --rm alpine echo "Hello"

# 交互式终端
docker run -it ubuntu bash
```

### 管理容器
```bash
# 列出运行容器
docker ps

# 列出所有容器（包括已停止）
docker ps -a

# 停止容器
docker stop container_name

# 启动已停止容器
docker start container_name

# 重启容器
docker restart container_name

# 删除容器
docker rm container_name

# 强制删除运行中容器
docker rm -f container_name

# 删除所有已停止容器
docker container prune
```

## 容器检查与调试
### 查看日志
```bash
# 显示日志
docker logs container_name

# 跟踪日志（如tail -f）
docker logs -f container_name

# 最后100行
docker logs --tail 100 container_name

# 带时间戳的日志
docker logs -t container_name
```

### 执行命令
```bash
# 在运行容器中执行命令
docker exec container_name ls -la

# 交互式shell
docker exec -it container_name bash

# 以特定用户执行
docker exec -u root -it container_name bash

# 带环境变量执行
docker exec -e VAR=value container_name env
```

### 检查
```bash
# 检查容器详情
docker inspect container_name

# 获取特定字段
docker inspect -f '{{.NetworkSettings.IPAddress}}' container_name

# 查看容器统计
docker stats

# 查看特定容器统计
docker stats container_name

# 查看容器进程
docker top container_name
```

## 映像管理
### 构建映像
```bash
# 从Dockerfile构建
docker build -t myapp:1.0 .

# 使用自定义Dockerfile构建
docker build -f Dockerfile.dev -t myapp:dev .

# 使用构建参数
docker build --build-arg VERSION=1.0 -t myapp .

# 无缓存构建
docker build --no-cache -t myapp .
```

### 管理映像
```bash
# 列出映像
docker images

# 拉取映像
docker pull nginx:latest

# 标记映像
docker tag myapp:1.0 myapp:latest

# 推送到注册表
docker push myrepo/myapp:1.0

# 删除映像
docker rmi image_name

# 删除未使用映像
docker image prune

# 删除所有未使用映像
docker image prune -a
```

## Docker Compose
### 基本操作
```bash
# 启动服务
docker-compose up

# 后台启动
docker-compose up -d

# 停止服务
docker-compose down

# 停止并删除卷
docker-compose down -v

# 查看日志
docker-compose logs

# 跟踪特定服务日志
docker-compose logs -f web

# 扩展服务
docker-compose up -d --scale web=3
```

### 服务管理
```bash
# 列出服务
docker-compose ps

# 在服务中执行命令
docker-compose exec web bash

# 重启服务
docker-compose restart web

# 重建服务
docker-compose build web

# 重建并重启
docker-compose up -d --build
```

## 网络管理
```bash
# 列出网络
docker network ls

# 创建网络
docker network create mynetwork

# 连接容器到网络
docker network connect mynetwork container_name

# 断开网络连接
docker network disconnect mynetwork container_name

# 检查网络
docker network inspect mynetwork

# 删除网络
docker network rm mynetwork
```

## 推荐安装评估

### 本地部署
**适用场景**:
- 个人开发者、小型团队
- 本地开发环境
- 个人项目部署
- 学习Docker技术

**优势**:
- 完全本地化，无网络依赖
- 开发环境配置简单
- 快速启动和使用
- 学习成本低
- 即时反馈

**ECS部署**
**适用场景**:
- 大型开发团队
- 企业级容器管理
- 多环境部署
- 生产容器编排

**优势**:
- 统一容器环境
- 容器编排能力
- 企业级管理功能
- 安全合规支持
- 监控和日志管理
- 生产环境稳定性

**选择建议**: 个人开发和小项目推荐本地部署，企业级生产环境选择ECS部署。