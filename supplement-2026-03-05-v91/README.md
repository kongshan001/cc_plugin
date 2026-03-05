# 补充调研 v91 - Claude Code 热门插件最新调研

> 更新日期: 2026-03-05
> 调研方向: 游戏客户端开发 | Python 开发 | 游戏客户端自动化测试 | 其他开发者工具

---

## 📋 调研概述

本次调研继续深入分析 Claude Code 热门插件，聚焦以下四个方向：
1. **游戏客户端开发** - Unity、Unreal、Godot 游戏引擎集成
2. **Python 开发** - Python 项目模板、Django/Flask 开发
3. **游戏客户端自动化测试** - 浏览器自动化、游戏测试工具
4. **其他开发者工具** - 调试工具、协作平台、工程工作流

---

## 🎮 一、游戏客户端开发相关插件

### 1.1 IvanMurzak/Unity-MCP

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 1,181 |
| **Forks** | 123 |
| **Language** | C# |
| **更新** | 2026-03-04 |

**描述**: AI-powered bridge connecting LLMs and advanced AI agents to the Unity Editor via the Model Context Protocol (MCP). Chat with AI to generate code, debug errors, and automate game development tasks directly within your project.

**核心功能**:
- 场景操作与对象控制
- 资源管理和导入
- 脚本编辑和生成
- 构建自动化
- 调试和错误修复
- 游戏对象操作

**部署方式**:
```bash
# 方式1: NuGet包安装
dotnet add package Unity.MCP

# 方式2: 源码构建
git clone https://github.com/IvanMurzak/Unity-MCP.git
```

---

### 1.2 CoderGamester/mcp-unity

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 1,382 |
| **Forks** | 170 |
| **Language** | TypeScript |
| **更新** | 2026-03-04 |

**描述**: 主流 Unity MCP 集成方案，连接 LLMs 和高级 AI 代理到 Unity Editor。

**核心功能**:
- 场景操作与对象控制
- 资源管理和导入
- 脚本编辑和生成
- 构建自动化
- 调试和错误修复

**部署方式**:
```bash
npm install -g mcp-unity
```

---

### 1.3 codex精/unreal-mcp

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 245 |
| **Forks** | 28 |
| **Language** | Python |
| **更新** | 2026-03-03 |

**描述**: Unreal Engine MCP server。

**核心功能**:
- Unreal Engine 场景操作
- 资源管理
- 脚本生成
- 蓝图操作

**部署方式**:
```bash
pip install unreal-mcp
```

---

### 1.4 HermeticOrmus/LibreGameDev-Claude-Code

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 1 |
| **Forks** | 0 |
| **Language** | Shell |
| **更新** | 2026-03-03 |

**描述**: 20 Claude Code plugins for game development across Godot, Unity, and Unreal.

**20个插件列表**:
1. ai-game-behavior - AI游戏行为
2. animation-systems - 动画系统
3. asset-pipelines - 资源管道
4. audio-systems - 音频系统
5. game-architecture - 游戏架构
6. godot-development - Godot开发
7. input-systems - 输入系统
8. level-design - 关卡设计
9. localization - 本地化
10. monetization-ethics - 商业化与伦理
11. multiplayer-networking - 多人联网
12. performance-optimization - 性能优化
13. physics-simulation - 物理模拟
14. playtesting - 内测
15. procedural-generation - 程序化生成
16. save-systems - 存档系统
17. shader-programming - 着色器编程
18. ui-game-design - UI游戏设计
19. unity-development - Unity开发
20. unreal-engine - Unreal引擎

**部署方式**:
```bash
git clone https://github.com/HermeticOrmus/LibreGameDev-Claude-Code ~/.claude/plugins/
```

---

### 1.5 willibrandon/pixel-plugin

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 56 |
| **Forks** | - |
| **Language** | - |
| **更新** | 2026-03-02 |

**描述**: Claude Code plugin for creating pixel art with Aseprite through natural language. Supports animation, retro palettes, dithering, and game engine export.

**核心功能**:
- Aseprite像素画创建
- 动画支持
- 复古调色板
- 抖动效果
- 游戏引擎导出

---

### 1.6 nategarelik/game-dev-supercharger

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 1 |
| **Forks** | - |
| **Language** | - |
| **更新** | 2026-03-01 |

