# Claude Code 插件调研报告 - 补充调研第五期

> 持续跟踪 Claude Code 生态热门插件，聚焦游戏开发、Python 开发、自动化测试、开发者工具方向

---

## 📋 本期调研概要

| 维度 | 统计 |
|-----|------|
| **调研时间** | 2026-03-04 |
| **覆盖方向** | 游戏开发、Python开发、自动化测试、开发者工具 |
| **新增技能** | 20+ |
| **数据来源** | Antigravity Skills, awesome-claude-code, GitHub trending |

---

## 一、游戏客户端开发技能 (补充)

### 1.1 Antigravity 游戏开发技能

#### 游戏开发技能分类

| 技能ID | 名称 | 说明 |
|--------|------|------|
| **2d-games** | 2D游戏开发 | Sprites, tilemaps, physics, camera |
| **3d-games** | 3D游戏开发 | Rendering, shaders, physics, cameras |
| **pc-games** | PC/主机游戏 | Engine selection, platform features, optimization |
| **mobile-games** | 移动游戏 | Touch input, battery, performance, app stores |
| **web-games** | 网页游戏 | Framework selection, WebGPU, optimization, PWA |
| **multiplayer** | 多人游戏 | Architecture, networking, synchronization |
| **vr-ar** | VR/AR开发 | Comfort, interaction, performance |
| **game-art** | 游戏美术 | Visual style, asset pipeline, animation |
| **game-audio** | 游戏音频 | Sound design, music integration, adaptive audio |
| **game-design** | 游戏设计 | GDD structure, balancing, player psychology |

### 1.2 游戏引擎选择

```
游戏类型 → 推荐引擎
│
├── 2D休闲游戏
│   └── Godot, GameMaker, Phaser
│
├── 3D主机/PC游戏
│   └── Unity, Unreal Engine
│
├── 移动游戏 (iOS/Android)
│   └── Unity (主导), Godot, Cocos Creator
│
├── 网页/H5游戏
│   └── Phaser, PixiJS, Babylon.js, Three.js
│
└── VR/AR游戏
    └── Unity (XR), Unreal Engine, Godot
```

### 1.3 Unity 帧同步游戏开发 (game-frame-sync)

针对用户正在开发的 game-frame-sync 项目，以下是推荐的 Claude Code 技能组合：

| 技能 | 用途 |
|------|------|
| **cc-plugin-unity-gamedev** | Unity C# 开发 |
| **Unity Test Framework** | 单元测试和帧同步确定性验证 |
| **playwright-skill** | Web/H5 游戏功能测试 |
| **Network Chronicles** | AI 游戏角色和网络同步 |

### 1.4 Web 游戏开发趋势

#### WebGPU 支持情况 (2025)

| 浏览器 | 支持版本 | 全球支持率 |
|--------|----------|------------|
| Chrome | v113+ | ✅ |
| Edge | v113+ | ✅ |
| Firefox | v131+ | ✅ |
| Safari | 18.0+ | ✅ |
| **总体** | - | **~73%** |

#### Web 游戏框架选择

| 框架 | 特点 | 适用场景 |
|------|------|----------|
| **Phaser 4** | 完整2D引擎 | 商业2D游戏 |
| **PixiJS 8** | 高性能渲染 | 需要自定义渲染 |
| **Babylon.js 7** | 完整3D引擎 | 3D游戏、XR |
| **Three.js** | 渲染为主 | 3D可视化 |

---

## 二、Python 开发技能 (补充)

### 2.1 Antigravity Python 技能汇总

| 技能ID | 名称 | 核心能力 |
|--------|------|----------|
| **python-pro** | Python专家 | 3.12+, async, uv, ruff, pydantic, FastAPI |
| **python-patterns** | 开发原则 | 框架选择, async, type hints |
| **python-fastapi-development** | FastAPI开发 | async, SQLAlchemy, Pydantic, auth |
| **python-testing-patterns** | 测试策略 | pytest, fixtures, mocking, TDD |
| **python-performance-optimization** | 性能优化 | cProfile, memory profiler |
| **python-packaging** | 包发布 | setup.py, pyproject.toml, PyPI |
| **async-python-patterns** | 异步编程 | asyncio, concurrent, I/O优化 |
| **temporal-python-pro** | Temporal工作流 | durable workflows, saga |
| **temporal-python-testing** | Temporal测试 | pytest, time-skipping, replay |
| **dbos-python** | DBOS工作流 | fault-tolerant, durable |

### 2.2 Python 测试框架对比

| 框架 | 特点 | 适用场景 |
|------|------|----------|
| **pytest** | 功能丰富, 插件多 | 通用测试 |
| **unittest** | 标准库 | 简单项目 |
| **pytest-asyncio** | 异步测试 | async/await |
| **hypothesis** | 属性测试 | 金融/科学计算 |
| **pytest-cov** | 覆盖率 | 质量追踪 |

### 2.3 Python 2025 生态工具

| 工具 | 用途 | 性能 |
|------|------|------|
| **uv** | 包管理器 | 10-100x faster than pip |
| **ruff** | Linter | 10-100x faster than flake8 |
| **pydantic** | 数据验证 | 类型安全 |
| **fastapi** | Web框架 | async first |
| **sqlalchemy** | ORM | 成熟稳定 |

