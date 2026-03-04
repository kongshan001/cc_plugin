# Claude Code 插件补充调研 - 第三十五期

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
| **Star** | ⭐ 26 |
| **更新** | 3天前 |
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

### 1.2 Antigravity Game Development 技能

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

### 1.3 Unity 开发技能（完整版）

#### 官方/社区技能对比

| 技能 | GitHub | Star | 特点 |
|-----|--------|------|------|
| **cc-plugin-unity-gamedev** | tjboudreaux/cc-plugin-unity-gamedev | ⭐1 | 21个专业技能，完整覆盖Unity开发栈 |
| **OH-Unity-GameDev-Skills** | OstrichHermit/OH-Unity-GameDev-Skills | ⭐6 | Unity基础开发+DoTween+MediaPipe |
| **unity-ai-workflow** | David-GD13/unity-ai-workflow | ⭐4 | Unity 6.2+ AI-first工作流 |
| **unity-developer** (Antigravity) | Antigravity | - | 全栈Unity开发专家 |

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

---

## 二、Python 开发技能（补充）

### 2.1 Python 测试技能

#### python-testing-patterns (Antigravity)

| 项目 | 说明 |
|-----|------|
| **来源** | Antigravity Skills |
| **功能** | pytest, fixtures, mocking, TDD |

#### 核心能力

- **单元测试**: 使用 pytest 编写 Python 单元测试
- **Fixtures**: 创建可复用的测试 fixtures
- **Mocking**: Mock 外部依赖和服务
- **参数化测试**: 使用 pytest 参数化
- **TDD**: 测试驱动开发实践
- **异步测试**: 测试 async 代码和并发操作
- **CI/CD 集成**: 持续测试集成

#### 测试模式示例

```python
# 参数化测试
@pytest.mark.parametrize("input,expected", [
    (1, 2),
    (2, 4),
    (3, 6),
])
def test_double(input, expected):
    assert double(input) == expected

# Fixture 示例
@pytest.fixture
def mock_database():
    with patch('module.Database') as mock:
        yield mock

# 异步测试
@pytest.mark.asyncio
async def test_async_fetch():
    result = await async_fetch()
    assert result is not None
```

### 2.2 Python Web 开发

| 技能 | 来源 | 描述 |
|-----|------|------|
| **python-fastapi-development** | Antigravity | FastAPI 开发技能 |
| **python-development-python-scaffold** | Antigravity | Python 项目脚手架 |
| **python-packaging** | Antigravity | Python 包开发 |
| **python-patterns** | Antigravity | Python 设计模式 |
| **python-performance-optimization** | Antigravity | Python 性能优化 |
| **python-pro** | Antigravity | 高级 Python 开发 |

### 2.3 数据库集成

#### read-only-postgres ⭐ 安全推荐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [jawwadfirdousi/agent-skills](https://github.com/jawwadfirdousi/agent-skills) |
| **特点** | PostgreSQL 只读查询，安全优先 |

**安全措施:**
- 只读查询 (SELECT/SHOW/EXPLAIN/WITH)
- 超时控制
- 行数限制
- 多连接支持

**支持的功能:**
```sql
-- 基础查询
SELECT * FROM users WHERE id = 1;
-- 分析查询
SHOW max_connections;
EXPLAIN ANALYZE SELECT * FROM orders;
-- CTE 查询
WITH recent AS (...) SELECT * FROM recent;
```

### 2.4 AI 框架集成

#### pydantic-ai-skills ⭐ 热门

