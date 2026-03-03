# Claude Code 插件调研报告 - 2026年3月 (第二期)

> 持续跟踪 Claude Code 生态热门插件，聚焦游戏开发、Python 开发、自动化测试、开发者工具方向

---

## 📋 调研概要

| 维度 | 统计 |
|-----|------|
| **调研时间** | 2026-03-03 |
| **覆盖方向** | 游戏开发、Python开发、自动化测试、开发者工具 |
| **技能总数** | 120+ |
| **数据来源** | awesome-claude-code, GitHub trending, Antigravity Skills |

---

## 一、游戏客户端开发技能

### 1.1 Unity 开发

| 技能 | GitHub | Star | 特点 |
|-----|--------|------|------|
| **cc-plugin-unity-gamedev** | tjboudreaux/cc-plugin-unity-gamedev | ⭐1 | 21个专业技能，完整覆盖Unity开发栈 |
| **OH-Unity-GameDev-Skills** | OstrichHermit/OH-Unity-GameDev-Skills | ⭐6 | Unity基础开发+DoTween+MediaPipe |
| **unity-ai-workflow** | David-GD13/unity-ai-workflow | ⭐4 | Unity 6.2+ AI-first工作流 |
| **Claude-Code-Skills-For-Unity** | flashwade03/Claude-Code-Skills-For-Unity-Game-Development | - | 知名Unity资产开发 |

**核心技能分类：**
- 工具类：Addressables、MemoryPack、ScriptableObjects、Profiling
- 动画/物理：Animation、Physics、NavMesh、Object Pooling、State Machine
- AI/行为：Behavior Designer、Gameplay Ability System (GAS)
- 音视频：Wwise音频、Cinemachine相机
- UI：UGUI、Mobile Optimization
- 测试：Unity Test Framework
- DI/异步：VContainer、UniTask

### 1.2 Godot 开发

| 技能 | GitHub | Star |
|-----|--------|------|
| **claude-resources** | kwhitejr/claude-resources | ⭐3 |

### 1.2.1 Antigravity 游戏开发技能 (全面覆盖)

| 分类 | 技能目录 | 说明 |
|-----|---------|------|
| **PC/Console Games** | `pc-games` | PC和主机游戏开发原理，引擎选择策略 |
| **Web Games** | `web-games` | H5/Web游戏开发，JavaScript/TypeScript |
| **Mobile Games** | `mobile-games` | 移动端游戏，iOS/Android平台适配 |
| **2D Games** | `2d-games` | 2D游戏开发，精灵动画，Tilemap |
| **3D Games** | `3d-games` | 3D游戏开发，模型，光照，渲染 |
| **Multiplayer** | `multiplayer` | 网络 multiplayer 游戏开发 |
| **VR/AR** | `vr-ar` | 虚拟现实/增强现实游戏 |
| **Game Audio** | `game-audio` | 游戏音频设计，Wwise/FMOD |
| **Game Art** | `game-art` | 游戏美术，材质，动画 |
| **Game Design** | `game-design` | 游戏设计，原型，玩家体验 |

#### Web Games 技能详解 (来自 Antigravity)

| 框架 | 类型 | 最佳场景 |
|------|------|---------|
| **Phaser 4** | 2D | 完整游戏引擎功能 |
| **PixiJS 8** | 2D | 渲染、UI |
| **Three.js** | 3D | 可视化、轻量级 |
| **Babylon.js 7** | 3D | 完整引擎、XR |

#### WebGPU 支持情况 (2025)

| 浏览器 | 支持 |
|--------|------|
| Chrome | ✅ v113+ |
| Edge | ✅ v113+ |
| Firefox | ✅ v131+ |
| Safari | ✅ 18.0+ |
| **全球支持率** | **~73%** |

#### 游戏引擎选择决策树

