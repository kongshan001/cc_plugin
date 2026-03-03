# Claude Code 热门插件补充调研 (2026-03-04 第十五期)

## 📋 文档信息

- **调研日期**: 2026-03-04
- **分类**: 游戏客户端开发 / Python 开发 / 自动化测试 / 开发者工具
- **状态**: ✅ 补充调研第十五期
- **来源**: awesome-claude-code + Antigravity Skills + GitHub 搜索

---

## 1. 游戏客户端开发技能补充

### 1.1 Claude Code Game Studios (新增 ⭐⭐⭐⭐⭐)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [Donchitos/Claude-Code-Game-Studios](https://github.com/Donchitos/Claude-Code-Game-Studios) |
| **Star** | ⭐ 26 (增长中) |
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

### 1.2 Unity 技能补充

#### cc-plugin-unity-gamedev

| 项目 | 说明 |
|-----|------|
| **GitHub** | [tjboudreaux/cc-plugin-unity-gamedev](https://github.com/tjboudreaux/cc-plugin-unity-gamedev) |
| **Star** | ⭐ 1 |
| **技能数量** | 21 个专业化技能 |

**技能分类**:

| 类别 | 数量 | 包含内容 |
|-----|-----|---------|
| 工具类 | 8 | Addressables, MemoryPack, ScriptableObjects, Profiling |
| 动画/物理 | 5 | Animation, Physics, NavMesh, Object Pooling |
| AI/行为 | 2 | Behavior Designer, GAS |
| UI | 2 | UGUI, Mobile Optimization |
| 测试 | 1 | Unity Test Framework |

#### unity-ai-workflow (2026 新增)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [David-GD13/unity-ai-workflow](https://github.com/David-GD13/unity-ai-workflow) |
| **Star** | ⭐ 4 |
| **特点** | Unity 6.2+ AI-first 开发工作流 |

**Dev Modes**:

| 模式 | 角色 | 适用场景 |
|------|------|---------|
| Assistant | 你构建，AI 辅助文档和解释 | 学习、创意控制 |
| Mix (默认) | 协作模式，AI 建议，你确认 | 大多数项目 |
| Automatic | AI 构建，短的 onboarding Q&A | 快速原型 |

### 1.3 游戏开发技能汇总表

| 方向 | 推荐技能 | Star | 特点 |
|-----|---------|------|------|
| **Unity 完整开发** | Claude-Code-Game-Studios | ⭐26 | 48代理全栈覆盖 |
| **Unity 基础** | cc-plugin-unity-gamedev | ⭐1 | 21技能专业栈 |
| **Unity AI工作流** | unity-ai-workflow | ⭐4 | Unity 6.2+ |
| **Godot** | claude-resources | ⭐3 | 开源游戏引擎 |
| **GameMaker** | gamemaker-skills | ⭐2 | 2D游戏专用 |
| **通用游戏** | game-development | - | Antigravity 编排器 |

---

## 2. Python 开发技能补充

### 2.1 Python 项目脚手架 (python-development-python-scaffold)

| 项目 | 说明 |
|-----|------|
| **来源** | Antigravity Skills |
| **评分** | 1.0+ |

#### 核心能力

```bash
# 项目初始化
uv init <project-name>
cd <project-name>

# 支持的项目类型
- FastAPI: REST APIs, microservices
- Django: Full-stack web
- Library: Reusable packages
- CLI: Command-line tools
```

#### 项目结构模板

```
project/
├── pyproject.toml
├── src/
│   └── project_name/
│       ├── __init__.py
│       ├── main.py
│       ├── api/
│       ├── core/
│       ├── models/
│       └── services/
└── tests/
```

### 2.2 Python 测试模式 (python-testing-patterns)

| 项目 | 说明 |
|-----|------|
| **来源** | Antigravity Skills |
| **核心** | pytest + 自动化测试最佳实践 |

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
```

### 2.3 数据库集成

#### read-only-postgres

| 项目 | 说明 |
|-----|------|
| **GitHub** | jawwadfirdousi/agent-skills |
| **安全等级** | ⭐⭐⭐⭐⭐ 只读 |

**支持的查询**:

```sql
SELECT * FROM users WHERE id = 1;
SHOW max_connections;
EXPLAIN ANALYZE SELECT * FROM orders;
WITH recent AS (...) SELECT * FROM recent;
```

### 2.4 uv - Python 包管理器 (2025最快)

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
```

### 2.5 Python Skills 汇总

| Skill | 核心能力 | 适用场景 |
|-------|---------|---------|
| python-pro | Python 3.12+ 全栈 | 通用开发 |
| python-patterns | 开发原则和决策 | 架构设计 |
| python-fastapi-development | FastAPI 后端 | API 服务 |
| python-testing-patterns | pytest/测试策略 | 质量保证 |
| async-python-patterns | asyncio 异步 | 高并发 |
| temporal-python-pro | Temporal 工作流 | 分布式事务 |

---

## 3. 自动化测试技能补充

### 3.1 Playwright 浏览器自动化 (playwright-skill)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [lackeyjb/playwright-skill](https://github.com/lackeyjb/playwright-skill) |
| **Star** | ⭐ 1.8k |
| **特点** | 完整浏览器自动化 |

#### 核心功能

- **Web 应用测试**: 自动化测试 Web 应用功能
- **UI 验证**: 验证前端功能和行为
- **截图捕获**: 自动截图记录测试状态
- **调试支持**: 辅助调试 UI 行为
- **反检测**: Patchright 支持绕过 Bot 检测

#### 使用流程

```bash
# 1. 检测开发服务器
cd $SKILL_DIR && node -e "require('./lib/helpers').detectDevServers().then(s => console.log(JSON.stringify(s)))"

# 2. 编写测试脚本到 /tmp
# /tmp/playwright-test-page.js

# 3. 执行测试
cd $SKILL_DIR && node run.js /tmp/playwright-test-*.js
```

### 3.2 游戏客户端测试方案

| 测试类型 | 方案 | 适用场景 |
|---------|------|---------|
| **Web/H5游戏** | Playwright | 功能测试、回归测试 |
| **Unity游戏** | Unity Test Framework | 单元测试、集成测试 |
| **性能测试** | Unity Profiler | 帧率、内存测试 |
| **Android游戏** | ADB + uiautomator | UI自动化 |
| **iOS游戏** | ios-simulator-skill | 模拟器测试 |

### 3.3 移动端游戏测试

#### Android UI 测试

```bash
# 设备校准 - 获取屏幕分辨率
adb shell wm size

# UI 检查 - 获取元素信息
adb shell uiautomator dump /sdcard/view.xml

# 交互操作
adb shell input tap <x> <y>
adb shell input swipe <x1> <y1> <x2> <y2> <duration_ms>
```

#### iOS 模拟器测试

| 项目 | 说明 |
|-----|------|
| **GitHub** | [conorluddy/ios-simulator-skill](https://github.com/conorluddy/ios-simulator-skill) |
| **Star** | ⭐ 557 |

 3.4### TDD 开发技能

| 命令 | 来源 | 功能 |
|-----|------|------|
| **/tdd** | zscott/pane | TDD开发流程 |
| **/tdd-implement** | jerseycheese/Narraitor | TDD实现 |
| **/repro-issue** | rzykov/metabase | 可复现测试用例 |
| **/check** | rygwdn/slack-tools | 代码质量检查 |
| **/clean** | Graphlet-AI/eridu | 代码格式化 |

### 3.5 测试质量工具

| Skill | GitHub | Star | 功能 |
|-------|--------|------|------|
| **claude-skills-marketplace** | mhattingpete/claude-skills-marketplace | ⭐427 | 测试/代码审查 |
| **fieldwork-skills** | buildoak/fieldwork-skills | ⭐12 | E2E测试/Bug修复 |

---

## 4. 开发者工具技能补充

### 4.1 编排工具

| Skill | GitHub | 特点 |
|-------|--------|------|
| **agentsys** | avifenesh/agentsys | 生产级工作流自动化 |
| **superpowers** | obra/superpowers | 核心工程技能集 |
| **claude-code-agents** | undeadlist/claude-code-agents | E2E开发工作流 |

### 4.2 安全审计

| Skill | GitHub | 特点 |
|-------|--------|------|
| **trailofbits-skills** | trailofbits/skills | CodeQL/Semgrep集成 |
| **parry** | vaporif/parry | 提示注入扫描器 |

### 4.3 Claude Code Pro

| Skill | GitHub | 特点 |
|-------|--------|------|
| **Claude CodePro** | maxritter/claude-codepro | TDD强制执行 |

### 4.4 DevOps 工具

| Skill | GitHub | 特点 |
|-------|--------|------|
| **cc-devops-skills** | akin-ozer/cc-devops-skills | IaC代码生成 |
| **ContextKit** | FlineDev/ContextKit | 4阶段规划方法论 |

### 4.5 Hooks 生态系统

| Skill | GitHub | 功能 |
|-------|--------|------|
| **claude-hooks** | johnlindquist/claude-hooks | TypeScript Hook 系统 |
| **cchooks** | GowayLee/cchooks | Python Hook SDK |

### 4.6 会话管理

| Skill | GitHub | 功能 |
|-------|--------|------|
| **claude-tmux** | nielsgroen/claude-tmux | tmux会话管理 |
| **ralph-claude-code** | frankbria/ralph-claude-code | 自主开发框架，75+测试 |

---

## 5. 技能选择决策树

### 5.1 游戏客户端开发

```
游戏客户端开发?
├─ Unity → Claude-Code-Game-Studios
├─ Godot → claude-resources
├─ GameMaker → gamemaker-skills
├─ Web/H5 → playwright-skill
└─ 通用 → Antigravity Skills
```

### 5.2 Python 开发

```
Python 开发?
├─ Web框架 → python-fastapi-development
├─ 数据库 → read-only-postgres
├─ 云服务 → aws-mcp-server
└─ 测试 → python-testing-patterns
```

### 5.3 自动化测试

```
自动化测试?
├─ 浏览器 → playwright-skill
├─ 单元测试 → Unity Test Framework
├─ 代码质量 → /check, /clean
└─ TDD → /tdd-implement
```

---

## 6. 技能组合推荐

### 6.1 游戏开发组合

```
Claude-Code-Game-Studios + Unity Test Framework + playwright-skill
```

### 6.2 Python开发组合

```
uv + python-development-python-scaffold + python-testing-patterns + pytest
```

### 6.3 测试自动化组合

```
playwright-skill + fieldwork-skills + claude-skills-marketplace
```

---

## 7. 安装指南

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

---

## 📎 相关资源

- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
- [awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills)
- [Antigravity Skills](https://github.com/AntigravityDevOrg/antigravity-awesome-skills)
- [Claude Code Handbook](https://nikiforovall.blog/claude-code-rules/)

---

*持续更新中，欢迎提交 PR 补充更多技能*
