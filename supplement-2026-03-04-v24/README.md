# Claude Code 热门插件补充调研 (第二十四期)

> 调研时间: 2026-03-04 | 数据来源: awesome-claude-code, GitHub trending

---

## 一、游戏客户端开发技能 (补充)

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

### 1.2 Unity 开发技能 (更新)

| 技能 | GitHub | Star | 特点 |
|-----|--------|------|------|
| **cc-plugin-unity-gamedev** | tjboudreaux/cc-plugin-unity-gamedev | ⭐1 | 21个专业技能，完整覆盖Unity开发栈 |
| **OH-Unity-GameDev-Skills** | OstrichHermit/OH-Unity-GameDev-Skills | ⭐6 | Unity基础开发+DoTween+MediaPipe |
| **unity-ai-workflow** | David-GD13/unity-ai-workflow | ⭐4 | Unity 6.2+ AI-first工作流 |

### 1.3 游戏开发技能汇总

| 方向 | 推荐技能 | Star | 特点 |
|-----|---------|------|------|
| **Unity 完整开发** | Claude-Code-Game-Studios | ⭐26 | 48代理全栈覆盖 |
| **Unity 基础** | cc-plugin-unity-gamedev | ⭐1 | 21技能专业栈 |
| **Unity AI工作流** | unity-ai-workflow | ⭐4 | Unity 6.2+ |
| **Godot** | claude-resources | ⭐3 | 开源游戏引擎 |

---

## 二、Python 开发技能

### 2.1 Python Web 开发

| 技能 | GitHub | Star | 特点 |
|-----|--------|------|------|
| **pydantic-ai-skills** | - | - | Pydantic AI 开发技能 |
| **uv** | - | - | 现代 Python 包管理 |
| **read-only-postgres** | jawwadfirdousi/agent-skills | - | 只读 PostgreSQL 查询 |

### 2.2 Python 测试与质量

| 技能 | GitHub | 功能 |
|-----|--------|------|
| **pytest** | - | Python 单元测试 |
| **/tdd** | zscott/pane | TDD 开发流程 |
| **/tdd-implement** | jerseycheese/Narraitor | TDD 实现 |

### 2.3 Python MCP 服务器

| 技能 | GitHub | 功能 |
|-----|--------|------|
| **aws-mcp-server** | - | AWS 云服务集成 |
| **cchooks** | GowayLee/cchooks | Python Hook SDK |

---

## 三、游戏客户端自动化测试

### 3.1 浏览器自动化测试

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **playwright-skill** | - | - | Web 游戏/H5 测试 |
| **playwright-mcp** | - | - | Playwright MCP 服务器 |

### 3.2 Unity 测试框架

| 技能 | GitHub | 功能 |
|-----|--------|------|
| **Unity Test Framework** | - | 单元测试、集成测试 |
| **Unity Profiler** | - | 帧率、内存测试 |

### 3.3 移动端游戏测试

| 平台 | 技能 | 功能 |
|-----|------|------|
| **Android** | ADB + uiautomator | UI自动化 |
| **iOS** | ios-simulator-skill | 模拟器测试 |

---

## 四、开发者工具技能 (补充)

### 4.1 编排工具

| 技能 | GitHub | 特点 |
|-----|--------|------|
| **agentsys** | avifenesh/agentsys | 生产级工作流自动化 |
| **superpowers** | obra/superpowers | 核心工程技能集 |
| **sudocode** | sudocode-ai/sudocode | 轻量级agent编排 |

### 4.2 安全审计

| 技能 | GitHub | 特点 |
|-----|--------|------|
| **trailofbits-skills** | trailofbits/skills | CodeQL/Semgrep集成 |
| **parry** | vaporif/parry | 提示注入扫描器 |

### 4.3 DevOps 工具

| 技能 | GitHub | 特点 |
|-----|--------|------|
| **cc-devops-skills** | akin-ozer/cc-devops-skills | IaC代码生成 |
| **ContextKit** | FlineDev/ContextKit | 4阶段规划方法论 |

### 4.4 Hooks 生态系统

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
| **Python 测试** | pytest + TDD | /tdd |
| **Web/H5游戏测试** | playwright-skill | - |
| **全栈开发** | fullstack-dev-skills (65+) | claude-code-templates |
| **DevOps** | cc-devops-skills | superpowers |

### 5.2 技能组合推荐

```
游戏开发组合:
Claude-Code-Game-Studios + Unity Test Framework + playwright-skill

Python开发组合:
uv + pydantic-ai-skills + read-only-postgres + pytest

测试自动化组合:
playwright-skill + fieldwork-skills
```

---

## 六、安装指南

### 6.1 快速安装

```bash
# 克隆技能仓库
git clone https://github.com/用户名/技能名.git

# 复制到 Claude Code 技能目录
cp -r 技能名 ~/.claude/skills/

# 或使用 claude install 命令
claude install github:用户名/技能名
```

---

*持续更新中...*