```
什么类型的游戏?
│
├── 2D 游戏
│   ├── 需要完整引擎功能? → Phaser
│   └── 需要原始渲染能力? → PixiJS
│
├── 3D 游戏
│   ├── 需要完整引擎(物理、XR)? → Babylon.js
│   └── 专注渲染? → Three.js
│
└── 混合/Canvas
    └── 自定义 → 原始 Canvas/WebGL
```

### 引擎选择决策树

```
What are you building?
│
├── 2D Game
│   ├── Open source important? → Godot
│   └── Large team/assets? → Unity
│
├── 3D Game
│   ├── AAA visual quality? → Unreal
│   ├── Cross-platform priority? → Unity
│   └── Indie/open source? → Godot 4
│
└── Specific Needs
    ├── DOTS performance? → Unity
    ├── Nanite/Lumen? → Unreal
    └── Lightweight? → Godot
```

### 1.3 GameMaker Studio

| 技能 | GitHub | Star |
|-----|--------|------|
| **gamemaker-skills** | leihaht/gamemaker-skills | ⭐2 |

### 1.4 其他游戏开发

| 技能 | GitHub | 用途 |
|-----|--------|------|
| **se-dev-skills** | viktor-ferenczi/se-dev-skills | Space Engineers插件开发 |
| **game-opus** | nightbs8/game-opus | 14个游戏开发+3D技能 |

### 1.5 游戏客户端自动化测试方案

#### 1.5.1 Unity 测试

| 技能 | 来源 | 功能 |
|-----|------|------|
| **Unity Test Framework** | cc-plugin-unity-gamedev | 单元测试、集成测试 |
| **Unity Profiling** | Unity Profiler | 性能测试 |

#### 1.5.2 H5/Web 游戏测试

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **playwright-skill** | lackeyjb/playwright-skill | ⭐1.8k | Web游戏自动化测试 |
| **playwright-undetected** | dalbit-mir/playwright-undetected-skill | ⭐4 | Bot检测绕过测试 |

#### 1.5.3 游戏客户端测试类型

| 类型 | 工具 | 适用场景 |
|-----|------|---------|
| **单元测试** | Unity Test Framework, pytest | 游戏逻辑验证 |
| **集成测试** | Playwright, Selenium | 客户端与服务端交互 |
| **UI测试** | Playwright, Appium | 游戏UI交互 |
| **性能测试** | Unity Profiler, RenderDoc | 帧率、内存测试 |
| **回归测试** | CI/CD + Playwright | 版本发布验证 |

---

## 二、Python 开发技能

### 2.1 数据库集成

| 技能 | GitHub | 功能 |
|-----|--------|------|
| **read-only-postgres** | jawwadfirdousi/agent-skills | PostgreSQL只读查询 |
| **postgres** | sanjay3290/ai-skills | PostgreSQL完整集成 |

### 2.2 AI 框架集成

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **pydantic-ai-skills** | DougTrajano/pydantic-ai-skills | ⭐136 | Pydantic AI集成 |

### 2.3 iOS 开发 (Python工具链)

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **ios-simulator-skill** | conorluddy/ios-simulator-skill | ⭐557 | iOS模拟器集成 |

### 2.4 开发者工具包

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **developer-kit** | giuseppe-trisciuoglio/developer-kit | ⭐128 | 模块化插件系统 |
| **claude-code-tools** | pchalasani/claude-code-tools | - | 会话连续性工具 |
| **claudekit** | carlrannaberg/claudekit | - | CLI工具包，20+子代理 |

### 2.5 AWS 云服务

| 技能 | GitHub | 功能 |
|-----|--------|------|
| **aws-mcp-server** | alexei-led/aws-mcp-server | AWS CLI集成 |

### 2.6 Antigravity Python 开发技能

#### Python 项目脚手架 (python-development-python-scaffold)

| 项目 | 说明 |
|-----|------|
| **来源** | Antigravity Skills |
| **功能** | 生产级 Python 项目脚手架生成 |

**支持的项目类型：**