| 项目 | 说明 |
|-----|------|
| **GitHub** | [DougTrajano/pydantic-ai-skills](https://github.com/DougTrajano/pydantic-ai-skills) |
| **Star** | ⭐ 136 |
| **特点** | Pydantic AI 深度集成 |

**核心能力:**
- **类型安全**: Pydantic 模型强制类型检查
- **渐进式提示**: 按需披露信息
- **AI 集成**: 与主流 LLM 无缝集成

### 2.5 AWS 云服务集成

#### AWS MCP Server

| 项目 | 说明 |
|-----|------|
| **GitHub** | [alexei-led/aws-mcp-server](https://github.com/alexei-led/aws-mcp-server) |
| **语言** | Python |
| **Star** | ⭐ 1350+ |
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

## 三、自动化测试技能（补充）

### 3.1 Playwright 测试

#### browser-automation (Antigravity)

| 项目 | 说明 |
|-----|------|
| **来源** | Antigravity Skills |
| **功能** | 浏览器自动化，Web测试，爬虫 |

**核心能力:**

- **测试隔离**: 每个测试在完全隔离的环境中运行
- **用户定位器**: 使用用户视角选择元素
- **自动等待**: 利用 Playwright 自动等待机制

**反模式:**

- ❌ 任意超时
- ❌ 首选 CSS/XPath
- ❌ 所有测试使用单一浏览器上下文

**常见问题解决:**

| 问题 | 严重性 | 解决方案 |
|-----|--------|---------|
| 手动等待 | 严重 | 移除所有 waitForTimeout |
| 选择器问题 | 高 | 使用用户-facing locators |
| 检测系统 | 高 | 使用 stealth 插件 |
| 状态污染 | 高 | 每个测试完全隔离 |
| 调试困难 | 中 | 启用 traces |
| 视口不一致 | 中 | 设置一致的 viewport |
| 请求过快 | 高 | 添加请求间延迟 |
| 弹窗处理 | 中 | 触发前等待弹窗 |

#### Playwright MCP Server

| 项目 | 说明 |
|-----|------|
| **GitHub** | [Bright/mcp](https://github.com/Bright/mcp) |
| **功能** | Playwright MCP 服务器 |

### 3.2 API 测试

| 技能 | 来源 | 描述 |
|-----|------|------|
| **api-testing-observability-api-mock** | Antigravity | API 测试与可观测性 |
| **api-security-testing** | Antigravity | API 安全测试 |

### 3.3 游戏客户端测试

#### Unity Test Framework

| 技能 | 来源 | 描述 |
|-----|------|------|
| **unity-test-framework** | cc-plugin-unity-gamedev | Unity 官方测试框架 |
| **Test-Driven Development** | various | TDD 开发模式 |

---

## 四、开发者工具技能（补充）

### 4.1 核心工程能力

#### Superpowers ⭐ 推荐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [obra/superpowers](https://github.com/obra/superpowers) |
| **Star** | ⭐ 热门 |
| **特点** | 核心软件工程能力，SDLC 全覆盖 |

**覆盖范围:**
- 规划 (Planning)
- 审查 (Reviewing)
- 测试 (Testing)
- 调试 (Debugging)
- 完整软件开发周期

#### AgentSys ⭐ 工作流自动化

| 项目 | 说明 |
|-----|------|
| **GitHub** | [avifenesh/agentsys](https://github.com/avifenesh/agentsys) |
| **Star** | ⭐ 活跃 |
| **特点** | 工作流自动化系统 |

**功能:**
- 任务到生产工作流自动化
- PR 管理
- 代码清理
- 性能调查
- 漂移检测
- 多代理代码审查

### 4.2 Claude Code Settings

| 项目 | 说明 |
|-----|------|
| **GitHub** | [fcakyon/claude-codex-settings](https://github.com/fcakyon/claude-codex-settings) |
| **Star** | ⭐ 活跃 |
| **特点** | 核心开发者活动覆盖 |

**覆盖平台:**
- GitHub
- Azure
- MongoDB
- Tavily
- Playwright

### 4.3 Claude Code 官方插件

| 插件 | 描述 | 命令/代理 |
|-----|------|----------|
| **agent-sdk-dev** | Agent SDK 开发工具包 | /new-sdk-app, agent-sdk-verifier-py/ts |
| **code-review** | PR 代码审查 | /code-review, 5个并行审查代理 |
| **commit-commands** | Git 工作流自动化 | /commit, /commit-push-pr |
| **feature-dev** | 功能开发工作流 | /feature-dev, 3个专业代理 |
| **frontend-design** | 前端设计技能 | 自动触发 |
| **plugin-dev** | 插件开发工具包 | /plugin-dev:create-plugin |
| **pr-review-toolkit** | PR 审查工具包 | /pr-review-toolkit:review-pr |
| **security-guidance** | 安全提醒 Hook | PreToolUse hook |

### 4.4 Trail of Bits 安全技能

| 项目 | 说明 |
|-----|------|
| **GitHub** | [trailofbits/skills](https://github.com/trailofbits/skills) |
| **特点** | 专业安全技能集 |

**技能覆盖:**
- CodeQL 静态分析
- Semgrep 扫描
- 变体分析
- 修复验证
- 差异代码审查

---

## 五、热门技能汇总

### 5.1 按方向分类

#### 游戏开发
| 技能 | Star | 特点 |
|-----|------|------|
| Claude-Code-Game-Studios | ⭐26 | 48代理全栈覆盖 |
| Unity 技能集 | ⭐6 | 21技能专业栈 |
| Godot 技能 | ⭐3 | 开源游戏引擎 |
| game-development | - | 路由到子技能 |

#### Python 开发
| 技能 | Star | 特点 |
|-----|------|------|
| pydantic-ai-skills | ⭐136 | Pydantic AI 集成 |
| AWS MCP Server | ⭐1350+ | AWS 云服务集成 |
| read-only-postgres | ⭐⭐ | 安全数据库查询 |
| python-testing-patterns | - | pytest 测试技能 |

#### 自动化测试
| 技能 | Star | 特点 |
|-----|------|------|
| Playwright MCP | ⭐⭐ | 浏览器自动化 |
| browser-automation | - | Playwright 专家 |
| Unity Test | ⭐⭐ | 游戏测试 |
| pytest | ⭐⭐ | Python 测试 |

#### 开发者工具
| 技能 | Star | 特点 |
|-----|------|------|
| Superpowers | ⭐⭐ | 核心工程能力 |
| AgentSys | ⭐⭐ | 工作流自动化 |
| Claude Code Settings | ⭐⭐ | 云平台集成 |
| Trail of Bits | ⭐⭐ | 安全审计 |

---

## 六、安装使用指南

### 6.1 安装 Claude Code

```bash
# MacOS/Linux
curl -fsSL https://claude.ai/install.sh | bash

# Windows
irm https://claude.ai/install.ps1 | iex
```

### 6.2 安装技能

```bash
# 克隆到 .claude/skills 目录
git clone https://github.com/hesreallyhim/awesome-claude-code.git ~/.claude/skills

# 使用 Antigravity 安装
npx antigravity-awesome-skills --claude
```

### 6.3 使用技能

```bash
# 在 Claude Code 中使用
/SKILL_NAME [your request]

# 或者
@skill-name to help with...
```

---

## 七、总结

### 7.1 关键发现

1. **游戏开发**: Claude-Code-Game-Studios (26 stars) 是最热门的游戏开发技能，提供48个专业代理
2. **Python 开发**: pydantic-ai-skills (136 stars) 是最热门的 Python 相关技能
3. **自动化测试**: Playwright + browser-automation 是浏览器自动化的主导方案
4. **开发者工具**: Superpowers 和 AgentSys 提供全面的开发支持

### 7.2 趋势分析

- **多代理协作**: 越来越多技能采用多代理架构
- **专业化**: 针对特定框架(Unity, Unreal)和语言(Python, TypeScript)的技能增多
- **安全重视**: 安全相关技能和 Hook 越来越受关注
- **记忆/上下文**: 会话记忆和上下文管理工具兴起
- **测试自动化**: Playwright 成为浏览器自动化的事实标准

---

## 参考链接

- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
- [antigravity-awesome-skills](https://github.com/sickn33/antigravity-awesome-skills)
- [Claude Code 官方插件](https://github.com/anthropics/claude-code/tree/main/plugins)
- [Claude Code 文档](https://docs.anthropic.com/en/docs/claude-code)

---

*文档更新时间: 2026-03-04*
*持续更新中...*