---

## 三、自动化测试技能 (补充)

### 3.1 Antigravity 测试/自动化技能

| 技能ID | 名称 | 说明 |
|--------|------|------|
| **browser-automation** | 浏览器自动化 | 选择器, 等待策略, 可靠脚本 |
| **playwright-mcp** | Playwright MCP | 浏览器自动化 MCP 服务器 |
| **api-testing-observability-api-mock** | API Mock | 模拟真实 API 行为 |
| **api-security-testing** | API 安全测试 | auth, authorization, rate limiting |
| **azure-microsoft-playwright-testing-ts** | Azure Playwright | 云端大规模测试 |
| **bats-testing-patterns** | Bats 测试 | Shell 脚本测试 |
| **ab-test-setup** | A/B测试 | hypothesis, metrics, gates |
| **cicd-automation-workflow-automate** | CI/CD自动化 | GitHub Actions, 管道优化 |

### 3.2 游戏客户端测试方案

| 测试类型 | 工具/技能 | 适用场景 |
|----------|----------|----------|
| **Web/H5游戏功能测试** | playwright-skill | 回归测试 |
| **Unity单元测试** | Unity Test Framework | 游戏逻辑 |
| **Unity集成测试** | Unity Test Framework | 系统交互 |
| **移动端UI测试** | android_ui_verification | Android游戏 |
| **iOS游戏测试** | ios-simulator-skill | iOS模拟器 |
| **性能测试** | Unity Profiler | 帧率/内存 |
| **网络同步测试** | 自定义帧同步测试 | 确定性验证 |

### 3.3 Slash Commands 测试命令

| 命令 | 来源 | 功能 |
|------|------|------|
| **/tdd** | zscott/pane | TDD开发流程 |
| **/tdd-implement** | Narrator | TDD实现 |
| **/repro-issue** | Metabase | 可复现测试用例 |
| **/check** | slack-tools | 代码质量检查 |
| **/clean** | eridu | 代码格式化 |
| **/fix-issue** | Metabase | GitHub issue修复 |
| **/optimize** | ai-project-rules | 性能优化 |

---

## 四、开发者工具技能 (补充)

### 4.1 工作流编排

| 技能 | GitHub | 特点 |
|------|--------|------|
| **agentsys** | avifenesh/agentsys | 生产级工作流, PR管理, 性能调查 |
| **Claude Code Flow** | ruvnet/claude-code-flow | 代码优先编排层 |
| **ralph-claude-code** | frankbria/ralph-claude-code | 自主开发框架, 75+测试 |
| **superpowers** | obra/superpowers | 核心工程技能集 |

### 4.2 Claude Code Settings

| 项目 | 说明 |
|------|------|
| **GitHub** | fcakyon/claude-codex-settings |
| **Star** | ⭐ 活跃 |
| **特点** | 插件覆盖核心开发者活动 |

#### 支持平台

- GitHub
- Azure
- MongoDB
- Tavily
- Playwright

### 4.3 Hooks 生态系统

| 技能 | 语言 | 说明 |
|------|------|------|
| **claude-hooks** | TypeScript | 官方 Hook 系统 |
| **cchooks** | Python | 轻量级 SDK |
| **claude-hooks-sdk** | PHP | PHP Hook SDK |
| **cc-tools** | Go | 高性能实现 |

### 4.4 DevOps 工具

| 技能 | 说明 |
|------|------|
| **aws-mcp-server** | AWS CLI 集成 |
| **azure-microsoft-playwright-testing-ts** | Azure 云测试 |
| **cicd-automation** | CI/CD 管道自动化 |

### 4.5 代码质量工具

| 工具 | 用途 |
|------|------|
| **/check** | 代码质量 + 安全检查 |
| **/clean** | 格式化 + import 整理 |
| **/optimize** | 性能分析 + 优化 |
| **/code_analysis** | 知识图谱 + 质量评估 |

---

## 五、技能组合推荐

### 5.1 游戏开发组合

```
基础: Antigravity game-development/*
Unity: Claude-Code-Game-Studios + Unity Test Framework
Web: Antigravity web-games + playwright-skill
帧同步: Unity Test Framework + 网络延迟模拟 + 确定性验证
```

### 5.2 Python 开发组合

```
基础: python-pro + python-patterns
Web后端: python-fastapi-development + pydantic-ai-skills
测试: python-testing-patterns + pytest + temporal-python-testing
性能: python-performance-optimization + uv + ruff
```

### 5.3 测试自动化组合

```
Web测试: playwright-skill + browser-automation
API测试: api-testing-observability-api-mock
安全: api-security-testing + cloud-penetration-testing
TDD: /tdd-implement + python-testing-patterns
```

---

## 📎 相关资源

- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
- [awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills)
- [Antigravity Skills](https://github.com/anthropics/antigravity)
- [Claude Code Handbook](https://nikiforovall.blog/claude-code-rules/)
- [Claude Code Ultimate Guide](https://github.com/FlorianBruniaux/claude-code-ultimate-guide)

---

*持续更新中，欢迎提交 PR 补充更多技能*
