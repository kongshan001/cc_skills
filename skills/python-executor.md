# Python Executor

> 在安全的沙箱环境中执行 Python 代码

## 基本信息

| 属性 | 值 |
|------|-----|
| **Slug** | `python-executor` |
| **作者** | okaris |
| **版本** | 0.1.5 |
| **更新时间** | 2026-04-06 |
| **标签** | python, executor, sandbox, data-processing |

## 功能列表

### 核心能力
- **沙箱执行** - 在安全的隔离环境中运行 Python 代码
- **预装库** - 100+ 常用库，开箱即用
- **文件输出** - 自动检测并返回输出文件

### 预装库分类
| 类别 | 库 |
|------|-----|
| Web 抓取 | requests, httpx, beautifulsoup4, lxml, selenium, playwright, scrapy |
| 数据处理 | numpy, pandas, scipy |
| 可视化 | matplotlib, seaborn, plotly |
| 图像处理 | pillow, opencv-python-headless, scikit-image |
| 视频音频 | moviepy, av, pydub |
| 3D 处理 | trimesh, open3d, numpy-stl |
| 文档 | reportlab, pypdf2 |

## 安装方式

### 1. 安装 inference.sh CLI
```bash
curl -fsSL https://cli.inference.sh | sh
infsh login
```

### 2. 运行 Python 代码
```bash
infsh app run infsh/python-executor --input '{
  "code": "print(\"Hello World!\")",
  "timeout": 30
}'
```

### 3. 高级用法
```bash
# 高内存版本 (16GB)
infsh app run infsh/python-executor@high_memory --input input.json
```

## 推荐安装评估

### 本地环境 ⭐⭐⭐⭐⭐
- 适合需要安全执行不可信代码的场景
- 适合快速原型开发和数据处理
- 无需配置，直接使用

### ECS 环境 ⭐⭐⭐⭐⭐
- 适合需要运行耗时任务的服务器场景
- 可集成到 CI/CD 管道
- 支持高并发调用

## 使用示例

### 数据分析
```bash
infsh app run infsh/python-executor --input '{
  "code": "import pandas as pd; import matplotlib.pyplot as plt; ..."
}'
```

### Web 抓取
```bash
infsh app run infsh/python-executor --input '{
  "code": "import requests; from bs4 import BeautifulSoup; ..."
}'
```

### 图像处理
```bash
infsh app run infsh/python-executor --input '{
  "code": "from PIL import Image; ..."
}'
```

## 优缺点分析

### ✅ 优点
- 预装 100+ 库，无需手动安装
- 沙箱环境，安全可靠
- 自动文件输出
- 支持高内存版本

### ⚠️ 限制
- CPU only，无 GPU/ML 库
- 非交互式，需用 plt.savefig() 而非 plt.show()
- 需要网络连接 inference.sh

## 替代方案

| 方案 | 特点 |
|------|------|
| 本地 Python 环境 | 更灵活，需自行管理依赖 |
| Docker 容器 | 可定制，但需要构建 |
| Jupyter Notebook | 交互式，但不适合自动化 |

## 相关技能

- `inference-sh/skills@ai-image-generation` - AI 图像生成
- `inference-sh/skills@ai-video-generation` - AI 视频生成