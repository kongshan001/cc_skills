# CI/CD Pipeline - CI/CD流水线技能

## 技能描述
使用GitHub Actions创建、调试和管理CI/CD流水线的专业技能。涵盖测试自动化、部署、发布自动化、流水线语法、常见模式和故障排除，为现代软件开发提供完整的自动化解决方案。

## 功能列表
- **快速入门**: Node.js、Python、Go、Rust项目的CI设置模板
- **矩阵构建**: 多版本/操作系统并行测试
- **条件作业**: 基于分支和事件的条件执行
- **缓存策略**: 依赖缓存、构建缓存优化
- **工件管理**: 构建产物保存、下载、共享
- **调度运行**: 定时任务、手动触发
- **部署流水线**: 生产部署、环境管理
- **Docker流水线**: 容器构建、推送
- **发布自动化**: npm发布、GitHub发布
- **密钥管理**: 环境变量、保护规则
- **调试工具**: headed模式、trace查看、失败调试

## 快速入门示例
### Node.js项目
```yaml
# .github/workflows/ci.yml
name: CI

on:
  push:
    branches: [main]
  pull_request:
    branches: [main]

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-node@v4
        with:
          node-version: 20
          cache: npm
      - run: npm ci
      - run: npm test
      - run: npm run lint
```

### Python项目
```yaml
# .github/workflows/ci.yml
name: CI

on:
  push:
    branches: [main]
  pull_request:
    branches: [main]

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-python@v5
        with:
          python-version: "3.12"
          cache: pip
      - run: pip install -r requirements.txt
      - run: pytest
      - run: ruff check .
```

### Go项目
```yaml
# .github/workflows/ci.yml
name: CI

on:
  push:
    branches: [main]
  pull_request:
    branches: [main]

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-go@v5
        with:
          go-version: "1.22"
      - run: go test ./...
      - run: go vet ./...
```

### Rust项目
```yaml
# .github/workflows/ci.yml
name: CI

on:
  push:
    branches: [main]
  pull_request:
    branches: [main]

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: dtolnay/rust-toolchain@stable
      - uses: Swatinem/rust-cache@v2
      - run: cargo test
      - run: cargo clippy -- -D warnings
```

## 矩阵构建模式
```yaml
jobs:
  test:
    strategy:
      fail-fast: false
      matrix:
        os: [ubuntu-latest, macos-latest, windows-latest]
        node-version: [18, 20, 22]
    runs-on: ${{ matrix.os }}
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-node@v4
        with:
          node-version: ${{ matrix.node-version }}
      - run: npm ci
      - run: npm test
```

## 条件作业
```yaml
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - run: npm test

  deploy:
    needs: test
    if: github.ref == 'refs/heads/main' && github.event_name == 'push'
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - run: ./deploy.sh
```

## 缓存策略
### Node.js（自动）
```yaml
- uses: actions/setup-node@v4
  with:
    node-version: 20
    cache: npm  # 或 yarn, pnpm
```

### 通用缓存
```yaml
- uses: actions/cache@v4
  with:
    path: |
      ~/.cache/pip
      ~/.cargo/registry
      node_modules
    key: ${{ runner.os }}-deps-${{ hashFiles('**/package-lock.json') }}
    restore-keys: |
      ${{ runner.os }}-deps-
```

## 工件管理
### 上传工件
```yaml
- uses: actions/upload-artifact@v4
  with:
    name: build-output
    path: dist/
    retention-days: 7
```

### 下载工件
```yaml
- uses: actions/download-artifact@v4
  with:
    name: build-output
    path: dist/
```

## 部署流水线
### 生产部署
```yaml
name: Release

on:
  push:
    tags:
      - "v*"

jobs:
  release:
    runs-on: ubuntu-latest
    permissions:
      contents: write
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-node@v4
        with:
          node-version: 20
          cache: npm
      - run: npm ci
      - run: npm run build
      - run: npm test

      - uses: softprops/action-gh-release@v2
        with:
          generate_release_notes: true
          files: |
            dist/*.js
            dist/*.css
```

