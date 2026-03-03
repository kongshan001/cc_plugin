# Claude Code 插件补充调研 - 2026年3月4日 (第四期补充)

## 📋 调研背景

本期调研继续深入分析 Claude Code 热门插件，基于 Antigravity Awesome Skills (968+ Skills) 和 Awesome Claude Code 社区资源，重点关注：
1. 游戏客户端开发 (Unity、Web/H5)
2. Python 开发
3. 游戏客户端自动化测试
4. 其他开发者工具

---

## 一、热门插件深度分析

### 1.1 游戏开发方向 ⭐

#### Claude-Code-Game-Studios (重点推荐)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [Donchitos/Claude-Code-Game-Studios](https://github.com/Donchitos/Claude-Code-Game-Studios) |
| **Star** | ⭐ 26+ |
| **更新** | 3天前活跃 |
| **特点** | 48个AI代理 + 36个工作流技能 |

**核心能力:**
- 48个专业AI代理覆盖游戏开发全流程
- 36个工作流技能完整游戏开发管线
- 工作室协调系统模拟真实游戏工作室工作流
- 多引擎支持: Unity, Unreal, Godot, WebGL

#### Unity 开发技能对比

| 技能 | GitHub | Star | 特点 |
|-----|--------|------|------|
| **cc-plugin-unity-gamedev** | tjboudreaux/cc-plugin-unity-gamedev | ⭐1 | 21个专业技能，完整覆盖Unity开发栈 |
| **OH-Unity-GameDev-Skills** | OstrichHermit/OH-Unity-GameDev-Skills | ⭐6 | Unity基础开发+DoTween+MediaPipe |
| **unity-ai-workflow** | David-GD13/unity-ai-workflow | ⭐4 | Unity 6.2+ AI-first工作流 |
| **solana-game-skill** | solanabr/solana-game-skill | ⭐5 | Solana区块链游戏开发 |

#### 游戏引擎技能汇总

| 方向 | 推荐技能 | Star | 特点 |
|-----|---------|------|------|
| **Unity 完整开发** | Claude-Code-Game-Studios | ⭐26 | 48代理全栈覆盖 |
| **Unity 基础** | cc-plugin-unity-gamedev | ⭐1 | 21技能专业栈 |
| **Unity AI工作流** | unity-ai-workflow | ⭐4 | Unity 6.2+ |
| **Godot** | claude-resources | ⭐3 | 开源游戏引擎 |
| **GameMaker** | gamemaker-skills | ⭐2 | 2D游戏专用 |
| **Solana链游** | solana-game-skill | ⭐5 | 区块链游戏 |

---

### 1.2 Python 开发方向 ⭐

#### uv - Python 包管理器 (2025最快)

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

#### pydantic-ai-skills

