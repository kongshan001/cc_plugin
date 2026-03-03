# Claude Code 热门插件补充调研 (2026-03-04 第十七期)

> 持续跟踪 Claude Code 生态热门插件，聚焦游戏开发、Python 开发、自动化测试、开发者工具方向

---

## 📋 文档信息

- **调研日期**: 2026-03-04
- **分类**: 游戏客户端开发 / Python 开发 / 自动化测试 / 开发者工具
- **状态**: ✅ 补充调研第十七期
- **数据来源**: GitHub Topics + awesome-claude-code + Antigravity Skills

---

## 一、Claude Code 生态概览

### 1.1 统计数据

根据 GitHub Topics 数据，Claude Code 相关仓库已突破 **8,516** 个，涵盖以下热门方向：

| 类别 | 仓库数量 | 热门项目 |
|------|---------|---------|
| **AI 工作室** | 500+ | CherryStudio, ruflo |
| **开发工具** | 1000+ | awesome-claude-code, Claude Code Templates |
| **游戏开发** | 200+ | Claude-Code-Game-Studios |
| **自动化测试** | 300+ | playwright-skill, fieldwork |
| **Agent编排** | 400+ | agentsys, ruflo, sudocode |
| **Skills** | 246+ | antigravity-awesome-skills (900+) |

### 1.2 最新热门项目 (2026年3月)

| 项目 | Star | 特点 |
|------|------|------|
| **CherryStudio** | ⭐ 8.5k+ | AI生产力工作室，300+助手 |
| **antigravity-awesome-skills** | ⭐ 900+ | 900+通用技能集合 |
| **awesome-claude-code** | ⭐ 7.1k | 精选技能列表 |
| **claude-mem** | ⭐ 600+ | 会话记忆自动捕获 |
| **ruflo** | ⭐ 500+ | Agent编排平台 |
| **everything-claude-code** | ⭐ 活跃 | Agent性能优化系统 |

---

## 二、游戏客户端开发技能

### 2.1 Claude Code Game Studios ⭐ 强烈推荐

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

### 2.2 Unity 开发技能

| 技能 | GitHub | Star | 特点 |
|-----|--------|------|------|
| **cc-plugin-unity-gamedev** | tjboudreaux/cc-plugin-unity-gamedev | ⭐1 | 21个专业技能 |
| **OH-Unity-GameDev-Skills** | OstrichHermit/OH-Unity-GameDev-Skills | ⭐6 | Unity基础+DoTween+MediaPipe |
| **unity-ai-workflow** | David-GD13/unity-ai-workflow | ⭐4 | Unity 6.2+ AI-first工作流 |

#### Unity 技能核心分类

| 分类 | 技能 |
|-----|------|
| **工具类** | Addressables, MemoryPack, ScriptableObjects, Profiling |
| **动画/物理** | Animation, Physics, NavMesh, Object Pooling |
| **AI/行为** | Behavior Designer, GAS |
| **UI** | UGUI, Mobile Optimization |
| **测试** | Unity Test Framework |

### 2.3 Unity AI Workflow (2026 新增)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [David-GD13/unity-ai-workflow](https://github.com/David-GD13/unity-ai-workflow) |
| **Star** | ⭐ 4 |
| **特点** | Unity 6.2+ AI-first 开发工作流 |

#### Dev Modes

| 模式 | 角色 | 适用场景 |
|------|------|---------|
| Assistant | 你构建，AI 辅助 | 学习、创意控制 |
| Mix (默认) | 协作模式 | 大多数项目 |
| Automatic | AI 构建 | 快速原型 |

#### 核心哲学

```markdown
### Game Feel 不是可选的
- 每项功能使用 /implement-feature 完整构建
- AI 在写代码前询问 VFX、SFX、相机反馈和触觉
- 迭代打磨，不是单独阶段

### TCREI Prompting 方法论
- Task: 明确任务
- Context: 提供上下文
- References: 提供参考
- Evaluate: 评估结果
- Iterate: 迭代改进
```

### 2.4 其他游戏引擎技能

| 方向 | 推荐技能 | Star | 特点 |
|-----|---------|------|------|
| **Godot** | godot-engine/godot | 161k | 开源游戏引擎 |
| **Godot Claude Skills** | claude-resources | ⭐3 | Godot 专用技能 |
| **GameMaker** | gamemaker-skills | ⭐2 | 2D游戏专用 |
| **Solana链游** | solana-game-skill | ⭐5 | 区块链游戏 |
| **Web/H5游戏** | Playwright | ⭐1.8k | 浏览器游戏测试 |

