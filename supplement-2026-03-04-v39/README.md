# Claude Code 热门插件补充调研 - 2026年3月

## 📋 文档信息

- **调研日期**: 2026-03-04
- **分类**: 游戏客户端开发 / Python 开发 / 自动化测试 / 开发者工具
- **状态**: ✅ 补充调研完成

---

## 🎮 一、游戏客户端开发插件

### 1.1 Claude Code Game Studios (推荐)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [Donchitos/Claude-Code-Game-Studios](https://github.com/Donchitos/Claude-Code-Game-Studios) |
| **Star** | ⭐ 28 |
| **版本** | 2026年2月新增 |
| **特点** | 48个AI代理团队，专业游戏工作室架构 |

### 核心功能

- **48个专业AI代理**：游戏设计师、程序员、美术、QA等
- **36个工作流技能**：覆盖完整游戏开发流程
- **多引擎支持**：Unity/Unreal/Godot
- **工作室层级**：模拟真实游戏开发团队架构

### 代理类型

| 代理类型 | 数量 | 功能 |
|---------|------|------|
| 游戏设计师 | 5 | 玩法设计、关卡设计 |
| 客户端编程 | 8 | Unity/Unreal/Godot开发 |
| 服务器编程 | 6 | 网络同步、后端服务 |
| 美术/动画 | 7 | 2D/3D资产、动画 |
| 音效 | 4 | 背景音乐、音效 |
| QA测试 | 6 | 功能测试、性能测试 |
| 项目管理 | 4 | 进度跟踪、任务分配 |

### 适用场景

- 大型游戏项目开发
- 独立游戏团队协作
- 游戏原型快速验证
- 跨引擎项目迁移

---

### 1.2 Unity AI Workflow 2026

