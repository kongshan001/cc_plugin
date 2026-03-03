# Pi Mono - AI Agent 工具箱

## 📋 文档信息

- **插件名称**: pi-mono (Pi)
- **GitHub**: [badlogic/pi-mono](https://github.com/badlogic/pi-mono)
- **Star**: 19k ⭐
- **状态**: ✅ 已调研
- **调研日期**: 2026-03-03
- **分类**: AI Agent / 编程助手 / 开发者工具

---

## 1. 插件背景需求

### 问题痛点

现有 AI 编程助手（如 Claude Code、Cursor）虽然功能强大，但存在以下局限：
- **工作流固化** - 无法按个人习惯定制
- **功能锁定** - 缺少的功能无法扩展
- **供应商绑定** - 只能使用特定模型提供商
- **扩展困难** - 需要 fork 源码才能定制

### 目标

Pi 是一个**极简终端编程工具**，倡导"适应你的工作流，而非相反"的理念。通过 TypeScript 扩展、Skills、提示模板和主题，让用户完全掌控自己的 AI 编程环境。

---

## 2. 设计方案

### 核心架构

```
┌─────────────────────────────────────────────────────────────────┐
│                        Pi Monorepo                               │
├─────────────────────────────────────────────────────────────────┤
│  ┌─────────────┐   ┌─────────────┐   ┌─────────────┐           │
│  │  pi-ai     │   │  pi-agent   │   │ pi-coding   │           │
│  │  统一LLM API│   │  Agent运行时 │   │  agent CLI  │           │
│  │  多提供商   │   │  工具调用    │   │  交互式终端  │           │
│  └─────────────┘   └─────────────┘   └─────────────┘           │
│        │                 │                  │                   │
│        ▼                 ▼                  ▼                   │
│  ┌─────────────┐   ┌─────────────┐   ┌─────────────┐           │
│  │  pi-tui    │   │  pi-web-ui  │   │   pi-mom    │           │
│  │  终端UI库   │   │  Web聊天组件 │   │  Slack机器人│           │
│  └─────────────┘   └─────────────┘   └─────────────┘           │
│                                                                 │
│                              ┌─────────────┐                    │
│                              │   pi-pods   │                   │
│                              │ vLLM部署CLI │                    │
│                              └─────────────┘                    │
└─────────────────────────────────────────────────────────────────┘
```

### 核心特性

| 包 | 功能 |
|-----|------|
| **pi-ai** | 统一多提供商 LLM API (OpenAI, Anthropic, Google, etc.) |
| **pi-agent-core** | Agent 运行时，支持工具调用和状态管理 |
| **pi-coding-agent** | 交互式编程 agent CLI (核心产品) |
| **pi-mom** | Slack 机器人，消息委托给 pi |
| **pi-tui** | 终端 UI 库，差分渲染 |
| **pi-web-ui** | AI 聊天界面 Web 组件 |
| **pi-pods** | GPU Pod 上 vLLM 部署管理 CLI |

---

## 3. 本地部署

### 前置要求

| 要求 | 说明 |
|-----|------|
| **Node.js** | 18+ 版本 |
| **npm** | 随 Node.js 一起安装 |
| **API Key** | 支持 Anthropic, OpenAI, Google 等 |

### 安装步骤

```bash
# 全局安装 pi
npm install -g @mariozechner/pi-coding-agent

# 方式 A: 使用 API Key
export ANTHROPIC_API_KEY=sk-ant-...
pi

# 方式 B: 使用现有订阅登录
pi
/login  # 然后选择提供商
```

### 快速使用

```bash
# 交互式模式（默认）
pi

# 指定模型
pi /model claude-sonnet-4-20250514

# 继续最近会话
pi -c

# 浏览历史会话
pi -r

# 临时模式（不保存）
pi --no-session
```

### Windows 部署

```powershell
# 使用 npm 安装
npm install -g @mariozechner/pi-coding-agent
pi

# 或使用 npx
npx @mariozechner/pi-coding-agent
```

### 从源码运行

```bash
git clone https://github.com/badlogic/pi-mono.git
cd pi-mono
npm install
npm run build
./pi-test.sh
```

---

## 4. 效果展示

### 交互式界面

```
┌─────────────────────────────────────────────────────────┐
│  ⌘ /hotkeys  │  /settings  │  /skills  │  Extensions    │
├─────────────────────────────────────────────────────────┤
│  > 请帮我创建一个 TODO 应用...                          │
│                                                          │
│  🤖 正在思考...                                          │
│  [调用工具: write - 创建文件]                            │
│  [调用工具: bash - 安装依赖]                              │
│                                                          │
├─────────────────────────────────────────────────────────┤
│  📝 ~/my-app  │  session:today  │  $0.02  │  45% ctx    │
└─────────────────────────────────────────────────────────┘
```

### 核心功能

| 功能 | 说明 |
|-----|------|
| **多模型支持** | Anthropic, OpenAI, Google Gemini, GitHub Copilot 等 |
| **智能补全** | @文件引用、路径补全、多行输入 |
| **会话管理** | 树形会话、分支、压缩 |
| **扩展系统** | 自定义工具、命令、快捷键 |
| **技能系统** | 按需加载 Agent Skills |
| **主题系统** | 深色/浅色主题，热重载 |
| **包管理** | 分享扩展、技能、主题 |

### 支持的模型提供商

**订阅认证：**
- Anthropic Claude Pro/Max
- OpenAI ChatGPT Plus/Pro (Codex)
- GitHub Copilot
- Google Gemini CLI
- Google Antigravity

**API Key：**
- Anthropic / OpenAI / Azure OpenAI
- Google Gemini / Vertex
- Amazon Bedrock / Mistral
- Groq / Cerebras / xAI
- OpenRouter / Vercel AI Gateway
- ZAI / Hugging Face / Kimi / MiniMax

---

## 5. 优缺点分析

### ✅ 优点

| 优点 | 说明 |
|-----|------|
| **极简核心** | 不内置子 agent、计划模式等，保持核心精简 |
| **高度可扩展** | 扩展、Skills、主题完全可定制 |
| **多提供商** | 统一 API，支持 15+ LLM 提供商 |
| **开源免费** | MIT 许可证 |
| **无需 MCP** | 内置扩展系统，无需额外协议 |
| **会话管理强大** | 树形结构支持分支、会话压缩 |
| **SDK 友好** | 支持 RPC 模式，便于集成 |

### ❌ 缺点

| 缺点 | 说明 |
|-----|------|
| **非传统插件** | 是独立 CLI 工具，类似 Claude Code 竞品 |
| **学习曲线** | 扩展系统需要 TypeScript 知识 |
| **社区较小** | 相比 Claude Code 生态较小 |
| **无内置 MCP** | 需要自行构建 MCP 支持 |
| **需自备模型** | 不包含模型，需额外配置 |

---

## 6. 平替插件对比

| 工具 | 特点 | 适用场景 |
|-----|------|---------|
| **Pi** | 极简可扩展编程助手 | 追求定制化的开发者 |
| **Claude Code** | 官方 AI 编程助手 | 日常开发任务 |
| **Cursor** | IDE 集成 AI | 偏好 GUI 的用户 |
| **Windsurf** | Agentic IDE | 完整开发环境 |

---

## 7. 落地过程

### 调研日期
2026-03-03

### 调研结果

#### 🔍 技术定位

Pi 是一个**独立的终端编程工具**，不是 Claude Code 插件。定位类似于：
- Claude Code 的竞品
- 极简版的 AI 编程助手
- 可高度定制的开发者工具

#### 📝 关键发现

1. **设计理念**
   - "Adapt pi to your workflows" - 适应你的工作流
   - 不内置子 agent、计划模式等功能
   - 需要自己用扩展实现

2. **扩展系统**
   - **Extensions**: TypeScript 模块，添加自定义工具、命令、UI
   - **Skills**: Agent Skills 标准，按需加载
   - **Themes**: 主题系统，支持热重载
   - **Pi Packages**: npm/git 包分发

3. **多模型支持**
   - 15+ LLM 提供商
   - 支持自定义 provider
   - 统一 API 接口

4. **Pi vs Claude Code**
   | 特性 | Pi | Claude Code |
   |-----|-----|-------------|
   | 核心大小 | 极简 | 完整 |
   | 扩展方式 | TypeScript | Agent Skills |
   | MCP | 不需要 | 原生支持 |
   | 子 Agent | 需自行实现 | 内置 |
   | 计划模式 | 需自行实现 | 内置 |

#### ✅ 适用场景

- 追求**高度定制化**的开发者
- 需要**多模型切换**的用户
- 喜欢**终端界面**的极客
- 想构建**自己 AI 工具**的开发者

#### ⚠️ 注意事项

- 不是 Claude Code 插件，是**替代品**
- 需要一定 TypeScript 能力进行扩展开发
- 社区生态较小，第三方包较少

---

## 8. 常见问题

### Q: Pi 是 Claude Code 插件吗？
A: 不是。Pi 是一个**独立的 CLI 工具**，与 Claude Code 是竞争关系。

### Q: 支持 MCP 协议吗？
A: 不支持。Pi 使用自己的扩展系统，无需 MCP。

### Q: 可以集成到现有项目吗？
A: 可以。使用 SDK 或 RPC 模式嵌入你的应用。

### Q: 和 Claude Code 相比有什么优势？
A: 更极简、更可定制、多提供商支持。但生态较小。

---

## 📎 相关链接

- [GitHub](https://github.com/badlogic/pi-mono)
- [官网](https://shittycodingagent.ai)
- [Discord](https://discord.com/invite/3cU7Bz4UPx)
- [npm 包](https://www.npmjs.com/package/@mariozechner/pi-coding-agent)
- [Pi 博客](https://mariozechner.at/posts/2025-11-30-pi-coding-agent/)

---

*让 AI 适应你的工作流* 🛠️