| 项目 | 说明 |
|-----|------|
| **GitHub** | [DougTrajano/pydantic-ai-skills](https://github.com/DougTrajano/pydantic-ai-skills) |
| **Star** | ⭐ 136 |

**核心能力:**
- Pydantic AI 深度集成
- 类型安全强制类型检查
- 渐进式提示按需披露信息
- 与主流 LLM 无缝集成

#### 数据库技能

| 技能 | GitHub | 功能 | 安全性 |
|-----|--------|------|--------|
| **read-only-postgres** | jawwadfirdousi/agent-skills | PostgreSQL只读查询 | ⭐⭐⭐⭐⭐ |
| **postgres** | sanjay3290/ai-skills | PostgreSQL完整集成 | ⭐⭐⭐ |

#### Python 测试技能

| 技能 | 功能 | 适用场景 |
|-----|------|---------|
| **pytest** | 单元测试/集成测试 | Python项目测试 |
| **pytest-cov** | 覆盖率报告 | 代码覆盖率分析 |
| **pytest-asyncio** | 异步测试 | 异步代码测试 |

---

### 1.3 游戏客户端自动化测试 ⭐

#### Playwright 技能

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **playwright-skill** | lackeyjb/playwright-skill | ⭐1.8k | Playwright浏览器自动化 |
| **playwright-undetected-skill** | dalbit-mir/playwright-undetected-skill | ⭐4 | Bot检测绕过 |

#### Unity 测试方案

| 测试类型 | 方案 | 适用场景 |
|---------|------|---------|
| **Web/H5游戏** | Playwright | 功能测试、回归测试 |
| **Unity游戏** | Unity Test Framework | 单元测试、集成测试 |
| **性能测试** | Unity Profiler | 帧率、内存测试 |
| **Android游戏** | ADB + uiautomator | UI自动化 |
| **iOS游戏** | ios-simulator-skill | 模拟器测试 |

#### 移动端游戏测试

##### Android UI 测试

```bash
# 设备校准 - 获取屏幕分辨率
adb shell wm size

# UI 检查 - 获取元素信息
adb shell uiautomator dump /sdcard/view.xml

# 交互操作
adb shell input tap <x> <y>
adb shell input swipe <x1> <y1> <x2> <y2> <duration_ms>
```

##### iOS 模拟器测试

| 项目 | 说明 |
|-----|------|
| **GitHub** | [conorluddy/ios-simulator-skill](https://github.com/conorluddy/ios-simulator-skill) |
| **Star** | ⭐ 557 |
| **平台** | macOS |

---

### 1.4 开发者工具方向 ⭐

#### 编排工具

| 技能 | GitHub | 特点 |
|-----|--------|------|
| **agentsys** | avifenesh/agentsys | 生产级工作流自动化 |
| **superpowers** | obra/superpowers | 核心工程技能集 |
| **claude-code-agents** | undeadlist/claude-code-agents | E2E开发工作流 |
| **sudocode** | sudocode-ai/sudocode | 轻量级agent编排工具 |

#### 安全审计

| 技能 | GitHub | 特点 |
|-----|--------|------|
| **trailofbits-skills** | trailofbits/skills | CodeQL/Semgrep集成 |
| **parry** | vaporif/parry | 提示注入扫描器 |
| **Dippy** | ldayton/Dippy | AST自动批准安全命令 |

#### Claude Code Pro

| 技能 | GitHub | 特点 |
|-----|--------|------|
| **Claude CodePro** | maxritter/claude-codepro | TDD强制执行，质量挂钩 |

#### DevOps 工具

| 技能 | GitHub | 特点 |
|-----|--------|------|
| **cc-devops-skills** | akin-ozer/cc-devops-skills | IaC代码生成 |
| **ContextKit** | FlineDev/ContextKit | 4阶段规划方法论 |

#### Hooks 生态系统

| 技能 | GitHub | 功能 |
|-----|--------|------|
| **claude-hooks** | johnlindquist/claude-hooks | TypeScript Hook 系统 |
| **cchooks** | GowayLee/cchooks | Python Hook SDK |
| **claude-code-hooks-sdk** | beyondcode/claude-hooks-sdk | PHP Hook SDK |

#### 会话管理

| 技能 | GitHub | 功能 |
|-----|--------|------|
| **claude-tmux** | nielsgroen/claude-tmux | tmux会话管理 |
| **claude-esp** | phiat/claude-esp | 隐藏输出流式传输 |
| **ralph-claude-code** | frankbria/ralph-claude-code | 自主开发框架，75+测试 |

---

## 二、Skills 统计汇总

| 类别 | Skills 数量 | 热门 Skills |
|------|------------|------------|
| 游戏开发 | 15+ | game-development, unity-developer, multiplayer, unity-ecs-patterns |
| Python 开发 | 18+ | python-pro, async-python-patterns, fastapi, uv-package-manager |
| 自动化测试 | 20+ | playwright-skill, e2e-testing, test-automator, python-testing-patterns |
| 开发者工具 | 25+ | github-automation, browser-automation, cicd-automation, docker-expert |

---

## 三、补充技能推荐

### 3.1 按场景推荐

| 场景 | 首推技能 | 安装命令 |
|-----|---------|---------|
| **Unity游戏开发** | Claude-Code-Game-Studios | gh-Donchitos-Claude-Code-Game-Studios |
| **Unity AI工作流** | unity-ai-workflow | gh-David-GD13-unity-ai-workflow |
| **Web游戏测试** | playwright-skill | gh-lackeyjb-playwright-skill |
| **反检测测试** | playwright-undetected-skill | gh-dalbit-mir-playwright-undetected-skill |
| **Python AI开发** | pydantic-ai-skills | gh-DougTrajano-pydantic-ai-skills |
| **数据库查询** | read-only-postgres | gh-jawwadfirdousi-read-only-postgres |
| **安全审计** | trailofbits-skills | gh-trailofbits-skills |
| **包管理** | uv | gh-astral-sh-uv |
| **自主开发** | ralph-claude-code | gh-frankbria-ralph-claude-code |
| **工作流编排** | agentsys | gh-avifenesh-agentsys |

### 3.2 技能组合推荐

```
游戏开发组合:
Claude-Code-Game-Studios + Unity Test Framework + playwright-skill

Python开发组合:
uv + pydantic-ai-skills + read-only-postgres + pytest + aws-mcp-server

测试自动化组合:
playwright-skill + fieldwork-skills + claude-skills-marketplace

游戏帧同步测试:
Unity Test Framework + 网络延迟模拟 + 帧同步确定性验证
```

---

## 四、趋势分析

### 4.1 热门方向

| 方向 | 趋势 | 说明 |
|-----|------|------|
| **Agent工作流** | ⬆️ 上升 | agentsys, claude-code-agents, Claude Code Flow |
| **安全审计** | ⬆️ 上升 | trailofbits-skills, parry, Dippy |
| **游戏开发** | ⬆️ 上升 | Claude-Code-Game-Studio 全栈覆盖 |
| **测试自动化** | ⬆️ 上升 | Playwright主导，TDD命令丰富 |
| **Hook 生态** | ⬆️ 上升 | 多语言 SDK (Python, PHP, TypeScript) |

### 4.2 技术栈分布

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
```

---

## 五、安装指南

### 5.1 快速安装

```bash
# 克隆技能仓库
git clone https://github.com/用户名/技能名.git

# 复制到 Claude Code 技能目录
cp -r 技能名 ~/.claude/skills/

# 或使用技能安装命令
claude --install-skill gh-用户名-技能名
```

### 5.2 验证安装

```bash
# 列出已安装技能
claude --list-skills

# 或在 Claude Code 中输入
/skill list
```

---

## 📎 相关资源

- [Claude-Code-Game-Studios](https://github.com/Donchitos/Claude-Code-Game-Studios)
- [unity-ai-workflow](https://github.com/David-GD13/unity-ai-workflow)
- [playwright-skill](https://github.com/lackeyjb/playwright-skill)
- [playwright-undetected-skill](https://github.com/dalbit-mir/playwright-undetected-skill)
- [pydantic-ai-skills](https://github.com/DougTrajano/pydantic-ai-skills)
- [read-only-postgres](https://github.com/jawwadfirdousi/agent-skills)
- [uv](https://github.com/astral-sh/uv)
- [ralph-claude-code](https://github.com/frankbria/ralph-claude-code)
- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
- [antigravity-awesome-skills](https://github.com/sickn33/antigravity-awesome-skills)
- [Claude Code Handbook](https://nikiforovall.blog/claude-code-rules/)
- [Claude Code Ultimate Guide](https://github.com/FlorianBruniaux/claude-code-ultimate-guide)

---

*补充调研完成 - 2026年3月4日*
