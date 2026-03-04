# Claude Code 热门插件补充调研 (v51)

> 2026年3月 游戏/Python/测试/开发者工具热门插件完整调研

---

## 一、游戏客户端开发插件

### 1.1 Claude-Code-Game-Studios 游戏工作室

> 48 个 AI 代理 + 36 个工作流技能的全能游戏开发工作室

#### 背景需求

游戏开发涉及多个专业领域（编程、美术、音频、测试），需要完整的开发工作室支持。

#### 目标

将 Claude Code 打造成完整游戏开发工作室，模拟真实游戏工作室工作流。

#### 设计方案

- **48 个 AI 代理**：设计、编程、美术、音频、测试
- **36 个工作流技能**：项目管理、代码审查、测试自动化
- **协调系统**：模拟真实工作室团队协作
- **多代理并行工作**：支持多个代理同时工作
- **多引擎支持**：Unity, Unreal, Godot, WebGL

#### 本地部署

```bash
git clone https://github.com/Donchitos/Claude-Code-Game-Studios ~/.claude/plugins/
```

#### 效果展示

- GitHub Stars：⭐ 28
- 更新频率：活跃（4天前更新）

#### 优缺点

✅ 功能全面，涵盖游戏开发全流程  
✅ 工作室级架构，多代理协作  
⚠️ 学习曲线陡峭  
⚠️ 配置相对复杂

---

### 1.2 Claude-Code-Game-Master RPG 游戏大师

> 使用 RAG 和 RPG 规则集在任意书籍或世界中玩持久冒险游戏

#### 背景需求

游戏爱好者希望通过 AI 在经典文学作品中体验沉浸式 RPG 冒险。

#### 目标

将任何书籍或世界变成可玩的 AI 驱动 RPG 冒险。

#### 设计方案

- **RAG 知识检索**：从书籍中提取角色和情节
- **RPG 规则引擎**：完整的游戏机制
- **持久化冒险**：跨会话的游戏进度
- **AI 驱动叙事**：动态生成对话和情节

#### 本地部署

```bash
git clone https://github.com/Sstobo/Claude-Code-Game-Master ~/.claude/plugins/
```

#### 效果展示

- GitHub Stars：⭐ 86
- 独特的书籍转游戏体验

#### 优缺点

✅ 创新的文学+游戏结合  
✅ RAG 技术应用  
✅ 持久化冒险系统  
⚠️ 特定用例，较窄受众

---

### 1.3 Unreal-MCP Unreal Engine 集成

> 通过自然语言控制 Unreal Engine 的 MCP 服务器

#### 背景需求

Unreal Engine 是业界领先的 3A 游戏引擎，需要与 AI 助手深度集成。

#### 目标

让 Claude Code、Cursor、Windsurf 等 AI 助手可以通过自然语言控制 Unreal Engine。

#### 设计方案

- **Actor 管理**：创建/删除 actors（立方体、球体、灯光、相机等）
- **Actor 属性**：设置 transform（位置、旋转、缩放）
- **Blueprint 开发**：
  - 创建 Blueprint 类
  - 添加/配置组件
  - 编写节点图
  - 编译 Blueprints
- **编辑器控制**：视口聚焦、相机控制

#### 本地部署

```bash
# 1. 克隆仓库
git clone https://github.com/chongdashu/unreal-mcp.git

# 2. 使用 starter 项目 (UE 5.5+)
cd MCPGameProject

# 3. 配置 MCP (Claude Desktop)
# ~/.config/claude-desktop/mcp.json
{
  "mcpServers": {
    "unrealMCP": {
      "command": "uv",
      "args": [
        "--directory",
        "<path/to/unreal-mcp/Python>",
        "run",
        "unreal_mcp_server.py"
      ]
    }
  }
}
```

#### 技术栈

- Unreal Engine 5.5+
- Python 3.12+
- FastMCP
- C++ Plugin

#### 效果展示

- **GitHub Stars**：活跃开发中
- **实验状态**：API 可能有重大变化
- **支持客户端**：Claude Desktop、Cursor、Windsurf

#### 优缺点

✅ 首个 Unreal Engine MCP 集成  
✅ 自然语言控制 UE  
✅ Blueprint 节点图操作  
✅ 完整 actor 生命周期管理  

⚠️ 实验阶段，不建议生产使用  
⚠️ 需要 UE 5.5+  
⚠️ 配置相对复杂

