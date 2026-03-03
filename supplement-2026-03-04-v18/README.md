# Claude Code 热门插件调研 (2026-03-04 第十八期)

> 持续跟踪 Claude Code 生态热门插件，聚焦游戏客户端开发、Python 开发、自动化测试、开发者工具方向

---

## 📋 文档信息

- **调研日期**: 2026-03-04
- **分类**: 游戏客户端开发 / Python 开发 / 自动化测试 / 开发者工具
- **状态**: ✅ 补充调研第十八期
- **数据来源**: GitHub Topics + awesome-claude-code + Antigravity Skills

---

## 一、生态概览

### 1.1 统计数据

根据 GitHub Topics 数据，Claude Code 相关仓库已突破 **8,517** 个，持续快速增长：

| 类别 | 仓库数量 | 热门项目 |
|------|---------|---------|
| **AI 工作室** | 500+ | CherryStudio (8.5k+ stars), ruflo |
| **开发工具** | 1000+ | awesome-claude-code, Claude Code Templates |
| **游戏开发** | 200+ | Claude-Code-Game-Studios, Unity-MCP |
| **自动化测试** | 300+ | playwright-skill, fieldwork |
| **Agent编排** | 400+ | agentsys, ruflo, sudocode |
| **Skills** | 970+ | antigravity-awesome-skills |

### 1.2 最新热门项目 (2026年3月)

| 项目 | Star | 特点 |
|------|------|------|
| **CherryStudio** | ⭐ 8.5k+ | AI生产力工作室，300+助手 |
| **Unity-MCP** | ⭐ 1.2k+ | Unity Editor MCP 集成，50+工具 |
| **antigravity-awesome-skills** | ⭐ 970+ | 970+通用技能集合 |
| **awesome-claude-code** | ⭐ 7.1k+ | 精选技能列表 |
| **playwright-skill** | ⭐ 1.8k+ | Playwright浏览器自动化 |
| **claude-mem** | ⭐ 600+ | 会话记忆自动捕获 |
| **ruflo** | ⭐ 500+ | Agent编排平台 |
| **everything-claude-code** | ⭐ 活跃 | Agent性能优化系统 |

---

## 二、游戏客户端开发技能

### 2.1 Claude Code Game Studios ⭐⭐⭐⭐⭐ 强烈推荐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [Donchitos/Claude-Code-Game-Studios](https://github.com/Donchitos/Claude-Code-Game-Studios) |
| **Star** | ⭐ 26 |
| **更新** | 3天前 |
| **特点** | 48个AI代理 + 36个工作流技能 + 完整协调系统 |

#### 核心能力

- **48个专业AI代理**: 覆盖游戏开发全流程
- **36个工作流技能**: 完整游戏开发管线
- **工作室协调系统**: 模拟真实游戏工作室工作流
- **多引擎支持**: Unity, Unreal, Godot, WebGL

#### 工作室层级结构

```
Tier 1 — Directors (Opus)
├── creative-director    # 创意总监
├── technical-director   # 技术总监
└── producer            # 制作人

Tier 2 — Department Leads (Sonnet)
├── game-designer       # 游戏设计师
├── lead-programmer     # 主程序员
├── art-director        # 美术总监
├── audio-director      # 音频总监
├── narrative-director  # 叙事总监
├── qa-lead            # QA主管
├── release-manager    # 发布经理
└── localization-lead  # 本地化主管

Tier 3 — Specialists (Sonnet/Haiku)
├── gameplay-programmer  # 玩法程序员
├── engine-programmer    # 引擎程序员
├── ai-programmer        # AI程序员
├── network-programmer   # 网络程序员
├── ui-programmer        # UI程序员
├── systems-designer     # 系统设计师
├── level-designer       # 关卡设计师
└── ... (共48个专业代理)
```

#### Slash Commands (36个)

