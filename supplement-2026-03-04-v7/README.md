# Claude Code 插件调研报告 - 补充调研第七期

> 持续跟踪 Claude Code 生态热门插件，聚焦游戏开发、Python 开发、自动化测试、开发者工具方向

---

## 📋 本期调研概要

| 维度 | 统计 |
|-----|------|
| **调研时间** | 2026-03-04 |
| **覆盖方向** | 游戏开发、Python开发、自动化测试、开发者工具 |
| **新增技能** | 40+ |
| **数据来源** | Antigravity Skills, awesome-claude-code, GitHub trending |

---

## 一、游戏客户端开发技能 (补充)

### 1.1 Antigravity 游戏开发技能体系

Antigravity 提供了完整的游戏开发技能体系，通过 `game-development` 技能作为入口进行路由：

| 技能ID | 名称 | 核心能力 |
|--------|------|----------|
| **game-development** | 游戏开发总览 | 路由到平台特定技能 |
| **2d-games** | 2D游戏开发 | Sprites, tilemaps, physics, camera |
| **3d-games** | 3D游戏开发 | Rendering, shaders, physics, cameras |
| **pc-games** | PC/主机游戏 | Engine selection, platform features |
| **mobile-games** | 移动游戏 | Touch input, battery, performance |
| **web-games** | 网页游戏 | WebGPU, PWA, optimization |
| **multiplayer** | 多人游戏 | Architecture, networking |
| **vr-ar** | VR/AR开发 | Comfort, interaction, performance |
| **game-art** | 游戏美术 | Visual style, asset pipeline |
| **game-audio** | 游戏音频 | Sound design, adaptive audio |
| **game-design** | 游戏设计 | GDD, balancing, psychology |

### 1.2 Unity 开发技能体系

#### Unity Developer 技能

| 项目 | 说明 |
|------|------|
| **技能ID** | unity-developer |
| **来源** | Antigravity |
| **特点** | Unity 完整开发技能 |

#### 核心能力

| 分类 | 能力 |
|------|------|
| **基础** | C# 编程, Unity 编辑器, 组件系统 |
| **物理** | Rigidbody, Collider, Physics 2D/3D |
| **动画** | Animator, Animation Clips, Timeline |
| **UI** | UGUI, UI Toolkit, Canvas |
| **音频** | AudioSource, AudioMixer, Spatial Audio |
| **网络** | Netcode for GameObjects, Mirror, Photon |
| **资源** | Addressables, AssetBundle |
| **测试** | Unity Test Framework, Play Mode Tests |

#### Unity ECS Patterns

| 技能 | 说明 |
|------|------|
| **unity-ecs-patterns** | Unity DOTS/ECS 开发模式 |

#### 适用场景

- 移动游戏开发
- PC/主机游戏开发
- VR/AR 应用开发
- 3D 可视化应用

### 1.3 Unreal Engine 开发技能

| 技能ID | 说明 |
|--------|------|
| **unreal-engine-cpp-pro** | Unreal Engine C++ 开发专家 |

#### 核心能力

| 分类 | 能力 |
|------|------|
| **C++** | Actor, Component, UObject |
| **蓝图** | 蓝图可视化编程 |
| **UMG** | UI 开发 |
| **物理** | Chaos 物理引擎 |
| **网络** | Replication, RPC |
| **AI** | Behavior Tree, EQS, Navigation |

### 1.4 Web 游戏开发

#### Web 游戏框架选择

| 框架 | 特点 | 适用场景 |
|------|------|----------|
| Phaser 4 | 完整2D引擎 | 商业2D游戏 |
| PixiJS 8 | 高性能渲染 | 自定义渲染 |
| Babylon.js 7 | 完整3D引擎 | 3D游戏、XR |
| Three.js | 渲染为主 | 3D可视化 |

#### WebGPU 浏览器支持 (2025)

| 浏览器 | 支持版本 | 状态 |
|--------|----------|------|
| Chrome | v113+ | ✅ |
| Edge | v113+ | ✅ |
| Firefox | v131+ | ✅ |
| Safari | 18.0+ | ✅ |
| **全球支持率** | - | **~73%** |

---

## 二、Python 开发技能 (补充)

### 2.1 Python Pro 技能详解

**python-pro** 是 Antigravity 技能市场中最重要的 Python 开发技能：

| 特性 | 说明 |
|------|------|
| **版本** | Python 3.12+ |
| **包管理** | uv (2024最快) |
| **代码质量** | ruff (替代black/isort/flake8) |
| **类型检查** | mypy, pyright |
| **Web框架** | FastAPI, Django, Flask |

#### 核心能力

