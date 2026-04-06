# LSP Python

> Python 代码质量检查和 LSP 集成

## 基本信息

| 属性 | 值 |
|------|-----|
| **Slug** | `lsp-python` |
| **作者** | genify |
| **版本** | 1.1.0 |
| **更新时间** | 2026-04-06 |
| **标签** | python, lsp, code-quality, pylint |

## 功能列表

### 代码诊断
- **pyflakes** - 代码错误检测 (未使用导入、未定义变量等)
- **pycodestyle** - PEP8 风格检查

### LSP 功能
- 代码补全
- 悬停提示 (函数签名、文档)
- 跳转定义

### 批量检查
- 批量检查项目文件
- 自动修复支持
- 生成检查报告

## 安装方式

### 1. 安装依赖
```bash
pip install python-lsp-server
pip install python-lsp-server[all]  # 完整插件集
pip install pylsp-mypy              # 类型检查
pip install pylsp-black             # 格式化
```

### 2. 使用方式
```bash
# 检查单个文件
python3 scripts/lsp-service.py check <文件路径>

# 批量检查
python3 scripts/check_python.py <文件或目录>

# 自动修复
python3 scripts/check_python.py --auto-fix <目录>
```

## 推荐安装评估

### 本地环境 ⭐⭐⭐⭐⭐
- 适合代码审查
- 适合 CI 集成
- 适合编辑器集成

### ECS 环境 ⭐⭐⭐⭐
- 适合自动化代码检查
- 适合批量项目审计

## 输出示例

```
⚠️ 第 3 行 [pyflakes]: 'os' imported but unused
⚠️ 第 6 行 [pycodestyle]: E302 expected 2 blank lines, found 1
✅ 没有发现问题
```

## 自动修复流程

```bash
# 1. 备份
cp -r project/ project.backup

# 2. 清理导入
autoflake --remove-all-unused-imports --in-place --recursive project/

# 3. 格式化
black project/

# 4. 验证
python3 scripts/lsp-service.py check project/main.py
```

## 优缺点分析

### ✅ 优点
- 轻量级 LSP 实现
- 支持自动修复
- 批量检查能力
- 中文输出

### ⚠️ 局限
- 需要 Python 环境
- 需要安装依赖

## 替代方案

| 方案 | 特点 |
|------|------|
| Pylint | 更严格的检查 |
| Ruff | 速度更快 |
| Pyright | 类型检查强 |