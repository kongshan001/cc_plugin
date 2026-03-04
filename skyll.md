# Skyll

> AI 技能自主发现与学习工具

## 项目信息

- **GitHub**: [assafelovic/skyll](https://github.com/assafelovic/skyll)
- **GitHub Stars**: ⭐ 活跃
- **语言**: Python
- **状态**: ✅ 已调研

---

## 简介

Skyll 是一个创新的 AI 工具，帮助 AI 代理（如 Claude Code）自主发现和学习新技能。它能够从文档、代码库和教程中提取技能知识，并将其转化为可执行的 AI 技能。

---

## 核心功能

| 功能 | 说明 |
|------|------|
| 技能发现 | 自动从各种来源发现新技能 |
| 技能学习 | 将文档转化为可执行技能 |
| 技能存储 | 结构化存储和管理技能 |
| 技能推荐 | 根据上下文推荐相关技能 |

---

## 工作原理

```
文档/代码 → Skyll 分析 → 技能提取 → 技能库 → Claude Code 使用
```

### 1. 技能发现

- 扫描 GitHub 仓库
- 分析 npm/pypi 包
- 提取 README 文档

### 2. 技能提取

- 解析代码示例
- 提取 API 调用模式
- 生成技能定义

### 3. 技能存储

- 结构化 JSON 格式
- 版本控制
- 分类标签

---

## 安装方式

```bash
# 从源码安装
git clone https://github.com/assafelovic/skyll.git
cd skyll
pip install -e .

# 或使用 pip
pip install skyll
```

---

## 使用示例

### 基本使用

```bash
# 发现技能
skyll discover --source github

# 学习新技能
skyll learn --package fastapi

# 列出可用技能
skyll list

# 搜索技能
skyll search "web development"
```

### 高级使用

```bash
# 从自定义源学习
skyll learn --source docs/tensorflow

# 导出技能
skyll export --format json

# 导入技能
skyll import --file skills.json
```

---

## 技能格式

```json
{
  "name": "fastapi_get_started",
  "description": "Create a basic FastAPI application",
  "category": "web",
  "examples": [
    {
      "code": "from fastapi import FastAPI\napp = FastAPI()",
      "explanation": "Basic FastAPI setup"
    }
  ],
  "tags": ["python", "api", "web"],
  "difficulty": "beginner"
}
```

---

## 优缺点

### ✅ 优点

- 自动化技能获取
- 减少手动配置
- 持续更新技能库
- 社区贡献支持

### ❌ 缺点

- 仍在开发中
- 准确性待验证
- 需要网络连接

---

## 对比传统技能

| 方面 | 传统方式 | Skyll |
|------|---------|-------|
| 获取方式 | 手动克隆 | 自动发现 |
| 更新频率 | 依赖维护者 | 实时更新 |
| 覆盖范围 | 有限 | 广泛 |
| 准确性 | 较高 | 待验证 |

---

## 相关资源

- [Skyll 官方文档](https://github.com/assafelovic/skyll)
- [awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills)
- [MCP 官方文档](https://modelcontextprotocol.io)
