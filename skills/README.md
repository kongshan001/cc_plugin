# OpenAI Skills - Codex 官方技能目录

## 📋 文档信息

- **插件名称**: OpenAI Skills
- **GitHub**: [openai/skills](https://github.com/openai/skills)
- **Star**: 10k ⭐
- **状态**: ✅ 已调研
- **调研日期**: 2026-03-03
- **分类**: Agent Skills / Codex 扩展 / 官方技能库

---

## 1. 插件背景需求

### 问题痛点

AI 编程助手（如 Claude Code、Codex）虽然功能强大，但存在以下局限：
- **能力边界固定** - 无法按需扩展特定领域能力
- **工作流重复** - 相同任务每次都需要重新描述
- **知识零散** - 领域知识需要每次手动提供
- **缺乏标准化** - 团队无法共享最佳实践

### 目标

OpenAI Skills 作为 **Codex 官方技能目录**，提供可发现、可复用的 AI Agent 能力扩展包，让团队和个人能够以标准化方式封装和分发专业领域的 AI 工作流。

---

## 2. 设计方案

### 核心架构

```
┌─────────────────────────────────────────────────────────────────┐
│                    OpenAI Skills 架构                            │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│   ┌─────────────┐   ┌─────────────┐   ┌─────────────┐           │
│   │  .system   │   │  .curated   │   │ .experimental│          │
│   │  系统内置   │   │   精选技能   │   │  实验性技能  │          │
│   │  (2个)     │   │   (30个)    │   │   (多个)    │           │
│   └─────────────┘   └─────────────┘   └─────────────┘           │
│                                                                 │
│                              │                                    │
│                              ▼                                    │
│   ┌─────────────────────────────────────────────────────────┐    │
│   │                    Codex AI 助手                         │    │
│   │         (Skills 被动态加载到 Agent 上下文)               │    │
│   └─────────────────────────────────────────────────────────┘    │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### 技能类型

| 类型 | 位置 | 说明 | 安装方式 |
|-----|------|------|---------|
| **系统技能** | `.system/` | Codex 内置，无需安装 | 自动可用 |
| **精选技能** | `.curated/` | 官方验证的质量技能 | `$skill-installer gh-address-comments` |
| **实验性技能** | `.experimental/` | 社区贡献的测试技能 | 指定 GitHub 目录 URL |

### 技能目录结构

```
skill-name/
├── SKILL.md (required)          # 技能定义文件
├── agents/                      # UI 元数据
│   └── openai.yaml             # 显示名称、描述
├── scripts/                     # 可执行脚本
│   └── *.py / *.sh             # 辅助代码
├── references/                  # 参考文档
│   └── *.md                    # 领域知识
└── assets/                      # 资源文件
    └── *.*                     # 模板、图片等
```

### SKILL.md 格式

```yaml
---
name: skill-name
description: 技能描述（触发条件），当用户请求匹配时自动加载
metadata:
  short-description: 简短描述
---

# 技能使用指南

## 触发条件
- 详细说明何时应该使用此技能

## 使用方法
- 步骤1
- 步骤2

## 参考资源
- [详细文档](references/detail.md)
```

### 渐进式加载设计

Skills 使用三层加载机制优化上下文：

1. **元数据** (name + description) - 始终加载 (~100 tokens)
2. **SKILL.md 正文** - 技能触发后加载 (<5k tokens)
3. **Bundled Resources** - 按需加载（脚本可执行而不加载到上下文）

---

## 3. 本地部署

### 前置要求

| 要求 | 说明 |
|-----|------|
| **Codex** | OpenAI Codex IDE 或 CLI |
| **网络** | 访问 GitHub 下载技能 |

### 安装步骤

#### 方式 1: 使用 $skill-installer（推荐）

```bash
# 在 Codex 中直接安装
$skill-installer gh-address-comments

# 或指定 GitHub 目录 URL
$skill-installer install https://github.com/openai/skills/tree/main/skills/.experimental/create-plan
```

#### 方式 2: 手动复制

```bash
# 克隆技能仓库
git clone https://github.com/openai/skills.git

# 复制到 Codex 技能目录
cp -r skills/.curated/gh-address-comments ~/.codex/skills/
```

### 验证安装

```bash
# 在 Codex 中列出可用技能
$skill-installer list

# 或查看技能是否出现在 Codex UI 中
```

### 常用技能列表

#### .system (内置)

| 技能 | 功能 |
|-----|------|
| **skill-creator** | 创建新技能的指导 |
| **skill-installer** | 安装和管理技能 |

#### .curated (精选)

| 类别 | 技能列表 |
|-----|---------|
| **开发** | develop-web-game, jupyter-notebook, playwright |
| **部署** | cloudflare-deploy, netlify-deploy, render-deploy, vercel-deploy |
| **设计** | figma, figma-implement-design, screenshot |
| **文档** | doc, openai-docs, notion-* (多个) |
| **安全** | security-best-practices, security-ownership-map, security-threat-model |
| **GitHub** | gh-address-comments, gh-fix-ci |
| **其他** | chatgpt-apps, imagegen, linear, pdf, speech, spreadsheet, transcribe, yeet |

---

## 4. 效果展示

### 技能触发机制

Codex 根据 SKILL.md 中的 `description` 字段自动判断何时加载技能：

```
用户请求 → 匹配 description → 加载 SKILL.md → 按需加载 resources
```

### 使用示例

#### 示例 1: GitHub PR 评论处理

```bash
# 在 Codex 中
$skill-installer gh-address-comments

# 然后自然语言触发
"帮我处理这个 PR 的 review comments"
```

Codex 自动：
1. 获取当前分支的 open PR
2. 列出所有评论和讨论
3. 询问用户需要处理哪些
4. 应用修复

#### 示例 2: 创建新技能

```bash
# 使用内置 skill-creator
"帮我创建一个用于代码审查的新技能"
```

Codex 自动：
1. 引导完成技能规划
2. 生成 SKILL.md 模板
3. 创建目录结构
4. 提供验证工具

### 技能市场

```
skills/.curated/
├── chatgpt-apps/          # ChatGPT 应用开发
├── cloudflare-deploy/    # Cloudflare 部署
├── develop-web-game/     # 网页游戏开发
├── doc/                  # 文档处理
├── figma/                # Figma 设计
├── figma-implement-design/ # Figma 设计实现
├── gh-address-comments/  # GitHub PR 评论处理 ← 最热门
├── gh-fix-ci/            # CI 修复
├── imagegen/              # 图像生成
├── jupyter-notebook/     # Jupyter Notebook
├── linear/               # Linear 项目管理
├── notion-*/             # Notion 集成 (多个)
├── openai-docs/         # OpenAI 文档
├── pdf/                  # PDF 处理
├── playwright/           # Playwright 测试
├── security-*/           # 安全相关 (多个)
├── speech/               # 语音处理
├── spreadsheet/          # 电子表格
├── transcribe/           # 转录
└── vercel-deploy/       # Vercel 部署
```

---

## 5. 优缺点分析

### ✅ 优点

| 优点 | 说明 |
|-----|------|
| **官方支持** | OpenAI 官方维护，质量有保障 |
| **标准化格式** | 统一的技能结构，易于理解和创建 |
| **渐进式加载** | 优化上下文使用，不会一次性加载所有内容 |
| **社区活跃** | 实验性技能不断更新 |
| **可扩展性** | 任何人都可以创建和分享技能 |
| **MCP 互补** | 与 MCP 协议互补，提供更高层次的抽象 |

### ❌ 缺点

| 缺点 | 说明 |
|-----|------|
| **Codex 限定** | 仅适用于 OpenAI Codex，不支持 Claude Code |
| **生态较小** | 相比 Claude Code Skills 生态较小 |
| **需要 Codex** | 非 Codex 用户无法使用 |
| **技能数量有限** | 精选技能仅 30+ 个 |

---

## 6. 平替插件对比

| 工具 | 特点 | 适用场景 |
|-----|------|---------|
| **OpenAI Skills** | Codex 官方技能系统 | Codex 用户 |
| **Claude Code Skills** | Agent Skills 框架 | Claude Code 用户 |
| **MCP** | 模型上下文协议 | 跨平台工具集成 |
| **Pi Extensions** | TypeScript 扩展 | Pi 用户 |

---

## 7. 落地过程

### 调研日期
2026-03-03

### 调研结果

#### 🔍 技术定位

OpenAI Skills 是 **Codex (OpenAI AI 编程工具) 的官方技能系统**，类似于：
- Claude Code 的 Agent Skills
- 但更标准化、官方维护
- 使用 YAML frontmatter + Markdown 格式

#### 📝 关键发现

1. **技能结构**
   - 统一的 `SKILL.md` 格式
   - 支持 scripts/references/assets 分离
   - 渐进式上下文加载

2. **安装方式**
   - 内置 `$skill-installer` 命令
   - 支持从 GitHub 直接安装
   - 简单易用

3. **创建流程**
   - `skill-creator` 提供完整指导
   - `init_skill.py` 生成模板
   - `quick_validate.py` 验证格式

4. **与 Claude Code 对比**
   | 特性 | OpenAI Skills | Claude Code Skills |
   |-----|---------------|-------------------|
   | 维护 | OpenAI 官方 | 社区 |
   | 格式 | YAML+Markdown | 自定义 |
   | 数量 | 30+ 精选 | 更多样 |
   | 加载 | 渐进式 | 一次性 |

#### ✅ 适用场景

- **Codex 用户** - 扩展 Codex 能力
- **团队协作** - 共享标准化工作流
- **技能开发** - 创建可复用 AI 技能

#### ⚠️ 注意事项

- 仅适用于 **OpenAI Codex**
- 不是 Claude Code 插件
- 需要网络访问安装技能

---

## 8. 常见问题

### Q: OpenAI Skills 是 Claude Code 插件吗？
A: 不是。它是 **OpenAI Codex** 的官方技能系统。

### Q: 可以在 Claude Code 中使用吗？
A: 不可以直接使用，但可以参考其格式创建 Claude Code Skills。

### Q: 如何创建自定义技能？
A: 使用 Codex 中的 `$skill-installer` 或运行 `scripts/init_skill.py`。

### Q: 技能和 MCP 有什么区别？
A: Skills 提供更高层次的抽象（工作流、领域知识），MCP 提供底层工具集成。两者互补。

---

## 📎 相关链接

- [GitHub](https://github.com/openai/skills)
- [Codex Skills 文档](https://developers.openai.com/codex/skills)
- [创建技能指南](https://developers.openai.com/codex/skills/create-skill)
- [Agent Skills 开放标准](https://agentskills.io)

---

*让 AI 掌握你的专业技能* 🛠️