| 类型 | 框架 | 特点 |
|------|------|------|
| **FastAPI** | REST APIs, 微服务 | 异步应用 |
| **Django** | 全栈Web应用 | 管理面板、ORM |
| **Library** | 可复用包 | 工具类 |
| **CLI** | 命令行工具 | 自动化脚本 |
| **Generic** | 标准应用 | 通用项目 |

**现代化工具链：**
- `uv` - 快速包管理
- 类型提示 (Type Hints)
- 测试设置 (pytest)
- 现代配置管理

#### Python 测试模式 (python-testing-patterns)

| 项目 | 说明 |
|-----|------|
| **来源** | Antigravity Skills |
| **功能** | 全面测试策略与最佳实践 |

**核心能力：**

| 能力 | 说明 |
|------|------|
| **pytest** | 单元测试框架 |
| **Fixtures** | 测试数据管理 |
| **Mocking** | 依赖模拟 |
| **参数化** | 测试参数化 |
| **TDD** | 测试驱动开发 |
| **Async测试** | 异步代码测试 |
| **CI/CD集成** | 持续测试集成 |
| **属性测试** | 属性-based 测试 |

#### Python 异步模式 (async-python-patterns)

| 项目 | 说明 |
|-----|------|
| **来源** | Antigravity Skills |
| **功能** | 异步编程模式与最佳实践 |

#### Python 性能优化 (python-performance-optimization)

| 项目 | 说明 |
|-----|------|
| **来源** | Antigravity Skills |
| **功能** | Python 性能分析与优化 |

#### Python Pro 技能

| 技能 | 说明 |
|------|------|
| **python-pro** | 高级 Python 开发模式 |
| **dbos-python** | Python 工作流编排 |
| **temporal-python-pro** | Temporal 工作流 |
| **python-patterns** | 设计模式 |

### 2.7 Python 项目快速启动

```bash
# 使用 uv 初始化项目
uv init <project-name>
cd <project-name>

# 创建虚拟环境
uv venv
source .venv/bin/activate

# 安装依赖
uv add fastapi pytest

# 运行测试
uv run pytest
```

---

## 三、自动化测试技能

### 3.1 浏览器自动化

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **playwright-skill** | lackeyjb/playwright-skill | ⭐1.8k | Playwright浏览器自动化 |
| **playwright-undetected-skill** | dalbit-mir/playwright-undetected-skill | ⭐4 | Bot检测绕过 |

### 3.2 软件工程测试

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **claude-skills-marketplace** | mhattingpete/claude-skills-marketplace | ⭐427 | Git/测试/代码审查 |
| **fieldwork-skills** | buildoak/fieldwork-skills | ⭐12 | 端到端测试/Bug修复 |

### 2.5 AWS 云服务

| 技能 | GitHub | 功能 |
|-----|--------|------|
| **aws-mcp-server** | alexei-led/aws-mcp-server | AWS CLI集成 |

### 2.6 Python 测试框架集成

| 技能 | 来源 | 功能 |
|-----|------|------|
| **pytest** | Python 标准 | 单元测试框架 |
| **Black + mypy** | EDSL 项目 | 代码格式化 + 类型检查 |
| **Vitest** | Giselle 项目 | 前端测试 |

### 2.7 TypeScript/JavaScript 开发

| 技能 | GitHub | 功能 |
|-----|--------|------|
| **TypeScript Quality Hooks** | bartolli/claude-code-typescript-hooks | TypeScript 质量检查 |
| **Inkline CLAUDE.md** | inkline/inkline | Vue 3 + TypeScript 项目 |
| **LangGraphJS** | langchain-ai/langgraphjs | TypeScript monorepo |

---

## 三、自动化测试技能

### 3.1 浏览器自动化

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **playwright-skill** | lackeyjb/playwright-skill | ⭐1.8k | Playwright浏览器自动化 |
| **playwright-undetected-skill** | dalbit-mir/playwright-undetected-skill | ⭐4 | Bot检测绕过 |
| **Cursor Tools** | eastlondoner/cursor-tools | 浏览器自动化 (Stagehand) |

