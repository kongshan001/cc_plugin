# 补充调研 v85 - Claude Code 热门插件完整调研

> 更新日期: 2026-03-05
> 调研方向: 游戏客户端开发 | Python 开发 | 游戏客户端自动化测试 | 其他开发者工具

---

## 📋 调研概述

本次调研继续关注 Claude Code 热门插件，聚焦以下四个方向：
1. **游戏客户端开发** - 游戏引擎集成、像素艺术工具
2. **Python 开发** - Python 项目模板、开发工具包
3. **游戏客户端自动化测试** - 浏览器自动化测试框架
4. **其他开发者工具** - 跨平台开发工具、Miro 集成

---

## 🎮 一、游戏客户端开发相关插件

### 1.1 Unity-MCP (IvanMurzak/Unity-MCP)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 1,174 |
| **Forks** | 123 |
| **Language** | C# |
| **更新** | 2026-03-04 |

**描述**: AI-powered bridge connecting LLMs and advanced AI agents to the Unity Editor via the Model Context Protocol (MCP). Chat with AI to generate code, debug errors, and automate game development tasks directly within your project.

**核心功能**:
- Unity Editor 与 Claude Code 的 MCP 协议集成
- AI 驱动的代码生成
- 错误调试自动化
- 游戏开发任务自动化
- 跨 AI 助手支持（Cursor、Claude Code、Codex、Windsurf）

**技术栈**:
- C# (Unity)
- Model Context Protocol
- Unity Editor API

**部署方式**:
```bash
npm install mcp-unity

# Claude Code 配置
{
  "mcpServers": {
    "unity": {
      "command": "npx",
      "args": ["-y", "mcp-unity"]
    }
  }
}
```

---

### 1.2 pixel-plugin (willibrandon/pixel-plugin)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 56 |
| **Forks** | 6 |
| **Language** | Shell |
| **更新** | 2026-03-04 |

**描述**: Claude Code plugin for creating pixel art with Aseprite through natural language. Supports animation, retro palettes, dithering, and game engine export.

**核心功能**:
- 像素艺术创作
- 动画支持
- 复古调色板
- 抖动效果 (Dithering)
- 游戏引擎导出

**技术栈**:
- Shell
- Aseprite API
- Claude Code 插件系统

---

### 1.3 mcp-unity (CoderGamester/mcp-unity)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 1,382 |
| **Forks** | 170 |
| **Language** | TypeScript |
| **更新** | 2026-03-04 |

**描述**: 主流 Unity MCP 集成方案，另一个流行的 Unity 集成方案。

**核心功能**:
- 场景操作
- 资源管理
- 脚本编辑
- 构建自动化
- 游戏对象控制

---

## 🐍 二、Python 开发相关插件

### 2.1 developer-kit (giuseppe-trisciuoglio/developer-kit)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 133 |
| **Forks** | 9 |
| **Language** | Python |
| **更新** | 2026-03-04 |

**描述**: Developer Kit for Claude Code - a modular plugin system providing reusable skills, agents, and commands for automating development tasks. The kit includes independent plugins covering Java/Spring Boot/LangChain4J, TypeScript/NestJS/React, Python, PHP/WordPress, AWS CloudFormation, and AI patterns.

**支持领域**:

| 领域 | 技术栈 |
|------|--------|
| Java | Spring Boot、LangChain4J |
| TypeScript | NestJS、React |
| Python | Python 开发 |
| PHP | WordPress |
| AWS | CloudFormation |
| AI | 常见 AI 开发模式 |

**核心特点**:
- 模块化插件系统
- 多语言技能支持
- 预置开发模式

**部署方式**:
```bash
git clone https://github.com/giuseppe-trisciuoglio/developer-kit.git
cd developer-kit
# 选择需要的技能目录 (python/, java/, typescript/)
```

---

### 2.2 claude-skills-collection-2026 (inollp7855/claude-skills-collection-2026)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 23 |
| **Forks** | - |
| **Language** | - |
| **更新** | 2026-03 |

**描述**: Complete collection of Claude Skills for 2026. 100+ production-ready skills for development, productivity, research, and automation.

**核心功能**:
- 100+ 生产级技能
- 开发工作流
- 生产力工具
- 研究辅助
- 自动化任务

---

### 2.3 claude-arsenal (majiayu000/claude-arsenal)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 9 |
| **Forks** | - |
| **Language** | - |
| **更新** | 2026-03 |

**描述**: 🚀 39+ battle-tested Claude Code skills & 9 specialized agents for professional software development.

