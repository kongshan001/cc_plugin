# Claude Code 插件调研补充文档 v21

> 调研日期: 2026-03-04
> 调研方向: 游戏客户端开发 / Python 开发 / 游戏客户端自动化测试 / 其他开发者工具

---

## 目录

1. [游戏客户端开发](#1-游戏客户端开发)
2. [Python 开发](#2-python-开发)
3. [游戏客户端自动化测试](#3-游戏客户端自动化测试)
4. [其他开发者工具](#4-其他开发者工具)
5. [热门技能推荐汇总](#5-热门技能推荐汇总)

---

## 1. 游戏客户端开发

### 1.1 Claude Code Game Studios ⭐⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [Donchitos/Claude-Code-Game-Studios](https://github.com/Donchitos/Claude-Code-Game-Studios) |
| **Star** | ⭐ 26 |
| **更新** | 2026-03-01 |
| **特点** | 48个AI代理 + 36个工作流技能 + 完整协调系统 |

#### 核心能力

- **48个专业AI代理**: 覆盖游戏开发全流程（设计、编程、美术、音效、测试）
- **36个工作流技能**: 完整游戏开发管线，从概念到发布
- **工作室协调系统**: 模拟真实游戏工作室工作流
- **多引擎支持**: Unity, Unreal, Godot, WebGL

#### 适用场景

- 大型游戏项目开发
- 游戏工作室工作流自动化
- 跨团队协作开发
- 全栈游戏开发

#### 安装

```bash
git clone https://github.com/Donchitos/Claude-Code-Game-Studios.git ~/.claude/skills/Claude-Code-Game-Studios
```

---

### 1.2 lazy-bird ⭐⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [yusufkaraaslan/lazy-bird](https://github.com/yusufkaraaslan/lazy-bird) |
| **Stars** | 210 |
| **语言** | Python |
| **特点** | 通用开发自动化工具，支持 Issue 驱动开发 |

#### 核心功能

- **Issue 驱动的自动开发**: 自动分析 Issue 并实现功能
- **15+ 框架预设**: 包括 **Godot 游戏开发框架**
- **自动测试和 PR**: 运行测试并创建 Pull Request
- **安全可扩展**: 生产级安全设计

#### 支持的框架

| 类别 | 框架 |
|------|------|
| 游戏引擎 | Godot |
| 前端 | React, Vue, Next.js |
| 后端 | Django, Node.js, Express |
| 其他 | Rust, Go, Flask |

#### 适用场景

- 游戏客户端功能迭代
- Bug 修复自动化
- 快速原型开发
- 自动化 PR 创建

---

### 1.3 Unity AI Workflow (2026 新增) ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [David-GD13/unity-ai-workflow](https://github.com/David-GD13/unity-ai-workflow) |
| **Star** | ⭐ 4 |
| **特点** | Unity 6.2+ AI-first 开发工作流 |

#### 核心特性

```markdown
### Dev Modes (三种开发模式)
| 模式 | 角色 | 适用场景 |
|------|------|---------|
| Assistant | 你构建，AI 辅助 | 学习、创意控制 |
| Mix (默认) | 协作模式 | 大多数项目 |
| Automatic | AI 构建 | 快速原型 |

### Game Feel 哲学
- 每项功能使用 /implement-feature 完整构建
- AI 询问 VFX、SFX、相机反馈和触觉
- 迭代打磨，不是单独阶段

### 技术架构
- TCREI Prompting: Task-Context-References-Evaluate-Iterate
- 验证系统: [VERIFIED]/[SYNTHESIZED]/[UNVERIFIED]
```

---

### 1.4 Network Chronicles (AI 游戏角色) ⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [Fimeg/NetworkChronicles](https://github.com/Fimeg/NetworkChronicles) |
| **特点** | AI 驱动游戏角色实现方案 |

#### 核心功能

- **LLM 集成**: 大语言模型驱动 NPC 行为
- **角色指南**: 详细的 AI 角色设计规范
- **服务发现**: 动态服务发现机制

#### 适用场景

- 开放世界游戏 NPC
- AI 驱动对话系统
- 游戏内智能实体

---

### 1.5 Godot 开发支持

#### lazy-bird Godot 预设

通过 lazy-bird 内置的 Godot 框架预设：

- GDScript 代码生成
- 场景管理辅助
- 节点和信号操作
- 2D/3D 游戏开发支持

#### claude-resources

| 项目 | 说明 |
|-----|------|
| **特点** | 社区维护的 Godot 技能 |

---

### 1.6 Web/H5 游戏开发

#### 引擎选择决策树

```
什么类型的游戏?
│
├── 2D 游戏
│   ├── 需要完整引擎功能? → Phaser 4
│   └── 需要原始渲染能力? → PixiJS 8
│
├── 3D 游戏
│   ├── 需要完整引擎(物理、XR)? → Babylon.js 7
│   └── 专注渲染? → Three.js
│
└── 自定义 → Canvas/WebGL
```

#### WebGPU 支持 (2026)

| 浏览器 | 支持 |
|--------|------|
| Chrome | ✅ v113+ |
| Firefox | ✅ v131+ |
| Safari | ✅ 18.0+ |
| **全球支持率** | **~73%** |

---

### 1.7 游戏开发技能汇总

| 技能 | GitHub | Star | 特点 |
|-----|--------|------|------|
| Claude-Code-Game-Studios | Donchitos | ⭐26 | 48代理全栈覆盖 |
| lazy-bird | yusufkaraaslan | ⭐210 | Godot + 自动化 |
| unity-ai-workflow | David-GD13 | ⭐4 | Unity 6.2+ |
| Network Chronicles | Fimeg | - | AI 游戏角色 |

---

## 2. Python 开发

### 2.1 Serena ⭐⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [oraios/serena](https://github.com/oraios/serena) |
| **Stars** | 20,941 |
| **语言** | Python |
| **官网** | https://oraios.github.io/serena |

#### 核心功能

- **语义代码检索**: 理解代码意图的智能搜索
- **智能代码编辑**: 上下文感知的代码修改
- **LSP 支持**: 完整的语言服务器协议
- **MCP 服务器集成**: 标准化集成方式

#### 适用场景

- 大型 Python 项目重构
- 代码理解与导航
- 智能代码编辑
- 团队知识库构建

---

### 2.2 PAL MCP Server ⭐⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [BeehiveInnovations/pal-mcp-server](https://github.com/BeehiveInnovations/pal-mcp-server) |
| **Stars** | 11,180 |
| **语言** | Python |

#### 核心功能

- **多模型协作**: Claude Code + Gemini + Codex + OpenAI + Ollama
- **模型切换**: 动态切换不同 AI 模型
- **负载均衡**: 自动分配请求
- **自定义模型**: 支持私有模型部署

#### 支持的模型

| 类别 | 模型 |
|------|------|
| Anthropic | Claude |
| Google | Gemini |
| OpenAI | GPT-4, GPT-4o |
| 本地 | Ollama |
| 其他 | OpenRouter, Azure, Grok |

---

### 2.3 claud-skills ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [Interstellar-code/claud-skills](https://github.com/Interstellar-code/claud-skills) |
| **Stars** | 11 |
| **语言** | Python |

#### 核心功能

- **13 个专用代理**: 覆盖开发全流程
- **9 个开发技能**: 模块化技能系统
- **自动文档生成**: 代码即文档
- **Playwright 集成**: E2E 测试支持

#### 支持语言

- Python
- JavaScript
- TypeScript
- PHP
- Laravel
- React

---

### 2.4 claude-arsenal ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [majiayu000/claude-arsenal](https://github.com/majiayu000/claude-arsenal) |
| **Stars** | 9 |
| **语言** | Python |

#### 核心功能

- **39+ 实战级技能**: 覆盖真实开发场景
- **9 个专业代理**: 细分领域专家
- **DevOps 工具链**: 完整的开发运维支持

---

### 2.5 koder ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [feiskyer/koder](https://github.com/feiskyer/koder) |
| **Stars** | 80 |
| **语言** | Python |

#### 核心功能

- **智能代码补全**: AI 驱动的代码建议
- **上下文感知**: 理解项目结构
- **交互式 CLI**: 直观的命令行界面

---

### 2.6 cchooks (Python Hook SDK) ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [GowayLee/cchooks](https://github.com/GowayLee/cchooks) |
| **语言** | Python |

#### 核心功能

- **轻量级 SDK**: 简洁的 API 设计
- **好文档**: 易于上手
- **Hook 集成**: 简化 Hook 配置流程
- **JSON 抽象**: 简化 JSON 配置文件处理

---

### 2.7 uv - Python 包管理器 (2025最快) ⭐⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [astral-sh/uv](https://github.com/astral-sh/uv) |
| **特点** | 10-100x faster than pip |

```bash
# 安装
curl -LsSf https://astral.sh/uv/install.sh | sh

# 项目初始化
uv init my-project
uv venv
uv pip install -r requirements.txt

# 快速运行
uv run script.py
uv run pytest
```

---

### 2.8 Python Skills 汇总

| 技能 | 核心能力 | 适用场景 |
|--------|---------|---------|
| **Serena** | 语义代码检索 | 重构、代码理解 |
| **PAL MCP Server** | 多模型协作 | AI 模型管理 |
| **claude-arsenal** | 39+技能 | 全栈开发 |
| **koder** | 智能编程 | 日常开发 |
| **cchooks** | Hook SDK | 自定义工作流 |
| **uv** | 极速包管理 | 项目初始化 |

---

## 3. 游戏客户端自动化测试

### 3.1 playwright-skill ⭐⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [lackeyjb/playwright-skill](https://github.com/lackeyjb/playwright-skill) |
| **Stars** | 1,844 |
| **语言** | JavaScript |
| **特点** | 模型调用式自动化 |

#### 核心功能

- **模型调用式自动化**: Claude 自主编写测试代码
- **E2E 测试自动化**: 端到端测试支持
- **Web 测试验证**: 功能测试、回归测试
- **无需手动脚本**: AI 自主完成

#### 适用场景

- **游戏 Web 客户端测试**
- 游戏官网/登录系统测试
- 游戏内嵌 Web 页面测试
- UI 交互验证

#### 安装

```bash
git clone https://github.com/lackeyjb/playwright-skill.git ~/.claude/skills/playwright-skill
```

---

### 3.2 claude-code-playwright-mcp-test ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [terryso/claude-code-playwright-mcp-test](https://github.com/terryso/claude-code-playwright-mcp-test) |
| **Stars** | 164 |
| **语言** | JavaScript |

#### 核心功能

- **YAML 配置驱动**: 声明式测试定义
- **MCP 协议集成**: 标准化接口
- **Claude Code 原生支持**: 无缝集成

#### 适用场景

- 低代码测试编写
- 游戏客户端 UI 自动化
- 快速测试脚本生成

---

### 3.3 playwright-bot-bypass ⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [greekr4/playwright-bot-bypass](https://github.com/greekr4/playwright-bot-bypass) |
| **Stars** | 127 |
| **语言** | JavaScript |

#### 核心功能

- **反爬虫检测绕过**: 绕过 Cloudflare、PerimeterX 等
- **CAPTCHA 处理**: 自动处理验证码
- **隐身浏览**: 模拟真实用户行为

#### ⚠️ 注意

仅用于合法测试目的，遵守网站服务条款。

---

### 3.4 Cursor Tools (Stagehand) ⭐⭐⭐⭐

| 项目 |说明 |
|-----|------|
| **GitHub** | [eastlondoner/cursor-tools](https://github.com/eastlondoner/cursor-tools) |
| **特点** | 浏览器自动化功能 (Stagehand) |

#### 核心功能

- **多模型支持**: 灵活切换 AI 模型
- **Stagehand 浏览器自动化**: 强大的 Web 自动化
- **多命令选项**: 灵活的扩展配置

---

### 3.5 Unity Test Framework

#### 游戏客户端测试方案

| 测试类型 | 方案 | 适用场景 |
|---------|------|---------|
| **Web/H5游戏** | Playwright | 功能测试、回归测试 |
| **Unity游戏** | Unity Test Framework | 单元测试、集成测试 |
| **性能测试** | Unity Profiler | 帧率、内存测试 |
| **Android游戏** | ADB + uiautomator | UI自动化 |
| **iOS游戏** | ios-simulator-skill | 模拟器测试 |

#### Unity 测试框架类型

| 测试类型 | 说明 | 适用场景 |
|---------|------|---------|
| **EditMode** | 编辑器环境测试 | 工具类、辅助功能 |
| **PlayMode** | 运行时测试 | 游戏逻辑、UI |
| **Performance** | 性能测试 | 性能优化 |

---

### 3.6 移动端游戏测试

#### Android UI 测试

```bash
# 设备校准
adb shell wm size

# UI 检查
adb shell uiautomator dump /sdcard/view.xml

# 交互操作
adb shell input tap <x> <y>
adb shell input swipe <x1> <y1> <x2> <y2> <duration_ms>

# 截图验证
adb shell screencap -p /sdcard/screen.png
```

#### iOS 模拟器测试

| 项目 | 说明 |
|-----|------|
| **GitHub** | [conorluddy/ios-simulator-skill](https://github.com/conorluddy/ios-simulator-skill) |
| **Star** | ⭐ 557 |

---

### 3.7 TDD 测试命令

| 命令 | 来源 | 功能 |
|-----|------|------|
| **/tdd** | zscott/pane | TDD 开发流程 |
| **/tdd-implement** | jerseycheese/Narraitor | TDD 实现 |
| **/repro-issue** | rzykov/metabase | 可复现测试用例 |

---

### 3.8 测试技能汇总

| 技能 | Star | 特点 |
|------|------|------|
| **playwright-skill** | ⭐1,844 | 模型调用式E2E |
| **claude-code-playwright-mcp-test** | ⭐164 | YAML驱动 |
| **playwright-bot-bypass** | ⭐127 | 反检测绕过 |
| **Cursor Tools** | - | Stagehand自动化 |
| **Unity Test Framework** | - | 单元/集成测试 |

---

## 4. 其他开发者工具

### 4.1 GitMCP ⭐⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [idosal/git-mcp](https://github.com/idosal/git-mcp) |
| **Stars** | 7,691 |
| **语言** | TypeScript |
| **官网** | https://gitmcp.io |

#### 核心功能

- **代码检索**: GitHub 项目代码智能搜索
- **上下文理解**: 代码关系理解
- **防止幻觉**: 确保 AI 生成准确代码

#### 适用场景

- 所有开发场景
- 代码审查
- 跨项目代码引用

---

### 4.2 DevDocs ⭐⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [cyberagiinc/DevDocs](https://github.com/cyberagiinc/DevDocs) |
| **Stars** | 2,037 |
| **语言** | TypeScript |
| **官网** | https://www.cyberagi.ai |

#### 核心功能

- **技术文档聚合**: 统一文档入口
- **私有部署**: 企业级安全
- **多 IDE 支持**: Cursor, Windsurf, Cline, Roo Code, Claude Desktop

---

### 4.3 cc-devops-skills ⭐⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [akin-ozer/cc-devops-skills](https://github.com/akin-ozer/cc-devops-skills) |
| **特点** | 详细的 DevOps 技能集 |

#### 核心功能

- **IaC 代码生成**: Terraform, CloudFormation, Kubernetes
- **多平台支持**: AWS, Azure, GCP
- **验证系统**: 代码质量检查

---

### 4.4 AgentSys ⭐⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [avifenesh/agentsys](https://github.com/avifenesh/agentsys) |
| **特点** | 生产级工作流自动化 |

#### 核心功能

- **任务到生产工作流**: 完整开发管线
- **PR 管理**: 自动化代码审查
- **性能调查**: 性能问题诊断
- **多代理代码审查**: 并行审查

---

### 4.5 Claude Code Agents ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [undeadlist/claude-code-agents](https://github.com/undeadlist/claude-code-agents) |
| **特点** | E2E 开发工作流 |

#### 核心功能

- **多个审计代理并行**: 全面代码审查
- **微检查点协议**: 自动化修复循环
- **浏览器 QA**: 基于浏览器的质量保证
- **严格协议**: 防止 AI 失控

---

### 4.6 Ralph for Claude Code ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [frankbria/ralph-claude-code](https://github.com/frankbria/ralph-claude-code) |
| **特点** | 自主 AI 开发框架 |

#### 核心功能

- **智能退出检测**: 自动判断任务完成
- **速率限制**: 防止 API 滥用
- **断路器模式**: 避免无限循环
- **安全护栏**: 保护系统资源
- **tmux 集成**: 实时监控
- **75+ 测试**: 全面测试覆盖

---

### 4.7 Superpowers ⭐⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [obra/superpowers](https://github.com/obra/superpowers) |
| **作者** | Jesse Vincent |
| **特点** | 核心工程技能集 |

#### 核心功能

- **SDLC 全覆盖**: 规划、审查、测试、调试
- **最佳实践**: 工程实践精华
- **良好组织**: 易于使用和扩展

---

### 4.8 Trail of Bits Security Skills

| 项目 | 说明 |
|-----|------|
| **GitHub** | [trailofbits/skills](https://github.com/trailofbits/skills) |
| **特点** | 专业安全技能集 |

#### 核心功能

- **CodeQL 集成**: 静态分析
- **Semgrep 集成**: 代码安全扫描
- **漏洞检测**: OWASP Top 10
- **修复验证**: 自动验证修复

---

### 4.9 Claude Code Pro

| 项目 | 说明 |
|-----|------|
| **GitHub** | [maxritter/claude-codepro](https://github.com/maxritter/claude-codepro) |
| **特点** | TDD 强制执行 |

#### 核心功能

- **规范驱动开发**: Spec-first 工作流
- **TDD 强制**: 测试优先开发
- **质量挂钩**: 代码质量控制

---

### 4.10 Antigravity Awesome Skills ⭐⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [sickn33/antigravity-awesome-skills](https://github.com/sickn33/antigravity-awesome-skills) |
| **Stars** | 900+ 技能 |
| **特点** | 跨 AI 助手通用 |

#### 核心功能

- **970+ 技能**: 覆盖所有开发领域
- **多 AI 助手**: Claude Code, Gemini CLI, Codex, Cursor, Antigravity
- **官方集成**: Anthropic, OpenAI, Google, Microsoft, Supabase, Vercel

#### 安装

```bash
# Claude Code
npx antigravity-awesome-skills --claude

# 或手动安装
git clone https://github.com/sickn33/antigravity-awesome-skills.git .claude/skills
```

---

### 4.11 cc-tools (Go 实现) ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [Veraticus/cc-tools](https://github.com/Veraticus/cc-tools) |
| **语言** | Go |

#### 核心功能

- **高性能**: Go 语言实现
- **智能 linting**: 代码质量检查
- **测试支持**: 集成测试工具
- **状态行生成**: 最小开销

---

### 4.12 Learn Claude Code ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [shareAI-lab/learn-claude-code](https://github.com/shareAI-lab/learn-claude-code) |
| **语言** | Python |
| **特点** | AI 编码代理设计学习资源 |

#### 核心功能

- **代理设计分析**: 深入理解 AI 代理原理
- **最小化实现**: 仅用几百行 Python 构建
- **完整组件**: Skills、子代理、待办列表

---

### 4.13 开发者工具汇总

| 技能 | Star | 特点 |
|------|------|------|
| **Antigravity Awesome Skills** | 900+ | 最大技能库 |
| **GitMCP** | ⭐7,691 | 防止代码幻觉 |
| **DevDocs** | ⭐2,037 | 文档聚合 |
| **cc-devops-skills** | - | DevOps 工具链 |
| **AgentSys** | - | 工作流自动化 |
| **Claude Code Agents** | - | E2E 开发 |
| **Superpowers** | - | 核心工程技能 |
| **cc-tools** | - | Go 高性能工具 |

---

## 5. 热门技能推荐汇总

### 5.1 游戏客户端开发推荐

| 排名 | 技能 | Star | 特点 |
|------|------|------|------|
| 1 | Claude-Code-Game-Studios | ⭐26 | 48代理全栈覆盖 |
| 2 | lazy-bird | ⭐210 | Godot + 自动化 |
| 3 | unity-ai-workflow | ⭐4 | Unity 6.2+ |
| 4 | Network Chronicles | - | AI 游戏角色 |

### 5.2 Python 开发推荐

| 排名 | 技能 | Star | 特点 |
|------|------|------|------|
| 1 | Serena | ⭐20,941 | 语义代码检索 |
| 2 | PAL MCP Server | ⭐11,180 | 多模型协作 |
| 3 | claude-arsenal | ⭐9 | 39+技能 |
| 4 | koder | ⭐80 | 智能编程助手 |
| 5 | uv | - | 极速包管理 |

### 5.3 游戏客户端自动化测试推荐

| 排名 | 技能 | Star | 特点 |
|------|------|------|------|
| 1 | playwright-skill | ⭐1,844 | 模型调用式E2E |
| 2 | claude-code-playwright-mcp-test | ⭐164 | YAML驱动 |
| 3 | playwright-bot-bypass | ⭐127 | 反检测绕过 |
| 4 | Unity Test Framework | - | 单元/集成测试 |
| 5 | Cursor Tools (Stagehand) | - | 浏览器自动化 |

### 5.4 通用开发者工具推荐

| 排名 | 技能 | Star | 特点 |
|------|------|------|------|
| 1 | Antigravity Awesome Skills | 900+ | 最大技能库 |
| 2 | GitMCP | ⭐7,691 | 防止代码幻觉 |
| 3 | DevDocs | ⭐2,037 | 文档聚合 |
| 4 | cc-devops-skills | - | DevOps 工具链 |
| 5 | AgentSys | - | 工作流自动化 |
| 6 | Superpowers | - | 核心工程技能 |

### 5.5 技能选择决策树

```
游戏客户端开发?
├─ Unity → Claude-Code-Game-Studios
├─ Godot → lazy-bird
├─ Web/H5 → playwright-skill
└─ AI角色 → Network Chronicles

Python 开发?
├─ 代码检索 → Serena
├─ 多模型 → PAL MCP Server
├─ 快速开发 → koder
├─ 包管理 → uv
└─ 全栈 → claude-arsenal

自动化测试?
├─ 浏览器 → playwright-skill
├─ 游戏客户端 → Unity Test Framework
├─ 移动端 → ADB/uiautomator
├─ YAML驱动 → claude-code-playwright-mcp-test
└─ TDD → /tdd-implement

开发者效率?
├─ 全栈 → Antigravity Skills
├─ DevOps → cc-devops-skills
├─ 安全 → trailofbits-skills
├─ 质量 → claude-codepro
└─ 工作流 → AgentSys
```

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
git clone https://github.com/用户名/技能名.git

# 复制到 Claude Code 技能目录
cp -r 技能名 ~/.claude/skills/
```

---

## 趋势分析 (2026年3月)

### 技术方向趋势

| 方向 | 趋势 | 说明 |
|------|------|------|
| **Agent工作流** | ⬆️ 上升 | AgentSys, Claude Code Flow, Ralph |
| **安全审计** | ⬆️ 上升 | Trail of Bits, parry, Dippy |
| **游戏开发** | ⬆️ 上升 | Claude-Code-Game-Studios 全栈覆盖 |
| **多模型协作** | ⬆️ 上升 | PAL MCP, Serena 主导 |
| **技能聚合** | ⬆️ 上升 | Antigravity 900+ 技能 |
| **Python 工具链** | ⬆️ 上升 | uv 主导性能优化 |

### 技术栈分布

```
编程语言:
├── TypeScript: 35+ 技能
├── Python: 25+ 技能
├── Go: 5+ 技能
└── PHP: 2+ 技能

测试框架:
├── Playwright: 主导 Web 测试
├── Unity Test Framework: 游戏
├── pytest: Python
└── Vitest: 前端
```

---

## 📎 相关资源

- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
- [awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills)
- [Antigravity Awesome Skills](https://github.com/sickn33/antigravity-awesome-skills)
- [Claude Code Handbook](https://nikiforovall.blog/claude-code-rules/)
- [Claude Code Ultimate Guide](https://github.com/FlorianBruniaux/claude-code-ultimate-guide)

---

*持续更新中，欢迎提交 PR 补充更多技能*

*文档版本: v21 (2026-03-04)*