### 3.2 Antigravity 浏览器自动化 (browser-automation)

| 项目 | 说明 |
|-----|------|
| **来源** | Antigravity Skills |
| **功能** | 浏览器自动化专家技能 |
| **核心框架** | Playwright, Puppeteer, Selenium |

#### 核心能力

| 能力 | 说明 |
|------|------|
| **测试隔离** | 每个测试在完全隔离的环境中运行 |
| **用户定位器** | 按用户视角选择元素 |
| **自动等待** | Playwright 自动等待机制 |

#### 常见问题与解决方案

| 问题 | 严重性 | 解决方案 |
|------|--------|---------|
| 手动等待 | 关键 | 移除所有 waitForTimeout |
| 选择器不稳定 | 高 | 使用用户定位器 |
| 检测拦截 | 高 | 使用 stealth 插件 |
| 状态污染 | 高 | 每个测试完全隔离 |

### 3.3 E2E 测试 (e2e-testing)

| 项目 | 说明 |
|-----|------|
| **来源** | Antigravity Skills |
| **功能** | 端到端测试工作流 |
| **框架** | Playwright |

#### 测试阶段

| 阶段 | 技能 | 关键活动 |
|------|------|---------|
| **Phase 1** | playwright-skill | Playwright 安装、配置 |
| **Phase 2** | e2e-testing-patterns | 测试策略设计 |
| **Phase 3** | playwright-skill | 测试脚本编写 |

### 3.4 测试自动化 (test-automator)

| 项目 | 说明 |
|-----|------|
| **来源** | Antigravity Skills |
| **功能** | AI 驱动的测试自动化 |

#### 核心能力

| 能力 | 说明 |
|------|------|
| **TDD 卓越** | 红-绿-重构循环自动化 |
| **AI 测试框架** | Self-healing 测试 |
| **现代框架** | Playwright, Appium, K6 |
| **CI/CD 集成** | Jenkins, GitLab CI, GitHub Actions |

### 3.5 软件工程测试

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **claude-skills-marketplace** | mhattingpete/claude-skills-marketplace | ⭐427 | Git/测试/代码审查 |
| **fieldwork-skills** | buildoak/fieldwork-skills | ⭐12 | 端到端测试/Bug修复 |
| **cc-tools** | Veraticus/cc-tools | Go 实现的质量工具 |

### 3.3 测试命令 (Slash Commands)

| 命令 | 来源 | 功能 |
|-----|------|------|
| **/tdd** | zscott/pane | TDD开发流程 |
| **/tdd-implement** | jerseycheese/Narraitor | TDD实现 |
| **/repro-issue** | rzykov/metabase | 可复现测试用例 |
| **/check** | rygwdn/slack-tools | 代码质量检查 |
| **/clean** | Graphlet-AI/eridu | 代码格式化 |
| **/fix-issue** | metabase/metabase | GitHub Issue 修复 |
| **/fix-github-issue** | jeremymailen/kotlinter-gradle | Gradle 项目 Issue 修复 |
| **/code_analysis** | kingler/n8n_agent | 高级代码分析 |
| **/optimize** | to4iki/ai-project-rules | 性能优化建议 |
| **/run-ci** | hackdays-io/toban-contribution-viewer | CI 检查运行 |

### 3.4 Claude Code Pro 测试功能

| 技能 | GitHub | 特点 |
|-----|--------|------|
| **Claude CodePro** | maxritter/claude-codepro | TDD 强制执行，质量挂钩 |

---

## 四、开发者工具技能

### 4.1 模板与资源

| 技能 | GitHub | 特点 |
|-----|--------|------|
| **claude-code-templates** | davila7/claude-code-templates | 超全面资源集合 |
| **claude-codex-settings** | fcakyon/claude-codex-settings | 云平台集成 |