**现代Python特性:**
- Python 3.12+ 特性 (改进的错误信息、性能优化)
- 高级 async/await 模式 (asyncio, aiohttp, trio)
- Pydantic 模型和数据验证
- 模式匹配 (match语句)
- 类型提示和 Protocol 类型

**现代工具链:**
```bash
# uv - 最快的Python包管理器
uv init my-project
uv venv
uv pip install -r requirements.txt

# ruff - 代码格式化和linting
ruff check .
ruff format .
```

### 2.2 Python 开发技能汇总

| 技能ID | 核心能力 | 适用场景 |
|--------|----------|----------|
| **python-pro** | Python 3.12+ 全栈 | 通用开发 |
| **python-patterns** | 开发原则和决策 | 架构设计 |
| **python-fastapi-development** | FastAPI 后端开发 | API 服务 |
| **python-testing-patterns** | pytest/测试策略 | 质量保证 |
| **async-python-patterns** | asyncio 异步编程 | 高并发 |
| **python-performance-optimization** | 性能优化 | 性能关键 |
| **temporal-python-pro** | Temporal 工作流 | 分布式事务 |
| **python-packaging** | Python 包发布 | 库开发 |

### 2.3 FastAPI 开发技能

#### python-fastapi-development

| 项目 | 说明 |
|------|------|
| **技能ID** | python-fastapi-development |
| **框架** | FastAPI |
| **特点** | 高性能 API 开发 |

#### 核心能力

| 分类 | 能力 |
|------|------|
| **API** | REST, GraphQL, WebSocket |
| **认证** | OAuth2, JWT, API Key |
| **数据库** | SQLAlchemy, AsyncPG |
| **验证** | Pydantic, 自定义验证器 |
| **文档** | OpenAPI, Swagger |
| **部署** | Docker, Uvicorn, Gunicorn |

### 2.4 异步 Python 编程

#### async-python-patterns

| 项目 | 说明 |
|------|------|
| **技能ID** | async-python-patterns |
| **库** | asyncio, aiohttp, trio |

#### 核心模式

| 模式 | 说明 | 适用场景 |
|------|------|----------|
| **Task Group** | 并发任务管理 | 多API调用 |
| **Stream** | 异步迭代器 | 实时数据流 |
| **Semaphore** | 并发限制 | 速率控制 |
| **awaitable** | 自定义等待对象 | 集成外部库 |

### 2.5 数据库集成

#### read-only-postgres 安全特性

| 特性 | 说明 |
|------|------|
| **查询类型** | SELECT/SHOW/EXPLAIN/WITH |
| **超时控制** | 可配置 |
| **行数限制** | 防止大规模查询 |
| **多连接** | 支持多数据库 |

---

## 三、自动化测试技能 (补充)

### 3.1 Playwright 浏览器自动化

**playwright-skill** 是 Claude Code 最热门的浏览器自动化技能：

| 项目 | 说明 |
|------|------|
| **技能ID** | playwright-skill |
| **Star** | ⭐ 1.8k+ |
| **功能** | 完整浏览器自动化 |

#### 核心工作流

1. **自动检测开发服务器**
2. **编写脚本到 /tmp** (不污染项目)
3. **使用可见浏览器** (默认 headless: false)
4. **参数化 URL** (可通过环境变量配置)

#### 典型用途
- Web 应用功能测试
- UI 验证
- 截图捕获
- 响应式测试
- 登录流程测试
- 表单自动化

#### 使用示例

```bash
# Step 1: 检测开发服务器
cd $SKILL_DIR && node -e "require('./lib/helpers').detectDevServers().then(s => console.log(JSON.stringify(s)))"

# Step 2: 运行测试
cd $SKILL_DIR && node run.js /tmp/playwright-test-*.js
```

### 3.2 浏览器自动化

#### browser-automation

| 技能ID | 功能 |
|--------|------|
| **browser-automation** | 通用浏览器自动化 |

#### 支持功能

| 功能 | 说明 |
|------|------|
| **页面操作** | 点击、输入、滚动 |
| **数据提取** | 抓取页面内容 |
| **表单处理** | 自动填写表单 |
| **截图** | 页面截图 |
| **PDF导出** | 导出页面为PDF |

### 3.3 Go Playwright

#### go-playwright

| 项目 | 说明 |
|------|------|
| **技能ID** | go-playwright |
| **语言** | Go |

#### 适用场景

- Go 项目浏览器测试
- 性能测试
- 集成测试

### 3.4 测试模式技能

| 技能ID | 功能 |
|--------|------|
| **e2e-testing** | 端到端测试 |
| **e2e-testing-patterns** | E2E 测试模式 |
| **testing-patterns** | 测试模式 |
| **testing-qa** | QA 测试 |
| **test-driven-development** | TDD 开发 |
| **test-fixing** | 测试修复 |
| **unit-testing-test-generate** | 单元测试生成 |

