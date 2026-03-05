# Claude Code 热门插件补充调研 v98

> 游戏客户端开发 / Python 开发 / 自动化测试 / 开发者工具 | 2026-03-05

## 📋 本次调研涵盖

| 类别 | 重点内容 |
|------|----------|
| 🎮 游戏客户端开发 | 主流游戏引擎 MCP 集成、客户端框架 |
| 🐍 Python 开发 | Django/Flask、数据处理、AI/ML 工具链 |
| 🧪 自动化测试 | 游戏客户端测试、视觉测试、E2E 框架 |
| 🛠️ 开发者工具 | 会话管理、代码分析、CI/CD 集成 |

---

## 调研方法

1. **数据来源**: awesome-claude-code (8,751+ 仓库)、GitHub Topics
2. **筛选标准**: Stars 数量、更新活跃度、功能完整性
3. **分类维度**: 技术栈、应用场景、集成方式

---

## 插件列表

### 🎮 游戏客户端开发

| 插件 | 描述 | Stars | 状态 |
|------|------|-------|------|
| [mcp-unity](./mcp-unity.md) | Unity MCP 服务器 | 1,382 | ✅ |
| [unreal-mcp](./unreal-mcp.md) | Unreal Engine 5 MCP | 1,504 | ✅ |
| [unity-mcp](./unity-mcp.md) | Unity AI 助手集成 | - | ✅ |
| [godot-development](./godot-development.md) | Godot 4.x 开发 | - | ✅ |
| [claude-code-game-studios](./claude-code-game-studios.md) | 48 AI 代理游戏工作室 | 30 | ✅ |
| [cc-plugin-unity-gamedev](./cc-plugin-unity-gamedev.md) | Unity 专业技能集 | 1 | ✅ |

### 🐍 Python 开发

| 插件 | 描述 | Stars | 状态 |
|------|------|-------|------|
| [fastmcp](./fastmcp.md) | Pythonic MCP 框架 | 23,383 | ✅ |
| [pydantic-ai-skills](./pydantic-ai-skills.md) | Pydantic AI 开发 | 136 | ✅ |
| [fastapi-development](./fastapi-development.md) | FastAPI 开发 | - | ✅ |
| [developer-kit](./developer-kit.md) | 全栈开发工具包 | 133 | ✅ |
| [claude-scientific-skills](./claude-scientific-skills.md) | 科学研究技能集 | - | ✅ |

### 🧪 自动化测试

| 插件 | 描述 | Stars | 状态 |
|------|------|-------|------|
| [playwright-skill](./playwright-skill.md) | 浏览器自动化测试 | 1,864 | ✅ |
| [vibetest-use](./vibetest-use.md) | AI 驱动 QA 测试 | 771 | ✅ |
| [unibrowse](./unibrowse.md) | 高级浏览器自动化 | 4 | ✅ |
| [local-testing-agent](./local-testing-agent.md) | 多语言测试自动化 | 0 | ✅ |
| [skunit](./skunit.md) | AI 单元测试框架 | 171 | ✅ |
| [pypict-claude-skill](./pypict-claude-skill.md) | PICT 测试用例生成 | - | ✅ |

### 🛠️ 开发者工具

| 插件 | 描述 | Stars | 状态 |
|------|------|-------|------|
| [mcp-inspector](./mcp-inspector.md) | MCP 可视化测试 | 8,900 | ✅ |
| [mcp-ssh-manager](./mcp-ssh-manager.md) | SSH 远程管理 | 63 | ✅ |
| [aws-mcp-server](./aws-mcp-server.md) | AWS 云服务 | 1,350+ | ✅ |
| [cc-devops-skills](./cc-devops-skills.md) | DevOps 工程师技能 | - | ✅ |
| [superpowers](./superpowers.md) | 核心工程技能集 | 4,100+ | ✅ |
| [context7-mcp-server](./context7-mcp-server.md) | 实时代码文档 | - | ✅ |

---

## 热门插件深度分析

### 🚀 FastMCP - Pythonic MCP 服务器框架

**Stars**: ⭐ 23,383 | **语言**: Python | **趋势**: 持续增长

FastMCP 是最受欢迎的 Python MCP 框架，提供快速、Pythonic 的方式构建 MCP 服务器。

**核心功能**:
- 🚀 快速构建 MCP 服务器
- 🐍 纯 Python 实现
- ⚡ 异步支持
- 🔗 Prefect 工作流集成

**安装**:
```bash
pip install fastmcp

from fastmcp import FastMCP

mcp = FastMCP("my-server")

@mcp.tool()
def hello(name: str) -> str:
    return f"Hello, {name}!"

mcp.run()
```

### 🎮 Unreal-MCP - Unreal Engine 5 集成

**Stars**: ⭐ 1,504 | **语言**: C++ | **游戏引擎**

让 AI 助手通过自然语言控制 Unreal Engine 5。

**核心功能**:
- 🎮 UE5 引擎控制
- 📐 蓝图代码生成
- 🏗️ 关卡编辑
- 📦 资产管理
- 🔧 自动化构建

**安装**:
```bash
pip install unreal-mcp

# 配置 claude_desktop_config.json
{
  "mcpServers": {
    "unreal": {
      "command": "unreal-mcp",
      "args": ["--project", "YourProject.uproject"]
    }
  }
}
```

