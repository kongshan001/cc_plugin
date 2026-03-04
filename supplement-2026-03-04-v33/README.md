# Claude Code 插件补充调研 - 第三十三期

> 聚焦 Claude Code 热门插件 - 游戏客户端开发、Python开发、自动化测试、开发者工具

---

## 调研时间
2026-03-04

## 数据来源
- awesome-claude-code (hesreallyhim/awesome-claude-code)
- Antigravity Skills (970+ 技能)
- GitHub Topics: claude-code, mcp-server

---

## 一、Claude Code 生态系统概览

### 1.1 核心资源

| 资源 | 地址 | 说明 |
|-----|------|------|
| awesome-claude-code | [hesreallyhim/awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code) | 精选 Claude Code 技能/插件列表 |
| Antigravity Skills | [sickn33/antigravity-awesome-skills](https://github.com/sickn33/antigravity-awesome-skills) | 970+ 通用代理技能库 |
| 官方文档 | [docs.anthropic.com](https://docs.anthropic.com/en/docs/claude-code) | Claude Code 官方文档 |

### 1.2 技能类型分布

```
编程语言:
├── TypeScript: 35+ 技能
├── Python: 25+ 技能
├── Go: 5+ 技能
└── PHP: 2+ 技能

测试框架:
├── Playwright: 浏览器自动化主导
├── Unity Test Framework: 游戏专用
├── pytest: Python 测试
└── Vitest: 前端测试
```

---

## 二、游戏客户端开发插件

### 2.1 Unity 开发

| 技能 | 来源 | 描述 |
|-----|------|------|
| **Claude-Code-Game-Studios** | [Donchitos/Claude-Code-Game-Studios](https://github.com/Donchitos/Claude-Code-Game-Studios) ⭐26 | 48个AI代理 + 36个工作流技能的全栈游戏开发系统 |
| **unity-developer** | Antigravity | Unity 6 LTS, URP/HDRP, 跨平台部署专家 |
| **unity-ecs-patterns** | Antigravity | Unity DOTS/ECS 开发模式 |
| **cc-plugin-unity-gamedev** | [tjboudreaux/cc-plugin-unity-gamedev](https://github.com/tjboudreaux/cc-plugin-unity-gamedev) ⭐1 | 21个专业技能覆盖 Unity 开发栈 |
| **OH-Unity-GameDev-Skills** | [OstrichHermit/OH-Unity-GameDev-Skills](https://github.com/OstrichHermit/OH-Unity-GameDev-Skills) ⭐6 | Unity 基础 + DoTween + MediaPipe |
| **unity-ai-workflow** | [David-GD13/unity-ai-workflow](https://github.com/David-GD13/unity-ai-workflow) ⭐4 | Unity 6.2+ AI-first 工作流 |

#### Claude-Code-Game-Studios 核心功能

```
## 48个专业AI代理
├── 动画/物理: Animation, Physics, NavMesh, Object Pooling
├── AI/行为: Behavior Designer, GAS (Gameplay Ability System)
├── 音视频: Wwise音频, Cinemachine相机
├── UI: UGUI, Mobile Optimization
├── 测试: Unity Test Framework
├── DI/异步: VContainer, UniTask
└── 工具类: Addressables, MemoryPack, ScriptableObjects

## 36个工作流技能
├── 项目管理: 任务规划、迭代管理
├── 代码开发: 架构设计、模式实现
├── 测试: 单元测试、集成测试
└── 部署: 构建优化、发布流程
```

### 2.2 Unreal Engine 开发

| 技能 | 来源 | 描述 |
|-----|------|------|
| **unreal-engine-cpp-pro** | Antigravity | UE5.x C++ 开发最佳实践 |
| **unreal-engine-developer** | Antigravity | Unreal Engine 5.x 全栈开发 |

### 2.3 Godot 开发

| 技能 | 来源 | 描述 |
|-----|------|------|
| **godot-gdscript-patterns** | Antigravity | Godot 4 GDScript 模式 |
| **godot-4-migration** | Antigravity | Godot 4 迁移指南 |
| **godot-developer** | Antigravity | Godot 游戏开发专家 |

### 2.4 通用游戏开发

| 技能 | 来源 | 描述 |
|-----|------|------|
| **game-development** | Antigravity | 游戏开发协调器 |
| **2d-games** | Antigravity | 2D 游戏开发原理 |
| **3d-games** | Antigravity | 3D 游戏开发原理 |
| **web-games** | Antigravity | Web 浏览器游戏开发 |
| **mobile-games** | Antigravity | 移动游戏开发 |
| **multiplayer** | Antigravity | 网络游戏开发 |
| **game-opus** | Antigravity | 游戏开发 opus 技能 |

---

## 三、Python 开发插件

### 3.1 核心 Python 技能

| 技能 | 来源 | 描述 |
|-----|------|------|
| **python-pro** | Antigravity | Python 3.12+ 现代开发 |
| **python-patterns** | Antigravity | Python 设计模式 |
| **python-development-python-scaffold** | Antigravity | Python 项目脚手架 |
| **python-fastapi-development** | Antigravity | FastAPI 开发最佳实践 |
| **python-packaging** | Antigravity | Python 包发布管理 |
| **python-performance-optimization** | Antigravity | Python 性能优化 |

### 3.2 Python 测试技能

| 技能 | 来源 | 描述 |
|-----|------|------|
| **python-testing-patterns** | Antigravity | pytest 测试策略 |
| **temporal-python-testing** | Antigravity | Temporal 工作流测试 |
| **unit-testing-test-generate** | Antigravity | 单元测试生成 |

### 3.3 Python 异步和数据处理

| 技能 | 来源 | 描述 |
|-----|------|------|
| **async-python-patterns** | Antigravity | asyncio 异步编程 |
| **backtesting-frameworks** | Antigravity | 金融回测框架 |
| **dbos-python** | Antigravity | DBOS Python 工作流 |

### 3.4 Python 云和 AI 集成

| 技能 | 来源 | 描述 |
|-----|------|------|
| **airflow-dag-patterns** | Antigravity | Apache Airflow DAG 开发 |
| **n8n-code-python** | Antigravity | n8n 工作流自动化 |
| **temporal-python-pro** | Antigravity | Temporal 工作流开发 |
| **pydantic-ai-skills** | [DougTrajano/pydantic-ai-skills](https://github.com/DougTrajano/pydantic-ai-skills) ⭐136 | Pydantic AI 深度集成 |

#### uv - Python 包管理利器

```
项目地址: astral-sh/uv
特点: 10-100x faster than pip

# 安装
curl -LsSf https://astral.sh/uv/install.sh | sh

# 项目初始化
uv init my-project
uv venv
uv pip install -r requirements.txt
```

---

## 四、自动化测试插件

### 4.1 浏览器自动化测试

| 技能 | 来源 | 描述 |
|-----|------|------|
| **playwright-skill** | [lackeyjb/playwright-skill](https://github.com/lackeyjb/playwright-skill) ⭐1.8k | Playwright 浏览器自动化 |
| **playwright-undetected-skill** | [dalbit-mir/playwright-undetected-skill](https://github.com/dalbit-mir/playwright-undetected-skill) ⭐4 | Bot 检测绕过 |
| **e2e-testing** | Antigravity | E2E 测试工作流 |
| **go-playwright** | Antigravity | Go 语言 Playwright |
| **azure-microsoft-playwright-testing-ts** | Antigravity | Azure Playwright 测试 |

### 4.2 通用测试技能

| 技能 | 来源 | 描述 |
|-----|------|------|
| **test-automator** | Antigravity | AI 驱动测试自动化 |
| **test-driven-development** | Antigravity | TDD 开发流程 |
| **testing-qa** | Antigravity | 综合测试和 QA 工作流 |
| **testing-patterns** | Antigravity | 测试模式最佳实践 |
| **test-fixing** | Antigravity | 测试修复指南 |

### 4.3 移动端测试

| 技能 | 来源 | 描述 |
|-----|------|------|
| **android_ui_verification** | Antigravity | Android UI 自动化测试 |
| **ios-simulator-skill** | [conorluddy/ios-simulator-skill](https://github.com/conorluddy/ios-simulator-skill) ⭐557 | iOS 模拟器测试 |

---

## 五、开发者工具插件

### 5.1 全栈开发技能

| 技能 | 来源 | 描述 |
|-----|------|------|
| **fullstack-dev-skills** | [jeffallan/claude-skills](https://github.com/jeffallan/claude-skills) | 65+ 全栈开发技能 |
| **developer-kit** | [giuseppe-trisciuoglio/developer-kit](https://github.com/giuseppe-trisciuoglio/developer-kit) ⭐128 | 模块化插件系统 |
| **claude-code-tools** | [pchalasani/claude-code-tools](https://github.com/pchalasani/claude-code-tools) | 会话连续性工具 |
| **claudekit** | [carlrannaberg/claudekit](https://github.com/carlrannaberg/claudekit) | CLI 工具包，20+ 子代理 |

### 5.2 DevOps 和云平台

| 技能 | 来源 | 描述 |
|-----|------|------|
| **aws-skills** | Antigravity | AWS 开发与云架构 |
| **aws-mcp-server** | [alexei-led/aws-mcp-server](https://github.com/alexei-led/aws-mcp-server) | AWS CLI 集成 |
| **cloud-devops** | Antigravity | 云端 DevOps |
| **cc-devops-skills** | [akin-ozer/cc-devops-skills](https://github.com/akin-ozer/cc-devops-skills) | IaC 代码生成 |
| **appdeploy** | Antigravity | Web 应用部署 |

#### AWS MCP Server 支持的服务

```
计算: EC2, Lambda, ECS, EKS
存储: S3, EBS, EFS
数据库: RDS, DynamoDB, ElastiCache
网络: VPC, CloudFront, Route53
```

### 5.3 安全和代码质量

| 技能 | 来源 | 描述 |
|-----|------|------|
| **trailofbits-skills** | [trailofbits/skills](https://github.com/trailofbits/skills) | CodeQL/Semgrep 安全审计 |
| **parry** | [vaporif/parry](https://github.com/vaporif/parry) | 提示注入扫描器 |
| **Dippy** | [ldayton/Dippy](https://github.com/ldayton/Dippy) | AST 自动批准安全命令 |

### 5.4 Hook 系统

| 技能 | 来源 | 描述 |
|-----|------|------|
| **claude-hooks** | [johnlindquist/claude-hooks](https://github.com/johnlindquist/claude-hooks) | TypeScript Hook 系统 |
| **cchooks** | [GowayLee/cchooks](https://github.com/GowayLee/cchooks) | Python Hook SDK |
| **claude-code-hooks-sdk** | [beyondcode/claude-hooks-sdk](https://github.com/beyondcode/claude-hooks-sdk) | PHP Hook SDK |

---

## 六、MCP 服务器

### 6.1 热门 MCP 服务器

| 服务器 | 来源 | 描述 |
|-------|------|------|
| **github-mcp-server** | [github/github-mcp-server](https://github.com/github/github-mcp-server) | GitHub 官方 MCP 服务器 |
| **context7** | [upstash/context7](https://github.com/upstash/context7) | 代码文档 MCP 服务器 |
| **chrome-devtools-mcp** | [ChromeDevTools/chrome-devtools-mcp](https://github.com/ChromeDevTools/chrome-devtools-mcp) | Chrome DevTools |
| **serena** | [oraios/serena](https://github.com/oraios/serena) | 语义检索和编辑能力 |

---

## 七、使用建议

### 7.1 游戏开发推荐技能栈

```
Unity 开发:
→ Claude-Code-Game-Studios + unity-developer + Unity Test Framework

Unreal Engine 开发:
→ unreal-engine-cpp-pro

Godot 开发:
→ godot-gdscript-patterns + godot-4-migration

通用游戏开发:
→ game-development → 2d-games/3d-games/web-games/mobile-games
```

### 7.2 Python 开发推荐技能栈

```
现代 Python 开发:
→ python-pro + python-patterns

Web/API 开发:
→ python-fastapi-development

测试:
→ python-testing-patterns + test-driven-development

异步编程:
→ async-python-patterns

包管理:
→ uv (astral-sh/uv)
```

### 7.3 测试推荐技能栈

```
浏览器自动化:
→ playwright-skill + e2e-testing

综合测试:
→ test-automator + testing-qa

TDD:
→ test-driven-development + python-testing-patterns
```

---

## 八、趋势分析

### 8.1 当前热门方向

| 方向 | 趋势 | 代表技能 |
|-----|------|---------|
| Agent 工作流 | ⬆️ 上升 | agentsys, claude-code-agents, Claude Code Flow |
| 安全审计 | ⬆️ 上升 | trailofbits-skills, parry, Dippy |
| 游戏开发 | ⬆️ 上升 | Claude-Code-Game-Studios |
| 测试自动化 | ⬆️ 上升 | Playwright 主导，TDD 命令丰富 |
| Hook 生态 | ⬆️ 上升 | 多语言 SDK (Python, PHP, TypeScript) |

### 8.2 安装方式

```bash
# 克隆技能仓库
git clone https://github.com/用户名/技能名.git

# 复制到 Claude Code 技能目录
cp -r 技能名 ~/.claude/skills/

# 或使用技能安装命令
claude --install-skill gh-用户名-技能名

# 列出已安装技能
claude --list-skills
```

---

## 九、总结

| 方向 | 技能数量 | 代表技能 |
|------|---------|---------|
| 游戏客户端开发 | 20+ | Claude-Code-Game-Studios, unity-developer, godot-gdscript-patterns |
| Python 开发 | 15+ | python-pro, python-testing-patterns, async-python-patterns, uv |
| 自动化测试 | 15+ | playwright-skill, test-automator, e2e-testing |
| 开发者工具 | 30+ | fullstack-dev-skills, trailofbits-skills, claude-hooks |

**数据来源**: 
- awesome-claude-code
- Antigravity Skills (970+ 技能索引)
- GitHub Topics

---

*持续更新中，欢迎提交 PR 补充更多技能*