**核心功能**:
- 39+ 实战技能
- 9 个专业代理
- 专业软件开发覆盖

---

### 2.4 spoon-awesome-skill (XSpoonAi/spoon-awesome-skill)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 12 |
| **Forks** | - |
| **Language** | Python |
| **更新** | 2026-03 |

**描述**: A curated collection of Claude Code skills for SpoonOS development and Web3 integrations. 57 Python scripts across 19 skills.

**核心功能**:
- SpoonOS 技能 (Vibe Coding)
- Web3 技能 (DeFi, NFT, DAO, Security)
- 19 个技能集

---

## 🧪 三、游戏客户端自动化测试相关插件

### 3.1 playwright-skill (lackeyjb/playwright-skill)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 1,863 |
| **Forks** | 105 |
| **Language** | JavaScript |
| **更新** | 2026-03-05 |

**描述**: Claude Code Skill for browser automation with Playwright. Model-invoked - Claude autonomously writes and executes custom automation for testing and validation.

**核心功能**:
- 浏览器自动化
- Playwright 集成
- 模型驱动的自动化
- 测试和验证
- E2E 测试

**技术栈**:
- JavaScript/Node.js
- Playwright
- Claude Code Skills

**Topics**: ai-tools, automation, browser-automation, claude, claude-code, claude-plugin, claude-skills, developer-tools, e2e-testing, model-invoked, nodejs, playwright, web-testing

---

### 3.2 claude-code-playwright-mcp-test (terryso/claude-code-playwright-mcp-test)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 164 |
| **Forks** | 16 |
| **Language** | JavaScript |
| **更新** | 2026-03-03 |

**描述**: A YAML-based Playwright MCP automation testing framework designed for Claude Code

**核心功能**:
- YAML 配置的测试框架
- Playwright MCP 集成
- Claude Code 专用
- 自动化测试

---

### 3.3 unibrowse (sackio/unibrowse)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 4 |
| **Forks** | 0 |
| **Language** | JavaScript |
| **更新** | 2026-01-30 |

**描述**: 🤨 Advanced browser automation plugin for Claude Code with 5 specialized sub-agents, 57+ macros, and intelligent delegation for web scraping, form filling, e-commerce automation, and QA testing

**核心功能**:
- 5 个专业子代理
- 57+ 宏
- 智能委托
- Web 爬取
- 表单自动化
- 电商自动化
- QA 测试

---

### 3.4 ai-testing-mcp (Twisted66/ai-testing-mcp)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 6 |
| **Forks** | - |
| **Language** | - |
| **更新** | 2026-02 |

**描述**: AI-powered testing automation MCP server for Claude Code - TestSprite alternative

---

### 3.5 local-testing-agent (marcelkurvers/local-testing-agent)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 0 |
| **Forks** | - |
| **Language** | - |
| **更新** | 2026-02 |

**描述**: Multi-language testing automation MCP server for Claude Code and AI assistants. Supports Python, JS/TS, Go, Rust, Java, and Ruby with automated test discovery and execution.

**支持语言**:
- Python
- JavaScript/TypeScript
- Go
- Rust
- Java
- Ruby

---

## 🛠️ 四、其他开发者工具

### 4.1 claude-skills-marketplace (mhattingpete/claude-skills-marketplace)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 431 |
| **Forks** | 50 |
| **Language** | HTML |
| **更新** | 2026-03-04 |

**描述**: Claude Code Skills for software engineering workflows - Git automation, testing, and code review

**核心功能**:
- Git 自动化
- 测试工作流
- 代码审查
- 软件工程流程

---

### 4.2 miro-ai (miroapp/miro-ai)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 66 |
| **Forks** | 6 |
| **Language** | TypeScript |
| **更新** | 2026-03-03 |

**描述**: Official Miro AI developer tools and integrations. Includes MCP server configuration, Claude Code skills, and resources for building AI-powered experiences with Miro boards.

**核心功能**:
- Miro 板 AI 集成
- MCP 服务器配置
- Claude Code 技能
- 可视化协作增强

---

### 4.3 claude-tmux (nielsgroen/claude-tmux)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 新增 |
| **Forks** | - |
| **Language** | - |
| **更新** | 2026-03 |

**描述**: Manage Claude Code within tmux. A tmux popup of all your Claude Code instances, enabling quick switching, status monitoring, session lifecycle management, with git worktree and pull request support.

