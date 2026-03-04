# Claude Code 插件调研补充文档 v20

> 调研日期: 2026-03-04
> 调研方向: 游戏客户端开发 / Python 开发 / 游戏客户端自动化测试 / 其他开发者工具

---

## 目录

1. [游戏客户端开发](#1-游戏客户端开发)
2. [Python 开发](#2-python-开发)
3. [游戏客户端自动化测试](#3-游戏客户端自动化测试)
4. [其他开发者工具](#4-其他开发者工具)
5. [热门 MCP 服务器汇总](#5-热门-mcp-服务器汇总)
6. [快速推荐](#6-快速推荐)

---

## 1. 游戏客户端开发

### 1.1 Claude Code Game Studios ⭐⭐⭐⭐⭐ NEW
- **GitHub**: https://github.com/Donchitos/Claude-Code-Game-Studios
- **Stars**: 26 | **更新**: 3天前
- **描述**: 48个AI代理 + 36个工作流技能 + 完整协调系统，模拟真实游戏工作室工作流
- **核心功能**:
  - 48个专业AI代理覆盖游戏开发全流程
  - 36个工作流技能完整游戏开发管线
  - 工作室协调系统
  - 多引擎支持: Unity, Unreal, Godot, WebGL
- **适用场景**: 大型游戏项目开发、游戏工作室工作流自动化、跨团队协作开发

### 1.2 Unity AI Workflow ⭐⭐⭐⭐ NEW
- **GitHub**: https://github.com/David-GD13/unity-ai-workflow
- **Stars**: 4 | **特点**: 专为 Unity 6.2+ 设计的 AI-first 开发工作流
- **核心功能**:
  - 三种开发模式: Assistant / Mix (默认) / Automatic
  - TCREI Prompting: Task-Context-References-Evaluate-Iterate 方法论
  - 验证系统: [VERIFIED]/[SYNTHESIZED]/[UNVERIFIED]
  - 专家 Skills: UI Toolkit、ScriptableObject、Netcode、game feel
- **安装**: 
```bash
git clone https://github.com/David-GD13/unity-ai-workflow.git
cp -r unity-ai-workflow ~/.claude/skills/
```

### 1.3 lazy-bird ⭐⭐⭐⭐⭐
- **GitHub**: https://github.com/yusufkaraaslan/lazy-bird
- **Stars**: 210 | **语言**: Python
- **描述**: 通用开发自动化工具，支持 ANY 项目。Claude Code 可自主实现功能、运行测试、创建 PR
- **支持框架**: Godot、React、Django、Node.js、Rust 等15+框架
- **核心功能**:
  - Issue 驱动的自动开发
  - 自动运行测试并创建 PR
  - 安全、可扩展
- **安装**: `pip install lazy-bird`

### 1.4 cc-plugin-unity-gamedev ⭐⭐⭐
- **GitHub**: https://github.com/tjboudreaux/cc-plugin-unity-gamedev
- **Stars**: 1
- **描述**: 21个专业技能，完整覆盖Unity开发栈
- **技能分类**:
  - 工具类: Addressables, MemoryPack, ScriptableObjects, Profiling
  - 动画/物理: Animation, Physics, NavMesh, Object Pooling, State Machine
  - AI/行为: Behavior Designer, GAS (Gameplay Ability System)
  - 音视频: Wwise音频, Cinemachine相机
  - UI: UGUI, Mobile Optimization
  - 测试: Unity Test Framework
  - DI/异步: VContainer, UniTask

### 1.5 Godot MCP Server ⭐⭐⭐⭐
- **描述**: Godot 游戏引擎 MCP 服务器集成
- **功能**: Godot 项目代码生成、场景管理、GDScript 辅助
- **适用**: 2D/3D 游戏客户端开发

---

## 2. Python 开发

### 2.1 Serena ⭐⭐⭐⭐⭐
- **GitHub**: https://github.com/oraios/serena
- **Stars**: 20,941 | **语言**: Python
- **描述**: 强大的编程代理工具包，提供语义检索和编辑能力（MCP 服务器及其他集成）
- **核心功能**:
  - 语义代码检索
  - 智能代码编辑
  - 语言服务器协议支持
  - MCP 服务器集成
- **官网**: https://oraios.github.io/serena
- **适用场景**: 大型 Python 项目重构、代码理解、智能编辑

### 2.2 PAL MCP Server ⭐⭐⭐⭐⭐
- **GitHub**: https://github.com/BeehiveInnovations/pal-mcp-server
- **Stars**: 11,180 | **语言**: Python
- **描述**: 多模型协作 MCP 服务器，支持 Claude Code / GeminiCLI / CodexCLI + Gemini / OpenAI / OpenRouter / Azure / Grok / Ollama
- **核心功能**:
  - 多 AI 模型协同工作
  - 模型切换和负载均衡
  - 自定义模型支持

### 2.3 claudekit ⭐⭐⭐⭐⭐
- **GitHub**: https://github.com/carlrannaberg/claudekit
- **描述**: Impressive CLI toolkit 提供 auto-save checkpointing、code quality hooks、specification generation and execution
- **子代理**:
  - **oracle**: GPT-5 集成
  - **code-reviewer**: 6方面深度分析
  - **typescript-expert**: TypeScript 专家
  - **ai-sdk-expert**: Vercel AI SDK
- **功能**: 20+  specialized subagents

### 2.4 claude-arsenal ⭐⭐⭐⭐
- **GitHub**: https://github.com/majiayu000/claude-arsenal
- **Stars**: 9 | **语言**: Python
- **描述**: 39+ 实战级 Claude Code 技能 + 9 个专业代理，专业软件开发综合技能库
- **核心功能**:
  - 39+ 技能覆盖
  - DevOps 工具链
  - 多语言支持（Python, TypeScript）
- **适用场景**: Python 全栈开发、DevOps

### 2.5 claud-skills ⭐⭐⭐⭐
- **GitHub**: https://github.com/Interstellar-code/claud-skills
- **Stars**: 11 | **语言**: Python
- **描述**: 生产级 Claude Code 框架，包含 13 个代理、9 个技能
- **支持语言**: JavaScript, TypeScript, PHP, Laravel, React, Python
- **核心功能**:
  - 13 个专用代理
  - 9 个开发技能
  - 自动文档生成
  - Playwright 测试集成

### 2.6 koder ⭐⭐⭐⭐
- **GitHub**: https://github.com/feiskyer/koder
- **Stars**: 80 | **语言**: Python
- **描述**: 直观的 AI 编程助手和交互式 CLI 工具
- **核心功能**:
  - 智能代码补全
  - 上下文感知
  - 交互式 CLI
- **适用场景**: Python 日常开发

### 2.7 uv - Python 包管理器 ⭐⭐⭐⭐⭐
- **GitHub**: https://github.com/astral-sh/uv
- **描述**: 10-100x faster than pip
- **安装**:
```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```
- **使用**:
```bash
uv init my-project
uv venv
uv pip install -r requirements.txt
```

### 2.8 read-only-postgres ⭐⭐⭐⭐⭐
- **GitHub**: https://github.com/jawwadfirdousi/agent-skills
- **描述**: PostgreSQL 只读查询技能
- **安全特性**:
  - 只读查询 (SELECT/SHOW/EXPLAIN/WITH)
  - 超时控制
  - 行数限制
  - 多连接支持

---

## 3. 游戏客户端自动化测试

### 3.1 playwright-skill ⭐⭐⭐⭐⭐
- **GitHub**: https://github.com/lackeyjb/playwright-skill
- **Stars**: 1,844 | **语言**: JavaScript
- **描述**: Claude Code 的 Playwright 浏览器自动化技能。模型调用式 - Claude 自主编写和执行自定义自动化测试和验证
- **核心功能**:
  - 模型调用式自动化（Claude 自主编写测试）
  - E2E 测试自动化
  - Web 测试验证
  - 无需手动编写测试脚本
- **适用场景**: 
  - 游戏 Web 客户端测试
  - 游戏官网/登录系统测试
  - 游戏内嵌 Web 页面测试
- **安装**: 
```bash
git clone https://github.com/lackeyjb/playwright-skill.git
cp -r playwright-skill ~/.claude/skills/playwright
```

### 3.2 claude-code-playwright-mcp-test ⭐⭐⭐⭐
- **GitHub**: https://github.com/terryso/claude-code-playwright-mcp-test
- **Stars**: 164 | **语言**: JavaScript
- **描述**: 基于 YAML 的 Playwright MCP 自动化测试框架，专为 Claude Code 设计
- **核心功能**:
  - YAML 配置驱动测试
  - MCP 协议集成
  - Claude Code 原生支持
- **文档**: https://terryso.github.io/blog/yaml-playwright-testing-revolution
- **适用场景**: 低代码测试编写、游戏客户端 UI 自动化

### 3.3 playwright-bot-bypass ⭐⭐⭐
- **GitHub**: https://github.com/greekr4/playwright-bot-bypass
- **Stars**: 127 | **语言**: JavaScript
- **描述**: Claude Code 技能，用于绕过机器人检测（如 Google CAPTCHA）
- **核心功能**:
  - 反爬虫检测绕过
  - CAPTCHA 处理
  - 隐身浏览
- **适用场景**: 
  - 游戏客户端自动化测试（绕过反作弊）
  - 游戏数据采集
- **注意**: 仅用于合法测试目的

### 3.4 Unity Test Framework ⭐⭐⭐⭐
- **描述**: Unity 官方测试框架
- **测试类型**:
  - **EditMode**: 编辑器环境测试（工具类、辅助功能）
  - **PlayMode**: 运行时测试（游戏逻辑、UI）
  - **Performance**: 性能测试
- **适用场景**: Unity 游戏客户端单元测试、集成测试

### 3.5 Android UI 测试 ⭐⭐⭐
- **工具**: ADB + uiautomator
- **核心命令**:
```bash
# 设备校准 - 获取屏幕分辨率
adb shell wm size

# UI 检查 - 获取元素信息
adb shell uiautomator dump /sdcard/view.xml

# 交互操作
adb shell input tap <x> <y>
adb shell input swipe <x1> <y1> <x2> <y2> <duration_ms>
adb shell input text "Hello"

# 截图验证
adb shell screencap -p /sdcard/screen.png
```
- **适用场景**: Android 游戏客户端 UI 自动化测试

### 3.6 iOS 模拟器测试 ⭐⭐⭐
- **GitHub**: https://github.com/conorluddy/ios-simulator-skill
- **Stars**: 557 | **平台**: macOS
- **核心功能**:
  - 模拟器控制 (启动/停止)
  - 应用安装
  - UI 交互自动化
  - 截图捕获
- **适用场景**: iOS 游戏客户端模拟器测试

---

## 4. 其他开发者工具

### 4.1 GitMCP ⭐⭐⭐⭐⭐
- **GitHub**: https://github.com/idosal/git-mcp
- **Stars**: 7,691 | **语言**: TypeScript
- **描述**: 终结代码幻觉！GitMCP 是免费开源的远程 MCP 服务器，适用于任何 GitHub 项目
- **核心功能**:
  - GitHub 项目代码检索
  - 代码上下文理解
  - 防止 AI 生成幻觉代码
- **官网**: https://gitmcp.io

### 4.2 DevDocs ⭐⭐⭐⭐⭐
- **GitHub**: https://github.com/cyberagiinc/DevDocs
- **Stars**: 2,037 | **语言**: TypeScript
- **描述**: 完全免费、私有的 UI 技术文档 MCP 服务器，专为程序员设计
- **核心功能**:
  - 技术文档聚合
  - 私有部署
  - UI 界面管理
  - 支持 Cursor, Windsurf, Cline, Roo Code, Claude Desktop
- **官网**: https://www.cyberagi.ai

### 4.3 AgentSys ⭐⭐⭐⭐⭐
- **GitHub**: https://github.com/avifenesh/agentsys
- **描述**: Workflow automation system for Claude with a group of useful plugins, agents, and skills
- **核心功能**:
  - 任务到生产工作流自动化
  - PR 管理
  - 代码清理
  - 性能调查
  - 多代理代码审查
- **特点**: 生产级，使用 regex、AST 确定性检测 + LLM 判断

### 4.4 Superpowers ⭐⭐⭐⭐⭐
- **GitHub**: https://github.com/obra/superpowers
- **描述**: A strong bundle of core competencies for software engineering
- **核心功能**:
  - 完整 SDLC 覆盖（规划、审查、测试、调试）
  - 核心工程技能集
  - 良好组织，适应性强的技能

### 4.5 Trail of Bits Security Skills ⭐⭐⭐⭐⭐
- **GitHub**: https://github.com/trailofbits/skills
- **描述**: A very professional collection of over a dozen security-focused skills
- **核心功能**:
  - CodeQL 静态分析
  - Semgrep 集成
  - 变体分析
  - 修复验证
  - 差异代码审查

### 4.6 ContextKit ⭐⭐⭐⭐
- **GitHub**: https://github.com/FlineDev/ContextKit
- **描述**: A systematic development framework that transforms Claude Code into a proactive development partner
- **核心功能**:
  - 4阶段规划方法论
  - 专业质量代理
  - 结构化工作流

### 4.7 Rulesync ⭐⭐⭐⭐
- **GitHub**: https://github.com/dyoshikawa/rulesync
- **描述**: A Node.js CLI tool that automatically generates configs for various AI coding agents
- **核心功能**:
  - 自动生成规则、ignore 文件、MCP 服务器、命令和子代理
  - Claude Code 与其他 AI agent 配置互转

### 4.8 Claude Code Flow ⭐⭐⭐⭐
- **GitHub**: https://github.com/ruvnet/claude-code-flow
- **描述**: Code-first orchestration layer enabling Claude to write, edit, test, and optimize code autonomously
- **核心功能**:
  - 递归代理循环
  - 自主代码优化

### 4.9 Claude Squad ⭐⭐⭐⭐
- **GitHub**: https://github.com/smtg-ai/claude-squad
- **描述**: Terminal app that manages multiple Claude Code, Codex in separate workspaces
- **核心功能**:
  - 多代理并行工作
  - 工作区隔离
  - 同时处理多个任务

### 4.10 cc-devops-skills ⭐⭐⭐⭐
- **GitHub**: https://github.com/akin-ozer/cc-devops-skills
- **描述**: Immensely detailed set of skills for DevOps Engineers
- **核心功能**:
  - IaC 代码生成（AWS, Azure, GCP 等）
  - 验证工具
  - 生成器
  - Shell 脚本和 CLI 工具

---

## 5. 热门 MCP 服务器汇总

| 名称 | Stars | 语言 | 用途 | 推荐度 |
|------|-------|------|------|--------|
| Serena | 20,941 | Python | 语义代码检索与编辑 | ⭐⭐⭐⭐⭐ |
| PAL MCP Server | 11,180 | Python | 多模型协作 | ⭐⭐⭐⭐⭐ |
| GitMCP | 7,691 | TypeScript | GitHub 项目代码检索 | ⭐⭐⭐⭐⭐ |
| DevDocs | 2,037 | TypeScript | 技术文档聚合 | ⭐⭐⭐⭐⭐ |
| playwright-skill | 1,844 | JavaScript | 浏览器自动化测试 | ⭐⭐⭐⭐⭐ |
| lazy-bird | 210 | Python | 通用开发自动化 | ⭐⭐⭐⭐⭐ |
| Claude Code Game Studios | 26 | TypeScript | 游戏开发全流程 | ⭐⭐⭐⭐⭐ |
| claude-arsenal | 9 | Python | 39+技能综合库 | ⭐⭐⭐⭐ |
| mcp-wireshark | 23 | Python | 网络流量分析 | ⭐⭐⭐ |

---

## 6. 快速推荐

### 游戏客户端开发推荐
1. **Claude Code Game Studios** - 48代理全栈覆盖
2. **Unity AI Workflow** - Unity 6.2+ AI工作流
3. **lazy-bird** - 支持 Godot，自动化功能开发
4. **Serena** - 大型项目代码理解和重构
5. **GitMCP** - GitHub 项目代码检索

### Python 开发推荐
1. **Serena** - 语义代码检索和编辑
2. **PAL MCP Server** - 多模型协作
3. **claude-arsenal** - 39+ 技能综合库
4. **claudekit** - 20+ 子代理工具包
5. **uv** - 最快 Python 包管理器
6. **read-only-postgres** - 安全数据库查询

### 游戏客户端自动化测试推荐
1. **playwright-skill** - 模型调用式 E2E 测试（强烈推荐）
2. **claude-code-playwright-mcp-test** - YAML 驱动测试框架
3. **playwright-bot-bypass** - 绕过机器人检测
4. **Unity Test Framework** - Unity 官方测试
5. **ADB + uiautomator** - Android UI 测试

### 通用开发者工具推荐
1. **GitMCP** - 防止代码幻觉
2. **DevDocs** - 技术文档聚合
3. **AgentSys** - 生产级工作流自动化
4. **Superpowers** - 核心工程技能集
5. **Trail of Bits Security Skills** - 安全审计
6. **ContextKit** - 4阶段规划方法论

---

## 安装指南

### MCP 服务器安装
```bash
# 大多数 MCP 服务器通过 npm 或 pip 安装
npm install -g @anthropic/mcp-server-name
# 或
pip install mcp-server-name
```

### Claude Code Skill 安装
```bash
# 克隆技能仓库
git clone https://github.com/xxx/skill-name.git

# 复制到 Claude Code 技能目录
cp -r skill-name ~/.claude/skills/
```

### Playwright Skill 安装
```bash
git clone https://github.com/lackeyjb/playwright-skill.git
cp -r playwright-skill ~/.claude/skills/playwright
```

---

## 相关资源

- [awesome-claude-code (hesreallyhim)](https://github.com/hesreallyhim/awesome-claude-code) - 最全 Claude Code 资源列表
- [awesome-claude-code (jqueryscript)](https://github.com/jqueryscript/awesome-claude-code) - 工具和集成列表
- [ClawHub](https://clawhub.com) - Agent Skills 发现平台
- [OpenClaw Docs](https://docs.openclaw.ai) - OpenClaw 文档

---

*文档生成时间: 2026-03-04 08:25 Asia/Shanghai*
