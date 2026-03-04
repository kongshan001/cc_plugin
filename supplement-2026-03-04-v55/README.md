# Claude Code 热门插件补充调研 (v55)

> 2026年3月 游戏/Python/测试/开发者工具热门插件完整调研

---

## 一、游戏客户端开发插件

### 1.1 Claude-Code-Game-Studios 游戏工作室 ⭐⭐⭐⭐⭐

> 48 个 AI 代理 + 36 个工作流技能的全能游戏开发工作室

#### 背景需求

游戏开发涉及多个专业领域（编程、美术、音频、测试），需要完整的开发工作室支持。传统游戏开发流程需要大量人工协调，效率低下。

#### 目标

将 Claude Code 打造成完整游戏开发工作室，模拟真实游戏工作室工作流，实现自动化任务分配和团队协作。

#### 设计方案

- **48 个 AI 代理**：设计、编程、美术、音频、测试专业代理
- **36 个工作流技能**：项目管理、代码审查、测试自动化
- **协调系统**：模拟真实游戏工作室团队协作
- **多代理并行工作**：支持多个代理同时工作
- **多引擎支持**：Unity, Unreal, Godot, WebGL

#### 本地部署

```bash
git clone https://github.com/Donchitos/Claude-Code-Game-Studios ~/.claude/plugins/
```

#### 效果展示

- GitHub Stars：⭐ 26-30
- 更新频率：活跃（4天前更新）

#### 优缺点

✅ 功能全面，涵盖游戏开发全流程  
✅ 工作室级架构，多代理协作  
✅ 多引擎支持  
⚠️ 学习曲线陡峭  
⚠️ 配置相对复杂

---

### 1.2 Claude-Code-Game-Master RPG 游戏大师 ⭐⭐⭐⭐

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

#### 优缺点

✅ 创新的文学+游戏结合  
✅ RAG 技术应用  
✅ 持久化冒险系统  
⚠️ 特定用例，较窄受众

---

### 1.3 Unreal-MCP Unreal Engine 集成 ⭐⭐⭐⭐⭐

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

- 实验状态：API 可能有重大变化
- 支持客户端：Claude Desktop、Cursor、Windsurf

#### 优缺点

✅ 首个 Unreal Engine MCP 集成  
✅ 自然语言控制 UE  
✅ Blueprint 节点图操作  
✅ 完整 actor 生命周期管理  

⚠️ 实验阶段，不建议生产使用  
⚠️ 需要 UE 5.5+

---

### 1.4 Unity GameDev Skills ⭐⭐⭐

> 符合 Claude Code Skills 规范的 Unity 专业开发技能集

#### 背景需求

Unity 是最流行的游戏引擎之一，需要专门的 Claude Code 技能支持。

#### 目标

提供符合 Claude Code Skills 规范的 Unity 专业开发技能。

#### 本地部署

```bash
# 选项 1: OstrichHermit 版本
git clone https://github.com/OstrichHermit/OH-Unity-GameDev-Skills ~/.claude/plugins/

# 选项 2: tjboudreaux 版本
git clone https://github.com/tjboudreaux/cc-plugin-unity-gamedev ~/.claude/plugins/
```

#### 技能分类

| 分类 | 技能 |
|-----|------|
| **工具类** | Addressables, MemoryPack, ScriptableObjects, Profiling |
| **动画/物理** | Animation, Physics, NavMesh, Object Pooling, State Machine |
| **AI/行为** | Behavior Designer, GAS (Gameplay Ability System) |
| **音视频** | Wwise音频, Cinemachine相机 |
| **UI** | UI Toolkit, UGUI |
| **测试** | Unity Test Framework |
| **DI/异步** | VContainer, UniTask |

#### 效果展示

- GitHub Stars：⭐ 1-6

---

### 1.5 Godot MCP 社区版 ⭐⭐⭐

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

### 1.6 lazy-bird 通用开发自动化 ⭐⭐⭐⭐⭐

> 通用开发自动化工具，支持 ANY 项目，包括 Godot 游戏开发框架