| 分类 | 命令 |
|------|------|
| **评审分析** | /design-review, /code-review, /balance-check, /asset-audit, /scope-check, /perf-profile, /tech-debt |
| **生产管理** | /sprint-plan, /milestone-review, /estimate, /retrospective, /bug-report |
| **项目管理** | /start, /project-stage-detect, /reverse-document, /gate-check, /design-systems |
| **发布** | /release-checklist, /launch-checklist, /changelog, /patch-notes, /hotfix |
| **创意** | /brainstorm, /playtest-report, /prototype, /onboard, /localize |
| **团队协调** | /team-combat, /team-narrative, /team-ui, /team-release, /team-polish, /team-audio, /team-level |

#### 引擎支持

| 引擎 | 主管代理 | 子专家 |
|------|---------|--------|
| **Godot 4** | godot-specialist | GDScript, Shaders, GDExtension |
| **Unity** | unity-specialist | DOTS/ECS, Shaders/VFX, Addressables, UI Toolkit |
| **Unreal 5** | unreal-specialist | GAS, Blueprints, Replication, UMG/CommonUI |

### 2.2 Unity-MCP ⭐⭐⭐⭐⭐ 强烈推荐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [IvanMurzak/Unity-MCP](https://github.com/IvanMurzak/Unity-MCP) |
| **Star** | ⭐ 1.2k+ |
| **更新** | 11小时前 |
| **特点** | Unity Editor MCP 集成，50+工具，支持运行时AI |

#### 核心能力

- **AI 集成**: 支持 Claude, Cursor, Windsurf 等多种 AI 工具
- **50+ MCP 工具**: 完整覆盖 Unity 开发流程
- **运行时支持**: 可在编译后的游戏中使用 LLM
- **自动生成 Skills**: 每个 MCP 工具自动生成对应技能
- **灵活部署**: 支持 stdio 和 HTTP 远程部署

#### 内置 MCP 工具分类

| 分类 | 工具数量 | 示例 |
|------|---------|------|
| **Project & Assets** | 18+ | assets-copy, assets-find, assets-prefab-create, package-add |
| **Scene & Hierarchy** | 16+ | gameobject-create, gameobject-modify, scene-open, screenshot-game-view |
| **Scripting & Editor** | 10+ | script-execute, tests-run, console-get-logs, reflection-method-call |

#### 关键工具示例

```bash
# 资产管理
assets-find        # 搜索资产数据库
assets-modify      # 修改资产文件
assets-prefab-create # 创建预制体

# 场景管理
gameobject-create  # 创建游戏对象
gameobject-modify  # 修改游戏对象
scene-open         # 打开场景
scene-save         # 保存场景

# 脚本执行
script-execute     # 动态执行C#代码
script-read        # 读取脚本内容
tests-run          # 运行Unity测试

# 调试
console-get-logs   # 获取Unity日志
screenshot-game-view # 游戏视图截图
```

#### 扩展包

