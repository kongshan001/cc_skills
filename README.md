# ClawHub 热门技能调研报告

> 自动化调研 ClawHub 热门 Skills 并生成文档

## 技能索引

| 序号 | 技能名称 | Slug | 版本 | 作者 | 描述 | 推荐安装 |
|:---:|---------|------|------|------|------|:--------:|
| 1 | Code | code | 1.0.4 | ivangdavila | 编码工作流技能，规划、实施、验证和测试 | 本地/ECS |
| 2 | Test Runner | test-runner | 1.0.0 | cmanfre7 | 测试运行器，支持 TypeScript/Python/Swift | 本地/ECS |
| 3 | Web Pilot | web-pilot | 1.0.0 | liranudi | 网页导航，无需 API 密钥搜索和抓取 | ECS |
| 4 | Image Edit | image-edit | 1.0.0 | ivangdavila | AI 图像编辑，修复/扩展/去背景/放大 | 本地/ECS |
| 5 | AI PPT Generate | ai-ppt-generate | 1.0.0 | baiduqianfangroup | 百度智能 PPT 生成工具 | 本地/ECS |
| 6 | AI Image Generation | image-generation | 1.0.3 | ivangdavila | AI 图像生成，支持 GPT Image/FLUX/Imagen | 本地/ECS |
| 7 | Secure API Calls | secure-api-calls | 1.0.3 | smarcombes | 安全 API 调用，零信任凭据保护 | 本地/ECS |
| 8 | Security Auditor | security-auditor | 1.0.0 | jgarrison929 | 安全审计，OWASP Top 10 漏洞检测 | 本地/ECS |
| 9 | Database Operations | database-operations | 1.0.0 | jgarrison929 | 数据库操作，模式设计/迁移/优化 | 本地/ECS |
| 10 | imap-smtp-email | imap-smtp-email | 0.0.10 | gzlicanyi | 邮件收发，IMAP/SMTP 协议支持 | 本地/ECS |
| 11 | Self-Improving | self-improving | 1.2.16 | ivangdavila | 自我改进技能，反思/批评/学习/记忆 | 本地/ECS |
| 12 | Python Script Generator | python-script-generator | 1.0.0 | sunshine-del-ux | Python 脚本和应用模板生成 | 本地/ECS |
| 13 | Python Code Test | python-code-test | 1.0.3 | zhouhh2017 | 代码功能测试，生成测试用例 | 本地/ECS |
| 14 | Automation Workflows | automation-workflows | 0.1.0 | jk-0001 | 自动化工作流设计与实现 | 本地/ECS |
| 15 | AI Web Automation | ai-web-automation | 1.0.0 | arthasking123 | 网页自动化，表单/爬虫/测试 | ECS |
| 16 | Security Audit Toolkit | security-audit-toolkit | 1.0.0 | gitgoodordietrying | 安全审计工具包，依赖扫描/OWASP | 本地/ECS |
| 17 | Git Essentials | git-essentials | 1.0.0 | arnarsson | 基础 Git 命令和工作流 | 本地/ECS |
| 18 | Git Workflows | git-workflows | 1.0.0 | gitgoodordietrying | 高级 Git 操作，变基/调试/并行开发 | 本地/ECS |
| 19 | Git Helper | git-helper | 1.0.0 | xejrax | 常用 Git 操作速查 | 本地 |
| 20 | Docker Essentials | docker-essentials | 1.0.0 | arnarsson | 容器管理、镜像操作、调试 | 本地/ECS |
| 21 | Docker Helper | docker-helper | 2.0.0 | ckchzh | Dockerfile/Compose 生成、调试优化 | 本地/ECS |
| 22 | Docker Sandbox | docker-sandbox | 1.0.0 | gitgoodordietrying | 安全沙箱环境，隔离执行 | 本地/ECS |
| 23 | Test Master | test-master | 0.1.0 | veeramanikandanr48 | 测试策略和自动化框架 | 本地/ECS |
| 24 | K8s Debug | k8s-debug | 0.1.0 | qq280948982 | K8s 故障诊断，Pod/网络/存储问题 | ECS |

## 调研方法

1. 使用 `clawhub search` 搜索热门技能关键词（docker, git, python, test）
2. 使用 `clawhub inspect <slug>` 获取每个技能详细信息
3. 为每个技能生成独立 MD 文件
4. 更新本 README.md 索引
5. 推送到 GitHub 仓库

## 安装方式

```bash
# 安装 ClawHub
npm i -g clawhub

# 安装单个技能
clawhub install <slug>

# 或使用 npx
npx clawhub@latest install <slug>
```

## 技能分类

### 版本控制 (Git)
- [Git Essentials](skills/git-essentials.md) - 基础 Git 命令
- [Git Workflows](skills/git-workflows.md) - 高级 Git 操作
- [Git Helper](skills/git-helper.md) - Git 操作速查

### 容器化 (Docker)
- [Docker Essentials](skills/docker-essentials.md) - 容器基础管理
- [Docker Helper](skills/docker-helper.md) - Dockerfile/Compose 辅助
- [Docker Sandbox](skills/docker-sandbox.md) - 安全沙箱

### 测试
- [Test Runner](skills/test-runner.md) - 测试运行器
- [Test Master](skills/test-master.md) - 测试策略
- [Python Code Test](skills/python-code-test.md) - Python 代码测试

### Python 开发
- [Python Script Generator](skills/python-script-generator.md) - 脚本模板生成

### Kubernetes
- [K8s Debug](skills/k8s-debug.md) - 故障诊断

### 开发工具
- [Code](skills/code.md) - 编码工作流
- [Database Operations](skills/database-operations.md) - 数据库操作
- [Security Auditor](skills/security-auditor.md) - 安全审计

### AI 能力
- [AI Image Generation](skills/image-generation.md) - AI 图像生成
- [Image Edit](skills/image-edit.md) - 图像编辑
- [AI PPT Generate](skills/ai-ppt-generate.md) - PPT 生成

### 工具和自动化
- [Web Pilot](skills/web-pilot.md) - 网页导航
- [imap-smtp-email](skills/imap-smtp-email.md) - 邮件收发
- [Secure API Calls](skills/secure-api-calls.md) - 安全 API
- [Self-Improving](skills/self-improving.md) - 自我改进
- [Automation Workflows](skills/automation-workflows.md) - 自动化工作流
- [AI Web Automation](skills/ai-web-automation.md) - 网页自动化

## 贡献

欢迎提交新的技能调研报告！

1. Fork 仓库
2. 创建技能调研 MD 文件
3. 更新本 README.md 索引
4. 提交 PR

## License

MIT