### 4.2 全栈开发

| 技能 | GitHub | 技能数量 |
|-----|--------|---------|
| **fullstack-dev-skills** | jeffallan/claude-skills | 65+专业化技能 |

### 4.3 DevOps

| 技能 | GitHub | 特点 |
|-----|--------|------|
| **cc-devops-skills** | akin-ozer/cc-devops-skills | IaC代码生成 |

### 4.3.1 Antigravity DevOps 技能

| 技能目录 | 说明 |
|---------|------|
| **docker-expert** | Docker 专家技能 |
| **cloud-devops** | 云端 DevOps |
| **git-advanced-workflows** | 高级 Git 工作流 |
| **github-actions-templates** | GitHub Actions 模板 |
| **github-automation** | GitHub 自动化 |
| **gitlab-automation** | GitLab 自动化 |
| **terraform-aws-modules** | AWS Terraform 模块 |
| **k8s-manifest-generator** | Kubernetes Manifest 生成 |

### 4.4 工作流系统

| 技能 | GitHub | 特点 |
|-----|--------|------|
| **agentsys** | avifenesh/agentsys | 生产级工作流自动化 |
| **superpowers** | obra/superpowers | 核心工程技能集 |
| **claude-code-agents** | undeadlist/claude-code-agents | E2E开发工作流 |

### 4.5 Claude Code Pro

| 技能 | GitHub | 特点 |
|-----|--------|------|
| **claude-codepro** | maxritter/claude-codepro | 专业开发环境 |

### 4.6 安全审计

| 技能 | GitHub | 特点 |
|-----|--------|------|
| **trailofbits-skills** | trailofbits/skills | CodeQL/Semgrep集成 |

### 4.7 MCP 服务器

| 技能 | GitHub | 功能 |
|-----|--------|------|
| **stt-mcp-server-linux** | marcindulak/stt-mcp-server-linux | 语音转文字 |
| **Codex Skill** | klaudworks/skill-codex | Codex CLI集成 |
| **aws-mcp-server** | alexei-led/aws-mcp-server | AWS 服务集成 |

### 4.8 代码质量与安全

| 技能 | GitHub | 特点 |
|-----|--------|------|
| **Trail of Bits Skills** | trailofbits/skills | CodeQL/Semgrep 安全审计 |
| **parry** | vaporif/parry | 提示注入扫描器 |
| **Dippy** | ldayton/Dippy | AST 自动批准安全命令 |
| **TDD Guard** | nizos/tdd-guard | TDD 原则监控 Hook |

### 4.9 Hooks 生态系统

| 技能 | GitHub | 功能 |
|-----|--------|------|
| **claude-hooks** | johnlindquist/claude-hooks | TypeScript Hook 系统 |
| **cchooks** | GowayLee/cchooks | Python Hook SDK |
| **claude-code-hooks-sdk** | beyondcode/claude-hooks-sdk | PHP Hook SDK |
| **Britfix** | Taleisin/britfix | 英式英语转换 |
| **CC Notify** | dazhuiba/CCNotify | 桌面通知 |

---

## 五、热门技能推荐

### 5.1 按用途推荐

| 用途 | 首推技能 | 备选 |
|-----|---------|------|
| **游戏开发 (Unity)** | cc-plugin-unity-gamedev | OH-Unity-GameDev-Skills |
| **游戏开发 (通用)** | Antigravity pc-games/mobile-games | game-opus |
| **Python 后端** | pydantic-ai-skills | read-only-postgres |
| **Python 测试** | EDSL (Black + mypy) | pytest |
| **Web/H5游戏测试** | playwright-skill | playwright-undetected |
| **全栈开发** | fullstack-dev-skills (65+) | claude-code-templates |
| **DevOps** | cc-devops-skills | superpowers |
| **代码审查** | agentsys | claude-code-agents |
| **安全审计** | trailofbits-skills | parry |
| **质量保证** | Claude CodePro | TypeScript Quality Hooks |

