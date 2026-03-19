# API Tester - API 测试技能

## 1. 背景需求

API 是现代应用的核心，API 测试是保证系统稳定性的关键。开发者需要：

- 快速测试 RESTful API
- 自动化 API 测试用例生成
- 集成测试支持
- API 文档验证

## 2. 目标

API Tester 是专注于 API 测试的 Claude Code 插件，帮助开发者高效创建和维护 API 测试。

## 3. 设计方案

### 核心功能

| 功能 | 说明 |
|------|------|
| HTTP 请求 | 发送各种 HTTP 请求 |
| 测试生成 | 自动生成 API 测试用例 |
| 响应验证 | 状态码、响应体验证 |
| 认证支持 | OAuth, Bearer Token, API Key |

### 测试类型

1. **单元测试**：单个 API 端点测试
2. **集成测试**：多端点工作流测试
3. **冒烟测试**：核心功能快速验证
4. **回归测试**：变更后的 API 验证

## 4. 本地部署

### 安装方式

```bash
/plugin install api-tester
```

### 环境要求

- Claude Code 已安装
- 测试框架（可选：Jest, pytest）

## 5. 效果展示

### 使用示例

```
"Test the user login API endpoint"
"Write tests for all CRUD operations"
"Verify the API response format"
"Run integration tests for the checkout flow"
```

### 输出示例

```javascript
// 生成的 API 测试
describe('User API', () => {
  const baseUrl = 'https://api.example.com';
  
  describe('POST /users/login', () => {
    it('should return 200 with token on valid credentials', async () => {
      const response = await fetch(`${baseUrl}/users/login`, {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify({
          email: 'test@example.com',
          password: 'validpassword'
        })
      });
      
      expect(response.status).toBe(200);
      const data = await response.json();
      expect(data.token).toBeDefined();
    });
    
    it('should return 401 on invalid credentials', async () => {
      const response = await fetch(`${baseUrl}/users/login`, {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify({
          email: 'test@example.com',
          password: 'wrongpassword'
        })
      });
      
      expect(response.status).toBe(401);
    });
  });
});
```

## 6. 优缺点分析

### 优点

| 优势 | 说明 |
|------|------|
| 快速生成 | 一键生成完整测试 |
| 全面覆盖 | 支持多种测试场景 |
| 认证支持 | 主流认证方式 |
| 易于维护 | 清晰的测试结构 |

### 缺点

| 劣势 | 说明 |
|------|------|
| 运行环境 | 需要运行测试的环境 |
| Mock 处理 | 复杂场景可能需要手动配置 |
| 性能测试 | 不适合性能压测 |

## 7. 平替对比

| 工具 | 定位 | 优势 | 劣势 |
|------|------|------|------|
| API Tester | API 测试生成 | Claude 集成、智能化 | 功能有限 |
| Postman | API 调试 | 功能全面、界面友好 | 自动化有限 |
| JMeter | 性能测试 | 强大的性能测试 | 重量级 |

## 8. 落地过程

### 使用场景

```bash
# 开发阶段
"Test the new user registration endpoint"

# 集成测试
"Write integration tests for the checkout API"

# 回归测试
"Run API tests to verify the changes"

# 文档验证
"Verify API matches OpenAPI spec"
```

### 最佳实践

- 为关键 API 端点编写测试
- 包含正向和负向测试用例
- 集成到 CI/CD 流程

---

**推荐安装方式**：本地开发环境（Desktop/Laptop）

**资源链接**：Code Quality Testing 类别 - ccplugins/awesome-claude-code-plugins
