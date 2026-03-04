# Claude Code 热门插件补充调研 (第二十五期)

> 调研时间: 2026-03-04 | 数据来源: awesome-claude-code, GitHub trending

---

## 一、游戏客户端开发技能 (新增)

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

#### 工作室层级架构

| 层级 | 代理 | 描述 |
|------|------|------|
| **Tier 1** | creative-director, technical-director, producer | 决策层 (Opus) |
| **Tier 2** | game-designer, lead-programmer, art-director, qa-lead | 部门lead (Sonnet) |
| **Tier 3** | gameplay-programmer, ui-programmer, tools-programmer |  specialist (Sonnet/Haiku) |

#### 适用场景

- 大型游戏项目开发
- 游戏工作室工作流自动化
- 跨团队协作开发
- 全栈游戏开发

### 1.2 Unity 开发技能 (更新)

| 技能 | GitHub | Star | 特点 |
|-----|--------|------|------|
| **cc-plugin-unity-gamedev** | tjboudreaux/cc-plugin-unity-gamedev | ⭐1 | 21个专业技能，完整覆盖Unity开发栈 |
| **OH-Unity-GameDev-Skills** | OstrichHermit/OH-Unity-GameDev-Skills | ⭐6 | Unity基础开发+DoTween+MediaPipe |
| **unity-ai-workflow** | David-GD13/unity-ai-workflow | ⭐4 | Unity 6.2+ AI-first工作流 |

#### Unity 技能核心分类

| 分类 | 技能 |
|-----|------|
| **工具类** | Addressables, MemoryPack, ScriptableObjects, Profiling |
| **动画/物理** | Animation, Physics, NavMesh, Object Pooling, State Machine |
| **AI/行为** | Behavior Designer, GAS (Gameplay Ability System) |
| **音视频** | Wwise音频, Cinemachine相机 |
| **UI** | UGUI, Mobile Optimization |
| **测试** | Unity Test Framework |
| **DI/异步** | VContainer, UniTask |

### 1.3 Godot 开发技能

| 项目 | GitHub | Star | 说明 |
|-----|--------|------|------|
| **claude-resources** | kwhitejr/claude-resources | ⭐3 | Godot游戏开发自定义代理和技能 |

### 1.4 GameMaker 开发技能

| 项目 | GitHub | Star | 说明 |
|-----|--------|------|------|
| **gamemaker-skills** | leihaht/gamemaker-skills | ⭐2 | GameMaker Studio 2和GML开发技能 |

### 1.5 游戏开发技能汇总

| 方向 | 推荐技能 | Star | 特点 |
|-----|---------|------|------|
| **Unity 完整开发** | Claude-Code-Game-Studios | ⭐26 | 48代理全栈覆盖 |
| **Unity 基础** | cc-plugin-unity-gamedev | ⭐1 | 21技能专业栈 |
| **Unity AI工作流** | unity-ai-workflow | ⭐4 | Unity 6.2+ |
| **Godot** | claude-resources | ⭐3 | 开源游戏引擎 |
| **GameMaker** | gamemaker-skills | ⭐2 | 2D游戏开发 |

---

## 二、Python 开发技能 (补充)

### 2.1 Pydantic AI 技能 ⭐ 推荐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [DougTrajano/pydantic-ai-skills](https://github.com/DougTrajano/pydantic-ai-skills) |
| **Star** | ⭐ 136 |
| **特点** | Agent Skills 渐进式披露支持 |

#### 核心特性

- **渐进式披露**: 按需加载技能信息，减少token消耗
- **类型安全**: Python dataclasses和类型提示
- **验证**: 技能元数据和结构自动验证
- **多目录**: 支持从多个来源加载技能

### 2.2 Python Web 框架技能

| 技能 | GitHub | 功能 |
|-----|--------|------|
| **Django/Flask/FastAPI** | - | Web应用开发 |
| **aws-mcp-server** | alexei-led/aws-mcp-server | AWS CLI集成 |
| **read-only-postgres** | jawwadfirdousi/agent-skills | PostgreSQL只读查询 |

#### AWS MCP Server 支持服务

| 服务类别 | 支持内容 |
|---------|---------|
| **计算** | EC2, Lambda, ECS, EKS |
| **存储** | S3, EBS, EFS |
| **数据库** | RDS, DynamoDB, ElastiCache |
| **网络** | VPC, CloudFront, Route53 |
| **安全** | IAM, Secrets Manager |

### 2.3 Python 测试与质量

| 技能 | GitHub | 功能 |
|-----|--------|------|
| **pytest** | - | Python单元测试 |
| **/tdd** | zscott/pane | TDD开发流程 |
| **/tdd-implement** | jerseycheese/Narraitor | TDD实现 |

### 2.4 Python MCP 服务器

| 技能 | GitHub | 功能 |
|-----|--------|------|
| **cchooks** | GowayLee/cchooks | Python Hook SDK |
| **aws-mcp-server** | alexei-led/aws-mcp-server | AWS云服务集成 |

---

## 三、游戏客户端自动化测试 (补充)

### 3.1 浏览器自动化测试

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **playwright-skill** | lackeyjb/playwright-skill | ⭐1.8k | Playwright浏览器自动化 |
| **playwright-undetected-skill** | dalbit-mir/playwright-undetected-skill | ⭐4 | Bot检测绕过 |
| **playwright-mcp** | - | - | Playwright MCP服务器 |

