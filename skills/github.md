# GitHub - GitHub技能

## 技能描述
使用`gh` CLI与GitHub交互的专业技能。支持issues、PRs、CI运行和高级查询，提供全面的GitHub操作能力。

## 功能列表
- **Pull Requests**: 检查PR CI状态、获取PR列表、查看运行详情
- **CI/CD流水线**: 获取最近流水线运行、查看特定运行、查看失败步骤日志
- **API查询**: 使用`gh api`进行高级数据查询、获取特定字段数据
- **JSON输出**: 支持结构化输出，可使用`--jq`过滤数据
- **批量操作**: 批量处理PRs、issues和流水线

## 主要功能
### Pull Requests管理
```bash
# 检查PR的CI状态
gh pr checks 55 --repo owner/repo

# 列出最近的流水线运行
gh run list --repo owner/repo --limit 10

# 查看特定运行详情
gh run view <run-id> --repo owner/repo

# 仅查看失败步骤的日志
gh run view <run-id> --repo owner/repo --log-failed
```

### API高级查询
```bash
# 获取带特定字段的PR
gh api repos/owner/repo/pulls/55 --jq '.title, .state, .user.login'

# 列出Issues
gh issue list --repo owner/repo --json number,title --jq '.[] | "\(.number): \(.title)"'
```

## JSON输出与过滤
大多数命令支持`--json`进行结构化输出，可以使用`--jq`进行过滤：

```bash
# JSON输出
gh issue list --repo owner/repo --json number,title --jq '.[] | "\(.number): \(.title)"'
```

## 使用场景
- GitHub项目管理
- CI/CD流水线监控
- Pull Request审核和状态检查
- Issues管理和跟踪
- 团队协作和代码审查
- 自动化工作流管理

## API特点
- **REST API**: 通过`gh api`访问GitHub REST API
- **GraphQL支持**: 支持复杂查询和过滤
- **结构化输出**: JSON格式便于后续处理
- **批量操作**: 支持批量处理多个项目
- **权限管理**: 基于GitHub访问权限

## 安装方式
```bash
# 安装gh CLI
# macOS
brew install gh

# Ubuntu/Debian
sudo apt install gh

# Windows
choco install gh

# 验证安装
gh --version

# 登录GitHub
gh auth login

# 验证认证
gh auth status
```

## 配置选项
```bash
# 设置默认仓库
gh repo set-default owner/repo

# 配置默认分支
gh config set default-branch main

# 设置git配置
gh config set git_protocol https
```

## 最佳实践
- 使用`--repo owner/repo`参数指定仓库
- 使用`--json`和`--jq`进行结构化处理
- 定期更新gh CLI到最新版本
- 使用`gh auth status`检查认证状态
- 使用`gh config`进行个性化配置

## 推荐安装评估

### 本地部署
**适用场景**:
- 个人开发者、小型团队
- 本地开发环境
- 个人项目管理
- 学习GitHub操作

**优势**:
- 完全本地化，无网络依赖
- 命令行操作便捷
- 即时反馈和调试
- 学习成本低
- 与本地开发工具集成好

**ECS部署**
**适用场景**:
- 大型开发团队
- 企业级GitHub管理
- 多仓库管理
- 团队协作需求

**优势**:
- 统一GitHub环境
- 集成到CI/CD流水线
- 团队权限管理
- 企业级功能支持
- 监控和审计功能
- 安全策略管理

**选择建议**: 个人开发者和小团队推荐本地部署，企业级团队和大规模项目选择ECS部署。