# ClaudeForge

> CLAUDE.md 生成和维护工具 - 高质量项目配置

## 项目信息

- **GitHub**: [alirezarezvani/ClaudeForge](https://github.com/alirezarezvani/ClaudeForge)
- **GitHub Stars**: ⭐ 活跃
- **语言**: Python
- **状态**: ✅ 已调研

---

## 简介

ClaudeForge 是一个 Claude.md 生成和维护工具，帮助开发者创建高质量的 CLAUDE.md 指令文件，遵循 Anthropic 的 Claude Code 最佳实践。

---

## 核心功能

| 功能 | 说明 |
|------|------|
| 自动生成 | 根据项目结构自动生成 CLAUDE.md |
| 最佳实践 | 遵循 Anthropic 官方指南 |
| 维护提醒 | 定期提醒更新文档 |
| 多项目支持 | 支持多个项目配置 |

---

## 功能详解

### 1. 自动分析项目

```bash
# 分析当前项目
claudeforge analyze
```

- 检测项目类型
- 识别依赖关系
- 生成项目结构

### 2. 生成 CLAUDE.md

```bash
# 生成配置文件
claudeforge generate

# 交互式生成
claudeforge init
```

### 3. 维护检查

```bash
# 检查配置是否需要更新
claudeforge check

# 更新配置
claudeforge update
```

---

## 安装方式

```bash
# 从源码安装
git clone https://github.com/alirezarezvani/ClaudeForge.git
cd ClaudeForge
pip install -e .

# 或使用 pip
pip install claudeforge
```

---

## 使用示例

### 基本使用

```bash
# 初始化项目
claudeforge init my-project

# 分析现有项目
claudeforge analyze ./my-project

# 生成 CLAUDE.md
claudeforge generate --template standard
```

### 高级选项

```bash
# 自定义模板
claudeforge generate --template advanced

# 仅生成特定部分
claudeforge generate --section rules

# 导出配置
claudeforge export --format yaml
```

---

## 模板类型

| 模板 | 适用场景 |
|------|----------|
| basic | 小型项目 |
| standard | 中型项目 |
| advanced | 大型/复杂项目 |
| minimal | 快速启动 |

---

## 优缺点

### ✅ 优点

- 遵循官方最佳实践
- 自动分析项目结构
- 减少手动配置
- 支持多种模板

### ❌ 缺点

- 仍在活跃开发中
- 部分功能待完善

---

## 相关资源

- [Anthropic Claude Code 文档](https://docs.anthropic.com/en/docs/claude-code)
- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