### 2.5 游戏开发技能汇总

| 方向 | 推荐技能 | Star | 特点 |
|-----|---------|------|------|
| **Unity 完整开发** | Claude-Code-Game-Studios | ⭐26 | 48代理全栈 |
| **Unity 基础** | cc-plugin-unity-gamedev | ⭐1 | 21技能专业栈 |
| **Godot** | godot-resources | ⭐3 | 开源游戏引擎 |
| **Web游戏测试** | playwright-skill | ⭐1.8k | 浏览器自动化 |

---

## 三、Python 开发技能

### 3.1 数据库集成

| 技能 | GitHub | 功能 | 安全性 |
|-----|--------|------|--------|
| **read-only-postgres** | jawwadfirdousi/agent-skills | PostgreSQL只读查询 | ⭐⭐⭐⭐⭐ |
| **postgres** | sanjay3290/ai-skills | PostgreSQL完整集成 | ⭐⭐⭐ |

#### read-only-postgres 核心特性

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

#### pydantic-ai-skills 核心能力

- **类型安全**: Pydantic 模型强制类型检查
- **渐进式提示**: 按需披露信息
- **AI 集成**: 与主流 LLM 无缝集成
- **验证系统**: 内置强大的数据验证

### 3.3 uv - Python 包管理器 (2025最快)

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
| **claude-code-tools** | pchalasani/claude-code-tools | - | 会话连续性工具 |

#### Claudekit 子代理

| 代理 | 功能 |
|------|------|
| **oracle** | GPT-5 集成 |
| **code-reviewer** | 6方面深度分析 |
| **typescript-expert** | TypeScript 专家 |
| **ai-sdk-expert** | Vercel AI SDK |

### 3.5 云服务集成

| 技能 | GitHub | 功能 |
|-----|--------|------|
| **aws-mcp-server** | alexei-led/aws-mcp-server | AWS CLI 集成 |

**支持服务:**
- 计算: EC2, Lambda, ECS, EKS
- 存储: S3, EBS, EFS
- 数据库: RDS, DynamoDB, ElastiCache
- 网络: VPC, CloudFront, Route53

### 3.6 Python Skills 汇总

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
| **playwright-undetected-skill** | dalbit-mir/playwright-undetected-skill | ⭐4 | Bot检测绕过 |
| **playwright-bot-bypass** | greekr4/playwright-bot-bypass | - | 绕过Google CAPTCHA等 |

#### Playwright 核心功能

- **Web 应用测试**: 自动化测试 Web 应用功能
- **UI 验证**: 验证前端功能和行为
- **截图捕获**: 自动截图记录测试状态
- **调试支持**: 辅助调试 UI 行为
- **反检测**: Patchright 支持绕过 Bot 检测

### 4.2 游戏客户端测试方案

| 测试类型 | 方案 | 适用场景 |
|---------|------|---------|
| **Web/H5游戏** | Playwright | 功能测试、回归测试 |
| **Unity游戏** | Unity Test Framework | 单元测试、集成测试 |
| **性能测试** | Unity Profiler | 帧率、内存测试 |
| **Android游戏** | ADB + uiautomator | UI自动化 |
| **iOS游戏** | ios-simulator-skill | 模拟器测试 |

#### Unity Test Framework

| 测试类型 | 说明 | 适用场景 |
|---------|------|---------|
| **EditMode** | 编辑器环境测试 | 工具类、辅助功能 |
| **PlayMode** | 运行时测试 | 游戏逻辑、UI |
| **Performance** | 性能测试 | 性能优化 |

#### Android UI 测试

```bash
# 设备校准 - 获取屏幕分辨率
adb shell wm size

# UI 检查 - 获取元素信息
adb shell uiautomator dump /sdcard/view.xml

# 交互操作
adb shell input tap <x> <y>
adb shell input swipe <x1> <y1> <x2> <y2> <duration_ms>

# 截图验证
adb shell screencap -p /sdcard/screen.png
```

### 4.3 移动端测试

#### iOS 模拟器测试

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

### 4.4 测试质量工具

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **claude-skills-marketplace** | mhattingpete/claude-skills-marketplace | ⭐427 | 测试/代码审查 |
| **fieldwork-skills** | buildoak/fieldwork-skills | ⭐12 | E2E测试/Bug修复 |