---

### 1.4 Unity GameDev Skills

> 符合 Claude Code Skills 规范的 Unity 专业开发技能集

#### 本地部署

```bash
# 选项 1: OstrichHermit 版本
git clone https://github.com/OstrichHermit/OH-Unity-GameDev-Skills ~/.claude/plugins/

# 选项 2: tjboudreaux 版本
git clone https://github.com/tjboudreaux/cc-plugin-unity-gamedev ~/.claude/plugins/
```

#### 效果展示

- GitHub Stars：⭐ 1-6

#### 技能分类

| 分类 | 技能 |
|-----|------|
| **工具类** | Addressables, MemoryPack, ScriptableObjects, Profiling |
| **动画/物理** | Animation, Physics, NavMesh, Object Pooling, State Machine |
| **AI/行为** | Behavior Designer, GAS (Gameplay Ability System) |
| **音视频** | Wwise音频, Cinemachine相机 |
| **UI** | UGUI, Mobile Optimization |
| **测试** | Unity Test Framework |
| **DI/异步** | VContainer, UniTask |

---

### 1.5 Godot MCP (社区版)

> Godot 引擎的 MCP 集成（社区开发）

#### 背景需求

Godot 是开源游戏引擎的重要选择，需要 MCP 集成支持。

#### 目标

让 AI 助手可以通过自然语言控制 Godot 引擎。

#### 设计方案

- **场景管理**：创建/操作场景和节点
- **脚本生成**：GDScript 自动生成
- **资源操作**：导入/导出资源
- **调试支持**：查看和修改运行时状态

#### 本地部署

```bash
# 社区版本（需要自行编译）
git clone https://github.com/godotengine/godot-mcp.git
```

---

## 二、Python 开发插件

### 2.1 FastAPI-MCP FastAPI MCP 服务器

> 将 FastAPI 端点暴露为 MCP 工具，支持认证！

#### 背景需求

FastAPI 是现代 Python Web 开发的主流框架，需要与 AI 助手深度集成。

#### 目标

零/最小配置将 FastAPI 应用转换为 MCP 服务器。

#### 设计方案

- **原生认证**：使用现有的 FastAPI 依赖注入
- **FastAPI 原生**：不只是 OpenAPI → MCP 转换器
- **零配置**：指向 FastAPI 应用即可工作
- **保留 Schema**：请求/响应模型的完整 schema
- **保留文档**：所有端点的文档如同 Swagger
- **灵活部署**：可挂载到同一应用或独立部署
- **ASGI 传输**：直接使用 FastAPI 的 ASGI 接口

#### 本地部署

```bash
# 安装
uv add fastapi-mcp
# 或
pip install fastapi-mcp

# 简单使用
from fastapi import FastAPI
from fastapi_mcp import FastApiMCP

app = FastAPI()
mcp = FastApiMCP(app)
mcp.mount()

# 访问 MCP 端点: https://app.base.url/mcp
```

#### 配置 MCP 客户端

```json
{
  "mcpServers": {
    "my-fastapi": {
      "command": "uv",
      "args": [
        "run",
        "fastapi-mcp",
        "--app",
        "main:app"
      ]
    }
  }
}
```

#### 效果展示

- PyPI 包：fastapi-mcp
- 官方文档：fastapi-mcp.tadata.com
- 趋势排名：trendshift.io #14064

#### 优缺点

✅ 原生认证集成  
✅ 零配置  
✅ FastAPI 原生设计  
✅ 保留完整 schema 和文档  
✅ 支持独立部署  

⚠️ 需要 Python 3.10+（推荐 3.12）

---

### 2.2 Pydantic AI Skills

> Agent Skills 支持 + Pydantic AI 渐进式披露

#### 背景需求

Pydantic AI 是构建生产级 AI 代理的流行框架，需要专门的 Claude Code 技能支持。

#### 目标

提供 Pydantic AI 开发的最佳实践和技能。

#### 本地部署

```bash
# PyPI 安装
pip install pydantic-ai-skills

# 或 GitHub 克隆
git clone https://github.com/DougTrajano/pydantic-ai-skills ~/.claude/plugins/
```

#### 效果展示

- GitHub Stars：⭐ 138
- 更新频率：活跃（3小时前更新）

---

### 2.3 cc-devops-skills

> 详细到令人发指的 DevOps 工程师技能集

