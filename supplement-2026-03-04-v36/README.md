# Claude Code 插件补充调研 - 第三十六期

> 聚焦 Claude Code 热门插件 - 游戏客户端开发、Python开发、自动化测试、开发者工具

---

## 调研时间
2026-03-04

## 数据来源
- awesome-claude-code (hesreallyhim/awesome-claude-code)
- Antigravity Skills (970+ 技能)
- GitHub Topics: claude-code, mcp-server
- Claude Code 官方插件库

---

## 一、游戏客户端开发技能（最新补充）

### 1.1 Claude Code Game Studios ⭐ 强烈推荐

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

#### 适用场景

- 大型游戏项目开发
- 游戏工作室工作流自动化
- 跨团队协作开发
- 全栈游戏开发

### 1.2 Unity 开发技能（完整版）

#### 官方/社区技能对比

| 技能 | GitHub | Star | 特点 |
|-----|--------|------|------|
| **cc-plugin-unity-gamedev** | tjboudreaux/cc-plugin-unity-gamedev | ⭐1 | 21个专业技能，完整覆盖Unity开发栈 |
| **OH-Unity-GameDev-Skills** | OstrichHermit/OH-Unity-GameDev-Skills | ⭐6 | Unity基础开发+DoTween+MediaPipe |
| **unity-ai-workflow** | David-GD13/unity-ai-workflow | ⭐4 | Unity 6.2+ AI-first工作流 |
| **unity-developer** (Antigravity) | Antigravity | - | 全栈Unity开发专家 |

#### Unity 技能核心分类

| 分类 | 技能 |
|-----|------|
| **工具类** | Addressables, MemoryPack, ScriptableObjects, Profiling, Package Manager |
| **动画/物理** | Animation, Physics, NavMesh, Object Pooling, State Machine |
| **AI/行为** | Behavior Designer, GAS (Gameplay Ability System) |
| **音视频** | Wwise音频, Cinemachine相机, PrimeTween |
| **UI** | UGUI, Mobile Optimization |
| **测试** | Unity Test Framework |
| **DI/异步** | VContainer, UniTask |
| **渲染** | URP, HDRP, Shader Graph, HLSL |
| **性能** | Job System, Burst Compiler, DOTS/ECS |

### 1.3 Unity AI Workflow (2026 新增)

