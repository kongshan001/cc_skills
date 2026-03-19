# Database Operations

> 全面的数据库设计、迁移和优化专家 - PostgreSQL、查询性能、架构设计、EF Core 迁移

## 📋 基本信息

| 项目 | 内容 |
|------|------|
| **技能名称** | database-operations |
| **版本** | 1.0.0 |
| **作者** | jgarrison929 |
| **许可证** | MIT |
| **评分** | ⭐ 3.0+ |

## 🎯 技能描述

Database Operations 是全面的数据库设计、迁移和优化专家，基于 Dave Poon 的 buildwithclaude 改编。专注于 PostgreSQL、查询性能和架构设计。

## 🛠️ 功能列表

### 1. 核心原则
- **先测量** - 优化前始终使用 EXPLAIN ANALYZE
- **策略性索引** - 基于查询模式，非每个列
- **选择性反规范化** - 仅在读取模式证明合理时使用
- **缓存昂贵计算** - Redis/物化视图用于热路径
- **计划回滚** - 每个迁移都有反向迁移
- **零停机迁移** - 先添加，后破坏

### 2. 架构设计模式
- 用户管理表结构
- 审计日志表
- 软删除支持
- 触发器函数

### 3. 性能优化
- 查询分析 (EXPLAIN ANALYZE)
- 索引优化
- 缓存策略
- 连接池配置

### 4. 迁移管理
- 零停机迁移
- 回滚程序
- 数据迁移

## 📦 安装方式

```bash
# 使用 ClawHub 安装
clawhub install database-operations
```

## 📊 推荐安装评估

| 场景 | 推荐度 | 说明 |
|------|--------|------|
| **本地安装** | ⭐⭐⭐⭐⭐ | 强烈推荐，数据库开发必备 |
| **ECS 安装** | ⭐⭐⭐⭐⭐ | 完美支持，生产环境 |

### 评分理由

- ✅ 完整的数据库设计模式
- ✅ PostgreSQL 详细示例
- ✅ 性能优化指南
- ✅ 零停机迁移策略

## 💡 核心模式示例

### 用户管理表
```sql
CREATE TYPE user_status AS ENUM ('active', 'inactive', 'suspended', 'pending');

CREATE TABLE users (
  id BIGSERIAL PRIMARY KEY,
  email VARCHAR(255) UNIQUE NOT NULL,
  username VARCHAR(50) UNIQUE NOT NULL,
  password_hash VARCHAR(255) NOT NULL,
  first_name VARCHAR(100) NOT NULL,
  last_name VARCHAR(100) NOT NULL,
  status user_status DEFAULT 'active',
  email_verified BOOLEAN DEFAULT FALSE,
  created_at TIMESTAMPTZ DEFAULT CURRENT_TIMESTAMP,
  updated_at TIMESTAMPTZ DEFAULT CURRENT_TIMESTAMP,
  deleted_at TIMESTAMPTZ, -- Soft delete

  CONSTRAINT users_email_format CHECK (email ~* '^[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Za-z]{2,}$')
);

-- 策略性索引
CREATE INDEX idx_users_email ON users(email);
CREATE INDEX idx_users_status ON users(status) WHERE status != 'active';
CREATE INDEX idx_users_created_at ON users(created_at);
```

### 审计日志
```sql
CREATE TABLE audit_log (
  id BIGSERIAL PRIMARY KEY,
  table_name VARCHAR(255) NOT NULL,
  record_id BIGINT NOT NULL,
  operation audit_operation NOT NULL,
  old_values JSONB,
  new_values JSONB,
  changed_fields TEXT[],
  user_id BIGINT REFERENCES users(id),
  created_at TIMESTAMPTZ DEFAULT CURRENT_TIMESTAMP
);

CREATE INDEX idx_audit_table_record ON audit_log(table_name, record_id);
CREATE INDEX idx_audit_user_time ON audit_log(user_id, created_at);
```

## 🔧 性能优化流程

1. **识别慢查询** - 查看慢查询日志
2. **分析执行计划** - `EXPLAIN ANALYZE`
3. **识别瓶颈** - 全表扫描、缺失索引
4. **实施优化** - 添加索引、重写查询
5. **验证效果** - 再次测量
6. **监控** - 持续监控性能

---

*本报告由 OpenClaw 自动生成，更新时间: 2026-03-17*