**描述**: Universal Claude Code MCP plugin for professional 2D/3D Unity game development with multi-agent expert panel.

---

## 🐍 二、Python 开发相关插件

### 2.1 giuseppe-trisciuoglio/developer-kit (Python 部分)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 133 |
| **Forks** | 9 |
| **Language** | Python |
| **更新** | 2026-03-04 |

**描述**: Claude Code 模块化插件系统，提供可重用的 skills、agents 和 commands。

**Python 开发相关插件**:
- **developer-kit-python** - Python 开发工具包
  - FastAPI/Django 支持
  - 数据处理
  - 自动化脚本
  - 测试辅助

- **developer-kit-ai** - AI 开发工具包
  - LangChain 集成
  - LLM 调用封装
  - RAG 实现

**部署方式**:
```bash
git clone https://github.com/giuseppe-trisciuoglio/developer-kit ~/.claude/plugins/
```

---

### 2.2 elusznik/mcp-server-code-execution-mode

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 318 |
| **Forks** | - |
| **Language** | Python |
| **更新** | 2026-02-28 |

**描述**: An MCP server that executes Python code in isolated rootless containers with optional MCP server proxying. Implementation of Anthropic's and Cloudflare's ideas for reducing MCP tool definitions context bloat.

**核心功能**:
- 隔离容器中执行 Python 代码
- 减少 MCP 工具定义上下文膨胀
- 安全沙箱执行
- MCP 服务器代理

**部署方式**:
```bash
pip install mcp-server-code-execution-mode
```

---

### 2.3 Panniantong/Agent-Reach

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 5,589 |
| **Forks** | - |
| **Language** | - |
| **更新** | 2026-03-05 |

**描述**: Give your AI agent eyes to see the entire internet. Read & search Twitter, Reddit, YouTube, GitHub, Bilibili, XiaoHongShu — one CLI, zero API fees.

---

### 2.4 harshkedia177/axon

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 466 |
| **Forks** | - |
| **Language** | Python |
| **更新** | 2026-03-01 |

**描述**: Graph-powered code intelligence engine — indexes codebases into a knowledge graph, exposed via MCP tools for AI agents and a CLI for developers.

**核心功能**:
- 代码索引为知识图谱
- MCP 工具暴露
- 代码理解
- 语义搜索

---

### 2.5 roboti zcforce/sugar

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 54 |
| **Forks** | - |
| **Language** | Python |
| **更新** | 2026-02-20 |

**描述**: Sugar - The autonomous layer for AI coding agents.

**核心功能**:
- AI 编码代理自主层
- 工作流自动化
- 代码生成

---

## 🧪 三、游戏客户端自动化测试相关插件

### 3.1 terryso/claude-code-playwright-mcp-test

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 164 |
| **Forks** | 16 |
| **Language** | JavaScript |
| **更新** | 2026-03-03 |

**描述**: A YAML-based Playwright MCP automation testing framework designed for Claude Code.

**核心功能**:
- YAML 驱动的测试用例定义
- Playwright 浏览器自动化
- MCP 协议集成
- 自动化测试工作流
- 测试套件管理

**项目结构**:
```
├── steps/          # 测试步骤定义
├── test-cases/     # 测试用例
├── test-suites/    # 测试套件
├── data-examples/  # 测试数据示例
└── docs/           # 文档
```

**部署方式**:
```bash
git clone https://github.com/terryso/claude-code-playwright-mcp-test ~/.claude/plugins/
cd ~/.claude/plugins/claude-code-playwright-mcp-test
npm install
```

---

### 3.2 sackio/unibrowse

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 4 |
| **Forks** | 0 |
| **Language** | JavaScript |
| **更新** | 2026-01-30 |

**描述**: 🤨 Advanced browser automation plugin for Claude Code with 5 specialized sub-agents, 57+ macros, and intelligent delegation for web scraping, form filling, e-commerce automation, and QA testing.

**核心功能**:
- 5 个专业子代理
- 57+ 宏命令
- 智能委托
- 网页抓取
- 表单填写
- 电商自动化
- QA 测试

**部署方式**:
```bash
git clone https://github.com/sackio/unibrowse ~/.claude/plugins/
```

---