- **Animation**: [Unity-AI-Animation](https://github.com/IvanMurzak/Unity-AI-Animation/)
- **ParticleSystem**: [Unity-AI-ParticleSystem](https://github.com/IvanMurzak/Unity-AI-ParticleSystem/)
- **ProBuilder**: [Unity-AI-ProBuilder](https://github.com/IvanMurzak/Unity-AI-ProBuilder/)

### 2.3 Unity AI Workflow

| 项目 | 说明 |
|-----|------|
| **GitHub** | [David-GD13/unity-ai-workflow](https://github.com/David-GD13/unity-ai-workflow) |
| **Star** | ⭐ 4 |
| **特点** | Unity 6.2+ AI-first 开发工作流 |

#### Dev Modes

| 模式 | 角色 | 适用场景 |
|------|------|---------|
| Assistant | 你构建，AI 辅助文档和解释 | 学习、创意控制 |
| Mix (默认) | 协作模式，AI 建议，你确认 | 大多数项目 |
| Automatic | AI 构建，短的 onboarding Q&A | 快速原型、Game Jam |

#### 核心哲学

- **Game Feel 不是可选的**: 每项功能完整构建
- **TCREI Prompting**: Task-Context-References-Evaluate-Iterate 方法论
- **验证系统**: [VERIFIED]/[SYNTHESIZED]/[UNVERIFIED] 标记

### 2.4 其他游戏开发技能

| 方向 | GitHub | Star | 特点 |
|-----|--------|------|------|
| **OH-Unity-GameDev-Skills** | OstrichHermit/OH-Unity-GameDev-Skills | ⭐6 | Unity基础+DoTween+MediaPipe |
| **claude-code-game-development** | HermeticOrmus/claude-code-game-development | ⭐2 | 游戏开发模式和工作流 |
| **claude-resources (Godot)** | kwhitejr/claude-resources | ⭐3 | Godot 游戏开发 |
| **LibreGameDev-Claude-Code** | HermeticOrmus/LibreGameDev-Claude-Code | ⭐1 | 20个Godot/Unity/Unreal插件 |
| **claude-code-plugins (C++)** | hiddenpeopleclub/claude-code-plugins | ⭐0 | C++游戏开发插件 |

---

## 三、Python 开发技能

### 3.1 数据库集成

| 技能 | GitHub | 功能 | 安全性 |
|-----|--------|------|--------|
| **read-only-postgres** | jawwadfirdousi/agent-skills | PostgreSQL只读查询 | ⭐⭐⭐⭐⭐ |
| **postgres** | sanjay3290/ai-skills | PostgreSQL完整集成 | ⭐⭐⭐ |

#### read-only-postgres 特性

```sql
-- 支持的查询类型
SELECT * FROM users WHERE id = 1;
SHOW max_connections;
EXPLAIN ANALYZE SELECT * FROM orders;
WITH recent AS (...) SELECT * FROM recent;
```

**安全措施:**
- 只读查询 (SELECT/SHOW/EXPLAIN/WITH)
- 超时控制
- 行数限制
- 多连接支持

### 3.2 AI 框架集成

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **pydantic-ai-skills** | DougTrajano/pydantic-ai-skills | ⭐136 | Pydantic AI 深度集成 |
| **langgraph-agent-skill** | SpillwaveSolutions/mastering-langgraph-agent-skill | - | LangGraph 状态机工作流 |

### 3.3 Python 包管理 - uv

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

# 或使用 uv run
uv run python main.py
```

### 3.4 开发者工具包

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **developer-kit** | giuseppe-trisciuoglio/developer-kit | ⭐128 | 模块化插件系统 |
| **claudekit** | carlrannaberg/claudekit | - | CLI工具包，20+子代理 |
| **lazy-bird** | yusufkaraaslan/lazy-bird | ⭐210 | 通用开发自动化，15+框架 |
| **claude-arsenal** | majiayu000/claude-arsenal | ⭐9 | 39+技能，9专业代理 |

### 3.5 云服务集成

| 技能 | GitHub | 功能 |
|-----|--------|------|
| **aws-mcp-server** | alexei-led/aws-mcp-server | AWS CLI 集成 |

**支持服务:**
- 计算: EC2, Lambda, ECS, EKS
- 存储: S3, EBS, EFS
- 数据库: RDS, DynamoDB, ElastiCache
- 网络: VPC, CloudFront, Route53

### 3.6 MCP Server 构建

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **fastmcp-builder** | husniadil/fastmcp-builder | ⭐5 | FastMCP MCP服务器构建 |
| **mcp-wireshark** | khuynh22/mcp-wireshark | ⭐23 | Wireshark/tshark集成 |

### 3.7 Python Skills 汇总

| Skill 名称 | 核心能力 | 适用场景 |
|-----------|---------|---------|
| python-pro | Python 3.12+ 全栈 | 通用开发 |
| python-patterns | 开发原则和决策 | 架构设计 |
| python-fastapi-development | FastAPI 后端 | API 服务 |
| python-testing-patterns | pytest/测试策略 | 质量保证 |
| async-python-patterns | asyncio 异步编程 | 高并发 |
| temporal-python-pro | Temporal 工作流 | 分布式事务 |

---

## 四、自动化测试技能

### 4.1 浏览器自动化

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **playwright-skill** | lackeyjb/playwright-skill | ⭐1.8k | Playwright浏览器自动化 |
| **playwright-bot-bypass** | greekr4/playwright-bot-bypass | ⭐127 | 绕过Google CAPTCHA等 |
| **playwright-undetected-skill** | dalbit-mir/playwright-undetected-skill | ⭐4 | Bot检测绕过 |
| **claude-code-playwright-mcp-test** | terryso/claude-code-playwright-mcp-test | ⭐164 | YAML-based Playwright MCP |
| **ubrowser** | Lulzx/ubrowser | ⭐12 | 最快最便宜的浏览器自动化 |

#### Playwright 核心功能

- **Web 应用测试**: 自动化测试 Web 应用功能
- **UI 验证**: 验证前端功能和行为
- **截图捕获**: 自动截图记录测试状态
- **调试支持**: 辅助调试 UI 行为
- **反检测**: Patchright 支持绕过 Bot 检测

### 4.2 视觉测试

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **claude-code-frontend-dev** | hemangjoshi37a/claude-code-frontend-dev | ⭐12 | 多模态AI视觉测试，10x更快前端开发 |

**核心特点:**
- AI 能"看见"你的 UI
- 视觉回归测试
- 前端开发自动化

### 4.3 游戏客户端测试方案

| 测试类型 | 方案 | 适用场景 |
|---------|------|---------|
| **Web/H5游戏** | Playwright | 功能测试、回归测试 |
| **Unity游戏** | Unity Test Framework | 单元测试、集成测试 |
| **Unity MCP** | tests-run 工具 | AI驱动测试执行 |
| **性能测试** | Unity Profiler | 帧率、内存测试 |
| **Android游戏** | ADB + uiautomator | UI自动化 |
| **iOS游戏** | ios-simulator-skill | 模拟器测试 |

### 4.4 Unity Test Framework

| 测试类型 | 说明 | 适用场景 |
|---------|------|---------|
| **EditMode** | 编辑器环境测试 | 工具类、辅助功能 |
| **PlayMode** | 运行时测试 | 游戏逻辑、UI |
| **Performance** | 性能测试 | 性能优化 |

**Unity-MCP tests-run 工具:**
```bash
# 通过 AI 运行测试
tests-run --mode EditMode
tests-run --mode PlayMode --filter "MyTestClass"
```

### 4.5 移动端测试

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
| **平台** | macOS |

### 4.6 测试质量工具

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **claude-skills-marketplace** | mhattingpete/claude-skills-marketplace | ⭐427 | 测试/代码审查 |
| **fieldwork-skills** | buildoak/fieldwork-skills | ⭐12 | E2E测试/Bug修复 |
| **code-quality-guardian** | terry80s/code-quality-guardian | ⭐2 | 代码质量分析 |

### 4.7 TDD 开发技能

| 命令 | 来源 | 功能 |
|-----|------|------|
| **/tdd** | zscott/pane | TDD开发流程 |
| **/tdd-implement** | jerseycheese/Narraitor | TDD实现 |
| **/repro-issue** | rzykov/metabase | 可复现测试用例 |

#### TDD 开发流程

```
红色 (Red)     → 编写失败的测试
       ↓
绿色 (Green)   → 实现最小代码通过测试
       ↓
重构 (Refactor)→ 重构代码保持测试通过
```

---

## 五、开发者工具技能

### 5.1 编排工具

| 技能 | GitHub | 特点 |
|-----|--------|------|
| **agentsys** | avifenesh/agentsys | 生产级工作流自动化 |
| **superpowers** | obra/superpowers | 核心工程技能集 |
| **claude-code-agents** | undeadlist/claude-code-agents | E2E开发工作流 |
| **sudocode** | sudocode-ai/sudocode | 轻量级编排工具 |
| **ruflo** | ruvnet/ruflo | Agent编排平台 |

#### AgentSys 核心功能

- 工作流自动化: 任务到生产的完整流程
- PR 管理: 自动管理 Pull Request
- 代码清理: 自动代码清理和维护
- 性能调查: 性能问题调查和优化
- 漂移检测: 检测代码偏离
- 多代理代码审查: 并行多代理审查

### 5.2 安全审计

| 技能 | GitHub | 特点 |
|-----|--------|------|
| **trailofbits-skills** | trailofbits/skills | CodeQL/Semgrep集成 |
| **parry** | vaporif/parry | 提示注入扫描 |
| **Dippy** | ldayton/Dippy | AST智能命令批准 |

#### Trail of Bits 技能分类

| 技能 | 功能 |
|------|------|
| codeql | 静态代码分析 |
| semgrep | 模式匹配分析 |
| variant-analysis | 变体分析 |
| fix-verification | 修复验证 |
| diff-review | 差异代码审查 |

### 5.3 DevOps 工具

| 技能 | GitHub | 特点 |
|-----|--------|------|
| **cc-devops-skills** | akin-ozer/cc-devops-skills | IaC代码生成 |
| **ContextKit** | FlineDev/ContextKit | 4阶段规划方法论 |
| **claude-cli-advanced-starter-pack** | evan043/claude-cli-advanced-starter-pack | 高级CLI工具包 |

### 5.4 Hooks 生态系统

| 技能 | GitHub | 功能 |
|-----|--------|------|
| **claude-hooks** | johnlindquist/claude-hooks | TypeScript Hook |
| **cchooks** | GowayLee/cchooks | Python Hook SDK |
| **claude-hooks-sdk** | beyondcode/claude-hooks-sdk | PHP Hook SDK |

### 5.5 会话管理

| 技能 | GitHub | 功能 |
|-----|--------|------|
| **claude-tmux** | nielsgroen/claude-tmux | tmux会话管理 |
| **claude-esp** | phiat/claude-esp | 隐藏输出流式传输 |
| **ralph-claude-code** | frankbria/ralph-claude-code | 自主开发框架 |

### 5.6 Claude Scientific Skills ⭐⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [K-Dense-AI/claude-scientific-skills](https://github.com/K-Dense-AI/claude-scientific-skills) |
| **特点** | 科研/工程/分析/金融/写作全能技能集 |

#### 核心功能

- **研究技能**: 文献检索、学术写作、研究方法
- **科学计算**: 数据分析、模型构建、实验设计
- **工程分析**: 结构分析、仿真、计算
- **金融分析**: 量化分析、风险评估、投资策略
- **写作技能**: 技术文档、论文撰写、内容创作

---

## 六、Antigravity Awesome Skills (970+ 技能)

### 6.1 项目信息

| 项目 | 说明 |
|-----|------|
| **GitHub** | [sickn33/antigravity-awesome-skills](https://github.com/sickn33/antigravity-awesome-skills) |
| **Star** | ⭐ 970+ |
| **特点** | 970+ 通用技能集合，支持所有主流 AI 编码助手 |

### 6.2 支持的 AI 工具

- 🟣 Claude Code (Anthropic CLI)
- 🔵 Gemini CLI (Google DeepMind)
- 🟢 Codex CLI (OpenAI)
- 🟠 Kiro CLI/IDE (AWS)
- 🔴 Antigravity IDE (Google DeepMind)
- 🩵 GitHub Copilot (VSCode Extension)
- 🟠 Cursor (AI-native IDE)
- ⚪ OpenCode (Open-source CLI)
- 🌸 AdaL CLI (Self-evolving Coding Agent)

### 6.3 技能分类

| Category | Focus | Example skills |
|----------|-------|----------------|
| **Architecture** | 系统设计, ADR, C4, 可扩展模式 | architecture, c4-context, senior-architect |
| **Business** | 增长, 定价, CRO, SEO | copywriting, pricing-strategy, seo-audit |
| **Data & AI** | LLM应用, RAG, 代理, 分析 | rag-engineer, prompt-engineer, langgraph |
| **Development** | 语言精通, 框架模式, 代码质量 | typescript-expert, python-patterns, react-patterns |
| **General** | 规划, 文档, 产品运营 | brainstorming, doc-coauthoring, writing-plans |
| **Infrastructure** | DevOps, 云, 无服务器, CI/CD | docker-expert, aws-serverless, vercel-deployment |
| **Security** | AppSec, 渗透测试, 漏洞分析 | api-security-best-practices, sql-injection-testing |
| **Testing** | TDD, 测试设计, QA工作流 | test-driven-development, testing-patterns |
| **Workflow** | 自动化, 编排, 代理 | workflow-automation, inngest, trigger-dev |

### 6.4 安装方式

```bash
# 默认安装 (Antigravity)
npx antigravity-awesome-skills

# Claude Code
npx antigravity-awesome-skills --claude

# Gemini CLI
npx antigravity-awesome-skills --gemini

# Codex CLI
npx antigravity-awesome-skills --codex

# Cursor
npx antigravity-awesome-skills --cursor

# Kiro
npx antigravity-awesome-skills --kiro

# OpenCode
npx antigravity-awesome-skills --path .agents/skills
```

---

## 七、热门技能推荐

### 7.1 按用途推荐

| 用途 | 首推技能 | 备选 |
|-----|---------|------|
| **游戏开发 (Unity)** | Unity-MCP + Claude-Code-Game-Studios | cc-plugin-unity-gamedev |
| **游戏开发 (通用)** | Claude-Code-Game-Studios | Antigravity game skills |
| **Python 后端** | pydantic-ai-skills | read-only-postgres |
| **Python 测试** | pytest + TDD | playwright-skill |
| **Web/H5游戏测试** | playwright-skill | playwright-undetected |
| **全栈开发** | fullstack-dev-skills (65+) | claude-code-templates |
| **DevOps** | cc-devops-skills | superpowers |
| **代码审查** | agentsys | claude-code-agents |
| **安全审计** | trailofbits-skills | parry |
| **科学研究** | claude-scientific-skills | - |
| **通用技能库** | antigravity-awesome-skills | awesome-claude-code |

### 7.2 技能选择决策树

```
游戏客户端开发?
├─ Unity → Unity-MCP + Claude-Code-Game-Studios
├─ Godot → claude-resources + Claude-Code-Game-Studios
├─ Unreal → Claude-Code-Game-Studios (Unreal agent set)
├─ Web/H5 → playwright-skill
└─ 通用 → Claude-Code-Game-Studios

Python 开发?
├─ Web框架 → pydantic-ai-skills
├─ 数据库 → read-only-postgres
├─ 云服务 → aws-mcp-server
├─ 测试 → pytest + TDD
├─ 包管理 → uv
└─ MCP Server → fastmcp-builder

自动化测试?
├─ 浏览器 → playwright-skill
├─ 视觉测试 → claude-code-frontend-dev
├─ Unity → Unity-MCP tests-run
├─ 移动端 → ios-simulator-skill
├─ 代码质量 → code-quality-guardian
└─ TDD → /tdd-implement

开发者效率?
├─ 全栈 → fullstack-dev-skills
├─ DevOps → cc-devops-skills
├─ 安全 → trailofbits-skills
├─ 编排 → ruflo / agentsys
├─ 通用 → antigravity-awesome-skills
└─ 科学 → claude-scientific-skills
```

### 7.3 技能组合推荐

```
游戏开发组合:
Unity-MCP + Claude-Code-Game-Studios + Unity Test Framework

Python开发组合:
uv + pydantic-ai-skills + read-only-postgres + pytest + aws-mcp-server

测试自动化组合:
playwright-skill + claude-code-frontend-dev + fieldwork-skills

游戏帧同步测试:
Unity Test Framework + Unity-MCP tests-run + 网络延迟模拟

科研工作流:
claude-scientific-skills + langgraph-agent-skill + pydantic-ai-skills

通用开发:
antigravity-awesome-skills + superpowers + agentsys
```

---

## 八、安装指南

### 8.1 Unity-MCP 安装

```bash
# 下载安装包
https://github.com/IvanMurzak/Unity-MCP/releases

# 或使用 OpenUPM
openupm add com.ivanmurzak.unity.mcp

# 配置 Claude Code
# 在 Unity 中打开 Window/AI Game Developer — MCP
# 点击 Configure 自动配置
```

### 8.2 Claude Code Game Studios 安装

```bash
# 克隆模板
git clone https://github.com/Donchitos/Claude-Code-Game-Studios.git my-game
cd my-game

# 启动 Claude Code
claude

# 运行初始化
/start
```

### 8.3 Antigravity Skills 安装

```bash
# Claude Code
npx antigravity-awesome-skills --claude

# 验证
test -d .claude/skills && echo "Skills installed"
```

### 8.4 Playwright Skill 安装

```bash
# 克隆
git clone https://github.com/lackeyjb/playwright-skill.git

# 复制到 Claude Code 技能目录
cp -r playwright-skill ~/.claude/skills/
```

---

## 九、趋势分析

### 9.1 热门方向

| 方向 | 趋势 | 说明 |
|-----|------|------|
| **Unity MCP 集成** | ⬆️ 上升 | Unity-MCP 1.2k+ stars，实时 AI 调试 |
| **Agent工作流** | ⬆️ 上升 | agentsys, claude-code-agents, ruflo |
| **游戏工作室模拟** | ⬆️ 上升 | Claude-Code-Game-Studios 48代理架构 |
| **安全审计** | ⬆️ 上升 | trailofbits-skills, parry, Dippy |
| **测试自动化** | ⬆️ 上升 | Playwright主导，视觉测试兴起 |
| **通用技能库** | ⬆️ 上升 | antigravity-awesome-skills 970+ 技能 |

### 9.2 技术栈分布

```
编程语言:
├── TypeScript: 40+ 技能
├── Python: 30+ 技能
├── C#: Unity-MCP 支持
├── Go: 5+ 技能
└── PHP: 2+ 技能

游戏引擎:
├── Unity: Unity-MCP, Claude-Code-Game-Studios
├── Godot: claude-resources, Game-Studios
├── Unreal: Game-Studios agent set
└── Web: Phaser, Babylon.js, Three.js

测试框架:
├── Playwright: 主导浏览器测试
├── Unity Test Framework: 游戏测试
├── pytest: Python 测试
└── Vitest: 前端测试
```

---

## 📎 相关资源

- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code) - 精选技能列表
- [antigravity-awesome-skills](https://github.com/sickn33/antigravity-awesome-skills) - 970+通用技能
- [Unity-MCP](https://github.com/IvanMurzak/Unity-MCP) - Unity Editor MCP 集成
- [Claude-Code-Game-Studios](https://github.com/Donchitos/Claude-Code-Game-Studios) - 48代理游戏工作室
- [Claude Code Handbook](https://nikiforovall.blog/claude-code-rules/) - 最佳实践
- [Claude Code Ultimate Guide](https://github.com/FlorianBruniaux/claude-code-ultimate-guide) - 完整指南

---

## 📂 补充调研文档

- [补充调研-第十六期](../supplement-2026-03-04-v16/README.md) (2026-03-04 GitHub热门趋势分析)
- [补充调研-第十七期](../supplement-2026-03-04-v17/README.md) (2026-03-04 完整调研更新)

---

*持续更新中，欢迎提交 PR 补充更多技能*