### 4.5 TDD 开发技能

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

#### pytest 最佳实践

```bash
# 运行所有测试
pytest

# 运行带标记的测试
pytest -m "unit"

# 生成覆盖率报告
pytest --cov=src --cov-report=html

# 并行执行
pytest -n auto
```

### 4.6 测试自动化汇总

| 用途 | 首推技能 | 备选 |
|-----|---------|------|
| **浏览器测试** | playwright-skill | playwright-undetected |
| **Unity测试** | Unity Test Framework | - |
| **移动端测试** | ios-simulator-skill | android_ui_verification |
| **代码质量** | claude-skills-marketplace | fieldwork-skills |

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

- **工作流自动化**: 任务到生产的完整流程
- **PR 管理**: 自动管理 Pull Request
- **代码清理**: 自动代码清理和维护
- **性能调查**: 性能问题调查和优化
- **漂移检测**: 检测代码偏离
- **多代理代码审查**: 并行多代理审查

### 5.2 安全审计

| 技能 | GitHub | 特点 |
|-----|--------|------|
| **trailofbits-skills** | trailofbits/skills | CodeQL/Semgrep集成 |
| **parry** | vaporif/parry | 提示注入扫描 |
| **Dippy** | ldayton/Dippy | AST智能命令批准 |

#### Trail of Bits 技能分类

| 技能 | 功能 |
|------|------|
| **codeql** | 静态代码分析 |
| **semgrep** | 模式匹配分析 |
| **variant-analysis** | 变体分析 |
| **fix-verification** | 修复验证 |
| **diff-review** | 差异代码审查 |

### 5.3 DevOps 工具

| 技能 | GitHub | 特点 |
|-----|--------|------|
| **cc-devops-skills** | akin-ozer/cc-devops-skills | IaC代码生成 |
| **ContextKit** | FlineDev/ContextKit | 4阶段规划方法论 |

#### ContextKit 方法论

```
阶段1: 理解 → 分析需求和上下文
阶段2: 规划 → 制定详细计划
阶段3: 执行 → 实施解决方案
阶段4: 验证 → 验证结果质量
```

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
| **Star** | ⭐ 活跃 |
| **特点** | 科研/工程/分析/金融/写作全能技能集 |

#### 核心功能

- **研究技能**: 文献检索、学术写作、研究方法
- **科学计算**: 数据分析、模型构建、实验设计
- **工程分析**: 结构分析、仿真、计算
- **金融分析**: 量化分析、风险评估、投资策略
- **写作技能**: 技术文档、论文撰写、内容创作

---

## 六、热门技能推荐

### 6.1 按用途推荐

| 用途 | 首推技能 | 备选 |
|-----|---------|------|
| **游戏开发 (Unity)** | Claude-Code-Game-Studios | cc-plugin-unity-gamedev |
| **游戏开发 (通用)** | Antigravity pc-games/mobile-games | game-opus |
| **Python 后端** | pydantic-ai-skills | read-only-postgres |
| **Python 测试** | pytest + TDD | playwright-skill |
| **Web/H5游戏测试** | playwright-skill | playwright-undetected |
| **全栈开发** | fullstack-dev-skills (65+) | claude-code-templates |
| **DevOps** | cc-devops-skills | superpowers |
| **代码审查** | agentsys | claude-code-agents |
| **安全审计** | trailofbits-skills | parry |
| **科学研究** | claude-scientific-skills | - |

### 6.2 技能选择决策树

```
游戏客户端开发?
├─ Unity → Claude-Code-Game-Studios
├─ Godot → godot-resources
├─ GameMaker → gamemaker-skills
├─ Web/H5 → playwright-skill
└─ 通用 → Antigravity Skills

Python 开发?
├─ Web框架 → pydantic-ai-skills
├─ 数据库 → read-only-postgres
├─ 云服务 → aws-mcp-server
├─ 测试 → pytest + TDD
└─ 包管理 → uv

自动化测试?
├─ 浏览器 → playwright-skill
├─ 单元测试 → Unity Test Framework
├─ 移动端 → ios-simulator-skill
├─ 代码质量 → /check, /clean
└─ TDD → /tdd-implement

开发者效率?
├─ 全栈 → fullstack-dev-skills
├─ DevOps → cc-devops-skills
├─ 安全 → trailofbits-skills
├─ 编排 → ruflo
└─ 科学 → claude-scientific-skills
```

