# Claude Code 热门插件补充调研 (v49)

> 2026年3月 热门插件深度调研 - 游戏/Python/测试/开发者工具

---

## 一、游戏客户端开发插件

### 1.1 Unreal-MCP Unreal Engine 集成

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

# 3. 生成 Visual Studio 项目文件
Right-click .uproject > Generate Visual Studio project files

# 4. 构建项目

# 5. 配置 MCP (Claude Desktop)
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

### 1.2 Claude-Code-Game-Studios 游戏工作室

> 48 个 AI 代理 + 36 个工作流技能的全能游戏开发工作室

#### 背景需求

游戏开发涉及多个专业领域，需要完整的开发工作室支持。

#### 目标

将 Claude Code 打造成完整游戏开发工作室。

#### 设计方案

- 48 个 AI 代理：设计、编程、美术、音频、测试
- 36 个工作流技能：项目管理、代码审查、测试自动化
- 协调系统：模拟真实工作室团队协作
- 多代理并行工作

#### 本地部署

```bash
git clone https://github.com/Donchitos/Claude-Code-Game-Studios ~/.claude/plugins/
```

#### 效果展示

- GitHub Stars：⭐ 28
- 更新频率：活跃（4天前更新）

#### 优缺点

✅ 功能全面 ✅ 工作室级架构 ✅ 多代理协作  
⚠️ 学习曲线陡峭 ⚠️ 配置复杂

---

### 1.3 Unity GameDev Skills

> 符合 Claude Code Skills 规范的 Unity 专业开发技能集

#### 本地部署

```bash
git clone https://github.com/OstrichHermit/OH-Unity-GameDev-Skills ~/.claude/plugins/
# 或
git clone https://github.com/tjboudreaux/cc-plugin-unity-gamedev ~/.claude/plugins/
```

#### 效果展示

- GitHub Stars：⭐ 1-6

---

## 二、Python 开发插件

### 2.1 FastAPI-MCP FastAPI MCP 服务器

> 将 FastAPI 端点暴露为 MCP 工具，支持认证！

#### 背景需求

FastAPI 是现代 Python Web 开发的主流框架，需要与 AI 助手深度集成。

#### 目标

零/最小配置将 FastAPI 应用转换为 MCP 服务器。

#### 设计方案

- **原生认证**：使用现有的 FastAPI 依赖
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

✅ 原生认证集成 ✅ 零配置 ✅ FastAPI 原生设计  
✅ 保留完整 schema 和文档  
✅ 支持独立部署  

⚠️ 需要 Python 3.10+（推荐 3.12）

---

### 2.2 Pydantic AI Skills

> Agent Skills 支持 + Pydantic AI 渐进式披露

#### 本地部署

```bash
pip install pydantic-ai-skills
# 或
git clone https://github.com/DougTrajano/pydantic-ai-skills ~/.claude/plugins/
```

#### 效果展示

- GitHub Stars：⭐ 138
- 更新频率：活跃（3小时前更新）

---

### 2.3 Claude Scientific Skills

> 研究、科学、工程、分析、金融和写作的即用型技能集

#### 本地部署

```bash
git clone https://github.com/K-Dense-AI/claude-scientific-skills ~/.claude/plugins/
```

#### 效果展示

- GitHub Stars：⭐ 很高（官方推荐）
- 被描述为"GitHub 上最好的技能仓库之一"

---

### 2.4 cc-devops-skills

> 详细到令人发指的 DevOps 工程师技能集

#### 本地部署

```bash
git clone https://github.com/akin-ozer/cc-devops-skills ~/.claude/plugins/
```

#### 设计方案

- 验证器
- 生成器
- Shell 脚本
- CLI 工具
- IaC 代码生成（AWS、Azure、GCP、K8s等）

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

✅ 免费前沿模型 ✅ 无需 ngrok ✅ 完整调试功能  
✅ 桌面应用 + CLI ✅ OAuth 调试专家  

⚠️ 需要理解 MCP 协议

---

### 3.2 Playwright Skill

> 浏览器自动化 Claude Code 技能，模型驱动

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

#### 本地部署

```bash
git clone https://github.com/terryso/claude-code-playwright-mcp-test ~/.claude/plugins/
```

#### 效果展示

- GitHub Stars：⭐ 164

---

### 3.4 TDD Guard

> 基于 Hook 的实时 TDD 监控系统

#### 本地部署

