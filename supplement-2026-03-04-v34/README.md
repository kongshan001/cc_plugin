# Claude Code 插件补充调研 - 第三十四期

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

## 一、Claude Code 生态系统概览

### 1.1 核心资源

| 资源 | 地址 | 说明 |
|-----|------|------|
| awesome-claude-code | [hesreallyhim/awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code) | 精选 Claude Code 技能/插件列表 |
| Antigravity Skills | [sickn33/antigravity-awesome-skills](https://github.com/sickn33/antigravity-awesome-skills) | 970+ 通用代理技能库 |
| Claude Code 官方插件 | [anthropics/claude-code/plugins](https://github.com/anthropics/claude-code/tree/main/plugins) | 13个官方插件 |
| 官方文档 | [docs.anthropic.com](https://docs.anthropic.com/en/docs/claude-code) | Claude Code 官方文档 |

### 1.2 官方插件列表

| 插件 | 描述 | 命令/代理 |
|-----|------|----------|
| **agent-sdk-dev** | Agent SDK 开发工具包 | /new-sdk-app, agent-sdk-verifier-py/ts |
| **claude-opus-4-5-migration** | 模型迁移工具 | claude-opus-4-5-migration skill |
| **code-review** | PR 代码审查 | /code-review, 5个并行审查代理 |
| **commit-commands** | Git 工作流自动化 | /commit, /commit-push-pr |
| **explanatory-output-style** | 教育性输出风格 | SessionStart hook |
| **feature-dev** | 功能开发工作流 | /feature-dev, 3个专业代理 |
| **frontend-design** | 前端设计技能 | 自动触发的前端设计指导 |
| **hookify** | 自定义 Hook 创建 | /hookify 系列命令 |
| **learning-output-style** | 交互式学习模式 | SessionStart hook |
| **plugin-dev** | 插件开发工具包 | /plugin-dev:create-plugin, 7个专家技能 |
| **pr-review-toolkit** | PR 审查工具包 | /pr-review-toolkit:review-pr, 6个审查代理 |
| **ralph-wiggum** | 迭代开发循环 | /ralph-loop, /cancel-ralph |
| **security-guidance** | 安全提醒 Hook | PreToolUse hook |

---

## 二、游戏客户端开发插件

### 2.1 Unity 开发 (重点)

#### 2.1.1 Claude-Code-Game-Studios ⭐ 推荐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [Donchitos/Claude-Code-Game-Studios](https://github.com/Donchitos/Claude-Code-Game-Studios) |
| **Star** | ⭐ 26 |
| **更新** | 3天前 |
| **特点** | 48个AI代理 + 36个工作流技能 + 完整协调系统 |

**核心能力:**
- 48个专业AI代理覆盖游戏开发全流程
- 36个工作流技能完整游戏开发管线
- 工作室协调系统模拟真实游戏工作室工作流
- 多引擎支持: Unity, Unreal, Godot, WebGL

#### 2.1.2 Unity 技能对比

| 技能 | GitHub | Star | 特点 |
|-----|--------|------|------|
| **cc-plugin-unity-gamedev** | tjboudreaux/cc-plugin-unity-gamedev | ⭐1 | 21个专业技能，完整覆盖Unity开发栈 |
| **OH-Unity-GameDev-Skills** | OstrichHermit/OH-Unity-GameDev-Skills | ⭐6 | Unity基础开发+DoTween+MediaPipe |
| **unity-ai-workflow** | David-GD13/unity-ai-workflow | ⭐4 | Unity 6.2+ AI-first工作流 |
| **solana-game-skill** | solanabr/solana-game-skill | ⭐5 | Solana区块链游戏开发 |

#### 2.1.3 Unity 技能核心分类

| 分类 | 技能 |
|-----|------|
| **工具类** | Addressables, MemoryPack, ScriptableObjects, Profiling |
| **动画/物理** | Animation, Physics, NavMesh, Object Pooling, State Machine |
| **AI/行为** | Behavior Designer, GAS (Gameplay Ability System) |
| **音视频** | Wwise音频, Cinemachine相机 |
| **UI** | UGUI, Mobile Optimization |
| **测试** | Unity Test Framework |
| **DI/异步** | VContainer, UniTask |

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

### 2.4 Web/H5 游戏开发

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

## 三、Python 开发插件

### 3.1 数据库集成

| 技能 | GitHub | 功能 | 安全性 |
|-----|--------|------|--------|
| **read-only-postgres** | jawwadfirdousi/agent-skills | PostgreSQL只读查询 | ⭐⭐⭐⭐⭐ |
| **postgres** | sanjay3290/ai-skills | PostgreSQL完整集成 | ⭐⭐⭐ |
| **mysql** | various | MySQL 集成技能 | ⭐⭐⭐ |

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

#### 核心能力

- **类型安全**: Pydantic 模型强制类型检查
- **渐进式提示**: 按需披露信息
- **AI 集成**: 与主流 LLM 无缝集成

### 3.3 Python Web 框架

| 框架 | 技能 | 描述 |
|-----|------|------|
| **Django** | various | 全栈 Web 框架 |
| **FastAPI** | various | 现代 Python Web 框架 |
| **Flask** | various | 轻量级 Web 框架 |

### 3.4 AWS 云服务集成

#### AWS MCP Server

| 项目 | 说明 |
|-----|------|
| **GitHub** | [alexei-led/aws-mcp-server](https://github.com/alexei-led/aws-mcp-server) |
| **语言** | Python |
| **特点** | AWS CLI 集成，多环境支持 |

**支持的服务:**

| 服务类别 | 支持内容 |
|---------|---------|
| **计算** | EC2, Lambda, ECS, EKS |
| **存储** | S3, EBS, EFS |
| **数据库** | RDS, DynamoDB, ElastiCache |
| **网络** | VPC, CloudFront, Route53 |
| **安全** | IAM, Secrets Manager |

---

## 四、自动化测试插件

### 4.1 Playwright 测试

| 技能 | 来源 | 描述 |
|-----|------|------|
| **playwright-testing** | Antigravity | Playwright 端到端测试 |
| **playwright-mcp** | [Bright/mcp](https://github.com/Bright/mcp) | Playwright MCP 服务器 |
| **go-playwright** | Antigravity | Go Playwright  语言绑定 |

#### Playwright 核心能力

```python
# 基础测试示例
def test_example(page):
    page.goto("https://example.com")
    page.click("#submit")
    expect(page.locator("#result")).to_be_visible()
```

### 4.2 Unity 测试

| 技能 | 来源 | 描述 |
|-----|------|------|
| **unity-test-framework** | cc-plugin-unity-gamedev | Unity 官方测试框架 |
| **nunit** | Unity | .NET 单元测试框架 |

### 4.3 pytest 测试

| 技能 | 来源 | 描述 |
|-----|------|------|
| **pytest** | various | Python 单元测试框架 |
| **pytest-cov** | various | 测试覆盖率 |

### 4.4 测试模式

| 模式 | 描述 |
|-----|------|
| **TDD** | 测试驱动开发 |
| **BDD** | 行为驱动开发 |
| **E2E** | 端到端测试 |
| **集成测试** | 模块集成测试 |
| **单元测试** | 最小单位测试 |

---

## 五、开发者工具插件

### 5.1 代码质量

| 技能 | 来源 | 描述 |
|-----|------|------|
| **superpowers** | [obra/superpowers](https://github.com/obra/superpowers) | 核心软件工程能力集 |
| **code-review** | 官方插件 | PR 代码审查 |
| **pr-review-toolkit** | 官方插件 | PR 审查工具包 |

### 5.2 安全工具

| 技能 | 来源 | 描述 |
|-----|------|------|
| **security-guidance** | 官方插件 | 安全提醒 Hook |
| **trailofbits-skills** | [trailofbits/skills](https://github.com/trailofbits/skills) | Trail of Bits 安全技能集 |

#### Trail of Bits 安全技能

| 技能 | 功能 |
|-----|------|
| **codeql** | CodeQL 静态分析 |
| **semgrep** | Semgrep 代码扫描 |
| **variant-analysis** | 变体分析 |

### 5.3 DevOps 工具

| 技能 | 来源 | 描述 |
|-----|------|------|
| **docker** | various | Docker 容器化 |
| **kubernetes** | various | Kubernetes 编排 |
| **aws-serverless** | various | AWS 无服务器架构 |

### 5.4 记忆/上下文工具

| 技能 | GitHub | 描述 |
|-----|--------|------|
| **claude-mem** | [thedotmack/claude-mem](https://github.com/thedotmack/claude-mem) | 自动捕获会话上下文并注入未来会话 |
| **beads** | [steveyegge/beads](https://github.com/steveyegge/beads) | 记忆升级工具 |

#### claude-mem 核心功能

- 自动捕获 Claude 在编码会话期间执行的操作
- 使用 AI 压缩（通过 Claude 的 agent-sdk）
- 将相关上下文注入未来会话

---

## 六、热门技能汇总

### 6.1 按方向分类

#### 游戏开发
| 技能 | Star | 特点 |
|-----|------|------|
| Claude-Code-Game-Studios | ⭐26 | 48代理全栈覆盖 |
| Unity 技能集 | ⭐6 | 21技能专业栈 |
| Godot 技能 | ⭐3 | 开源游戏引擎 |

#### Python 开发
| 技能 | Star | 特点 |
|-----|------|------|
| pydantic-ai-skills | ⭐136 | Pydantic AI 集成 |
| cc-devops-skills | ⭐⭐ | DevOps 工具集 |
| read-only-postgres | ⭐⭐ | 安全数据库查询 |

#### 自动化测试
| 技能 | Star | 特点 |
|-----|------|------|
| Playwright | ⭐⭐ | 浏览器自动化 |
| Unity Test | ⭐⭐ | 游戏测试 |
| pytest | ⭐⭐ | Python 测试 |

#### 开发者工具
| 技能 | Star | 特点 |
|-----|------|------|
| superpowers | ⭐⭐ | 核心工程能力 |
| AgentSys | ⭐⭐ | 工作流自动化 |
| Trail of Bits | ⭐⭐ | 安全审计 |

---

## 七、安装使用指南

### 7.1 安装 Claude Code

```bash
# MacOS/Linux
curl -fsSL https://claude.ai/install.sh | bash

# Windows
irm https://claude.ai/install.ps1 | iex
```

### 7.2 安装技能

```bash
# 克隆到 .claude/skills 目录
git clone https://github.com/hesreallyhim/awesome-claude-code.git ~/.claude/skills

# 使用 Antigravity 安装
npx antigravity-awesome-skills --claude
```

### 7.3 使用技能

```bash
# 在 Claude Code 中使用
/SKILL_NAME [your request]

# 或者
@skill-name to help with...
```

---

## 八、总结

### 8.1 关键发现

1. **游戏开发**: Claude-Code-Game-Studios (26 stars) 是最热门的游戏开发技能，提供48个专业代理
2. **Python 开发**: pydantic-ai-skills (136 stars) 是最热门的 Python 相关技能
3. **自动化测试**: Playwright 是浏览器自动化的主导框架
4. **开发者工具**: superpowers 和 AgentSys 提供全面的开发支持

### 8.2 趋势分析

- **多代理协作**: 越来越多技能采用多代理架构
- **专业化**: 针对特定框架(Unity, Unreal)和语言(Python, TypeScript)的技能增多
- **安全重视**: 安全相关技能和 Hook 越来越受关注
- **记忆/上下文**: 会话记忆和上下文管理工具兴起

---

## 参考链接

- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
- [antigravity-awesome-skills](https://github.com/sickn33/antigravity-awesome-skills)
- [Claude Code 官方插件](https://github.com/anthropics/claude-code/tree/main/plugins)
- [Claude Code 文档](https://docs.anthropic.com/en/docs/claude-code)

---

*文档更新时间: 2026-03-04*
*持续更新中...*