#### 背景需求

游戏客户端功能迭代、Bug 修复需要自动化支持。

#### 目标

提供 Issue 驱动的自动开发能力。

#### 设计方案

- **Issue 驱动开发**：自动分析 issue 并实现
- **框架支持**：Godot、React、Django、Node.js、Rust 等
- **自动测试**：运行测试并验证
- **PR 创建**：自动创建 Pull Request
- **安全机制**：代码审查和沙箱执行

#### 本地部署

```bash
pip install lazy-bird
```

#### 效果展示

- GitHub Stars：⭐ 210
- 支持 15+ 框架预设

---

### 1.7 OH-Unity-GameDev-Skills ⭐⭐⭐⭐

> OstrichHermit 出品的 Unity 技能集

#### 本地部署

```bash
git clone https://github.com/OstrichHermit/OH-Unity-GameDev-Skills ~/.claude/plugins/
```

#### 技能分类

- 核心概念：Game Loop, Components, Prefabs
- 工具：Addressables, ScriptableObjects, Odin Inspector
- 动画：Cinemachine, Animation, Timeline
- 物理：Physics, Colliders, Rigidbody
- AI：FSM, Pathfinding
- UI：UI Toolkit, UGUI
- 网络：Mirror, Netcode for GameObjects
- 性能：Profiling, Object Pooling
- 测试：Unity Test Framework

---

### 1.8 game-skill ⭐⭐⭐⭐

> 通用游戏开发技能集

#### 背景需求

需要通用的游戏开发辅助能力。

#### 目标

提供游戏逻辑、关卡设计、资源管理等方面的技能。

#### 本地部署

```bash
git clone https://github.com/nextlevelbuilder/game-skill ~/.claude/plugins/
```

---

### 1.9 GDScript MCP Server ⭐⭐⭐⭐

> Godot GDScript MCP 服务器

#### 背景需求

Godot 引擎使用 GDScript，需要专门的代码辅助。

#### 目标

提供 GDScript 代码补全、错误检测、格式化等能力。

#### 本地部署

```bash
# 配置 MCP
{
  "mcpServers": {
    "gdscript": {
      "command": "npx",
      "args": ["-y", "gdscript-mcp-server"]
    }
  }
}
```

---

## 二、Python 开发插件

### 2.1 FastAPI-MCP ⭐⭐⭐⭐⭐

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
- 趋势排名：trendshift.io #14064

#### 优缺点

✅ 原生认证集成  
✅ 零配置  
✅ FastAPI 原生设计  
✅ 保留完整 schema 和文档  

⚠️ 需要 Python 3.10+（推荐 3.12）

---

### 2.2 Pydantic AI Skills ⭐⭐⭐⭐⭐

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

- GitHub Stars：⭐ 136-140
- 更新频率：活跃（3小时前更新）

---

### 2.3 Serena ⭐⭐⭐⭐⭐

> 强大的编程代理工具包，提供语义检索和编辑能力

#### 背景需求

大型 Python 项目需要智能代码理解和编辑能力。

#### 目标

提供语义代码检索和智能编辑能力。

#### 设计方案

- **语义代码检索**：理解代码意图
- **智能代码编辑**：上下文感知的编辑
- **语言服务器协议**：标准化的开发支持
- **MCP 服务器集成**：与各种 AI 助手兼容

#### 本地部署

```bash
pip install serena
```

#### 效果展示

- GitHub Stars：⭐ 20,941
- 官网：https://oraios.github.io/serena

#### 优缺点

✅ 强大的语义检索能力  
✅ 多模型支持  
✅ 生产级稳定性  

---

### 2.4 PAL MCP Server ⭐⭐⭐⭐⭐

> 多模型协作 MCP 服务器

#### 背景需求

Python 开发中需要多模型协作的场景。

#### 目标

支持 Claude Code / GeminiCLI / CodexCLI + Gemini / OpenAI / OpenRouter / Azure / Grok / Ollama 多模型协同。

#### 设计方案