| 项目 | 说明 |
|-----|------|
| **GitHub** | [David-GD13/unity-ai-workflow](https://github.com/David-GD13/unity-ai-workflow) |
| **Star** | ⭐ 4 |
| **版本** | v2026.03 |
| **特点** | AI驱动的Unity开发工作流 |

### 三种开发模式

| 模式 | 角色 | 适用场景 |
|------|------|---------|
| Assistant | AI辅助文档和解释 | 学习、创意控制 |
| Mix (默认) | 协作模式，AI建议 | 大多数项目 |
| Automatic | AI构建为主 | 快速原型、游戏jam |

### 核心哲学：Game Feel

- 每项功能使用 `/implement-feature` 完整构建
- AI在写代码前询问VFX、SFX、相机反馈和触觉
- 迭代打磨，不是单独阶段

### 技术架构

- **TCREI Prompting**: Task-Context-References-Evaluate-Iterate方法论
- **验证系统**: 每个AI推荐标记 [VERIFIED]/[SYNTHESIZED]/[UNVERIFIED]
- **专家技能**: UI Toolkit、ScriptableObject、Netcode、game feel

---

### 1.3 Game-Cog (CellCog)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [nitishgargiitd/CellCog](https://github.com/nitishgargiitd/CellCog) |
| **ClawHub评分** | ⭐ 1.132 (排名第一) |
| **特点** | 游戏世界构建器，DeepResearch Bench第一名 |

### 核心能力

- **游戏世界构建**：不同于传统sprite生成器
- **角色一致性艺术**：sprite生成
- **游戏设计推理**：深度能力
- **程序化内容生成**：PCG支持

### 技术特点

- Cell-based游戏世界架构
- 程序化内容生成
- 游戏设计模式库
- AI驱动的游戏机制设计

---

### 1.4 Godot 开发 Skills

| Skill | 评分 | 说明 |
|-------|------|------|
| godot-dev-guide | 0.983 | Godot 4.x完整开发指南 |
| godot | 0.920 | Godot基础 |
| gdscript-pro | 0.910 | GDScript专业开发 |

**Godot 4.x特性**:
- GDScript 2.0性能提升
- Vulkan渲染器
- 改进的节点系统
- 更好的C#支持

---

### 1.5 Unreal Engine Skills

| Skill | 评分 | 说明 |
|-------|------|------|
| unreal-engine | 0.935 | Unreal Engine开发 |
| ue5-blueprint | 0.920 | Blueprint可视化编程 |
| ue5-cpp | 0.910 | C++开发指南 |

---

## 🐍 二、Python 开发插件

### 2.1 uv - 最快Python包管理器 (推荐)

| 项目 | 说明 |
|-----|------|
| **ClawHub评分** | ⭐ 1.092 ⭐⭐⭐⭐⭐ |
| **特点** | 2024年最快Python包管理器，10-100x比pip快 |

### 核心特性

- **极速安装**：10-100x比pip快
- **内置版本管理**：Python版本切换
- **虚拟环境**：内置venv管理
- **依赖解析**：先进的依赖解析算法

### 安装与使用

```bash
# 安装
curl -LsSf https://astral.sh/uv/install.sh | sh

# 使用
uv pip install package-name
uv venv
uv sync
uv run python main.py
```

---

### 2.2 FastAPI Pro - 生产级API开发

| 项目 | 说明 |
|-----|------|
| **ClawHub评分** | ⭐ 1.054 |
| **目标** | 生产级FastAPI工程 |

### 核心能力

- **Pydantic v2**：类型验证
- **SQLAlchemy 2.0**：异步ORM
- **认证**：JWT/SSO
- **自动文档**：OpenAPI
- **部署**：Docker/K8s

### 项目结构

```
app/
├── api/
│   └── v1/
├── core/
├── models/
├── schemas/
├── services/
└── main.py
```

---

### 2.3 Pydantic AI Skills

| 项目 |说明 |
|-----|------|
| **GitHub** | [DougTrajano/pydantic-ai-skills](https://github.com/DougTrajano/pydantic-ai-skills) |
| **Star** | ⭐ 138 |
| **特点** | Agent Skills支持，LLM应用开发 |

### 核心功能

- **Agent Skills支持**：实现 agentskills.io 规范
- **渐进式披露**：Progressive Disclosure模式
- **工作流Skills**：文件系统和工作流
- **类型安全**：专为Pydantic AI设计

### 使用场景

- LLM应用开发
- AI Agent构建
- 类型安全的AI工作流

---

### 2.4 Python Testing Patterns

| Skill | 评分 | 说明 |
|-------|------|------|
| python-testing | 1.049 | Python测试模式 |
| pytest-master | 1.032 | pytest深入 |

### pytest最佳实践

- **Fixture生命周期**：scoped fixture
- **参数化测试**：@pytest.mark.parametrize
- **Mock和Patch**： unittest.mock
- **覆盖率**：pytest-cov

### 测试策略

| 类型 | 说明 |
|------|------|
| 单元测试 | Unit |
| 集成测试 | Integration |
| E2E测试 | 端到端 |
| 性能测试 | benchmark |

---

## 🧪 三、自动化测试插件

### 3.1 Test Runner (推荐)

| 项目 | 说明 |
|-----|------|
| **ClawHub评分** | ⭐ 1.189 ⭐⭐⭐⭐⭐ |
| **特点** | 智能测试运行器 |

### 核心功能

- **智能测试选择**：基于代码变更
- **并行执行**：优化测试速度
- **失败重试**：智能重试策略
- **测试分组**：按模块/标签

### 特性

- 增量测试运行
- 依赖感知调度
- 资源池管理
- CI/CD集成

---

### 3.2 E2E Testing Patterns - Playwright/Cypress

| Skill | 评分 | 核心能力 |
|-------|------|---------|
| e2e-testing-patterns | 1.072 | 端到端测试 |
| playwright-browser | 1.041 | 浏览器自动化 |
| cypress-master | 1.028 | Cypress深入 |

### Playwright特性

- **跨浏览器**：Chrome/Firefox/Safari
- **自动等待**：智能元素等待
- **截图录制**：调试友好
- **网络拦截**：请求控制
- **移动端模拟**：响应式测试

### Cypress特性

- **实时重载**：快速迭代
- **自动等待**：减少flaky
- **调试友好**：可视化断点
- **网络控制**：请求mock

---

### 3.3 游戏客户端测试专题

#### 3.3.1 Unity Test Framework

```csharp
// Edit Mode测试
[UnityTest]
public IEnumerator PlayerMove_Test()
{
    var player = new GameObject("Player");
    var mover = player.AddComponent<PlayerMover>();
    
    mover.Move(Vector2.right);
    yield return null;
    
    Assert.AreEqual(Vector2.right, mover.Velocity);
}
```

**测试类型**：
- Edit Mode：纯C#逻辑测试
- Play Mode：集成测试

#### 3.3.2 游戏网络同步测试

| 测试类型 | 说明 |
|---------|------|
| 帧同步测试 | 确定性验证 |
| 状态同步测试 | 状态一致性 |
| 延迟模拟 | 0-500ms RTT |

#### 3.3.3 移动端游戏测试

| 平台 | 框架 | 工具 |
|------|------|------|
| Android | uiautomator | ADB |
| iOS | XCUITest | Instruments |

---

### 3.4 Android ADB 测试

| 项目 | 说明 |
|-----|------|
| **功能** | Android自动化测试 |
| **Skill** | android-adb |

### 核心能力

- **ADB命令**：设备控制
- **UI检查**：uiautomator dump
- **触摸模拟**：input tap/swipe
- **截图验证**：screencap

---

## 🛠️ 四、开发者工具插件

### 4.1 Git Essentials (推荐)

| 项目 | 说明 |
|-----|------|
| **ClawHub评分** | ⭐ 1.298 ⭐⭐⭐⭐⭐ |
| **特点** | 版本控制必备技能 |

### 核心功能

- **基础命令**：add/commit/push/pull
- **分支管理**：创建/合并/删除
- **冲突解决**：三方合并
- **历史管理**：log/reflog

### 高级特性

```bash
# Rebase工作流
git rebase main
git rebase -i HEAD~3

# Cherry-pick
git cherry-pick <commit>

# Stash
git stash push -m "work in progress"
git stash pop
```

---

### 4.2 Docker Essentials (推荐)

| 项目 | 说明 |
|-----|------|
| **ClawHub评分** | ⭐ 1.254 ⭐⭐⭐⭐⭐ |
| **特点** | 容器化开发必备 |

### 核心概念

- 镜像和容器
- Dockerfile最佳实践
- Docker Compose
- 网络和存储

### 开发工作流

- 开发环境容器化
- 多阶段构建
- 体积优化
- 安全扫描

---

### 4.3 AgentSys - 工作流自动化

| 项目 | 说明 |
|-----|------|
| **GitHub** | [avifenesh/agentsys](https://github.com/avifenesh/agentsys) |
| **Star** | ⭐ 活跃 (v5.3.7) |
| **特点** | 生产级工作流自动化系统 |

### 核心功能

- **插件系统**：灵活插件机制
- **多代理集成**：协作开发
- **任务自动化**：端到端自动化
- **PR管理**：自动代码审查
- **性能调查**：性能问题诊断

### 技术特点

- **确定检测**：正则和AST
- **LLM判断**：智能决策
- **生产验证**：经过生产环境测试
- **全面测试**：数千行代码+数千测试

---

### 4.4 Superpowers - 核心工程能力

| 项目 | 说明 |
|-----|------|
| **GitHub** | [obra/superpowers](https://github.com/obra/superpowers) |
| **Star** | ⭐ 热门 (v4.1.1) |
| **状态** | ✅ 已验证可用 |

### 核心功能

- **SDLC全覆盖**：从规划到发布
- **代码审查**：专业化审查
- **测试驱动**：TDD开发
- **调试技能**：问题追踪定位

### 包含技能

| 技能名称 | 功能 |
|---------|------|
| brainstorming | 结构化头脑风暴 |
| test-driven-development | TDD开发流程 |
| finishing-a-development-branch | 分支完成工作流 |
| root-cause-tracing | 根因追踪 |
| using-git-worktrees | Git Worktree使用 |

---

### 4.5 Claude Code Pro

| 项目 | 说明 |
|-----|------|
| **GitHub** | [maxritter/claude-codepro](https://github.com/maxritter/claude-codepro) |
| **版本** | v7.1.3 |
| **特点** | 专业级开发环境 |

### 核心功能

- **规范驱动**：Spec-driven workflow
- **TDD强制**：测试驱动开发
- **跨会话记忆**：持久化上下文
- **语义搜索**：代码语义检索
- **质量钩子**：代码质量检查

---

### 4.6 Claude Scientific Skills

| 项目 | 说明 |
|-----|------|
| **GitHub** | [K-Dense-AI/claude-scientific-skills](https://github.com/K-Dense-AI/claude-scientific-skills) |
| **版本** | v2.25.0 |
| **特点** | 科研/工程/分析技能集 |

### 适用领域

- 研究
- 科学计算
- 工程分析
- 金融
- 写作

---

## 📊 五、评分排行榜

### 5.1 游戏开发插件排名

| 排名 | Skill | 评分 | 类别 |
|------|-------|------|------|
| 1 | game-cog | 1.132 | 游戏开发 |
| 2 | game-developer-skill | 0.975 | 游戏开发 |
| 3 | fivem-dev | 0.958 | 游戏开发 |
| 4 | godot-dev-guide | 0.983 | Godot |
| 5 | unity | 0.961 | Unity |
| 6 | unreal-engine | 0.935 | Unreal |

### 5.2 Python插件排名

| 排名 | Skill | 评分 | 类别 |
|------|-------|------|------|
| 1 | uv-global | 1.092 | 工具链 |
| 2 | fastapi | 1.054 | Web |
| 3 | py | 1.049 | 核心 |
| 4 | python | 1.000 | 基础 |

### 5.3 测试插件排名

| 排名 | Skill | 评分 | 类别 |
|------|-------|------|------|
| 1 | test-runner | 1.189 | 测试执行 |
| 2 | test-patterns | 1.157 | 测试设计 |
| 3 | test-master | 1.107 | 测试管理 |
| 4 | e2e-testing-patterns | 1.072 | E2E |

### 5.4 开发者工具排名

| 排名 | Skill | 评分 | 类别 |
|------|-------|------|------|
| 1 | git-essentials | 1.298 | 版本控制 |
| 2 | docker-essentials | 1.254 | 容器化 |
| 3 | git | 1.215 | 版本控制 |
| 4 | git-workflows | 1.155 | 协作 |

---

## 🎯 六、落地建议

### 6.1 游戏开发推荐

```
优先级顺序:
1. Claude Code Game Studios - 完整团队开发
2. game-cog - 通用游戏编排
3. unity-ai-workflow / godot-dev-guide - 引擎专用
```

### 6.2 Python开发推荐

```
优先级顺序:
1. uv-global - 现代化工具链
2. fastapi - API开发
3. pydantic-ai-skills - AI应用
4. python-testing - 测试
```

### 6.3 测试推荐

```
优先级顺序:
1. test-runner - 智能测试运行
2. e2e-testing-patterns - E2E测试
3. playwright-browser - 浏览器自动化
4. android-adb - 移动端测试
```

### 6.4 开发者工具推荐

```
优先级顺序:
1. git-essentials - 版本控制
2. docker-essentials - 容器化
3. agentsys - 工作流自动化
4. superpowers - 核心能力
```

---

## 📥 七、安装指南

### 7.1 快速安装

```bash
# 克隆仓库
git clone https://github.com/Donchitos/Claude-Code-Game-Studios.git
git clone https://github.com/David-GD13/unity-ai-workflow.git

# 安装到Claude Code
cp -r Claude-Code-Game-Studios/* ~/.claude/
cp -r unity-ai-workflow/* ~/.claude/
```

### 7.2 技能安装命令

```bash
# 安装Superpowers
claude --install-skill gh-obra-superpowers

# 安装uv
claude --install-skill gh-astral-sh-uv

# 安装test-runner
claude --install-skill gh-test-runner
```

---

## 📎 相关资源

- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
- [Antigravity Awesome Skills](https://github.com/sickn33/antigravity-awesome-skills) - 970+ Skills
- [ClawHub Skills市场](https://clawhub.com)
- [Claude Code官方文档](https://docs.anthropic.com/en/docs/claude-code)

---

*文档更新时间: 2026-03-04*