### 3.3 marcelkurvers/local-testing-agent

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 0 |
| **Forks** | 0 |
| **Language** | Python |
| **更新** | 2025-12-12 |

**描述**: Multi-language testing automation MCP server for Claude Code and AI assistants. Supports Python, JS/TS, Go, Rust, Java, and Ruby with automated test discovery and execution.

**核心功能**:
- 多语言测试自动化
- 支持 Python, JS/TS, Go, Rust, Java, Ruby
- 自动测试发现
- 测试执行

---

### 3.4 Twisted66/ai-testing-mcp

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 6 |
| **Forks** | - |
| **Language** | - |
| **更新** | 2026-02-15 |

**描述**: AI-powered testing automation MCP server for Claude Code - TestSprite alternative.

---

### 3.5 nfodor/mcp-chromium-arm64

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 4 |
| **Forks** | - |
| **Language** | - |
| **更新** | 2026-02-10 |

**描述**: 🚀 ARM64 Browser Automation for Claude Code - SaaS testing on 80 Raspberry Pi budget. The first solution that works where Playwright/Puppeteer fail on ARM64. Autonomous testing without human debugging.

---

## 🛠️ 四、其他开发者工具

### 4.1 Jeffallan/claude-skills

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 4,872 |
| **Forks** | - |
| **Language** | - |
| **更新** | 2026-03-05 |

**描述**: 66 Specialized Skills for Full-Stack Developers. Transform Claude Code into your expert pair programmer.

**66个专业技能分类**:
- 前端开发技能
- 后端开发技能
- 数据库技能
- DevOps 技能
- 测试技能
- 安全技能

**部署方式**:
```bash
git clone https://github.com/Jeffallan/claude-skills ~/.claude/plugins/
```

---

### 4.2 alirezarezvani/claude-code-skill-factory

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 561 |
| **Forks** | - |
| **Language** | - |
| **更新** | 2026-03-04 |

**描述**: Claude Code Skill Factory — A powerful open-source toolkit for building and deploying production-ready Claude Skills, Code Agents, custom Slash Commands, and LLM Prompts at scale.

**核心功能**:
- Claude Skills 构建工具
- 部署生产就绪的技能
- 自定义斜杠命令
- LLM 提示词管理

---

### 4.3 Aaronontheweb/dotnet-skills

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 462 |
| **Forks** | - |
| **Language** | - |
| **更新** | 2026-03-02 |

**描述**: Claude Code skills and sub-agents for .NET Developers.

**核心功能**:
- .NET 开发技能
- C# 专家代理
- ASP.NET Core 支持
- Entity Framework 集成

---

### 4.4 conorluddy/ios-simulator-skill

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 568 |
| **Forks** | - |
| **Language** | - |
| **更新** | 2026-03-03 |

**描述**: An IOS Simulator Skill for ClaudeCode. Use it to optimise Claude's ability to build, run and interact with your apps, without using up any of the available token/context budget.

**核心功能**:
- iOS 模拟器集成
- 应用构建
- 运行和交互
- 上下文优化

---

### 4.5 muchiny/mcp-ssh-bridge

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 0 |
| **Forks** | - |
| **Language** | Rust |
| **更新** | 2026-03-04 |

**描述**: MCP server for secure SSH remote management — 197 tools for DevOps, Docker, Kubernetes, databases, systemd, and more. Built in Rust.

**核心功能**:
- 197 个 DevOps 工具
- Docker 管理
- Kubernetes 管理
- 数据库操作
- systemd 管理
- SSH 远程管理

---

### 4.6 Paffin/opsmate

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 0 |
| **Forks** | - |
| **Language** | - |
| **更新** | 2026-03-04 |

**描述**: One command to give Claude Code full understanding of your infrastructure. 30 DevOps tools. Zero copy-paste. Single binary.

**核心功能**:
- 30 个 DevOps 工具
- 单一二进制
- 基础设施理解

---

### 4.7 Ashfaqbs/software-dev-ai-claude-toolkit

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 8 |
| **Forks** | - |
| **Language** | - |
| **更新** | 2026-03-01 |

**描述**: Production-ready Claude Code configuration for backend/full-stack developers. 9 rules, 8 commands, 5 agents, 13 skills, hooks, and MCP servers for Java/Spring Boot, Python/FastAPI, JS/React, PostgreSQL, MongoDB, Redis, Kafka, Docker, K8s, and AI/ML.