#### 核心功能

- **Web应用测试**: 自动化测试Web应用功能
- **UI验证**: 验证前端功能和行为
- **截图捕获**: 自动截图记录测试状态
- **调试支持**: 辅助调试UI行为
- **Bot检测绕过**: Patchright支持反检测

### 3.2 Unity 测试框架

| 技能 | GitHub | 功能 |
|-----|--------|------|
| **Unity Test Framework** | - | 单元测试、集成测试 |
| **Unity Profiler** | - | 帧率、内存测试 |

### 3.3 移动端游戏测试

| 平台 | 技能 | Star | 功能 |
|-----|------|------|------|
| **iOS** | ios-simulator-skill | ⭐558 | iOS模拟器测试 |
| **Android** | ADB + uiautomator | - | UI自动化 |

### 3.4 自动化测试技能汇总

| 方向 | 推荐技能 | Star | 特点 |
|-----|---------|------|------|
| **Web/H5游戏测试** | playwright-skill | ⭐1.8k | 浏览器自动化 |
| **反检测测试** | playwright-undetected | ⭐4 | Bot绕过 |
| **iOS测试** | ios-simulator-skill | ⭐558 | 模拟器自动化 |
| **Unity测试** | Unity Test Framework | - | 单元/集成测试 |

---

## 四、开发者工具技能 (补充)

### 4.1 编排工具

| 技能 | GitHub | Star | 特点 |
|-----|--------|------|------|
| **agentsys** | avifenesh/agentsys | - | 生产级工作流自动化 |
| **superpowers** | obra/superpowers | - | 核心工程技能集 |
| **sudocode** | sudocode-ai/sudocode | - | 轻量级agent编排 |
| **claude-code-agents** | undeadlist/claude-code-agents | - | E2E开发工作流 |

### 4.2 安全审计

| 技能 | GitHub | Star | 特点 |
|-----|--------|------|------|
| **trailofbits-skills** | trailofbits/skills | - | CodeQL/Semgrep集成 |
| **parry** | vaporif/parry | - | 提示注入扫描器 |

### 4.3 DevOps 工具

| 技能 | GitHub | Star | 特点 |
|-----|--------|------|------|
| **cc-devops-skills** | akin-ozer/cc-devops-skills | - | IaC代码生成 |
| **ContextKit** | FlineDev/ContextKit | - | 4阶段规划方法论 |

### 4.4 Hooks 生态系统

| 技能 | GitHub | 语言 | 功能 |
|-----|--------|------|------|
| **claude-hooks** | johnlindquist/claude-hooks | TypeScript | Hook系统 |
| **cchooks** | GowayLee/cchooks | Python | Hook SDK |
| **claude-code-hooks-sdk** | beyondcode/claude-hooks-sdk | PHP | Hook SDK |

### 4.5 完整开发工具包

| 技能 | GitHub | Star | 特点 |
|-----|--------|------|------|
| **claude-code-templates** | davila7/claude-code-templates | - | 完整资源集合 |
| **fullstack-dev-skills** | jeffallan/claude-skills | - | 65+专业技能 |
| **everything-claude-code** | affaan-m/everything-claude-code | - | 全领域资源 |

---

## 五、热门技能推荐

### 5.1 按用途推荐

| 用途 | 首推技能 | 备选 |
|-----|---------|------|
| **游戏开发 (Unity)** | Claude-Code-Game-Studios | cc-plugin-unity-gamedev |
| **游戏开发 (Godot)** | claude-resources | - |
| **Python 后端** | pydantic-ai-skills | read-only-postgres |
| **Python 测试** | pytest + TDD | /tdd |
| **Web/H5游戏测试** | playwright-skill | - |
| **iOS游戏测试** | ios-simulator-skill | - |
| **全栈开发** | fullstack-dev-skills (65+) | claude-code-templates |
| **DevOps** | cc-devops-skills | superpowers |
| **安全审计** | trailofbits-skills | parry |

### 5.2 技能组合推荐

```
游戏开发组合:
Claude-Code-Game-Studios + Unity Test Framework + playwright-skill

Python开发组合:
uv + pydantic-ai-skills + read-only-postgres + pytest

移动端游戏测试组合:
ios-simulator-skill + playwright-skill

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

### 6.2 技能验证

```bash
# 列出已安装的技能
claude skills list

# 查看技能详情
claude skills info 技能名
```

---

## 七、GitHub Trending 热门插件 (2026年3月)

### 7.1 本期新增发现

| 插件 | GitHub | Star | 分类 |
|------|--------|------|------|
| **Claude-Code-Game-Studios** | Donchitos/Claude-Code-Game-Studios | ⭐26 | 游戏开发 |
| **ios-simulator-skill** | conorluddy/ios-simulator-skill | ⭐558 | iOS测试 |
| **pydantic-ai-skills** | DougTrajano/pydantic-ai-skills | ⭐136 | Python |
| **playwright-skill** | lackeyjb/playwright-skill | ⭐1.8k | 测试 |
| **casely-qa-skill** | JohnWayneeee/casely-qa-skill | ⭐2 | QA自动化 |

---

*持续更新中...*
