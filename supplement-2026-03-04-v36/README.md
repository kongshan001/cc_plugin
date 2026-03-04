# Claude Code 插件补充调研 - 第三十六期

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

## 一、游戏客户端开发技能（补充）

### 1.1 Claude Code Game Studios ⭐ 强烈推荐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [Donchitos/Claude-Code-Game-Studios](https://github.com/Donchitos/Claude-Code-Game-Studios) |
| **Star** | ⭐ 28 |
| **更新** | 2026-03-03 |
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

### 1.2 Unity 开发技能（更新）

#### GitHub 热门 Unity 技能

| 技能 | GitHub | Star | 特点 |
|-----|--------|------|------|
| **Besty0728/Unity-Skills** | Besty0728/Unity-Skills | ⭐ 253 | AI 自动化技能，专为 Unity 设计 |
| **Unity-Skills** | tjboudreaux/cc-plugin-unity-gamedev | ⭐ 1 | 21个专业技能，完整覆盖Unity开发栈 |
| **OH-Unity-GameDev-Skills** | OstrichHermit/OH-Unity-GameDev-Skills | ⭐ 6 | Unity基础开发+DoTween+MediaPipe |
| **unity-ai-workflow** | David-GD13/unity-ai-workflow | ⭐ 4 | Unity 6.2+ AI-first工作流 |
| **The1Studio/theone-training-skills** | The1Studio/theone-training-skills | ⭐ 44 | Unity 工程师培训技能 |
| **solana-game-skill** | solanabr/solana-game-skill | ⭐ 5 | Solana区块链游戏开发 |

#### Unity 技能核心分类

| 分类 | 技能 |
|-----|------|
| **工具类** | Addressables, MemoryPack, ScriptableObjects, Profiling, Package Manager |
| **动画/物理** | Animation, Physics, NavMesh, Object Pooling, State Machine |
| **AI/行为** | Behavior Designer, GAS (Gameplay Ability System) |
| **音视频** | Wwise音频, Cinemachine相机, PrimeTween |
| **UI** | UGUI, Mobile Optimization |
| **测试** | Unity Test Framework |
| **DI/异步** | VContainer, UniTask |
| **渲染** | URP, HDRP, Shader Graph, HLSL |
| **性能** | Job System, Burst Compiler, DOTS/ECS |

### 1.3 Antigravity Game Development 技能

| 技能 | 说明 |
|-----|------|
| **game-development** | 游戏开发路由技能，根据项目需求自动路由到平台特定技能 |
| **game-development/web-games** | Web游戏开发 (HTML5, WebGL) |
| **game-development/mobile-games** | 移动游戏开发 (iOS, Android) |
| **game-development/pc-games** | PC游戏开发 (Steam, Desktop) |
| **game-development/vr-ar** | VR/AR游戏开发 |
| **game-development/2d-games** | 2D游戏开发 (sprites, tilemaps) |
| **game-development/3d-games** | 3D游戏开发 (meshes, shaders) |
| **game-development/game-design** | 游戏设计 (GDD, balancing, player psychology) |
| **game-development/multiplayer** | 多人游戏开发 (networking) |
| **game-development/game-art** | 游戏美术 (asset pipeline, animation) |
| **game-development/game-audio** | 游戏音频 (sound design, adaptive audio) |

### 1.4 Unreal Engine 开发

| 技能 | 来源 | 描述 |
|-----|------|------|
| **unreal-engine-cpp-pro** | Antigravity | UE5.x C++ 开发最佳实践 |
| **unreal-engine-developer** | Antigravity | Unreal Engine 5.x 全栈开发 |

### 1.5 Godot 开发

| 技能 | 来源 | 描述 |
|-----|------|------|
| **godot-gdscript-patterns** | Antigravity | Godot 4 GDScript 模式 |
| **godot-4-migration** | Antigravity | Godot 4 迁移指南 |
| **godot-developer** | Antigravity | Godot 游戏开发专家 |

### 1.6 Web/H5 游戏开发

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

## 二、Python 开发技能

### 2.1 Python 开发核心技能

#### Antigravity Python 技能

| 技能 | 说明 |
|-----|------|
| **python-development-python-scaffold** | Python 项目脚手架 |
| **python-fastapi-development** | FastAPI 开发 |
| **python-packaging** | Python 包发布 |
| **python-patterns** | Python 设计模式 |
| **python-performance-optimization** | Python 性能优化 |
| **python-pro** | Python 专业开发 |
| **python-testing-patterns** | Python 测试模式 |
| **async-python-patterns** | 异步 Python 模式 |

