# Frontend Developer - 前端开发专家技能

## 1. 背景需求

前端开发技术栈日新月异，开发者需要：

- 现代前端框架开发支持（React, Vue, Angular）
- 响应式设计和用户体验优化
- 性能优化和加载速度提升
- 前端工程化实践

## 2. 目标

Frontend Developer 是专注于前端开发的 Claude Code 子代理，提供全面的前端开发支持。

## 3. 设计方案

### 核心能力

| 能力 | 说明 |
|------|------|
| 框架开发 | React, Vue, Angular 项目开发 |
| 组件设计 | 可复用组件架构设计 |
| 状态管理 | Redux, Vuex, Zustand 等 |
| 样式方案 | CSS, SCSS, Tailwind, CSS-in-JS |
| 构建工具 | Vite, Webpack, Rollup |

### 专业领域

1. **React**：Hooks, Context, Server Components
2. **Vue**：Composition API, Pinia
3. **TypeScript**：类型安全的前端开发
4. **性能**：代码分割、懒加载、CDN
5. **测试**：Jest, React Testing Library, Vitest

## 4. 本地部署

### 安装方式

```bash
/plugin install frontend-developer
```

### 环境要求

- Node.js 18+ 环境
- Claude Code 已安装

## 5. 效果展示

### 使用示例

```
"Create a React component for user dashboard"
"Set up a Vue 3 project with TypeScript"
"Optimize this React app's performance"
"Write tests for this component"
```

### 输出示例

```tsx
// React 组件示例
import { useState, useMemo } from 'react';
import { useQuery } from '@tanstack/react-query';

interface User {
  id: number;
  name: string;
  email: string;
}

export const UserDashboard: React.FC = () => {
  const [filter, setFilter] = useState('');
  
  const { data, isLoading } = useQuery<User[]>({
    queryKey: ['users'],
    queryFn: () => fetch('/api/users').then(res => res.json()),
  });

  const filteredUsers = useMemo(() => 
    data?.filter(u => u.name.includes(filter)) ?? [],
    [data, filter]
  );

  if (isLoading) return <Skeleton />;

  return (
    <div className="dashboard">
      <SearchInput value={filter} onChange={setFilter} />
      <UserList users={filteredUsers} />
    </div>
  );
};
```

## 6. 优缺点分析

### 优点

| 优势 | 说明 |
|------|------|
| 现代框架 | 熟悉主流前端框架最新特性 |
| 性能优化 | 专业的性能优化建议 |
| 组件设计 | 良好的组件架构思维 |
| TypeScript | 强类型前端开发支持 |

### 缺点

| 劣势 | 说明 |
|------|------|
| 单一领域 | 只专注前端 |
| 环境依赖 | 需要完整的 Node.js 环境 |

## 7. 平替对比

| 工具 | 定位 | 优势 | 劣势 |
|------|------|------|------|
| Frontend Developer | 前端专项开发 | 深度前端支持 | 单一领域 |
| Web Dev | Web 全栈开发 | 前后端都能 | 前端深度有限 |
| Claude Code | 通用编码 | 全栈支持 | 不专注前端 |

## 8. 落地过程

### 使用场景

```bash
# 新项目启动
"Create a new React project with Vite and TypeScript"

# 组件开发
"Build a data table component with sorting and filtering"

# 性能优化
"Lazy load these images and optimize bundle size"

# 问题调试
"Debug this React useEffect infinite loop"
```

### 最佳实践

- 前端项目作为主力代理使用
- 配合 ESLint 和 Prettier 使用
- 关注 React/Vue 最新最佳实践

---

**推荐安装方式**：本地开发环境（Desktop/Laptop）

**资源链接**：Development Engineering 类别 - ccplugins/awesome-claude-code-plugins