**核心功能**:
- tmux 会话管理
- Claude Code 实例管理
- 快速切换
- 状态监控
- 会话生命周期管理
- Git worktree 支持
- PR 支持

---

### 4.4 claude-esp (phiat/claude-esp)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 新增 |
| **Forks** | - |
| **Language** | Go |
| **更新** | 2026-03 |

**描述**: Go-based TUI that streams Claude Code's hidden output (thinking, tool calls, subagents) to a separate terminal.

**核心功能**:
- Claude Code 隐藏输出流
- 多会话同时监控
- 内容类型过滤
- 后台任务跟踪
- 调试辅助

---

### 4.5 popkit-claude (jrc1883/popkit-claude)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 4 |
| **Forks** | - |
| **Language** | - |
| **更新** | 2026-02 |

**描述**: AI-powered development workflow automation for Claude Code. Modular plugin suite with 23 commands, 38 skills, and 22 specialized agents for professional software development.

**核心功能**:
- 23 个命令
- 38 个技能
- 22 个专业代理
- 模块化插件套件

---

### 4.6 langchain-community-plugin (Codeblockz/langchain-community-plugin)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 3 |
| **Forks** | - |
| **Language** | - |
| **更新** | 2026-02 |

**描述**: Claude Code plugin for LangChain and LangGraph development. Skills, commands, and reviewer agents for building AI agents, RAG pipelines, and LCEL chains.

**核心功能**:
- LangChain 开发
- LangGraph 开发
- AI Agent 构建
- RAG 管道
- LCEL 链

---

### 4.7 claude-awesome-stack (giacomogaglione/claude-awesome-stack)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 2 |
| **Forks** | - |
| **Language** | - |
| **更新** | 2026-02 |

**描述**: Installable stack packs for Claude Code — production-ready skills, hooks, and project configs for domain-specific development

---

### 4.8 pactkit (pactkit/pactkit)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 1 |
| **Forks** | - |
| **Language** | - |
| **更新** | 2026-02 |

**描述**: 🚀 Give Claude Code an operating system — 9 specialized AI agents, 11 PDCA commands, 10 skills. Spec-driven development: your AI writes specs before code, runs TDD, never commits without green tests.

**核心功能**:
- 9 个专业 AI 代理
- 11 个 PDCA 命令
- 10 个技能
- 规范驱动开发
- TDD 流程

---

## 📊 五、热门插件排行汇总

### 游戏开发类
| 插件 | Stars | 描述 |
|------|-------|------|
| mcp-unity | 1,382 | 主流 Unity MCP 集成 |
| Unity-MCP | 1,174 | Unity AI 桥接 |
| pixel-plugin | 56 | 像素艺术 Aseprite |
| claude-code-game-studios | 26-30 | 48 AI 代理游戏工作室 |

### Python 开发类
| 插件 | Stars | 描述 |
|------|-------|------|
| developer-kit | 133 | 全栈开发工具包 |
| claude-skills-collection-2026 | 23 | 100+ 生产技能 |
| claude-arsenal | 9 | 39+ 实战技能 |
| spoon-awesome-skill | 12 | SpoonOS/Web3 |

### 测试自动化类
| 插件 | Stars | 描述 |
|------|-------|------|
| playwright-skill | 1,863 | Playwright 浏览器自动化 |
| claude-code-playwright-mcp-test | 164 | YAML 测试框架 |
| unibrowse | 4 | 高级浏览器自动化 |
| ai-testing-mcp | 6 | AI 测试自动化 |

### 开发者工具类
| 插件 | Stars | 描述 |
|------|-------|------|
| claude-skills-marketplace | 431 | Git/测试/代码审查 |
| miro-ai | 66 | Miro AI 集成 |
| popkit-claude | 4 | 模块化开发工作流 |
| claude-tmux | 新增 | tmux 会话管理 |

---

## 💡 关键发现

1. **Playwright 集成最热门**: playwright-skill 以 1,863 Stars 领跑测试自动化领域
2. **Unity MCP 方案成熟**: 两个主要的 Unity 集成方案 (mcp-unity, Unity-MCP) 都有很高的关注度
3. **Python 开发工具多样化**: 从通用开发工具包到 Web3 专用技能
4. **新兴工具涌现**: claude-tmux, claude-esp 等工具解决实际开发痛点

---

## 🔗 相关资源

- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
- [awesome-claude-skills](https://github.com/travisvn/awesome-claude-skills)
- [Claude Code 官方文档](https://docs.anthropic.com/en/docs/claude-code)