#### 背景需求

DevOps 工程师需要处理各种云平台和基础设施。

#### 目标

提供全能的 DevOps 技能集。

#### 设计方案

- 验证器（Validators）
- 生成器（Generators）
- Shell 脚本
- CLI 工具
- IaC 代码生成（AWS、Azure、GCP、K8s等）

#### 本地部署

```bash
git clone https://github.com/akin-ozer/cc-devops-skills ~/.claude/plugins/
```

---

### 2.4 read-only-postgres

> PostgreSQL 只读查询技能

#### 背景需求

数据库查询是常见开发需求，需要安全的方式让 AI 执行查询。

#### 目标

提供安全的 PostgreSQL 只读查询能力。

#### 设计方案

- 支持 SELECT/SHOW/EXPLAIN/WITH 查询
- 严格验证
- 超时和行数限制
- 多连接配置

#### 本地部署

```bash
git clone https://github.com/jawwadfirdousi/agent-skills ~/.claude/plugins/
```

---

### 2.5 cchooks Python Hooks SDK

> 轻量级 Python SDK，简化 Claude Code Hooks 开发

#### 背景需求

编写 Claude Code Hooks 需要处理复杂的 JSON 配置。

#### 目标

提供简洁的 API 来编写和集成 Hooks。

#### 设计方案

- 简洁的 API 设计
- 良好的文档
- 抽象 JSON 配置细节
- 支持常见的 Hook 场景

#### 本地部署

```bash
# PyPI 安装
pip install cchooks

# 或克隆
git clone https://github.com/GowayLee/cchooks ~/.claude/plugins/
```

#### 效果展示

- GitHub Stars：⭐ 关注中

---

### 2.6 ty-lsp-claude-code

> Python 类型检查器 ty (from Astral) 的 Claude Code 插件

#### 背景需求

ty 是新一代 Python 类型检查器，需要 Claude Code 集成。

#### 目标

提供 ty 类型检查的 Claude Code 支持。

#### 本地部署

```bash
# 安装 ty
pip install ty

# 配置 Claude Code 使用 ty 进行类型检查
```

#### 效果展示

- GitHub Stars：⭐ 4

---

## 三、自动化测试插件

### 3.1 MCPJam Inspector MCP 测试调试工具

> 测试和调试 MCP 服务器、ChatGPT 应用和 MCP Apps 的本地开发客户端

#### 背景需求

MCP 生态快速发展，需要专业的测试和调试工具。

#### 目标

成为迭代任何 MCP 项目的最快方式。

#### 设计方案

- **ChatGPT Apps SDK**：本地开发支持
- **MCP Apps (Claude)**：完整的 MCP Apps 本地开发
- **OAuth 调试器**：可视化检查每条网络消息
- **LLM Playground**：与任何 LLM 对话
- **MCP 服务器调试**：手动调用工具、资源、提示
- **服务器信息**：查看服务器图标、版本、能力

#### 本地部署

```bash
# npx 方式（推荐）
npx @mcpjam/inspector@latest

# 桌面应用
# Mac: https://github.com/MCPJam/inspector/releases/latest/download/MCPJam.Inspector.dmg
# Windows: https://github.com/MCPJam/inspector/releases/latest/download/MCPJam-Inspector-Setup.exe

# Docker
docker run -p 6274:6274 mcpjam/mcp-inspector
```

#### 核心功能

| 功能 | 描述 |
|------|------|
| Apps Builder | 本地模拟器快速查看和迭代 widgets |
| OAuth Debugger | 逐步可视化 OAuth 握手，支持所有协议版本 |
| LLM Playground | 免费使用 GPT-5、Claude Sonnet 等前沿模型 |
| MCP Tools Testing | 测试工具、资源、提示，完整 JSON-RPC 日志 |

#### 效果展示

- 官方文档：mcpjam.com
- Discord 社区支持
- 支持 Mac、Windows、Linux

#### 优缺点

✅ 免费前沿模型  
✅ 无需 ngrok  
✅ 完整调试功能  
✅ 桌面应用 + CLI  
✅ OAuth 调试专家  

⚠️ 需要理解 MCP 协议

---

### 3.2 Playwright Skill

> 浏览器自动化 Claude Code 技能，模型驱动

#### 背景需求

浏览器自动化是 Web 开发测试的重要部分。

#### 目标

