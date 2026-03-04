# Claude Code 插件补充调研 (第三十八期)

> 聚焦: 游戏客户端开发 | Python 开发 | 自动化测试 | 开发者工具

---

## 一、游戏客户端开发技能 (更新)

### 1.1 Claude Code Game Studios ⭐ 26

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

### 1.2 Unity 开发技能

| 技能 | GitHub | Star | 特点 |
|-----|--------|------|------|
| **cc-plugin-unity-gamedev** | tjboudreaux/cc-plugin-unity-gamedev | ⭐1 | 21个专业技能，完整覆盖Unity开发栈 |
| **OH-Unity-GameDev-Skills** | OstrichHermit/OH-Unity-GameDev-Skills | ⭐6 | Unity基础开发+DoTween+MediaPipe |
| **unity-ai-workflow** | David-GD13/unity-ai-workflow | ⭐4 | Unity 6.2+ AI-first工作流 |

### 1.3 Web/H5 游戏开发

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

### 1.4 游戏开发技能汇总

| 方向 | 推荐技能 | Star | 特点 |
|-----|---------|------|------|
| **Unity 完整开发** | Claude-Code-Game-Studios | ⭐26 | 48代理全栈覆盖 |
| **Unity 基础** | cc-plugin-unity-gamedev | ⭐1 | 21技能专业栈 |
| **Godot** | claude-resources | ⭐3 | 开源游戏引擎 |
| **GameMaker** | gamemaker-skills | ⭐2 | 2D游戏专用 |

---

## 二、Python 开发技能 (更新)

### 2.1 数据库集成

| 技能 | GitHub | 功能 | 安全性 |
|-----|--------|------|--------|
| **read-only-postgres** | jawwadfirdousi/agent-skills | PostgreSQL只读查询 | ⭐⭐⭐⭐⭐ |
| **postgres** | sanjay3290/ai-skills | PostgreSQL完整集成 | ⭐⭐⭐ |

### 2.2 AI 框架集成

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **pydantic-ai-skills** | DougTrajano/pydantic-ai-skills | ⭐136 | Pydantic AI 深度集成 |

### 2.3 uv - Python 包管理器

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

### 2.4 开发者工具包

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **developer-kit** | giuseppe-trisciuoglio/developer-kit | ⭐128 | 模块化插件系统 |
| **claude-code-tools** | pchalasani/claude-code-tools | - | 会话连续性工具 |
| **claudekit** | carlrannaberg/claudekit | - | CLI工具包，20+子代理 |

### 2.5 Python Skills 汇总

| Skill 名称 | 核心能力 | 适用场景 |
|-----------|---------|---------|
| python-pro | Python 3.12+ 全栈指南 | 通用 Python 开发 |
| python-patterns | 开发原则和决策 | 架构设计 |
| python-fastapi-development | FastAPI 后端开发 | API 服务 |
| python-testing-patterns | pytest/测试策略 | 质量保证 |

---

## 三、自动化测试技能 (更新)

### 3.1 浏览器自动化

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **playwright-skill** | lackeyjb/playwright-skill | ⭐1.8k | Playwright浏览器自动化 |
| **playwright-undetected-skill** | dalbit-mir/playwright-undetected-skill | ⭐4 | Bot检测绕过 |

#### Playwright 核心功能

- **Web 应用测试**: 自动化测试 Web 应用功能
- **UI 验证**: 验证前端功能和行为
- **截图捕获**: 自动截图记录测试状态
- **调试支持**: 辅助调试 UI 行为
- **反检测**: Patchright 支持绕过 Bot 检测

### 3.2 游戏客户端测试方案

| 测试类型 | 方案 | 适用场景 |
|---------|------|---------|
| **Web/H5游戏** | Playwright | 功能测试、回归测试 |
| **Unity游戏** | Unity Test Framework | 单元测试、集成测试 |
| **性能测试** | Unity Profiler | 帧率、内存测试 |
| **Android游戏** | ADB + uiautomator | UI自动化 |

### 3.3 测试质量工具

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **claude-skills-marketplace** | mhattingpete/claude-skills-marketplace | ⭐427 | 测试/代码审查 |
| **fieldwork-skills** | buildoak/fieldwork-skills | ⭐12 | E2E测试/Bug修复 |

---

## 四、开发者工具技能 (更新)

### 4.1 编排工具

| 技能 | GitHub | 特点 |
|-----|--------|------|
| **agentsys** | avifenesh/agentsys | 生产级工作流自动化 |
| **superpowers** | obra/superpowers | 核心工程技能集 |
| **claude-code-agents** | undeadlist/claude-code-agents | E2E开发工作流 |
| **sudocode** | sudocode-ai/sudocode | 轻量级agent编排工具 |

### 4.2 安全审计

| 技能 | GitHub | 特点 |
|-----|--------|------|
| **trailofbits-skills** | trailofbits/skills | CodeQL/Semgrep集成 |
| **parry** | vaporif/parry | 提示注入扫描器 |
| **Dippy** | ldayton/Dippy | AST自动批准安全命令 |

### 4.3 Claude Code Pro

| 技能 | GitHub | 特点 |
|-----|--------|------|
| **Claude CodePro** | maxritter/claude-codepro | TDD强制执行，质量挂钩 |

### 4.4 DevOps 工具

| 技能 | GitHub | 特点 |
|-----|--------|------|
| **cc-devops-skills** | akin-ozer/cc-devops-skills | IaC代码生成 |
| **ContextKit** | FlineDev/ContextKit | 4阶段规划方法论 |

### 4.5 Hooks 生态系统

| 技能 | GitHub | 功能 |
|-----|--------|------|
| **claude-hooks** | johnlindquist/claude-hooks | TypeScript Hook 系统 |
| **cchooks** | GowayLee/cchooks | Python Hook SDK |
| **claude-code-hooks-sdk** | beyondcode/claude-hooks-sdk | PHP Hook SDK |

---

## 五、热门技能推荐

### 5.1 按用途推荐

| 用途 | 首推技能 | 备选 |
|-----|---------|------|
| **游戏开发 (Unity)** | Claude-Code-Game-Studios | cc-plugin-unity-gamedev |
| **Python 后端** | pydantic-ai-skills | read-only-postgres |
| **Python 测试** | pytest + TDD | playwright-skill |
| **Web/H5游戏测试** | playwright-skill | playwright-undetected |
| **全栈开发** | fullstack-dev-skills (65+) | claude-code-templates |
| **DevOps** | cc-devops-skills | superpowers |
| **代码审查** | agentsys | claude-code-agents |
| **安全审计** | trailofbits-skills | parry |

---

## 六、安装指南

### 6.1 快速安装

```bash
# 克隆技能仓库
git clone https://github.com/用户名/技能名.git

# 复制到 Claude Code 技能目录
cp -r 技能名 ~/.claude/skills/
```

### 6.2 验证安装

```bash
# 列出已安装技能
claude --list-skills
```

---

## 📎 相关资源

- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
- [awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills)
- [Claude Code Handbook](https://nikiforovall.blog/claude-code-rules/)
- [Claude Code Ultimate Guide](https://github.com/FlorianBruniaux/claude-code-ultimate-guide)

---

*持续更新中，欢迎提交 PR 补充更多技能*