```bash
git clone https://github.com/nizos/tdd-guard ~/.claude/plugins/
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

✅ 15+ 安全风险检测 ✅ 自动发现 ✅ 持续监控选项  
✅ 企业级安全团队背书  

⚠️ 扫描数据会与 Snyk 共享（用于验证）

---

### 4.2 Superpowers 超级能力包

> 软件工程核心能力的强大组合

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

#### 本地部署

```bash
git clone https://github.com/pchalasani/claude-code-tools ~/.claude/plugins/
```

#### 设计方案

- 避免上下文压缩的技能
- 跨会话上下文恢复
- Claude Code ↔ Codex CLI 跨代理切换
- Rust/Tantivy 全文本搜索
- tmux-cli 集成
- 安全 Hook

---

### 4.4 Claude Starter Kit 启动模板

> Claude Code、MCP 服务器和 AI 开发工作流的完整模板

#### 本地部署

```bash
git clone https://github.com/serpro69/claude-starter-kit ~/.claude/plugins/
```

#### 效果展示

- GitHub Stars：⭐ 61

---

### 4.5 Claude Session Restore 会话恢复

> 从之前的 Claude Code 会话高效恢复上下文

#### 本地部署

```bash
git clone https://github.com/ZENG3LD/claude-session-restore ~/.claude/plugins/
```

---

### 4.6 Trail of Bits Security Skills 安全技能

> Trail of Bits 的专业安全技能集

#### 本地部署

```bash
git clone https://github.com/trailofbits/skills ~/.claude/plugins/
```

---

### 4.7 Claude Code Agents 端到端开发

> 完整的 E2E 开发工作流

#### 本地部署

```bash
git clone https://github.com/undeadlist/claude-code-agents ~/.claude/plugins/
```

---

### 4.8 Claude Code Marketplace

> Git 自动化、测试和代码审查的软件工程技能

#### 本地部署

```bash
git clone https://github.com/mhattingpete/claude-skills-marketplace ~/.claude/plugins/
```

#### 效果展示

- GitHub Stars：⭐ 428

---

## 五、总结

### 5.1 游戏开发插件生态

| 插件 | 方向 | Stars | 特点 |
|------|------|-------|------|
| unreal-mcp | Unreal Engine | 实验中 | 首个 UE MCP 集成 |
| Claude-Code-Game-Studios | 全栈 | 28 | 48代理+36技能 |
| Unity GameDev Skills | Unity | 1-6 | Unity 专业技能 |
| cc-plugin-unity-gamedev | Unity | 1 | 21 个专业技能 |

**推荐**：
- Unreal 开发 → unreal-mcp
- Unity 开发 → Claude-Code-Game-Studios + Unity GameDev Skills
- 快速原型 → Love2D + Claude Code

---

### 5.2 Python 开发插件生态

| 插件 | 方向 | Stars | 特点 |
|------|------|-------|------|
| fastapi-mcp | Web 框架 | 趋势#14064 | FastAPI 原生 MCP |
| pydantic-ai-skills | AI框架 | 138 | Pydantic 官方 |
| cc-devops-skills | DevOps | - | IaC 全能 |
| claude-scientific-skills | 科研 | 高 | 科研神器 |

**推荐**：
- FastAPI 开发 → fastapi-mcp
- AI 开发 → pydantic-ai-skills
- 科研/数据分析 → claude-scientific-skills

---

### 5.3 自动化测试插件生态

| 插件 | 方向 | Stars | 特点 |
|------|------|-------|------|
| mcpjam-inspector | MCP 调试 | - | 完整调试工具 |
| playwright-skill | 浏览器 | 1.9k | 最流行 |
| claude-code-playwright-mcp-test | 框架 | 164 | YAML 驱动 |
| tdd-guard | TDD | - | 实时监控 |

**推荐**：
- MCP 开发调试 → mcpjam-inspector
- 浏览器自动化 → playwright-skill
- 声明式测试 → claude-code-playwright-mcp-test

---

### 5.4 开发者工具插件生态

| 插件 | 方向 | 特点 |
|------|------|------|
| snyk-agent-scan | 安全扫描 | 15+ 风险检测 |
| superpowers | 最佳实践 | 4.1k+ Stars |
| claude-code-tools | 会话连续 | 跨会话上下文 |
| claude-starter-kit | 模板 | 快速启动 |
| claude-session-restore | 恢复 | 智能上下文 |
| trailofbits-skills | 安全 | 企业级审计 |

**推荐**：
- 安全扫描 → snyk-agent-scan
- 快速启动 → claude-starter-kit
- 会话连续 → claude-code-tools
- 安全审计 → trailofbits/skills

---

## 六、部署建议

### 游戏开发
```bash
# Unreal Engine 开发
git clone https://github.com/chongdashu/unreal-mcp.git

# Unity/通用游戏开发
git clone https://github.com/Donchitos/Claude-Code-Game-Studios ~/.claude/plugins/
git clone https://github.com/tjboudreaux/cc-plugin-unity-gamedev ~/.claude/plugins/
```

### Python 开发
```bash
# FastAPI + MCP
uv add fastapi-mcp

# Python 技能集
git clone https://github.com/DougTrajano/pydantic-ai-skills ~/.claude/plugins/
git clone https://github.com/akin-ozer/cc-devops-skills ~/.claude/plugins/
```

### 测试调试
```bash
# MCP 调试
npx @mcpjam/inspector@latest

# 浏览器自动化
git clone https://github.com/lackeyjb/playwright-skill ~/.claude/plugins/
### 安全运维```


```bash
# 安全扫描
uvx snyk-agent-scan@latest --skills

# 核心技能
git clone https://github.com/obra/superpowers ~/.claude/plugins/
git clone https://github.com/trailofbits/skills ~/.claude/plugins/
```