- **多 AI 模型协同**：同时使用多个 AI 模型
- **模型切换**：灵活的模型选择
- **负载均衡**：优化资源利用
- **自定义模型**：支持自定义模型配置

#### 本地部署

```bash
pip install pal-mcp-server
```

#### 效果展示

- GitHub Stars：⭐ 11,180

---

### 2.5 cc-devops-skills ⭐⭐⭐⭐

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

### 2.6 read-only-postgres ⭐⭐⭐⭐

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

### 2.7 cchooks Python Hooks SDK ⭐⭐⭐

> 轻量级 Python SDK，简化 Claude Code Hooks 开发

#### 背景需求

编写 Claude Code Hooks 需要处理复杂的 JSON 配置。

#### 目标

提供简洁的 API 来编写和集成 Hooks。

#### 本地部署

```bash
# PyPI 安装
pip install cchooks

# 或克隆
git clone https://github.com/GowayLee/cchooks ~/.claude/plugins/
```

---

### 2.8 ty-lsp-claude-code ⭐⭐⭐

> Python 类型检查器 ty 的 Claude Code 插件

#### 背景需求

ty 是新一代 Python 类型检查器（来自 Astral），需要 Claude Code 集成。

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

### 2.9 claude-arsenal ⭐⭐⭐⭐

> 39+ 实战级 Claude Code 技能 + 9 个专业代理

#### 背景需求

需要综合性的软件开发技能库。

#### 目标

提供专业软件开发综合技能库。

#### 设计方案

- 39+ 技能覆盖
- DevOps 工具链
- 多语言支持（Python, TypeScript）

#### 本地部署

```bash
git clone https://github.com/majiayu000/claude-arsenal ~/.claude/plugins/
```

#### 效果展示

- GitHub Stars：⭐ 9

---

### 2.10 claud-skills ⭐⭐⭐⭐

> 生产级 Claude Code 框架，包含 13 个代理、9 个技能

#### 背景需求

需要生产级的 Claude Code 框架。

#### 目标

提供自动文档生成和专业开发代理。

#### 设计方案

- 13 个专用代理
- 9 个开发技能
- 自动文档生成
- Playwright 测试集成
- 支持 JavaScript, TypeScript, PHP, Laravel, React, Python

#### 本地部署

```bash
git clone https://github.com/Interstellar-code/claud-skills ~/.claude/plugins/
```

#### 效果展示

- GitHub Stars：⭐ 11

---

### 2.11 Python MCP Servers ⭐⭐⭐⭐⭐

> 官方 Python MCP 服务器集合

#### 背景需求

需要标准的 Python 工具 MCP 服务器。

#### 目标

提供官方维护的 Python MCP 工具。

#### 本地部署

```bash
# 安装官方 MCP 服务器
pip install mcp-servers

# 配置
{
  "mcpServers": {
    "python": {
      "command": "python",
      "args": ["-m", "mcp_servers.python"]
    }
  }
}
```

---

### 2.12 uv Python 包管理 ⭐⭐⭐⭐⭐

> 现代 Python 包管理器和构建系统

#### 背景需求

Python 项目需要快速的包管理工具。

#### 目标

提供极速的 Python 包管理能力。

#### 本地部署

```bash
# 安装 uv
curl -LsSf https://astral.sh/uv/install.sh | sh

# 或
pip install uv
```

#### 效果展示

- 官方推荐的高速 Python 包管理器
- 支持 Python 3.8+

---

### 2.13 Python Linting/Formatting MCP ⭐⭐⭐⭐

> Python 代码质量工具 MCP 服务器

#### 背景需求

需要自动化的 Python 代码质量检查。

#### 目标

提供 ruff、black、mypy 等工具的 MCP 集成。

#### 本地部署

```bash
# 安装
pip install ruff black mypy

# 配置 MCP
{
  "mcpServers": {
    "python-linting": {
      "command": "python",
      "args": ["-m", "python_linting_mcp"]
    }
  }
}
```

---

## 三、自动化测试插件

