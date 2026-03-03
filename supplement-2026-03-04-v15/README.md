# Claude Code 热门插件补充调研 (2026-03-04 第十六期)

> 持续跟踪 Claude Code 生态热门插件，聚焦游戏开发、Python 开发、自动化测试、开发者工具方向

---

## 📋 文档信息

- **调研日期**: 2026-03-04
- **分类**: 游戏客户端开发 / Python 开发 / 自动化测试 / 开发者工具
- **状态**: ✅ 补充调研第十六期
- **数据来源**: GitHub Topics + awesome-claude-code + Antigravity Skills

---

## 一、GitHub 热门趋势分析

### 1.1 Claude Code 生态概览

根据 GitHub Topics 数据，Claude Code 相关仓库已突破 **8,514** 个，涵盖以下热门方向：

| 类别 | 仓库数量 | 热门项目 |
|------|---------|---------|
| **AI 工作室** | 500+ | CherryStudio, ruflo |
| **开发工具** | 1000+ | awesome-claude-code, Claude Code Templates |
| **游戏开发** | 200+ | Claude-Code-Game-Studios |
| **自动化测试** | 300+ | playwright-skill, fieldwork |
| **Agent编排** | 400+ | agentsys, ruflo, sudocode |

### 1.2 最新热门项目 (2026年3月)

| 项目 | Star | 特点 |
|------|------|------|
| **CherryStudio** | ⭐ 8.5k+ | AI生产力工作室，300+助手 |
| **antigravity-awesome-skills** | ⭐ 900+ | 900+通用技能集合 |
| **awesome-claude-code** | ⭐ 7.1k | 精选技能列表 |
| **claude-mem** | ⭐ 600+ | 会话记忆自动捕获 |
| **ruflo** | ⭐ 500+ | Agent编排平台 |

### 1.3 Claude Scientific Skills ⭐⭐⭐⭐⭐

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

### 1.4 parry - 提示注入扫描器