提供基于模型的浏览器自动化能力。

#### 本地部署

```bash
# MCP 服务器方式
npx -y @modelcontextprotocol/server-playwright

# 技能方式
git clone https://github.com/lackeyjb/playwright-skill ~/.claude/plugins/
```

#### 效果展示

- GitHub Stars：⭐ 1.9k
- 最流行的 Claude Code 自动化技能

---

### 3.3 Claude Code Playwright MCP Test

> 专为 Claude Code 设计的 YAML-based Playwright MCP 自动化测试框架

#### 背景需求

需要声明式的自动化测试方式。

#### 目标

提供 YAML 驱动的 Playwright 测试框架。

#### 本地部署

```bash
git clone https://github.com/terryso/claude-code-playwright-mcp-test ~/.claude/plugins/
```

#### 效果展示

- GitHub Stars：⭐ 164

---

### 3.4 TDD Guard

> 基于 Hook 的实时 TDD 监控系统

#### 背景需求

TDD 开发需要实时监控测试状态。

#### 目标

提供实时的 TDD 监控。

#### 本地部署

```bash
git clone https://github.com/nizos/tdd-guard ~/.claude/plugins/
```

---

### 3.5 /repro-issue 命令

> 创建可复现的测试用例

#### 背景需求

Bug 修复需要可复现的测试用例。

#### 目标

为 GitHub issues 创建可复现的测试用例。

#### 本地部署

```bash
# 来自 Metabase 项目
# 使用方式：/repro-issue <issue-number>
```

#### 效果展示

- 来自 Metabase 项目
- 确保测试可靠失败

---

### 3.6 /tdd-implement 命令

> TDD 实现命令

#### 背景需求

需要遵循 TDD 原则的实现命令。

#### 目标

分析需求 → 创建测试(红) → 实现代码(绿) → 重构

#### 本地部署

```bash
# 来自 Narraitor 项目
git clone https://github.com/jerseycheese/Narraitor ~/.claude/plugins/
```

---

### 3.7 /run-ci 命令

> CI 环境中的自动化测试执行

#### 背景需求

需要在 CI 环境中运行完整的测试套件。

#### 目标

激活虚拟环境，运行 CI 兼容的检查脚本，迭代修复错误，确保所有测试通过。

#### 本地部署

```bash
# 来自 toban-contribution-viewer 项目
git clone https://github.com/hackdays-io/toban-contribution-viewer ~/.claude/plugins/
```

---

## 四、其他开发者工具

### 4.1 Snyk Agent Scan AI Agent 安全扫描

> AI agents、MCP servers 和 agent skills 的安全扫描器

#### 背景需求

AI agent 生态快速发展，安全威胁日益突出。

#### 目标

发现并扫描本地安装的 agent 组件的提示注入和漏洞。

#### 设计方案

- **自动发现**：MCP 配置、agent 工具、skills
- **扫描范围**：Claude、Cursor、Windsurf、Gemini CLI 等
- **检测 15+ 安全风险**：

**MCP 服务器**：
- E001: Prompt Injection
- E002: Tool Shadowing
- E003: Tool Poisoning
- TF001: Toxic Flows
- W005: Rug Pull

**Skills**：
- E004: Prompt Injection
- E006: Malware Payloads
- W007: Credential Handling
- W008: Hardcoded Secrets
- W011: Untrusted Content

#### 本地部署

```bash
# 需要先安装 uv
# 完整扫描
uvx snyk-agent-scan@latest --skills

# 扫描 MCP 配置
uvx snyk-agent-scan@latest ~/.vscode/mcp.json

# 扫描单个 skill
uvx snyk-agent-scan@latest --skills ~/path/to/my/SKILL.md

# 扫描所有 claude skills
uvx snyk-agent-scan@latest --skills ~/.claude/skills
```

#### 效果展示

- PyPI 包：snyk-agent-scan
- 官方技术报告：skills-report.pdf
- 社区：Discord 支持

#### 优缺点

✅ 15+ 安全风险检测  
✅ 自动发现  
✅ 持续监控选项  
✅ 企业级安全团队背书  

⚠️ 扫描数据会与 Snyk 共享（用于验证）

---

### 4.2 Superpowers 超级能力包

> 软件工程核心能力的强大组合

#### 背景需求

软件工程需要全面的最佳实践支持。

#### 目标

提供覆盖完整 SDLC 的核心能力。