### 3.1 MCPJam Inspector ⭐⭐⭐⭐⭐

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
npx -y @mcpjam/inspector@latest

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

⚠️ 需要理解 MCP 协议

---

### 3.2 Playwright Skill ⭐⭐⭐⭐⭐

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

- GitHub Stars：⭐ 1.8k-1.9k
- 最流行的 Claude Code 自动化技能

---

### 3.3 Claude Code Playwright MCP Test ⭐⭐⭐⭐

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

### 3.4 playwright-bot-bypass ⭐⭐⭐

> 绕过 Bot 检测的 Playwright 技能

#### 背景需求

需要绕过网站 Bot 检测进行自动化测试。

#### 目标

提供绕过 Google CAPTCHA 等检测的能力。

#### 本地部署

```bash
git clone https://github.com/greekr4/playwright-bot-bypass ~/.claude/plugins/
```

---

### 3.5 TDD Guard ⭐⭐⭐

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

### 3.6 /repro-issue 命令 ⭐⭐⭐⭐

> 创建可复现的测试用例

#### 背景需求

Bug 修复需要可复现的测试用例。

#### 目标

为 GitHub issues 创建可复现的测试用例。

#### 本地部署

从 Metabase 项目复制命令文件：

```bash
# 复制到项目 .claude/commands/ 目录
curl -o .claude/commands/repro-issue.md \
  https://raw.githubusercontent.com/metabase/metabase/master/.claude/commands/repro-issue.md
```

---

### 3.7 /tdd-implement 命令 ⭐⭐⭐⭐

> 实现 Test-Driven Development

#### 背景需求

需要遵循 TDD 原则进行开发。

#### 目标

分析需求 → 创建测试（红色）→ 实现最小代码（绿色）→ 重构。

#### 本地部署

```bash
curl -o .claude/commands/tdd-implement.md \
  https://raw.githubusercontent.com/jerseycheese/Narraitor/feature/issue-227-ai-suggestions/.claude/commands/tdd-implement.md
```

---

### 3.8 iOS Simulator Skill ⭐⭐⭐⭐

> iOS 模拟器自动化测试

#### 背景需求

iOS 游戏和应用需要模拟器测试支持。

#### 目标

提供 iOS 模拟器控制和应用测试能力。

#### 本地部署

```bash
git clone https://github.com/conorluddy/ios-simulator-skill ~/.claude/plugins/
```

#### 效果展示

- GitHub Stars：⭐ 557
- 平台：macOS

---

### 3.9 Android Emulator Skill ⭐⭐⭐⭐

> Android 模拟器自动化测试

#### 背景需求

Android 游戏和应用需要模拟器测试支持。

#### 目标

提供 Android 模拟器控制和应用测试能力。

#### 本地部署

```bash
git clone https://github.com/Acid-Overflow/android-emulator-skill ~/.claude/plugins/
```

---

### 3.10 Game Testing Framework ⭐⭐⭐⭐

> 游戏客户端自动化测试框架

#### 背景需求

游戏客户端需要专门的自动化测试支持。

#### 目标

提供游戏特定的测试能力和工具。

#### 设计方案

- 图像识别测试
- UI 自动化测试
- 性能基准测试
- 内存泄漏检测

#### 本地部署

```bash
git clone https://github.com/gaming-test-ai/game-testing-framework ~/.claude/plugins/
```

---

### 3.11 Screenshot Testing Skill ⭐⭐⭐⭐

> 截图比对测试技能

#### 背景需求

需要 UI 视觉回归测试。

#### 目标

提供截图比对和视觉测试能力。

#### 本地部署

```bash
git clone https://github.com/visual-testing/screenshot-skill ~/.claude/plugins/
```

---

## 四、开发者工具插件

### 4.1 GitMCP ⭐⭐⭐⭐⭐

> Git 版本控制 MCP 服务器

#### 背景需求

开发者需要通过自然语言与 Git 仓库交互。

#### 目标

让 AI 助手可以执行 Git 操作。

#### 本地部署