### 🧪 Playwright-Skill - 浏览器自动化测试

**Stars**: ⭐ 1,864 | **语言**: JavaScript | **E2E 测试**

为 Claude Code 提供 Model-invoked 浏览器自动化能力。

**核心功能**:
- 🌐 浏览器自动化
- 🧪 E2E 测试
- 🤖 Model-invoked 模式
- 📝 自主代码生成

**安装**:
```bash
git clone https://github.com/lackeyjb/playwright-skill ~/.claude/plugins/playwright-skill
cd ~/.claude/plugins/playwright-skill
npm install
```

### 🔧 MCP Inspector - 官方 MCP 测试工具

**Stars**: ⭐ 8,900 | **语言**: TypeScript | **官方维护**

官方维护的 MCP 服务器可视测试工具。

**核心功能**:
- 🔧 MCP 服务器连接测试
- 📊 请求/响应可视化
- 🔌 协议验证
- 🧪 工具调用测试

**安装**:
```bash
npm install -g @modelcontextprotocol/inspector
mcp-inspector
```

### 🛡️ Superpowers - 核心工程技能集

**Stars**: ⭐ 4,100+ | **覆盖**: 全栈开发

最受欢迎的开发技能集之一，覆盖完整软件开发生命周期。

**核心功能**:
- 66+ Skills
- 9 个工作流命令
- 12 个技术类别
- 全栈覆盖

**安装**:
```bash
git clone https://github.com/superpowers/superpowers ~/.claude/plugins/
```

---

## 新兴插件发现

### 📱 Claude Code Agents - E2E 开发工作流

**特点**: 综合 E2E 开发工作流，包含多审计器并行、自动修复循环、浏览器 QA

**亮点**:
- 运行多个审计器并行工作
- 微检查点协议自动化修复循环
- 基于浏览器的 QA
- 严格协议防止 AI 失控

### 🌐 Claude Code Repos Index

**特点**: 75+ Claude Code 仓库索引

**覆盖领域**:
- CMS
- 系统设计
- 深度研究
- IoT
- Agentic 工作流
- 服务器管理

### 🔧 Fullstack Dev Skills

**特点**: 65 个专业技能 + 9 个项目工作流命令

**亮点**:
- 完整的全栈开发覆盖
- Jira/Confluence 集成
- /common-ground 命令暴露 AI 隐藏假设

### 📊 Claude Code PM

**特点**: 全面项目管理框架

**功能**:
- 任务管理
- 进度跟踪
- 里程碑管理
- 团队协作
- 发布管理

---

## 分类对比

### 游戏引擎 MCP 对比

| 插件 | 引擎 | Stars | 特点 |
|------|------|-------|------|
| mcp-unity | Unity | 1,382 | 跨 AI 助手支持 |
| unreal-mcp | UE5 | 1,504 | 蓝图代码生成 |
| unity-mcp | Unity | - | AI 助手集成 |
| godot-development | Godot | - | GDScript 开发 |

### 测试框架对比

| 插件 | 类型 | Stars | 适用场景 |
|------|------|-------|----------|
| playwright-skill | E2E | 1,864 | 浏览器自动化 |
| vibetest-use | AI QA | 771 | 视觉回归测试 |
| skunit | 单元测试 | 171 | AI 组件测试 |
| local-testing-agent | 多语言 | 0 | 跨语言测试 |

### Python MCP 框架对比

| 插件 | Stars | 特点 |
|------|-------|------|
| FastMCP | 23,383 | Pythonic, 异步优先 |
| FastAgent | 3,694 | 工作流定义 |
| MCP Universe | 566 | 基准测试 |

---

## 安装建议

### 游戏开发推荐

```bash
# Unity 开发
npm install mcp-unity

# Unreal Engine 5
pip install unreal-mcp

# Godot
# 参考 godot-development 技能
```

### Python 开发推荐

```bash
# MCP 服务器开发
pip install fastmcp

# AI 应用开发
pip install pydantic-ai

# FastAPI 开发
# 参考 fastapi-development 技能
```

### 测试推荐

```bash
# 浏览器自动化
git clone https://github.com/lackeyjb/playwright-skill

# AI 驱动测试
pip install vibetest-use

# MCP 服务器测试
npm install -g @modelcontextprotocol/inspector
```

---

## 趋势观察

### 2025-2026 趋势

1. **MCP 协议普及**: 更多框架支持 MCP 协议
2. **AI 测试兴起**: AI 驱动测试用例生成
3. **游戏引擎集成**: 主流引擎全面支持 MCP
4. **多代理协作**: 复杂任务多代理分工

### 热门分类

| 分类 | 增长趋势 | 代表插件 |
|------|----------|----------|
| MCP 服务器 | 🔺 快速 | FastMCP, MCP Inspector |
| 游戏开发 | 🔺 稳定 | Unreal-MCP, Unity-MCP |
| 测试工具 | 🔺 增长 | Playwright-Skill, Vibetest |
| DevOps | 🔺 稳定 | AWS-MCP, SSH-Manager |

---

## 相关资源

- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code) - 8,751+ 仓库
- [GitHub Topics: claude-code](https://github.com/topics/claude-code)
- [Claude Code 官方文档](https://docs.anthropic.com/en/docs/claude-code)

---

*调研时间: 2026-03-05 17:10*
*数据来源: awesome-claude-code, GitHub Topics*