### 5.2 技能选择决策树

```
游戏客户端开发?
├─ Unity → cc-plugin-unity-gamedev
├─ Godot → claude-resources
├─ GameMaker → gamemaker-skills
├─ Web/H5 → playwright-skill
└─ 通用 → Antigravity Skills (pc/mobile/web/2d/3d)

Python 开发?
├─ Web框架 → pydantic-ai-skills
├─ 数据库 → read-only-postgres
├─ 云服务 → aws-mcp-server
└─ 测试 → Black + mypy

自动化测试?
├─ 浏览器 → playwright-skill
├─ 单元测试 → Unity Test Framework
├─ 代码质量 → /check, /clean
└─ TDD → /tdd-implement

开发者效率?
├─ 全栈 → fullstack-dev-skills
├─ DevOps → cc-devops-skills
├─ 安全 → trailofbits-skills
└─ 专业 → claude-codepro
```

---

## 六、安装指南

### 6.1 快速安装

```bash
# 克隆技能仓库
git clone https://github.com/用户名/技能名.git

# 复制到 Claude Code 技能目录
cp -r 技能名 ~/.claude/skills/

# 或使用技能安装命令
claude --install-skill gh-用户名-技能名
```

### 6.2 验证安装

```bash
# 列出已安装技能
claude --list-skills

# 或在 Claude Code 中输入
/skill list
```

---

## 七、趋势分析

### 7.1 热门方向

| 方向 | 趋势 | 说明 |
|-----|------|------|
| **Agent工作流** | ⬆️ 上升 | agentsys, claude-code-agents, Claude Code Flow |
| **安全审计** | ⬆️ 上升 | trailofbits-skills, parry, Dippy |
| **多云集成** | ➡️ 稳定 | AWS/Azure/GCP MCP |
| **游戏开发** | ⬆️ 上升 | Antigravity Skills 全覆盖 |
| **测试自动化** | ⬆️ 上升 | Playwright主导，TDD命令丰富 |
| **Hook 生态** | ⬆️ 上升 | 多语言 SDK (Python, PHP, TypeScript) |
| **上下文工程** | ⬆️ 上升 | Context Engineering Kit |

### 7.2 值得关注的新兴技能

| 技能 | 方向 | 特点 |
|-----|------|------|
| **Claude Scientific Skills** | 科研 | MIT许可，2026年3月新增 |
| **Context Engineering Kit** | 工程 | 最小token占用 |
| **Everything Claude Code** | 全栈 | 全面资源库 |
| **Book Factory** | 出版 | 自动化出版工作流 |
| **parry** | 安全 | 提示注入扫描器 |
| **Dippy** | 安全 | AST自动批准安全命令 |
| **Ralph Wiggum** | 开发方法 | 自主循环开发框架 |
| **ContextKit** | 开发框架 | 4阶段规划方法论 |

### 7.3 技术栈分布

```
编程语言:
├── TypeScript: 35+ 技能
├── Python: 25+ 技能
├── Go: 5+ 技能 (cc-tools, ccexp)
└── PHP: 2+ 技能 (claude-hooks-sdk)

测试框架:
├── Playwright: 主导
├── Unity Test Framework: 游戏
├── pytest: Python
└── Vitest: 前端

云服务:
├── AWS: aws-mcp-server
├── Azure: claude-codex-settings
└── GCP: 集成中
```

---

## 八、2026年3月新增插件

### 8.1 最新热门技能