```bash
# 安装
npm install -g @github/github-mcp-server

# 配置
# 添加到 MCP 配置
{
  "mcpServers": {
    "github": {
      "command": "github-mcp-server"
    }
  }
}
```

#### 核心功能

- 仓库操作
- 分支管理
- PR 创建和审查
- Issue 管理

---

### 4.2 Context7 MCP Server ⭐⭐⭐⭐⭐

> 为 LLM 和 AI 代码编辑器提供最新的代码文档

#### 背景需求

AI 助手需要访问最新的代码文档。

#### 目标

提供最新的代码文档检索。

#### 本地部署

```bash
# 安装
npx -y @context7/mcp-server

# 配置 MCP
{
  "mcpServers": {
    "context7": {
      "command": "npx",
      "args": ["-y", "@context7/mcp-server"]
    }
  }
}
```

#### 效果展示

- 更新频率：活跃（3月4日更新）
- 趋势排名：MCP 服务器热门

---

### 4.3 Chrome DevTools MCP ⭐⭐⭐⭐⭐

> Chrome 开发者工具 MCP 服务器

#### 背景需求

需要通过 AI 控制浏览器进行开发测试。

#### 目标

提供 Chrome 开发者工具的 MCP 集成。

#### 本地部署

```bash
# 安装
npm install -g @chromedevtools/mcp-server-chrome

# 配置
{
  "mcpServers": {
    "chrome-devtools": {
      "command": "npx",
      "args": ["-y", "@chromedevtools/mcp-server-chrome"]
    }
  }
}
```

#### 效果展示

- 更新频率：活跃（3月4日更新）
- 支持 Chrome/Chromium

---

### 4.4 DevDocs MCP ⭐⭐⭐⭐⭐

> 开发者文档聚合 MCP 服务器

#### 背景需求

开发者需要快速访问各种开发文档。

#### 目标

提供统一的开发文档访问接口。

#### 本地部署

```bash
# 配置 MCP
{
  "mcpServers": {
    "devdocs": {
      "command": "npx",
      "args": ["-y", "devdocs-mcp"]
    }
  }
}
```

---

### 4.5 n8n MCP ⭐⭐⭐⭐

> n8n 工作流自动化 MCP

#### 背景需求

需要通过自然语言创建 n8n 工作流。

#### 目标

让 AI 助手可以构建 n8n 工作流。

#### 本地部署

```bash
npm install -g n8n-mcp
```

#### 效果展示

- GitHub Stars：关注中

---

### 4.6 AgentSys ⭐⭐⭐⭐⭐

> 生产级工作流自动化系统

#### 背景需求

需要自动化任务到生产的完整流程。

#### 目标

提供工作流自动化、PR 管理、代码清理等功能。

#### 设计方案

- 工作流自动化
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

- GitHub Stars：活跃

---

### 4.7 Superpowers ⭐⭐⭐⭐⭐

> 核心工程技能集

#### 背景需求

需要覆盖软件开发生命周期全流程的技能。

#### 目标

提供从规划、审查、测试到调试的核心工程技能。

#### 本地部署

```bash
git clone https://github.com/obra/superpowers ~/.claude/plugins/
```

#### 效果展示

- GitHub Stars：⭐ 4.1k+

---

### 4.8 Claude Code Agents ⭐⭐⭐⭐

> E2E 开发工作流

#### 背景需求

需要完整的端到端开发工作流支持。

#### 目标

提供多审计员并行、自动修复周期、浏览器 QA。

#### 本地部署

```bash
git clone https://github.com/undeadlist/claude-code-agents ~/.claude/plugins/
```

---

### 4.9 ruflo ⭐⭐⭐⭐⭐

> Agent 编排平台

#### 背景需求

需要编排多个 AI 代理协同工作。

#### 目标

提供企业级架构、分布式代理智能、RAG 集成。

#### 效果展示

- GitHub Stars：⭐ 500+
- 支持 Claude Code / Codex 集成

---

### 4.10 developer-kit ⭐⭐⭐⭐

> 模块化插件系统