#### 本地部署

```bash
git clone https://github.com/obra/superpowers ~/.claude/plugins/
```

#### 效果展示

- GitHub Stars：⭐ 4.1k+
- 覆盖完整 SDLC

---

### 4.3 Claude Code Tools 开发者工具集

> 会话连续性的精心设计工具集

#### 背景需求

Claude Code 会话可能因为上下文压缩而丢失重要信息。

#### 目标

避免上下文压缩，提供跨会话上下文恢复。

#### 设计方案

- 避免上下文压缩的技能
- 跨会话上下文恢复
- Claude Code ↔ Codex CLI 跨代理切换
- Rust/Tantivy 全文本搜索
- tmux-cli 集成
- 安全 Hook

#### 本地部署

```bash
git clone https://github.com/pchalasani/claude-code-tools ~/.claude/plugins/
```

---

### 4.4 Claude Starter Kit 启动模板

> Claude Code、MCP 服务器和 AI 开发工作流的完整模板

#### 背景需求

新项目需要快速启动的开发环境。

#### 目标

提供开箱即用的开发模板。

#### 本地部署

```bash
git clone https://github.com/serpro69/claude-starter-kit ~/.claude/plugins/
```

#### 效果展示

- GitHub Stars：⭐ 61

---

### 4.5 Claude Session Restore 会话恢复

> 从之前的 Claude Code 会话高效恢复上下文

#### 背景需求

需要从之前的会话恢复上下文。

#### 本地部署

```bash
git clone https://github.com/ZENG3LD/claude-session-restore ~/.claude/plugins/
```

---

### 4.6 Trail of Bits Security Skills 安全技能

> Trail of Bits 的专业安全技能集

#### 背景需求

企业级安全审计需要专业工具。

#### 目标

提供专业安全审计技能。

#### 设计方案

- 静态分析（CodeQL、Semgrep）
- 变体分析
- 修复验证
- 差异代码审查

#### 本地部署

```bash
git clone https://github.com/trailofbits/skills ~/.claude/plugins/
```

---

### 4.7 Claude Code Agents 端到端开发

> 完整的 E2E 开发工作流

#### 背景需求

独立开发者需要完整的开发工作流。

#### 目标

提供 E2E 开发工作流支持。

#### 本地部署

```bash
git clone https://github.com/undeadlist/claude-code-agents ~/.claude/plugins/
```

---

### 4.8 Claude Code Marketplace

> Git 自动化、测试和代码审查的软件工程技能

#### 背景需求

需要一站式软件工程技能。

#### 本地部署

```bash
git clone https://github.com/mhattingpete/claude-skills-marketplace ~/.claude/plugins/
```

#### 效果展示

- GitHub Stars：⭐ 428

---

### 4.9 AgentSys 工作流自动化

> 完整的工作流自动化系统

#### 背景需求

需要自动化任务到生产的工作流。

#### 目标

提供 PR 管理、代码清理、性能调查、漂移检测等功能。

#### 设计方案

- 工作流自动化系统
- PR 管理
- 代码清理
- 性能调查
- 漂移检测
- 多代理代码审查

#### 本地部署

```bash
git clone https://github.com/avifenesh/agentsys ~/.claude/plugins/
```

#### 效果展示

- GitHub Stars：⭐ 活跃
- 更新频率：v5.3.7

---

### 4.10 Claude Code MCP Enhanced

> 增强版 MCP 服务器，带编排能力和可靠性改进

#### 背景需求

需要更可靠的 MCP 执行模式。

#### 目标

提供自包含执行模式和编排能力。

#### 本地部署

```bash
git clone https://github.com/grahama1970/claude-code-mcp-enhanced ~/.claude/plugins/
```

#### 效果展示

- GitHub Stars：⭐ 106

---

### 4.11 Claude Code MCP Install

> 轻松配置和初始化 MCP 的轻量级 CLI 工具

#### 背景需求

MCP 配置复杂，需要简化安装过程。

#### 目标

提供一键安装 MCP 的能力。

#### 本地部署

```bash
git clone https://github.com/undeadpickle/claude-code-mcpinstall ~/.claude/plugins/
```

#### 效果展示

- GitHub Stars：⭐ 240

---

### 4.12 Obsidian MCP for Claude Code

> 使用 MCP 将 Claude Code 连接到 Obsidian 笔记