### 多环境部署
```yaml
name: Deploy

on:
  push:
    branches: [main, staging]

jobs:
  deploy:
    runs-on: ubuntu-latest
    environment: ${{ github.ref == 'refs/heads/main' && 'production' || 'staging' }}
    steps:
      - uses: actions/checkout@v4
      - run: npm ci && npm run build
      - run: |
          if [ "${{ github.ref }}" = "refs/heads/main" ]; then
            ./deploy.sh production
          else
            ./deploy.sh staging
          fi
        env:
          DEPLOY_TOKEN: ${{ secrets.DEPLOY_TOKEN }}
```

## Docker构建与推送
```yaml
name: Docker

on:
  push:
    branches: [main]
    tags: ["v*"]

jobs:
  build:
    runs-on: ubuntu-latest
    permissions:
      packages: write
    steps:
      - uses: actions/checkout@v4
      - uses: docker/setup-buildx-action@v3
      - uses: docker/login-action@v3
        with:
          registry: ghcr.io
          username: ${{ github.actor }}
          password: ${{ secrets.GITHUB_TOKEN }}
      - uses: docker/build-push-action@v6
        with:
          push: true
          tags: |
            ghcr.io/${{ github.repository }}:latest
            ghcr.io/${{ github.repository }}:${{ github.sha }}
          cache-from: type=gha
          cache-to: type=gha,mode=max
```

## npm发布
```yaml
name: Publish

on:
  release:
    types: [published]

jobs:
  publish:
    runs-on: ubuntu-latest
    permissions:
      id-token: write
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-node@v4
        with:
          node-version: 20
          registry-url: https://registry.npmjs.org
      - run: npm ci
      - run: npm test
      - run: npm publish --provenance
        env:
          NODE_AUTH_TOKEN: ${{ secrets.NPM_TOKEN }}
```

## 密钥管理
### CLI设置密钥
```bash
# 设置仓库密钥
gh secret set DEPLOY_TOKEN --body "my-secret-value"

# 从文件设置
gh secret set SSH_KEY < ~/.ssh/deploy_key

# 设置环境特定密钥
gh secret set DB_PASSWORD --env production --body "p@ssw0rd"

# 列出密钥
gh secret list

# 删除密钥
gh secret delete OLD_SECRET
```

### 流水线中使用密钥
```yaml
env:
  DATABASE_URL: ${{ secrets.DATABASE_URL }}

steps:
  - run: echo "Deploying..."
    env:
      API_KEY: ${{ secrets.API_KEY }}
```

## 调试工具
### 重新运行失败作业
```bash
# 列出最近的运行
gh run list --limit 10

# 查看特定运行
gh run view <run-id>

# 查看失败作业日志
gh run view <run-id> --log-failed

# 重新运行失败作业
gh run rerun <run-id> --failed

# 重新运行整个流水线
gh run rerun <run-id>
```

### 使用SSH调试
```yaml
- uses: mxschmitt/action-tmate@v3
  if: failure()
  with:
    limit-access-to-actor: true
```

## 故障排除
### 常见问题和解决方案
| 问题 | 解决方案 |
|------|----------|
| 权限错误 | 添加permissions块 |
| 工具安装失败 | 检查工具版本和路径 |
| 缓存不恢复 | 验证cache key匹配 |
| 测试超时 | 设置timeout-minutes |
| 网络问题 | 使用代理或镜像源 |

## 推荐安装评估

### 本地部署
**适用场景**:
- 个人开发者、小型团队
- 个人项目CI/CD
- 学习流水线概念
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
- 企业级CI/CD管理
- 多项目流水线
- 生产环境部署

**优势**:
- 统一流水线环境
- 企业级安全策略
- 监控和日志管理
- 高可用性和容错能力
- 自动化运维
- 团队权限管理

**选择建议**: 个人学习和开发推荐本地部署，生产环境和企业级管理选择ECS部署。