#### 背景需求

需要可重用的开发任务自动化技能。

#### 目标

提供模块化插件系统。

#### 设计方案

- Java/Spring Boot/LangChain4J
- TypeScript/NestJS/React
- Python
- PHP/WordPress
- AWS CloudFormation

#### 本地部署

```bash
git clone https://github.com/giuseppe-trisciuoglio/developer-kit ~/.claude/plugins/
```

#### 效果展示

- GitHub Stars：⭐ 128

---

### 4.11 Nelson ⭐⭐⭐⭐

> 皇家海军风格的代理团队协调系统

#### 背景需求

需要结构化的复杂任务管理。

#### 目标

提供海军指挥结构风格的多代理协调。

#### 本地部署

```bash
git clone https://github.com/harrymunro/nelson ~/.claude/plugins/
```

---

### 4.12 Trail of Bits Skills ⭐⭐⭐⭐⭐

> 安全审计技能

#### 背景需求

需要代码安全审计能力。

#### 目标

提供 CodeQL/Semgrep 集成。

#### 技能分类

| 技能 | 功能 |
|------|------|
| codeql | 静态代码分析 |
| semgrep | 模式匹配分析 |
| variant-analysis | 变体分析 |
| fix-verification | 修复验证 |
| diff-review | 差异代码审查 |

#### 本地部署

```bash
git clone https://github.com/trailofbits/skills ~/.claude/plugins/
```

---

### 4.13 jira-skill ⭐⭐⭐⭐

> 智能 Jira 集成

#### 背景需求

需要与 Jira 项目管理工具集成。

#### 目标

提供 Jira 任务管理和 MCP 配置。

#### 本地部署

```bash
git clone https://github.com/netresearch/jira-skill ~/.claude/plugins/
```

#### 效果展示

- 更新频率：活跃（3月1日更新）

---

### 4.14 Sudocode ⭐⭐⭐⭐⭐

> 轻量级 Agent 编排开发工具

#### 背景需求

需要集成各种规范框架的开发工具。

#### 目标

提供 Jira 风格的任务管理。

#### 效果展示

- GitHub Stars：关注中

---

### 4.15 Dippy ⭐⭐⭐⭐⭐

> AST 解析自动批准安全命令

#### 背景需求

解决权限提示疲劳问题。

#### 目标

通过 AST 解析自动批准安全命令，对破坏性操作进行提示。

#### 本地部署

```bash
git clone https://github.com/ldayton/Dippy ~/.claude/plugins/
```

#### 效果展示

- 支持 Claude Code、Gemini CLI、Cursor

---

### 4.16 Parry ⭐⭐⭐⭐

> Prompt 注入扫描器

#### 背景需求

需要检测 Claude Code Hooks 中的提示注入攻击。

#### 目标

扫描工具输入输出中的注入攻击、秘密泄露和数据外泄尝试。

#### 本地部署

```bash
git clone https://github.com/vaporif/parry ~/.claude/plugins/
```

---

### 4.17 Claude Scientific Skills ⭐⭐⭐⭐⭐

> 科学研究技能集

#### 背景需求

需要科学研究、工程、分析、金融和写作的技能。

#### 目标

提供可立即使用的代理技能集。

#### 本地部署

```bash
git clone https://github.com/K-Dense-AI/claude-scientific-skills ~/.claude/plugins/
```

#### 效果展示

- GitHub Stars：⭐ 活跃

---

## 五、快速推荐

### 游戏客户端开发推荐

| 优先级 | 技能 | 用途 |
|--------|------|------|
| ⭐⭐⭐⭐⭐ | Claude-Code-Game-Studios | 全流程游戏开发工作室 |
| ⭐⭐⭐⭐⭐ | Unreal-MCP | Unreal Engine 5.5+ 集成 |
| ⭐⭐⭐⭐ | lazy-bird | Godot + 通用自动化 |
| ⭐⭐⭐⭐ | Unity GameDev Skills | Unity 专业开发 |
| ⭐⭐⭐⭐ | OH-Unity-GameDev-Skills | OstrichHermit Unity 技能 |
| ⭐⭐⭐⭐ | GDScript MCP Server | Godot 脚本辅助 |
| ⭐⭐⭐ | Godot MCP | Godot 引擎集成 |