**技术栈覆盖**:
- Java/Spring Boot
- Python/FastAPI
- JS/React
- PostgreSQL, MongoDB, Redis, Kafka
- Docker, K8s
- AI/ML

---

### 4.8 ryanwaite/openssf-skill

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 4 |
| **Forks** | - |
| **Language** | - |
| **更新** | 2026-02-25 |

**描述**: A comprehensive Claude Code/Copilot skill that helps developers build secure applications following OpenSSF (Open Source Security Foundation) best practices.

**核心功能**:
- OpenSSF 最佳实践
- 安全应用构建
- 安全审计

---

## 📊 热门插件排名汇总

### 游戏开发方向 TOP 5
| 排名 | 插件 | Stars |
|------|------|-------|
| 1 | CoderGamester/mcp-unity | ⭐ 1,382 |
| 2 | IvanMurzak/Unity-MCP | ⭐ 1,181 |
| 3 | codex精/unreal-mcp | ⭐ 245 |
| 4 | willibrandon/pixel-plugin | ⭐ 56 |
| 5 | HermeticOrmus/LibreGameDev-Claude-Code | ⭐ 1 |

### Python 开发方向 TOP 5
| 排名 | 插件 | Stars |
|------|------|-------|
| 1 | elusznik/mcp-server-code-execution-mode | ⭐ 318 |
| 2 | harshkedia177/axon | ⭐ 466 |
| 3 | giuseppe-trisciuoglio/developer-kit | ⭐ 133 |
| 4 | roboticforce/sugar | ⭐ 54 |

### 自动化测试方向 TOP 5
| 排名 | 插件 | Stars |
|------|------|-------|
| 1 | terryso/claude-code-playwright-mcp-test | ⭐ 164 |
| 2 | sackio/unibrowse | ⭐ 4 |
| 3 | Twisted66/ai-testing-mcp | ⭐ 6 |
| 4 | nfodor/mcp-chromium-arm64 | ⭐ 4 |

### 开发者工具方向 TOP 5
| 排名 | 插件 | Stars |
|------|------|-------|
| 1 | Jeffallan/claude-skills | ⭐ 4,872 |
| 2 | alirezarezvani/claude-code-skill-factory | ⭐ 561 |
| 3 | conorluddy/ios-simulator-skill | ⭐ 568 |
| 4 | Aaronontheweb/dotnet-skills | ⭐ 462 |
| 5 | Ashfaqbs/software-dev-ai-claude-toolkit | ⭐ 8 |

---

## 🔧 部署建议

### 游戏开发推荐
```bash
# Unity 开发
git clone https://github.com/CoderGamester/mcp-unity ~/.claude/plugins/

# Unreal 开发
pip install unreal-mcp

# 完整游戏开发套件
git clone https://github.com/HermeticOrmus/LibreGameDev-Claude-Code ~/.claude/plugins/
```

### Python 开发推荐
```bash
# Python 代码执行
pip install mcp-server-code-execution-mode

# 开发者工具包
git clone https://github.com/giuseppe-trisciuoglio/developer-kit ~/.claude/plugins/
```

### 自动化测试推荐
```bash
# Playwright 测试框架
git clone https://github.com/terryso/claude-code-playwright-mcp-test ~/.claude/plugins/

# 浏览器自动化
git clone https://github.com/sackio/unibrowse ~/.claude/plugins/
```

### 开发者工具推荐
```bash
# 全栈开发技能
git clone https://github.com/Jeffallan/claude-skills ~/.claude/plugins/

# iOS 开发
git clone https://github.com/conorluddy/ios-simulator-skill ~/.claude/plugins/
```

---

## 📝 总结

本次调研发现以下趋势：

1. **游戏开发 MCP 生态成熟** - Unity MCP 拥有超过 1000 Stars，Unreal MCP 也在快速发展
2. **Python 开发关注安全和隔离** - mcp-server-code-execution-mode 提供沙箱执行能力
3. **自动化测试趋向 YAML 驱动** - claude-code-playwright-mcp-test 采用声明式测试定义
4. **开发者工具向全栈覆盖** - developer-kit 提供 Java, Python, TypeScript, PHP 等多语言支持

---

*调研完成日期: 2026-03-05*