| 项目 | 说明 |
|-----|------|
| **GitHub** | [vaporif/parry](https://github.com/vaporif/parry) |
| **状态** | 🔶 早期开发 |
| **功能** | Claude Code Hooks 提示注入扫描 |

#### 核心功能

- **注入攻击检测**: 扫描工具输入/输出中的提示注入
- **敏感信息检测**: 检测可能的敏感数据泄露
- **数据外泄防护**: 阻止数据外泄尝试
- **双向扫描**: 输入和输出同时监控

### 1.5 Dippy - 智能命令批准

| 项目 | 说明 |
|-----|------|
| **GitHub** | [ldayton/Dippy](https://github.com/ldayton/Dippy) |
| **支持平台** | Claude Code, Gemini CLI, Cursor |

#### 核心功能

- **AST 解析**: 使用 AST 分析 Bash 命令安全性
- **智能批准**: 自动批准安全命令
- **危险命令提示**: 危险操作才请求确认

---

## 二、游戏客户端开发技能 (更新)

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

### 2.4 游戏开发技能汇总

| 方向 | 推荐技能 | Star | 特点 |
|-----|---------|------|------|
| **Unity 完整开发** | Claude-Code-Game-Studios | ⭐26 | 48代理全栈 |
| **Unity 基础** | cc-plugin-unity-gamedev | ⭐1 | 21技能专业栈 |
| **Godot** | claude-resources | ⭐3 | 开源游戏引擎 |
| **GameMaker** | gamemaker-skills | ⭐2 | 2D游戏专用 |

---

## 三、Python 开发技能 (更新)

### 3.1 数据库集成

| 技能 | GitHub | 功能 | 安全性 |
|-----|--------|------|--------|
| **read-only-postgres** | jawwadfirdousi/agent-skills | PostgreSQL只读查询 | ⭐⭐⭐⭐⭐ |
| **postgres** | sanjay3290/ai-skills | PostgreSQL完整集成 | ⭐⭐⭐ |

#### read-only-postgres 核心特性

```sql
SELECT * FROM users WHERE id = 1;
SHOW max_connections;
EXPLAIN ANALYZE SELECT * FROM orders;
```

### 3.2 AI 框架集成

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **pydantic-ai-skills** | DougTrajano/pydantic-ai-skills | ⭐136 | Pydantic AI 深度集成 |

### 3.3 uv - Python 包管理器

| 项目 | 说明 |
|-----|------|
| **GitHub** | [astral-sh/uv](https://github.com/astral-sh/uv) |
| **特点** | 10-100x faster than pip |

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
uv init my-project
uv venv
uv pip install -r requirements.txt
```

### 3.4 开发者工具包

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **developer-kit** | giuseppe-trisciuoglio/developer-kit | ⭐128 | 模块化插件系统 |
| **claudekit** | carlrannaberg/claudekit | - | CLI工具包，20+子代理 |

### 3.5 Python Skills 汇总

| Skill 名称 | 核心能力 | 适用场景 |
|-----------|---------|---------|
| python-pro | Python 3.12+ 全栈 | 通用开发 |
| python-patterns | 开发原则和决策 | 架构设计 |
| python-fastapi-development | FastAPI 后端 | API 服务 |
| python-testing-patterns | pytest/测试策略 | 质量保证 |

---

## 四、自动化测试技能 (更新)

### 4.1 浏览器自动化

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **playwright-skill** | lackeyjb/playwright-skill | ⭐1.8k | Playwright浏览器自动化 |
| **playwright-undetected-skill** | dalbit-mir/playwright-undetected-skill | ⭐4 | Bot检测绕过 |

### 4.2 游戏客户端测试方案

| 测试类型 | 方案 | 适用场景 |
|---------|------|---------|
| **Web/H5游戏** | Playwright | 功能测试 |
| **Unity游戏** | Unity Test Framework | 单元测试 |
| **Android游戏** | ADB + uiautomator | UI自动化 |
| **iOS游戏** | ios-simulator-skill | 模拟器测试 |

### 4.3 测试质量工具

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **claude-skills-marketplace** | mhattingpete/claude-skills-marketplace | ⭐427 | 测试/代码审查 |
| **fieldwork-skills** | buildoak/fieldwork-skills | ⭐12 | E2E测试/Bug修复 |

### 4.4 TDD 开发技能

| 命令 | 来源 | 功能 |
|-----|------|------|
| **/tdd** | zscott/pane | TDD开发流程 |
| **/tdd-implement** | jerseycheese/Narraitor | TDD实现 |

---

## 五、开发者工具技能 (更新)

### 5.1 编排工具

| 技能 | GitHub | 特点 |
|-----|--------|------|
| **agentsys** | avifenesh/agentsys | 生产级工作流自动化 |
| **superpowers** | obra/superpowers | 核心工程技能集 |
| **claude-code-agents** | undeadlist/claude-code-agents | E2E开发工作流 |
| **sudocode** | sudocode-ai/sudocode | 轻量级编排工具 |

### 5.2 安全审计

| 技能 | GitHub | 特点 |
|-----|--------|------|
| **trailofbits-skills** | trailofbits/skills | CodeQL/Semgrep集成 |
| **parry** | vaporif/parry | 提示注入扫描 |
| **Dippy** | ldayton/Dippy | AST智能命令批准 |

### 5.3 DevOps 工具

| 技能 | GitHub | 特点 |
|-----|--------|------|
| **cc-devops-skills** | akin-ozer/cc-devops-skills | IaC代码生成 |

### 5.4 Hooks 生态系统

| 技能 | GitHub | 功能 |
|-----|--------|------|
| **claude-hooks** | johnlindquist/claude-hooks | TypeScript Hook |
| **cchooks** | GowayLee/cchooks | Python Hook SDK |

---

## 六、热门技能推荐

### 6.1 按用途推荐

| 用途 | 首推技能 | 备选 |
|-----|---------|------|
| **游戏开发 (Unity)** | Claude-Code-Game-Studios | cc-plugin-unity-gamedev |
| **Python 后端** | pydantic-ai-skills | read-only-postgres |
| **Python 测试** | pytest + TDD | playwright-skill |
| **全栈开发** | fullstack-dev-skills (65+) | claude-code-templates |
| **DevOps** | cc-devops-skills | superpowers |
| **代码审查** | agentsys | claude-code-agents |
| **安全审计** | trailofbits-skills | parry |

### 6.2 技能组合推荐

```
游戏开发组合:
Claude-Code-Game-Studios + Unity Test Framework + playwright-skill

Python开发组合:
uv + pydantic-ai-skills + read-only-postgres + pytest

测试自动化组合:
playwright-skill + fieldwork-skills + claude-skills-marketplace
```

---

## 七、安装指南

### 7.1 快速安装

```bash
git clone https://github.com/用户名/技能名.git
cp -r 技能名 ~/.claude/skills/
```

### 7.2 验证安装

```bash
claude --list-skills
```

---

## 八、趋势分析

### 8.1 热门方向

| 方向 | 趋势 |
|-----|------|
| **Agent工作流** | ⬆️ 上升 |
| **安全审计** | ⬆️ 上升 |
| **游戏开发** | ⬆️ 上升 |
| **测试自动化** | ⬆️ 上升 |

### 8.2 技术栈分布

- TypeScript: 35+ 技能
- Python: 25+ 技能
- 测试框架: Playwright, Unity Test Framework, pytest

---

## 📎 相关资源

- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
- [awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills)
- [Antigravity Skills](https://github.com/sickn33/antigravity-awesome-skills)
- [Claude Code Handbook](https://nikiforovall.blog/claude-code-rules/)

---

*持续更新中，欢迎提交 PR 补充更多技能*
