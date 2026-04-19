# K8s Debug

## 技能描述

诊断和修复 Kubernetes Pod 问题，包括 CrashLoopBackOff、Pending、DNS、网络、存储和滚动更新故障的排查。

## 功能列表

- Pod 状态诊断（CrashLoopBackOff、Pending）
- DNS 问题排查
- 网络故障诊断
- 存储问题排查
- 滚动更新失败修复
- kubectl 调试命令模板

## 安装方式

```bash
clawhub install k8s-debug
```

## 推荐安装评估

| 环境 | 推荐度 | 说明 |
|------|--------|------|
| 本地开发 | ⭐⭐ | 本地 K8s 开发需要 |
| ECS/服务器 | ⭐⭐⭐⭐⭐ | K8s 集群运维必备 |

## 使用场景

- Pod 启动失败排查
- 集群网络问题诊断
- 存储挂载异常处理
- 服务滚动更新故障