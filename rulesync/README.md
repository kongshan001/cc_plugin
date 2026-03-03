# Rulesync - Claude Code 配置同步工具

## 📋 文档信息

- **插件名称**: Rulesync
- **GitHub**: [dyoshikawa/rulesync](https://github.com/dyoshikawa/rulesync)
- **Star**: ⭐ (活跃维护)
- **状态**: ✅ 已调研
- **调研日期**: 2026-03-04
- **分类**: 开发者工具 / 配置管理 / 跨平台同步

---

## 1. 插件背景需求

### 问题痛点

- 多个 AI 编码 agent (Claude Code, Cursor, Codex, etc.) 需要不同的配置文件
- 手动维护多套配置耗时且容易出错
- 团队成员使用不同的 AI 工具，配置难以统一
- 配置更新需要同步到所有相关项目

### 目标

Rulesync 是一个 **Node.js CLI 工具**，可以自动为各种 AI 编码 agent 生成配置（规则、忽略文件、MCP 服务器、命令和子代理），并在不同 AI agent 之间双向转换配置。

---

## 2. 设计方案

### 核心架构

```
┌─────────────────────────────────────────────────────────────────┐
│                      Rulesync 架构                               │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│   ┌─────────────┐   ┌─────────────┐   ┌─────────────┐         │
│   │ Claude Code │   │   Cursor    │   │   Codex     │         │
│   │   Config   │   │   Config    │   │   Config    │         │
│   └──────┬──────┘   └──────┬──────┘   └──────┬──────┘         │
│          │                 │                 │                 │
│          └─────────────────┼─────────────────┘                 │
│                            ▼                                    │
│   ┌─────────────────────────────────────────────────────────┐   │
│   │                    Rulesync Core                         │   │
│   │         配置解析 / 格式转换 / 同步管理                     │   │
│   └─────────────────────────────────────────────────────────┘   │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### 支持的配置类型

| 配置类型 | 说明 |
|---------|------|
| **Rules** | Linting/格式化规则 |
| **Ignore Files** | .gitignore, .claudeignore 等 |
| **MCP Servers** | MCP 服务器配置 |
| **Commands** | Slash 命令定义 |
| **Subagents** | 子代理配置 |

### 支持的 AI Agent

| Agent | 支持情况 |
|-------|---------|
| Claude Code | ✅ 完整支持 |
| Cursor | ✅ 完整支持 |
| Codex | ✅ 完整支持 |
| OpenCode | ✅ 完整支持 |
| Others | 🔄 可扩展 |

---

## 3. 本地部署

### 前置要求

| 要求 | 说明 |
|-----|------|
| **Node.js** | 18+ |
| **npm** | 10+ |
| **Git** | 可选 |

### 安装步骤

```bash
# 1. 全局安装
npm install -g rulesync

# 2. 验证安装
rulesync --version

# 3. 查看帮助
rulesync --help
```

### 快速开始

```bash
# 1. 初始化项目配置
rulesync init

# 2. 从现有配置导入
rulesync import --source cursor --target claude

# 3. 同步配置到目标
rulesync sync --target cursor

# 4. 查看差异
rulesync diff --source claude --target cursor
```

---

## 4. 核心功能详解

### 4.1 配置转换

```markdown
### 功能说明
- 在不同 AI agent 配置格式之间转换
- 自动映射等效配置项
- 处理格式差异和特殊字段

### 示例转换
Claude Code → Cursor:
- .claude/commands/* → .cursorrules/commands/*
- settings.json → .cursorrules/settings.json
```

### 4.2 配置生成

```markdown
### 生成能力
- 根据项目类型自动生成基础配置
- 支持自定义模板
- 批量生成多套配置

### 模板变量
- {projectName}
- {language}
- {framework}
- {aiTool}
```

### 4.3 配置同步

```markdown
### 同步模式
- 单向同步: source → target
- 双向同步: 合并差异
- 增量同步: 只更新变更部分

### 冲突处理
- 提示用户手动解决
- 自动保留最新版本
- 支持规则优先级
```

### 4.4 MCP 服务器配置

```markdown
### 功能
- 自动发现可用的 MCP 服务器
- 生成 MCP 配置
- 跨平台 MCP 配置转换

### 支持的 MCP
- Filesystem
- Git
- GitHub
- Database
- Custom
```

---

## 5. 适用场景

### ✅ 适用场景

| 场景 | 说明 |
|------|------|
| **多工具协作** | 团队使用不同 AI 工具 |
| **配置迁移** | 从一个 AI 工具迁移到另一个 |
| **统一团队配置** | 维护一致的编码规范 |
| **项目模板** | 快速生成项目配置 |

### ⚠️ 注意事项

| 场景 | 说明 |
|------|------|
| 配置冲突 | 需要手动解决 |
| 自定义配置 | 可能无法完美转换 |
| 敏感信息 | 需要自行处理 |

---

## 6. 优缺点分析

### ✅ 优点

| 优点 | 说明 |
|-----|------|
| **多平台支持** | 支持主流 AI 编码工具 |
| **自动化** | 减少手动配置工作 |
| **双向转换** | 灵活的配置同步 |
| **开源免费** | MIT 许可证 |

### ❌ 缺点

| 缺点 | 说明 |
|-----|------|
| **转换不完美** | 部分自定义配置可能丢失 |
| **学习曲线** | 需要理解配置格式 |
| **维护频率** | AI 工具更新可能导致兼容问题 |

---

## 7. 常用命令

```bash
# 初始化新项目的配置
rulesync init [project-type]

# 导入现有配置
rulesync import --source <tool> --target <tool>

# 同步配置
rulesync sync --target <tool>

# 查看差异
rulesync diff --source <tool> --target <tool>

# 生成 MCP 配置
rulesync mcp generate --server <server-name>

# 列出支持的工具
rulesync list-tools

# 更新规则
rulesync update
```

---

## 8. 落地过程

### 调研日期
2026-03-04

### 快速开始示例

```bash
# 1. 全局安装
npm install -g rulesync

# 2. 初始化项目
mkdir my-game-project && cd my-game-project
rulesync init game-unity

# 3. 导入 Claude Code 配置
rulesync import --source claude-code --target cursor

# 4. 查看生成的配置
ls -la .cursorrules/
```

### 验证结果

| 验证项 | 结果 |
|-------|------|
| 仓库可访问 | ✅ |
| npm 包可用 | ✅ |
| 文档完整性 | ✅ |
| 活跃维护 | ✅ |

---

## 9. 与项目结合

### game-frame-sync 项目配置

```bash
# 为帧同步项目生成配置
rulesync init python-fastapi

# 添加 MCP 服务器
rulesync mcp generate --server filesystem
rulesync mcp generate --server github

# 同步到团队成员
rulesync sync --target cursor
rulesync sync --target claude-code
```

---

## 📎 相关链接

- [GitHub](https://github.com/dyoshikawa/rulesync)
- [npm 包](https://www.npmjs.com/package/rulesync)
- [文档](./docs/)

---

*跨平台配置同步，一键搞定* 🔄