#### 项目地址
- **GitHub**: [David-GD13/unity-ai-workflow](https://github.com/David-GD13/unity-ai-workflow)
- **Star**: ⭐ 4
- **特点**: 专为 Unity 6.2+ 设计的 AI-first 开发工作流

#### 核心特性

```markdown
### Dev Modes (三种开发模式)
| 模式 | 角色 | 适用场景 |
|------|------|---------|
| Assistant | 你构建，AI 辅助文档和解释 | 学习、创意控制 |
| Mix (默认) | 协作模式，AI 建议，你确认 | 大多数项目 |
| Automatic | AI 构建，短的 onboarding Q&A | 快速原型、游戏 jam |

### 核心哲学: Game Feel 不是可选的
- 每项功能使用 /implement-feature 完整构建
- AI 在写代码前询问 VFX、SFX、相机反馈和触觉
- 迭代打磨，不是单独阶段

### 技术架构
- TCREI Prompting: Task-Context-References-Evaluate-Iterate 方法论
- 验证系统: 每个 AI 推荐标记 [VERIFIED]/[SYNTHESIZED]/[UNVERIFIED]
- 专家 Skills: UI Toolkit、ScriptableObject、Netcode、game feel、测试、调试
```

### 1.4 Godot 开发

| 技能 | 来源 | 描述 |
|-----|------|------|
| **godot-gdscript-patterns** | Antigravity | Godot 4 GDScript 模式 |
| **godot-4-migration** | Antigravity | Godot 4 迁移指南 |
| **godot-developer** | Antigravity | Godot 游戏开发专家 |

### 1.5 Web/H5 游戏开发

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
└── 混合/Canvas
    └── 自定义 → 原始 Canvas/WebGL
```

---

## 二、Python 开发技能（最新补充）

### 2.1 uv - Python 包管理器 (2025最快)

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

# 快速依赖安装
uv add flask
uv add --dev pytest

# 运行脚本
uv run main.py

# 锁定依赖
uv lock
uv sync
```

**性能对比:**

| 操作 | pip | uv | 加速比 |
|-----|-----|-----|-------|
| 安装依赖 | 45s | 4.5s | 10x |
| 锁文件生成 | 30s | 0.5s | 60x |

### 2.2 Pydantic AI 技能

#### pydantic-ai-skills ⭐ 热门

| 项目 | 说明 |
|-----|------|
| **GitHub** | [DougTrajano/pydantic-ai-skills](https://github.com/DougTrajano/pydantic-ai-skills) |
| **Star** | ⭐ 136 |
| **特点** | Pydantic AI 深度集成 |

**核心能力:**
- **类型安全**: Pydantic 模型强制类型检查
- **渐进式提示**: 按需披露信息
- **AI 集成**: 与主流 LLM 无缝集成
- **验证系统**: 内置强大的数据验证

### 2.3 数据库集成

#### read-only-postgres ⭐ 安全推荐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [jawwadfirdousi/agent-skills](https://github.com/jawwadfirdousi/agent-skills) |
| **特点** | PostgreSQL 只读查询，安全优先 |

**安全措施:**
- 只读查询 (SELECT/SHOW/EXPLAIN/WITH)
- 超时控制
- 行数限制
- 多连接支持

### 2.4 AWS 云服务集成

#### AWS MCP Server

| 项目 | 说明 |
|-----|------|
| **GitHub** | [alexei-led/aws-mcp-server](https://github.com/alexei-led/aws-mcp-server) |
| **语言** | Python |
| **Star** | ⭐ 1350+ |
| **特点** | AWS CLI 集成，多环境支持 |

---

## 三、自动化测试技能（最新补充）

### 3.1 Playwright 测试

#### Playwright Skill ⭐ 主流

| 项目 | 说明 |
|-----|------|
| **GitHub** | [lackeyjb/playwright-skill](https://github.com/lackeyjb/playwright-skill) |
| **Star** | ⭐ 1.8k |
| **功能** | 浏览器自动化，Web测试 |

**核心能力:**
- **测试隔离**: 每个测试在完全隔离的环境中运行
- **用户定位器**: 使用用户视角选择元素
- **自动等待**: 利用 Playwright 自动等待机制
- **截图捕获**: 自动截图记录测试状态

#### Playwright Undetected Skill

| 项目 | 说明 |
|-----|------|
| **GitHub** | [dalbit-mir/playwright-undetected-skill](https://github.com/dalbit-mir/playwright-undetected-skill) |
| **Star** | ⭐ 4 |
| **功能** | Bot检测绕过 |

**特点:**
- Patchright 支持
- 绕过反爬虫检测
- 自动化测试场景

### 3.2 iOS 模拟器测试

#### iOS Simulator Skill

| 项目 | 说明 |
|-----|------|
| **GitHub** | [conorluddy/ios-simulator-skill](https://github.com/conorluddy/ios-simulator-skill) |
| **Star** | ⭐ 557 |
| **平台** | macOS |

**核心功能:**
- 模拟器控制 (启动/停止)
- 应用安装
- UI 交互自动化
- 截图捕获

### 3.3 Unity Test Framework

| 技能 | 来源 | 描述 |
|-----|------|------|
| **unity-test-framework** | cc-plugin-unity-gamedev | Unity 官方测试框架 |
| **Test-Driven Development** | various | TDD 开发模式 |

#### 测试类型

| 测试类型 | 说明 | 适用场景 |
|---------|------|---------|
| **EditMode** | 编辑器环境测试 | 工具类、辅助功能 |
| **PlayMode** | 运行时测试 | 游戏逻辑、UI |
| **Performance** | 性能测试 | 性能优化 |

### 3.4 游戏客户端自动化测试方案

| 测试类型 | 方案 | 适用场景 |
|---------|------|---------|
| **Web/H5游戏** | Playwright | 功能测试、回归测试 |
| **Unity游戏** | Unity Test Framework | 单元测试、集成测试 |
| **性能测试** | Unity Profiler | 帧率、内存测试 |
| **Android游戏** | ADB + uiautomator | UI自动化 |
| **iOS游戏** | ios-simulator-skill | 模拟器测试 |

---

## 四、开发者工具技能（最新补充）

### 4.1 编排工具

#### AgentSys ⭐ 生产级

| 项目 | 说明 |
|-----|------|
| **GitHub** | [avifenesh/agentsys](https://github.com/avifenesh/agentsys) |
| **特点** | 生产级工作流自动化 |

**核心功能:**
- 任务到生产工作流自动化
- PR 管理
- 代码清理
- 性能调查
- 漂移检测
- 多代理代码审查

#### Claude Code Agents

| 项目 | 说明 |
|-----|------|
| **GitHub** | [undeadlist/claude-code-agents](https://github.com/undeadlist/claude-code-agents) |
| **特点** | E2E 开发工作流 |

**特点:**
- 多个审计员并行运行
- 微检查点协议自动修复循环
- 基于浏览器的 QA
- 严格协议防止 AI 失控

#### sudocode

| 项目 | 说明 |
|-----|------|
| **GitHub** | [sudocode-ai/sudocode](https://github.com/sudocode-ai/sudocode) |
| **特点** | 轻量级 agent 编排工具 |

**集成框架:**
- Jira
- 项目管理
- 规范驱动开发

### 4.2 安全审计

#### Trail of Bits Security Skills ⭐ 专业

| 项目 | 说明 |
|-----|------|
| **GitHub** | [trailofbits/skills](https://github.com/trailofbits/skills) |
| **特点** | CodeQL/Semgrep 集成 |

**覆盖范围:**
- 静态分析 (CodeQL, Semgrep)
- 变体分析
- 修复验证
- 差异代码审查

#### parry

| 项目 | 说明 |
|-----|------|
| **GitHub** | [vaporif/parry](https://github.com/vaporif/parry) |
| **特点** | 提示注入扫描器 |

**功能:**
- 扫描工具输入/输出中的注入攻击
- 检测秘密泄露
- 数据外泄尝试检测

### 4.3 会话管理

#### claude-tmux

| 项目 | 说明 |
|-----|------|
| **GitHub** | [nielsgroen/claude-tmux](https://github.com/nielsgroen/claude-tmux) |
| **功能** | tmux 会话管理 |

**功能:**
- Claude Code 实例的 tmux 弹出窗口
- 快速切换
- 状态监控
- 会话生命周期管理
- git worktree 和 PR 支持

#### claude-esp

| 项目 |说明 |
|-----|------|
| **GitHub** | [phiat/claude-esp](https://github.com/phiat/claude-esp) |
| **功能** | 隐藏输出流式传输 |

**功能:**
- Go 编写的 TUI
- 流式传输 Claude Code 的隐藏输出
- 同时监控多个会话
- 按内容类型过滤
- 跟踪后台任务

### 4.4 Claude Code 设置

#### Claude Code Settings

| 项目 | 说明 |
|-----|------|
| **GitHub** | [fcakyon/claude-codex-settings](https://github.com/fcakyon/claude-codex-settings) |
| **特点** | 核心开发者活动覆盖 |

**覆盖范围:**
- GitHub
- Azure
- MongoDB
- Tavily
- Playwright

### 4.5 全栈开发

#### Fullstack Dev Skills

| 项目 | 说明 |
|-----|------|
| **GitHub** | [jeffallan/claude-skills](https://github.com/jeffallan/claude-skills) |
| **技能数** | 65+ 专业技能 |
| **特点** | 全栈开发覆盖 |

**核心功能:**
- 9 个项目工作流命令
- Jira/Confluence 集成
- /common-ground 命令 - 暴露 Claude 的隐藏假设

### 4.6 DevOps 工具

#### cc-devops-skills

| 项目 | 说明 |
|-----|------|
| **GitHub** | [akin-ozer/cc-devops-skills](https://github.com/akin-ozer/cc-devops-skills) |
| **特点** | IaC 代码生成 |

**功能:**
- 验证系统
- 生成器
- Shell 脚本
- CLI 工具
- 高质量 IaC 代码

### 4.7 Claude Scientific Skills

| 项目 | 说明 |
|-----|------|
| **GitHub** | [K-Dense-AI/claude-scientific-skills](https://github.com/K-Dense-AI/claude-scientific-skills) |
| **特点** | 科研/工程/分析技能 |

**覆盖范围:**
- 研究技能
- 科学计算
- 工程分析
- 金融分析
- 写作

### 4.8 Context Engineering Kit

| 项目 | 说明 |
|-----|------|
| **GitHub** | [NeoLabHQ/context-engineering-kit](https://github.com/NeoLabHQ/context-engineering-kit) |
| **特点** | 高级上下文工程 |

**技术:**
- 最小 token 占用
- 专注于提高代理结果质量
- 提示工程技术
- DDD 模式

---

## 五、热门技能推荐

### 5.1 按用途推荐

| 用途 | 首推技能 | 备选 |
|-----|---------|------|
| **游戏开发 (Unity)** | Claude-Code-Game-Studios | cc-plugin-unity-gamedev |
| **游戏开发 (Godot)** | godot-developer | godot-gdscript-patterns |
| **Python 后端** | pydantic-ai-skills | read-only-postgres |
| **Python 包管理** | uv | pip |
| **Python 测试** | pytest + TDD | playwright-skill |
| **Web/H5游戏测试** | playwright-skill | playwright-undetected |
| **全栈开发** | fullstack-dev-skills (65+) | claude-code-templates |
| **DevOps** | cc-devops-skills | superpowers |
| **代码审查** | agentsys | claude-code-agents |
| **安全审计** | trailofbits-skills | parry |
| **iOS 测试** | ios-simulator-skill | - |
| **会话管理** | claude-tmux | claude-esp |

### 5.2 技能选择决策树

```
游戏客户端开发?
├─ Unity → Claude-Code-Game-Studios + unity-ai-workflow
├─ Godot → godot-developer
├─ Web/H5 → playwright-skill
└─ 通用 → Antigravity Skills

Python 开发?
├─ 包管理 → uv (10-100x faster)
├─ Web框架 → pydantic-ai-skills
├─ 数据库 → read-only-postgres
├─ 云服务 → aws-mcp-server
└─ 测试 → pytest + TDD

自动化测试?
├─ 浏览器 → playwright-skill
├─ 反检测 → playwright-undetected-skill
├─ iOS → ios-simulator-skill
├─ 单元测试 → Unity Test Framework / pytest
└─ TDD → /tdd-implement

开发者效率?
├─ 全栈 → fullstack-dev-skills
├─ DevOps → cc-devops-skills
├─ 安全 → trailofbits-skills
├─ 会话 → claude-tmux
└─ 编排 → sudocode / agentsys
```

### 5.3 技能组合推荐

```
游戏开发组合:
Claude-Code-Game-Studios + Unity Test Framework + playwright-skill + ios-simulator-skill

Python开发组合:
uv + pydantic-ai-skills + read-only-postgres + pytest + aws-mcp-server

测试自动化组合:
playwright-skill + ios-simulator-skill + fieldwork-skills

企业开发组合:
agentsys + fullstack-dev-skills + trailofbits-skills + cc-devops-skills
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
| **Agent工作流** | ⬆️ 上升 | agentsys, claude-code-agents, sudocode |
| **安全审计** | ⬆️ 上升 | trailofbits-skills, parry |
| **游戏开发** | ⬆️ 上升 | Claude-Code-Game-Studios 全栈覆盖 |
| **测试自动化** | ⬆️ 上升 | Playwright主导，iOS模拟器支持 |
| **Python工具** | ⬆️ 上升 | uv 包管理器成为新标准 |
| **会话管理** | ⬆️ 上升 | claude-tmux, claude-esp |

### 7.2 技术栈分布

```
编程语言:
├── TypeScript: 35+ 技能
├── Python: 25+ 技能
├── Go: 5+ 技能
└── PHP: 2+ 技能

测试框架:
├── Playwright: 主导
├── Unity Test Framework: 游戏
├── pytest: Python
└── Vitest: 前端
```

---

## 📎 相关资源

- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
- [awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills)
- [Claude Code Handbook](https://nikiforovall.blog/claude-code-rules/)
- [Claude Code Ultimate Guide](https://github.com/FlorianBruniaux/claude-code-ultimate-guide)
- [ Antigravity Skills](https://sickn33/antigravity-awesome-skills)
- [第三十五期补充调研](./supplement-2026-03-04-v35/README.md)

---

*持续更新中，欢迎提交 PR 补充更多技能*