### 3.5 性能测试

| 技能ID | 功能 |
|--------|------|
| **performance-testing-review-ai-review** | 性能测试审查 |
| **performance-testing-review-multi-agent-review** | 多代理性能审查 |

### 3.6 移动端测试

#### Azure Playwright Testing

| 技能 | 说明 |
|------|------|
| **azure-microsoft-playwright-testing-ts** | Azure Playwright 测试 |
| **azure-resource-manager-playwright-dotnet** | Azure .NET Playwright |

---

## 四、开发者工具技能 (补充)

### 4.1 Claude Code Tools

| 项目 | 说明 |
|------|------|
| **GitHub** | pchalasani/claude-code-tools |
| **功能** | 会话连续性工具 |

#### 核心能力

| 功能 | 说明 |
|------|------|
| **会话保持** | 避免上下文压缩 |
| **跨会话恢复** | 恢复历史会话 |
| **全文搜索** | Tantivy 全文搜索 |
| **Tmux 集成** | CLI 交互 |

### 4.2 Superpowers 技能包

| 项目 | 说明 |
|------|------|
| **GitHub** | obra/superpowers |
| **Star** | ⭐ 500+ |
| **特点** | 核心工程能力 |

#### 覆盖范围

| 阶段 | 能力 |
|------|------|
| **规划** | 任务分解, 架构设计 |
| **审查** | 代码审查, PR 审查 |
| **测试** | 单元测试, 集成测试 |
| **调试** | 问题定位, 修复 |
| **部署** | CI/CD, 部署 |

### 4.3 AgentSys 工作流自动化

| 项目 | 说明 |
|------|------|
| **GitHub** | avifenesh/agentsys |
| **特点** | 工作流自动化系统 |

#### 核心能力

| 功能 | 说明 |
|------|------|
| **PR管理** | 自动管理 PR |
| **代码清理** | 代码质量优化 |
| **性能调查** | 性能问题定位 |
| **多代理审查** | 并行代码审查 |

### 4.4 Claude Code Settings

| 项目 | 说明 |
|------|------|
| **GitHub** | fcakyon/claude-codex-settings |
| **Star** | ⭐ 250+ |

#### 支持平台

| 平台 | 功能 |
|------|------|
| **GitHub** | API 集成 |
| **Azure** | 云服务 |
| **MongoDB** | 数据库 |
| **Tavily** | 搜索 |
| **Playwright** | 浏览器自动化 |

### 4.5 编排工具 (Orchestrators)

| 工具 | 说明 | 特点 |
|------|------|------|
| **Claude Squad** | 多代理并行工作 | 终端应用 |
| **Claude Swarm** | 代理群组 | 分布式 |
| **Claude Code Flow** | 递归代理循环 | 代码优先 |
| **Auto-Claude** | 自主多代理 | Kanban UI |
| **TSK** | Docker沙箱 | 隔离执行 |
| **sudocode** | 轻量编排 | 集成 Jira |

### 4.6 ContextKit 开发框架

| 项目 | 说明 |
|------|------|
| **GitHub** | FlineDev/ContextKit |
| **特点** | 4阶段规划方法论 |

#### 核心功能

| 阶段 | 说明 |
|------|------|
| **规划** | 系统化开发规划 |
| **质量** | 质量代理 |
| **工作流** | 结构化工作流 |
| **集成** | 外部工具集成 |

### 4.7 Claude Hub

| 项目 | 说明 |
|------|------|
| **GitHub** | claude-did-this/claude-hub |
| **功能** | GitHub Webhook 服务 |

#### 能力

| 功能 | 说明 |
|------|------|
| **PR 集成** | AI 辅助 PR |
| **Issue 集成** | Issue 分析 |
| **代码问答** | 代码库问答 |

---

## 五、技能索引

### 5.1 按方向分类

#### 游戏开发
| 技能 | 来源 | 优先级 |
|------|------|--------|
| game-development | Antigravity | ⭐⭐⭐⭐⭐ |
| unity-developer | Antigravity | ⭐⭐⭐⭐ |
| unity-ecs-patterns | Antigravity | ⭐⭐⭐⭐ |
| unreal-engine-cpp-pro | Antigravity | ⭐⭐⭐⭐ |
| game-design | Antigravity | ⭐⭐⭐⭐ |
| multiplayer | Antigravity | ⭐⭐⭐⭐ |