#### Python 测试技能

| 技能 | 来源 | 描述 |
|-----|------|------|
| **python-testing-patterns** | Antigravity | pytest、unittest 等测试框架 |
| **temporal-python-testing** | Antigravity | Temporal 工作流测试 |
| **unit-testing-test-generate** | Antigravity | 单元测试生成 |
| **test-driven-development** | Antigravity | TDD 开发模式 |
| **test-fixing** | Antigravity | 测试修复 |
| **testing-patterns** | Antigravity | 测试模式 |

### 2.2 AWS 云服务 Python MCP

| 项目 | 说明 |
|-----|------|
| **GitHub** | [alexei-led/aws-mcp-server](https://github.com/alexei-led/aws-mcp-server) |
| **Star** | ⭐ 活跃 |
| **语言** | Python |
| **特点** | AWS CLI 集成，多环境支持 |

### 2.3 Pydantic AI 深度集成

| 项目 | 说明 |
|-----|------|
| **GitHub** | [DougTrajano/pydantic-ai-skills](https://github.com/DougTrajano/pydantic-ai-skills) |
| **Star** | ⭐ 136 |
| **特点** | Agent Skills 支持 Pydantic AI |

---

## 三、自动化测试技能

### 3.1 Playwright 测试技能

| 项目 | 说明 |
|-----|------|
| **GitHub** | [lackeyjb/playwright-skill](https://github.com/lackeyjb/playwright-skill) |
| **Star** | ⭐ 1.8k |
| **功能** | Playwright 浏览器自动化 |
| **特点** | 模型调用的 Playwright 自动化 |

#### 核心功能

- **Web 应用测试**: 自动化测试 Web 应用功能
- **UI 验证**: 验证前端功能和行为
- **截图捕获**: 自动截图记录测试状态
- **调试支持**: 辅助调试 UI 行为

#### 适用场景

- Web 游戏测试
- H5 游戏测试
- 前端功能验证
- UI 自动化测试
- 回归测试

### 3.2 游戏客户端测试技能

#### Azure Playwright Testing

| 项目 | 说明 |
|-----|------|
| **技能** | azure-microsoft-playwright-testing-ts |
| **来源** | Antigravity |
| **特点** | Microsoft Playwright TypeScript 测试 |

#### E2E 测试

| 技能 | 来源 | 描述 |
|-----|------|------|
| **e2e-testing** | Antigravity | 端到端测试 |
| **e2e-testing-patterns** | Antigravity | E2E 测试模式 |
| **webapp-testing** | Antigravity | Web 应用测试 |
| **javascript-testing-patterns** | Antigravity | JavaScript 测试模式 |

### 3.3 安全测试技能

| 技能 | 来源 | 描述 |
|-----|------|------|
| **api-security-testing** | Antigravity | API 安全测试 |
| **burp-suite-testing** | Antigravity | Burp Suite 测试 |
| **web-security-testing** | Antigravity | Web 安全测试 |
| **pentest-checklist** | Antigravity | 渗透测试清单 |
| **pentest-commands** | Antigravity | 渗透测试命令 |

### 3.4 性能测试技能

| 技能 | 来源 | 描述 |
|-----|------|------|
| **performance-testing-review-ai-review** | Antigravity | 性能测试 AI 审查 |
| **performance-testing-review-multi-agent-review** | Antigravity | 多代理性能测试审查 |
| **backtesting-frameworks** | Antigravity | 回测框架 |

---

## 四、开发者工具技能

### 4.1 Superpowers (强烈推荐)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [obra/superpowers](https://github.com/obra/superpowers) |
| **Star** | ⭐ 活跃 |
| **特点** | 核心开发能力集，完整 SDLC 覆盖 |

#### 核心功能

- 规划 (Planning)
- 代码审查 (Reviewing)
- 测试 (Testing)
- 调试 (Debugging)
- 完整软件开发生命周期覆盖

### 4.2 AgentSys 工作流自动化

| 项目 | 说明 |
|-----|------|
| **GitHub** | [avifenesh/agentsys](https://github.com/avifenesh/agentsys) |
| **Star** | ⭐ 活跃 |
| **版本** | v5.3.7 |

#### 核心功能

- 任务到生产工作流自动化
- PR 管理
- 代码清理
- 性能调查
- 漂移检测
- 多代理代码审查
- Agent 配置 linting (agnix)

### 4.3 Claude Code Settings

| 项目 | 说明 |
|-----|------|
| **GitHub** | [fcakyon/claude-codex-settings](https://github.com/fcakyon/claude-codex-settings) |
| **Star** | ⭐ 活跃 |
| **版本** | v2.1.0 |
| **许可** | Apache-2.0 |

#### 核心功能

- 云平台集成 (GitHub, Azure, MongoDB)
- 服务集成 (Tavily, Playwright)
- 清晰的开发规范

### 4.4 MCP 服务器

#### 热门 MCP 服务器

| 项目 | Star | 描述 |
|-----|------|------|
| **serena** | ⭐ 20,946 | 语义检索和编辑能力 |
| **pal-mcp-server** | ⭐ 11,180 | 多模型集成 |
| **mcp-use** | ⭐ 9,359 | 全栈 MCP 框架 |
| **pg-aiguide** | ⭐ 1,579 | PostgreSQL 技能 |
| **notebooklm-mcp** | ⭐ 1,185 | NotebookLM 集成 |

---

## 五、趋势分析

### 5.1 游戏开发方向趋势

1. **AI-First 开发工作流**: Unity 6.2+ 引领 AI 驱动开发
2. **多引擎支持**: 技能正在覆盖 Unity、Unreal、Godot 全生态
3. **工作室级解决方案**: Claude Code Game Studios 提供完整团队协作
4. **区块链游戏**: Solana 游戏开发技能正在兴起

### 5.2 Python 开发方向趋势

1. **异步编程**: async-python-patterns 关注度上升
2. **AI 框架集成**: Pydantic AI 技能需求增长
3. **云服务集成**: AWS MCP 服务器持续活跃
4. **测试驱动开发**: TDD 技能重视程度提升

### 5.3 测试方向趋势

1. **Playwright 主导**: Web 测试领域 Playwright 成为首选
2. **E2E 测试**: 端到端测试技能需求增加
3. **安全测试**: API/Web 安全测试技能受到关注
4. **性能测试**: AI 辅助性能测试开始出现

---

## 六、推荐技能清单

### 6.1 游戏开发必装

| 优先级 | 技能 | 来源 |
|--------|------|------|
| ⭐⭐⭐ | Claude Code Game Studios | GitHub |
| ⭐⭐⭐ | Unity Skills (Besty0728) | GitHub |
| ⭐⭐⭐ | game-development | Antigravity |
| ⭐⭐ | unity-ai-workflow | GitHub |
| ⭐⭐ | godot-developer | Antigravity |

### 6.2 Python 开发必装

| 优先级 | 技能 | 来源 |
|--------|------|------|
| ⭐⭐⭐ | python-development-python-scaffold | Antigravity |
| ⭐⭐⭐ | python-testing-patterns | Antigravity |
| ⭐⭐⭐ | python-fastapi-development | Antigravity |
| ⭐⭐ | aws-mcp-server | GitHub |
| ⭐⭐ | pydantic-ai-skills | GitHub |

### 6.3 测试必装

| 优先级 | 技能 | 来源 |
|--------|------|------|
| ⭐⭐⭐ | playwright-skill | GitHub |
| ⭐⭐⭐ | e2e-testing | Antigravity |
| ⭐⭐ | test-driven-development | Antigravity |
| ⭐⭐ | api-security-testing | Antigravity |

### 6.4 开发者工具必装

| 优先级 | 技能 | 来源 |
|--------|------|------|
| ⭐⭐⭐ | superpowers | GitHub |
| ⭐⭐⭐ | agentsys | GitHub |
| ⭐⭐ | claude-codex-settings | GitHub |

---

## 附录：技能安装命令

### 游戏开发技能安装

```bash
# Claude Code Game Studios
claude install GitHub https://github.com/Donchitos/Claude-Code-Game-Studios

# Unity Skills
claude install GitHub https://github.com/Besty0728/Unity-Skills
```

### Python 开发技能安装

```bash
# Python 项目脚手架
claude install Antigravity python-development-python-scaffold

# FastAPI 开发
claude install Antigravity python-fastapi-development
```

### 测试技能安装

```bash
# Playwright
claude install GitHub https://github.com/lackeyjb/playwright-skill

# E2E 测试
claude install Antigravity e2e-testing
```

---

*文档更新时间: 2026-03-04*
*持续更新 Claude Code 热门插件调研*