#### 背景需求

需要将 Claude Code 与知识管理系统集成。

#### 目标

通过 MCP 协议连接 Obsidian 笔记。

#### 本地部署

```bash
git clone https://github.com/iansinnott/obsidian-claude-code-mcp ~/.claude/plugins/
```

#### 效果展示

- GitHub Stars：⭐ 166

---

## 五、热门 Skills 补充

### 5.1 Humanizer 人类化写作

> 移除 AI 生成文本痕迹的 Claude Code 技能

#### 背景需求

AI 生成的内容有时需要"人类化"处理。

#### 目标

消除文本中的 AI 生成痕迹。

#### 本地部署

```bash
git clone https://github.com/blader/humanizer ~/.claude/plugins/
```

#### 效果展示

- GitHub Stars：⭐ 7,609
- 极受欢迎的技能

---

### 5.2 Planning with Files

> Manus 风格的文件持久规划工作流

#### 背景需求

需要持久化的任务规划和进度跟踪。

#### 目标

实现 Manus 风格的 Markdown 规划。

#### 本地部署

```bash
git clone https://github.com/OthmanAdi/planning-with-files ~/.claude/plugins/
```

#### 效果展示

- GitHub Stars：⭐ 15,168
- 热门规划技能

---

### 5.3 Trail of Bits Skills

> 安全研究和漏洞检测的专业技能

#### 背景需求

安全审计需要专业工具。

#### 目标

提供漏洞检测和审计工作流。

#### 本地部署

```bash
git clone https://github.com/trailofbits/skills ~/.claude/plugins/
```

#### 效果展示

- GitHub Stars：⭐ 3,134

---

### 5.4 Solana Dev Skill

> Solana 现代开发技能

#### 背景需求

Solana 区块链开发需要专门的技能。

#### 目标

提供 2026 年 1 月最佳实践的 Solana 开发技能。

#### 本地部署

```bash
git clone https://github.com/solana-foundation/solana-dev-skill ~/.claude/plugins/
```

#### 效果展示

- GitHub Stars：⭐ 366

---

### 5.5 Dotnet Skills

> .NET 开发者的 Claude Code 技能

#### 背景需求

.NET 开发者需要专门的技能支持。

#### 目标

提供 .NET 开发的专业技能。

#### 本地部署

```bash
git clone https://github.com/Aaronontheweb/dotnet-skills ~/.claude/plugins/
```

#### 效果展示

- GitHub Stars：⭐ 454

---

### 5.6 Axiom (iOS 开发)

> 现代 iOS/iPadOS/watchOS/tvOS 开发的实战技能

#### 背景需求

iOS 开发者需要专业技能支持。

#### 目标

提供经过实战检验的 iOS 开发技能。

#### 本地部署

```bash
git clone https://github.com/CharlesWiltgen/Axiom ~/.claude/plugins/
```

#### 效果展示

- GitHub Stars：⭐ 546

---

## 六、总结与建议

### 6.1 游戏开发推荐

| 插件 | 特点 | 适用场景 |
|------|------|---------|
| Claude-Code-Game-Studios | 全功能工作室 | 大型游戏项目 |
| Unreal-MCP | UE5 集成 | Unreal 开发 |
| Unity GameDev Skills | Unity 专业技能 | Unity 开发 |

### 6.2 Python 开发推荐

| 插件 | 特点 | 适用场景 |
|------|------|---------|
| FastAPI-MCP | 原生认证 | FastAPI 项目 |
| Pydantic AI Skills | AI 代理开发 | Pydantic AI 项目 |
| cc-devops-skills | DevOps 全能 | 运维自动化 |

### 6.3 测试自动化推荐

| 插件 | 特点 | 适用场景 |
|------|------|---------|
| Playwright Skill | 浏览器自动化 | Web E2E 测试 |
| MCPJam Inspector | MCP 调试 | MCP 开发 |
| TDD Guard | 实时 TDD | 测试驱动开发 |

### 6.4 开发者工具推荐

| 插件 | 特点 | 适用场景 |
|------|------|---------|
| Superpowers | 全栈工程 | 日常开发 |
| Snyk Agent Scan | 安全扫描 | 安全审计 |
| Claude Code Tools | 会话管理 | 上下文保持 |

---

*文档生成时间：2026-03-04*
*数据来源：GitHub, awesome-claude-code, ClawHub*