### Python 开发推荐

| 优先级 | 技能 | 用途 |
|--------|------|------|
| ⭐⭐⭐⭐⭐ | FastAPI-MCP | FastAPI + MCP 集成 |
| ⭐⭐⭐⭐⭐ | Pydantic AI Skills | Pydantic AI 开发 |
| ⭐⭐⭐⭐⭐ | Serena | 语义代码检索 |
| ⭐⭐⭐⭐⭐ | uv | 现代 Python 包管理 |
| ⭐⭐⭐⭐⭐ | PAL MCP Server | 多模型协作 |
| ⭐⭐⭐⭐ | cc-devops-skills | DevOps 自动化 |
| ⭐⭐⭐⭐ | read-only-postgres | PostgreSQL 只读查询 |
| ⭐⭐⭐ | Python MCP Servers | 官方 Python 工具 |

### 自动化测试推荐

| 优先级 | 技能 | 用途 |
|--------|------|------|
| ⭐⭐⭐⭐⭐ | MCPJam Inspector | MCP 测试调试 |
| ⭐⭐⭐⭐⭐ | Playwright Skill | 浏览器自动化 |
| ⭐⭐⭐⭐ | Claude Code Playwright MCP Test | YAML 测试框架 |
| ⭐⭐⭐⭐ | /tdd-implement | TDD 开发流程 |
| ⭐⭐⭐⭐ | iOS Simulator Skill | iOS 模拟器测试 |
| ⭐⭐⭐⭐ | Android Emulator Skill | Android 模拟器测试 |
| ⭐⭐⭐⭐ | Game Testing Framework | 游戏客户端测试 |
| ⭐⭐⭐ | TDD Guard | TDD 实时监控 |

### 开发者工具推荐

| 优先级 | 技能 | 用途 |
|--------|------|------|
| ⭐⭐⭐⭐⭐ | GitMCP | Git 版本控制 |
| ⭐⭐⭐⭐⭐ | Context7 MCP | 代码文档检索 |
| ⭐⭐⭐⭐⭐ | Chrome DevTools MCP | 浏览器开发工具 |
| ⭐⭐⭐⭐⭐ | AgentSys | 工作流自动化 |
| ⭐⭐⭐⭐⭐ | Superpowers | 核心工程技能 |
| ⭐⭐⭐⭐⭐ | Claude Scientific Skills | 科学研究技能 |
| ⭐⭐⭐⭐⭐ | Dippy | AST 自动批准命令 |
| ⭐⭐⭐⭐ | dev-docs-mcp | 开发者文档聚合 |
| ⭐⭐⭐⭐ | n8n MCP | 工作流自动化 |
| ⭐⭐⭐⭐ | Trail of Bits Skills | 安全审计 |

---

## 六、MCP 服务器安装指南

### 通用安装方式

```bash
# npm 全局安装
npm install -g <package-name>

# uv 安装
uv add <package-name>

# npx 运行
npx -y <package-name>

# Docker
docker run -p <port>:<port> <image>

# pip 安装
pip install <package-name>
```

### MCP 配置示例

```json
{
  "mcpServers": {
    "<server-name>": {
      "command": "<command>",
      "args": ["<args>"]
    }
  }
}
```

---

## 七、相关资源

- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code) - Claude Code 精选技能列表
- [MCP 官方文档](https://modelcontextprotocol.io/) - Model Context Protocol 文档
- [antigravity-awesome-skills](https://github.com/anthropics/antigravity-awesome-skills) - 900+ 通用技能集合
- [Claude Code 游戏开发插件调研](./claude-code-game-studios.md)
- [Unity 专业技能集调研](./cc-plugin-unity-gamedev.md)
- [Pydantic AI 技能调研](./pydantic-ai-skills.md)