### 6.3 技能组合推荐

```
游戏开发组合:
Claude-Code-Game-Studios + Unity Test Framework + playwright-skill

Python开发组合:
uv + pydantic-ai-skills + read-only-postgres + pytest + aws-mcp-server

测试自动化组合:
playwright-skill + fieldwork-skills + claude-skills-marketplace

游戏帧同步测试:
Unity Test Framework + 网络延迟模拟 + 帧同步确定性验证

科研工作流:
claude-scientific-skills + langgraph-agent-skill + pydantic-ai-skills
```

---

## 七、安装指南

### 7.1 快速安装

```bash
# 克隆技能仓库
git clone https://github.com/用户名/技能名.git

# 复制到 Claude Code 技能目录
cp -r 技能名 ~/.claude/skills/

# 或使用技能安装命令
claude --install-skill gh-用户名-技能名
```

### 7.2 验证安装

```bash
# 列出已安装技能
claude --list-skills

# 或在 Claude Code 中输入
/skill list
```

### 7.3 技能更新

```bash
# 进入技能目录
cd ~/.claude/skills/技能名

# 拉取最新
git pull origin main
```

---

## 八、趋势分析

### 8.1 热门方向

| 方向 | 趋势 | 说明 |
|-----|------|------|
| **Agent工作流** | ⬆️ 上升 | agentsys, claude-code-agents, ruflo |
| **安全审计** | ⬆️ 上升 | trailofbits-skills, parry, Dippy |
| **游戏开发** | ⬆️ 上升 | Claude-Code-Game-Studios 全栈覆盖 |
| **测试自动化** | ⬆️ 上升 | Playwright主导，TDD命令丰富 |
| **Hook 生态** | ⬆️ 上升 | 多语言 SDK (Python, PHP, TypeScript) |
| **科学研究** | ⬆️ 上升 | claude-scientific-skills 全能 |

### 8.2 技术栈分布

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

游戏引擎:
├── Unity: Claude-Code-Game-Studios
├── Godot: godot-resources
├── Web: Phaser, Babylon.js, Three.js
└── 链游: Solana
```

### 8.3 新兴项目

| 项目 | Star | 特点 |
|------|------|------|
| **CherryStudio** | ⭐ 8.5k+ | AI生产力工作室 |
| **antigravity-awesome-skills** | ⭐ 900+ | 900+通用技能 |
| **claude-mem** | ⭐ 600+ | 会话记忆 |
| **ruflo** | ⭐ 500+ | Agent编排 |
| **nelson** | ⭐ 新 | 海军指挥结构化代理协调 |

---

## 📎 相关资源

- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
- [awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills)
- [Antigravity Skills](https://github.com/sickn33/antigravity-awesome-skills)
- [Claude Code Handbook](https://nikiforovall.blog/claude-code-rules/)
- [Claude Code Ultimate Guide](https://github.com/FlorianBruniaux/claude-code-ultimate-guide)

---

## 📂 补充调研文档

- [补充调研-第一期](./supplement-2026-03-03/README.md)
- [补充调研-第二期](./supplement-2026-03-04/README.md)
- [补充调研-第三期](./supplement-2026-03-04-v2/README.md)
- [补充调研-第四期](./supplement-2026-03-04-v3/README.md)
- [补充调研-第五期](./supplement-2026-03-04-v4/README.md)
- [补充调研-第六期](./supplement-2026-03-04-v5/README.md)
- [补充调研-第七期](./supplement-2026-03-04-v6/README.md)
- [补充调研-第八期](./supplement-2026-03-04-v7/README.md)
- [补充调研-第九期](./supplement-2026-03-04-v8/README.md)
- [补充调研-第十期](./supplement-2026-03-04-v9/README.md)
- [补充调研-第十一期](./supplement-2026-03-04-v10/README.md)
- [补充调研-第十二期](./supplement-2026-03-04-v11/README.md)
- [补充调研-第十三期](./supplement-2026-03-04-v12/README.md)
- [补充调研-第十四期](./supplement-2026-03-04-v14/README.md)
- [补充调研-第十五期](./supplement-2026-03-04-v15/README.md)
- [补充调研-第十六期](./supplement-2026-03-04-v16/README.md) (最新)

---

*持续更新中，欢迎提交 PR 补充更多技能*
