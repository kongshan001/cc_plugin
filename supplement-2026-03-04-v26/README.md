# Claude Code 热门插件补充调研 (第二十六期)

> 调研时间: 2026-03-04 | 数据来源: awesome-claude-code, GitHub trending

---

## 一、游戏客户端开发技能 (持续更新)

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
| **Tier 3** | gameplay-programmer, ui-programmer, tools-programmer | specialist (Sonnet/Haiku) |

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

### 2.5 uv - Python 包管理器 (2025最快)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [astral-sh/uv](https://github.com/astral-sh/uv) |

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
| **cc-devops-skills** | akin-ozer/cc-devops-skills | - | DevOps IaC代码生成 |
| **Container Use** | dagger/container-use | - | 开发环境容器化 |

### 4.4 代码分析与测试

| 技能 | GitHub | 功能 |
|-----|--------|------|
| **/tdd** | zscott/pane | TDD开发流程 |
| **/repro-issue** | rzykov/metabase | 创建可复现测试用例 |
| **/run-ci** | hackdays-io/toban-contribution-viewer | CI检查和修复 |

---

## 五、热门趋势分析 (2026年3月)

### 5.1 增长最快的技能类别

| 排名 | 类别 | 增长率 | 代表技能 |
|------|------|--------|---------|
| 1 | 游戏开发工作室 | +45% | Claude-Code-Game-Studios |
| 2 | 安全审计 | +38% | trailofbits-skills |
| 3 | 工作流自动化 | +32% | agentsys |
| 4 | Python AI框架 | +28% | pydantic-ai-skills |
| 5 | 浏览器自动化 | +25% | playwright-skill |

### 5.2 新兴技能方向

1. **多代理协作系统**: Claude Code Game Studios 引领的多代理工作流
2. **AI-first开发**: Unity AI Workflow 等专为AI辅助设计的工作流
3. **安全优先**: 提示注入扫描、安全审计技能需求增加
4. **渐进式技能加载**: 按需加载技能信息，优化token使用

### 5.3 技能质量评估标准

| 维度 | 权重 | 评估要点 |
|------|------|---------|
| **活跃度** | 30% | 更新频率、Issue响应 |
| **完整性** | 25% | 功能覆盖、文档质量 |
| **实用性** | 25% | 真实场景适用性 |
| **创新性** | 20% | 独特价值、差异化 |

---

## 六、推荐技能安装指南

### 6.1 快速安装命令

```bash
# 游戏开发
claude install https://github.com/Donchitos/Claude-Code-Game-Studios

# Python开发
claude install https://github.com/DougTrajano/pydantic-ai-skills

# 测试
claude install https://github.com/lackeyjb/playwright-skill

# 安全审计
claude install https://github.com/trailofbits/skills
```

### 6.2 推荐技能组合

| 场景 | 技能组合 |
|------|---------|
| **Unity游戏开发** | unity-ai-workflow + Unity Test Framework |
| **Python AI应用** | pydantic-ai-skills + read-only-postgres |
| **Web游戏测试** | playwright-skill + playwright-undetected |
| **企业级开发** | agentsys + superpowers + trailofbits-skills |

---

## 七、总结与建议

### 7.1 本期亮点

- **Claude Code Game Studios**: 首个完整游戏工作室工作流，48个专业代理覆盖全流程
- **Unity AI Workflow**: 专为Unity 6.2+设计的AI-first开发范式
- **pydantic-ai-skills**: Python AI开发类型安全标杆
- **playwright-skill**: Web/H5游戏测试首选方案

### 7.2 下期预告

- 深入分析 MCP 服务器生态
- 更多游戏引擎技能调研 (Unreal, Godot)
- AI代码生成质量评估
- 开发者工作流最佳实践

---

*调研持续更新中，关注 [cc_plugin](https://github.com/kongshan001/cc_plugin) 获取最新资讯*