| 技能 | GitHub | Star | 特点 |
|-----|--------|------|------|
| **Claude Scientific Skills** | K-Dense-AI/claude-scientific-skills | ⭐活跃 | 科研/工程/分析/金融/写作技能集 |
| **parry** | vaporif/parry | 新兴 | 提示注入扫描器，检测安全威胁 |
| **Dippy** | ldayton/Dippy | 新兴 | AST自动批准安全命令 |
| **Claude Code Flow** | ruvnet/claude-code-flow | ⭐活跃 | 代码优先编排层 |
| **Claude Swarm** | parruda/claude-swarm | 新兴 | 多代理协同工作 |
| **Everything Claude Code** | affaan-m/everything-claude-code | ⭐活跃 | Agent性能优化系统 |
| **Get Shit Done (GSD)** | gsd-build/get-shit-done | 新兴 | 轻量级元提示系统 |
| **claude-mem** | thedotmack/claude-mem | 新兴 | 自动捕获会话上下文 |
| **agents** | wshobson/agents | 新兴 | 多代理编排 |

### 8.2 生产力工具

| 技能 | GitHub | 功能 |
|-----|--------|------|
| **Claude Session Restore** | ZENG3LD/claude-session-restore | 跨会话上下文恢复 |
| **cc-switch** | farion1231/cc-switch | 跨平台桌面助手 |
| **Serena** | oraios/serena | 语义检索和编辑工具包 |
| **Ruflo** | ruvnet/ruflo | 企业级代理编排平台 |
| **Beads** | steveyegge/beads | 记忆升级工具 |
| **recall** | zippoxer/recall | 全文搜索会话历史 |
| **claude-tmux** | nielsgroen/claude-tmux | tmux会话管理 |
| **claude-esp** | phiat/claude-esp | 隐藏输出流式传输到独立终端 |
| **VoiceMode MCP** | mbailey/voicemode | 语音交互支持 |

### 8.3 客户端/IDE 工具

| 技能 | GitHub | 功能 | 特点 |
|-----|--------|------|------|
| **Cherry Studio** | CherryHQ/cherry-studio | AI 生产力工作室 | 300+ 助手，统一访问前沿 LLM |
| **OpenCode** | code-yeongyu/oh-my-opencode | Agent Harness | 最佳 agent harness 系统 |
| **nanoclaw** | qwibitai/nanoclaw | 轻量级 OpenClaw 替代 | 容器化运行，安全性高 |

### 8.4 Claude Code + Codex 集成

| 技能 | GitHub | 功能 |
|-----|--------|------|
| **Codex Skill** | skills-directory/skill-codex | 从Claude Code调用Codex CLI |
| **Claude Code Tools** | pchalasani/claude-code-tools | 会话连续性 + Rust全文索引 |

---

## 九、CLI/开发环境增强

### 9.1 编排工具

| 工具 | GitHub | 特点 |
|-----|--------|------|
| **Claude Squad** | smtg-ai/claude-squad | 多工作区管理 |
| **Claude Swarm** | parruda/claude-swarm | 多代理协同 |
| **Auto-Claude** | AndyMik90/Auto-Claude | 自主多代理框架 |

### 9.2 使用监控

| 工具 | GitHub | 特点 |
|-----|--------|------|
| **CC Usage** | ryoppippi/ccusage | CLI使用分析 |
| **ccflare** | snipeship/ccflare | Web仪表板 |
| **better-ccflare** | tombii/better-ccflare | ccflare增强版 |
| **Claudex** | kunwar-shah/claudex | 会话历史浏览器 |

### 9.3 IDE集成

| 工具 | 平台 | 功能 |
|-----|------|------|
| **Claude Code Chat** | VS Code | 聊天界面 |
| **claude-code.nvim** | Neovim | 无缝集成 |
| **claude-code.el** | Emacs | Emacs接口 |
| **Claudix** | VS Code | 交互式聊天 |

---

## 📎 相关资源

- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
- [awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills)
- [Claude Code Handbook](https://nikiforovall.blog/claude-code-rules/)
- [Claude Code Ultimate Guide](https://github.com/FlorianBruniaux/claude-code-ultimate-guide)
- [补充调研文档](./supplement-2026-03/README.md)

---

*持续更新中，欢迎提交 PR 补充更多技能*