#### Python 开发
| 技能 | 来源 | 优先级 |
|------|------|--------|
| python-pro | Antigravity | ⭐⭐⭐⭐⭐ |
| python-fastapi-development | Antigravity | ⭐⭐⭐⭐ |
| async-python-patterns | Antigravity | ⭐⭐⭐⭐ |
| python-testing-patterns | Antigravity | ⭐⭐⭐⭐ |
| python-performance-optimization | Antigravity | ⭐⭐⭐⭐ |
| read-only-postgres | GitHub | ⭐⭐⭐⭐ |

#### 自动化测试
| 技能 | 来源 | 优先级 |
|------|------|--------|
| playwright-skill | Antigravity | ⭐⭐⭐⭐⭐ |
| browser-automation | Antigravity | ⭐⭐⭐⭐ |
| e2e-testing | Antigravity | ⭐⭐⭐⭐ |
| testing-patterns | Antigravity | ⭐⭐⭐⭐ |
| test-driven-development | Antigravity | ⭐⭐⭐⭐ |
| Superpowers | GitHub | ⭐⭐⭐⭐ |

#### 开发者工具
| 技能 | 来源 | 优先级 |
|------|------|--------|
| claude-code-tools | GitHub | ⭐⭐⭐⭐⭐ |
| claudekit | GitHub | ⭐⭐⭐⭐ |
| Superpowers | GitHub | ⭐⭐⭐⭐ |
| AgentSys | GitHub | ⭐⭐⭐⭐ |
| Claude Code Settings | GitHub | ⭐⭐⭐⭐ |
| ContextKit | GitHub | ⭐⭐⭐⭐ |

---

## 六、推荐技能组合

### 6.1 帧同步游戏开发 (game-frame-sync)

```
python-pro (后端)
  ↓
unity-developer / unreal-engine-cpp-pro (客户端)
  ↓
playwright-skill (Web界面测试)
  ↓
Superpowers (代码质量)
```

### 6.2 Python Web 全栈

```
python-pro (核心开发)
  ↓
python-fastapi-development (API)
  ↓
python-testing-patterns (测试)
  ↓
read-only-postgres (数据)
```

### 6.3 游戏自动化测试

```
playwright-skill (Web测试)
  ↓
browser-automation (浏览器)
  ↓
Superpowers (质量保证)
```

### 6.4 企业级开发

```
AgentSys (工作流)
  ↓
Claude Code Settings (多平台)
  ↓
ContextKit (开发框架)
  ↓
Superpowers (质量)
```

---

## 七、热门技能排行 (2026年3月)

### 7.1 游戏开发 TOP 5

| 排名 | 技能 | Star | 特点 |
|------|------|------|------|
| 1 | game-development | - | 完整技能路由 |
| 2 | Claude-Code-Game-Studios | ⭐26 | 48代理系统 |
| 3 | unity-ai-workflow | ⭐4 | Unity 6.2+ AI工作流 |
| 4 | cc-plugin-unity-gamedev | ⭐1 | 21个Unity技能 |
| 5 | game-design | - | 游戏设计原则 |

### 7.2 Python 开发 TOP 5

| 排名 | 技能 | 来源 | 特点 |
|------|------|------|------|
| 1 | python-pro | Antigravity | Python 3.12+ 专家 |
| 2 | python-fastapi-development | Antigravity | FastAPI 开发 |
| 3 | async-python-patterns | Antigravity | 异步编程 |
| 4 | python-testing-patterns | Antigravity | 测试模式 |
| 5 | temporal-python-pro | Antigravity | 分布式事务 |

### 7.3 自动化测试 TOP 5

| 排名 | 技能 | Star | 特点 |
|------|------|------|------|
| 1 | playwright-skill | ⭐1.8k+ | 浏览器自动化 |
| 2 | browser-automation | - | 通用浏览器 |
| 3 | Superpowers | ⭐500+ | 完整SDLC |
| 4 | e2e-testing | - | 端到端测试 |
| 5 | test-driven-development | - | TDD 开发 |

### 7.4 开发者工具 TOP 5

| 排名 | 技能 | Star | 特点 |
|------|------|------|------|
| 1 | claude-code-tools | - | 会话连续性 |
| 2 | AgentSys | - | 工作流自动化 |
| 3 | Claude Code Settings | ⭐250+ | 多平台集成 |
| 4 | Superpowers | ⭐500+ | 核心工程能力 |
| 5 | claudekit | - | 20+子代理 |

---

## 📚 参考资源

- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
- [Antigravity Skills](https://github.com/purpleclay/antigravity-awesome-skills)
- [Claude Code 官方文档](https://docs.anthropic.com/en/docs/claude-code/overview)

---

*文档更新: 2026-03-04*
*下次更新: 2026-03-11*
