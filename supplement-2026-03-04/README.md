# Claude Code 插件调研报告 - 2026年3月 (补充-第四期)

> 持续跟踪 Claude Code 生态热门插件，聚焦游戏开发、Python 开发、自动化测试、开发者工具方向

---

## 📋 调研概要

| 维度 | 统计 |
|-----|------|
| **调研时间** | 2026-03-04 (深夜) |
| **覆盖方向** | 游戏开发、Python开发、自动化测试、开发者工具 |
| **技能总数** | 970+ (Antigravity Awesome Skills) |
| **数据来源** | awesome-claude-code, GitHub trending, Antigravity Skills, Composio |

---

## 一、游戏客户端开发技能 (更新)

### 1.1 Claude Code Game Studios ⭐ NEW

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

### 1.2 Unity 开发技能 (更新)

| 技能 | GitHub | Star | 特点 |
|-----|--------|------|------|
| **cc-plugin-unity-gamedev** | tjboudreaux/cc-plugin-unity-gamedev | ⭐1 | 21个专业技能，完整覆盖Unity开发栈 |
| **OH-Unity-GameDev-Skills** | OstrichHermit/OH-Unity-GameDev-Skills | ⭐6 | Unity基础开发+DoTween+MediaPipe |
| **unity-ai-workflow** | David-GD13/unity-ai-workflow | ⭐4 | Unity 6.2+ AI-first工作流 |
| **solana-game-skill** | solanabr/solana-game-skill | ⭐5 | Solana区块链游戏开发 |

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

### 1.3 Unity AI Workflow (2026 新增)

#### 项目地址
- **GitHub**: [David-GD13/unity-ai-workflow](https://github.com/David-GD13/unity-ai-workflow)
- **Star**: ⭐ 4
- **特点**: 专为 Unity 6.2+ 设计的 AI-first 开发工作流

#### 核心特性

```markdown
### Dev Modes (三种开发模式)
| 模式 | 角色 | 适用场景 |
|------|------|---------|
| Assistant | 你构建，AI 辅助文档和解释 | 学习、创意控制 |
| Mix (默认) | 协作模式，AI 建议，你确认 | 大多数项目 |
| Automatic | AI 构建，短的 onboarding Q&A | 快速原型、游戏 jam |

### 核心哲学: Game Feel 不是可选的
- 每项功能使用 /implement-feature 完整构建
- AI 在写代码前询问 VFX、SFX、相机反馈和触觉
- 迭代打磨，不是单独阶段

### 技术架构
- TCREI Prompting: Task-Context-References-Evaluate-Iterate 方法论
- 验证系统: 每个 AI 推荐标记 [VERIFIED]/[SYNTHESIZED]/[UNVERIFIED]
- 专家 Skills: UI Toolkit、ScriptableObject、Netcode、game feel、测试、调试
```

### 1.4 Web/H5 游戏开发

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

#### WebGPU 支持情况 (2025)

| 浏览器 | 支持 |
|--------|------|
| Chrome | ✅ v113+ |
| Edge | ✅ v113+ |
| Firefox | ✅ v131+ |
| Safari | ✅ 18.0+ |
| **全球支持率** | **~73%** |

### 1.5 游戏开发技能汇总

| 方向 | 推荐技能 | Star | 特点 |
|-----|---------|------|------|
| **Unity 完整开发** | Claude-Code-Game-Studios | ⭐26 | 48代理全栈覆盖 |
| **Unity 基础** | cc-plugin-unity-gamedev | ⭐1 | 21技能专业栈 |
| **Unity AI工作流** | unity-ai-workflow | ⭐4 | Unity 6.2+ |
| **Godot** | claude-resources | ⭐3 | 开源游戏引擎 |
| **GameMaker** | gamemaker-skills | ⭐2 | 2D游戏专用 |
| **Solana链游** | solana-game-skill | ⭐5 | 区块链游戏 |

---

## 二、Python 开发技能 (更新)

### 2.1 数据库集成 (更新)

| 技能 | GitHub | 功能 | 安全性 |
|-----|--------|------|--------|
| **read-only-postgres** | jawwadfirdousi/agent-skills | PostgreSQL只读查询 | ⭐⭐⭐⭐⭐ |
| **postgres** | sanjay3290/ai-skills | PostgreSQL完整集成 | ⭐⭐⭐ |

#### read-only-postgres 核心特性

```sql
-- 支持的查询类型
SELECT * FROM users WHERE id = 1;
SHOW max_connections;
EXPLAIN ANALYZE SELECT * FROM orders;
WITH recent AS (...) SELECT * FROM recent;
```

#### 安全特性

| 特性 | 描述 |
|-----|------|
| **只读查询** | 仅支持 SELECT/SHOW/EXPLAIN/WITH |
| **超时限制** | 防止长时间运行查询 |
| **行数限制** | 防止大数据集返回 |
| **多连接** | 支持配置多个数据库连接 |

### 2.2 AWS 云服务集成

#### AWS MCP Server

| 项目 | 说明 |
|-----|------|
| **GitHub** | [alexei-led/aws-mcp-server](https://github.com/alexei-led/aws-mcp-server) |
| **Star** | ⭐ 活跃 |
| **语言** | Python |
| **特点** | AWS CLI 集成，多环境支持 |

#### 支持的服务

| 服务类别 | 支持内容 |
|---------|---------|
| **计算** | EC2, Lambda, ECS, EKS |
| **存储** | S3, EBS, EFS |
| **数据库** | RDS, DynamoDB, ElastiCache |
| **网络** | VPC, CloudFront, Route53 |
| **安全** | IAM, Secrets Manager |

### 2.3 Pydantic AI 深度集成

#### pydantic-ai-skills

| 项目 | 说明 |
|-----|------|
| **GitHub** | [DougTrajano/pydantic-ai-skills](https://github.com/DougTrajano/pydantic-ai-skills) |
| **Star** | ⭐ 136 |
| **语言** | Python |
| **特点** | Agent Skills 支持 Pydantic AI |

#### 核心功能

- **类型安全**: Pydantic 模型强制类型检查
- **渐进式提示**: 按需披露信息
- **AI 集成**: 与主流 LLM 无缝集成
- **验证系统**: 内置强大的数据验证

### 2.4 Python 测试技能

#### 测试模式技能

| 技能 | 来源 | 功能 |
|-----|------|------|
| **python-testing-patterns** | Antigravity | Python 测试模式 |
| **temporal-python-testing** | Antigravity | Temporal 工作流测试 |
| **unit-testing-test-generate** | Antigravity | 单元测试生成 |

#### 测试框架

```bash
# pytest 最佳实践
pytest tests/ -v --cov=src --cov-report=html

# 标记测试
pytest -m "unit"  # 单元测试
pytest -m "integration"  # 集成测试
pytest -m "e2e"  # 端到端测试

# 参数化测试
@pytest.mark.parametrize("input,expected", [
    (1, 2),
    (2, 4),
])
def test_double(input, expected):
    assert double(input) == expected
```

### 2.5 Python 异步编程

| 技能 | 来源 | 功能 |
|-----|------|------|
| **async-python-patterns** | Antigravity | asyncio 异步模式 |
| **dbos-python** | Antigravity | DBOS 工作流 |

#### 异步模式

```python
# 异步模式示例
async def fetch_data(urls):
    async with aiohttp.ClientSession() as session:
        tasks = [fetch_url(session, url) for url in urls]
        return await asyncio.gather(*tasks)
```

### 2.6 Python 性能优化

| 技能 | 来源 | 功能 |
|-----|------|------|
| **python-performance-optimization** | Antigravity | 性能优化技能 |
| **python-packaging** | Antigravity | 包发布优化 |

### 2.7 Python 开发技能汇总

| 方向 | 推荐技能 | Star | 特点 |
|-----|---------|------|------|
| **数据库** | read-only-postgres | ⭐10 | 安全只读查询 |
| **云服务** | AWS MCP Server | ⭐活跃 | AWS 全服务支持 |
| **AI 框架** | pydantic-ai-skills | ⭐136 | 类型安全 AI 开发 |
| **测试** | python-testing-patterns | - | 测试模式 |
| **异步** | async-python-patterns | - | asyncio 模式 |
| **性能** | python-performance-optimization | - | 性能优化 |
| **Web 框架** | Django/Flask/FastAPI 技能 | - | 完整 Web 开发栈 |

---

## 三、游戏客户端自动化测试 (更新)

### 3.1 浏览器自动化测试

#### Playwright Skill (核心)

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
- **Bot 检测绕过**: Patchright 支持反检测

#### 技术架构

```
用户请求 → Claude Code → Playwright Skill → 浏览器自动化
                                        ↓
                              测试结果/截图 → 返回 Claude
```

#### 适用场景

- Web 游戏测试
- H5 游戏测试
- 前端功能验证
- UI 自动化测试
- 回归测试

### 3.2 Playwright Undetected Skill

| 项目 | 说明 |
|-----|------|
| **GitHub** | [dalbit-mir/playwright-undetected-skill](https://github.com/dalbit-mir/playwright-undetected-skill) |
| **Star** | ⭐ 4 |
| **特点** | Bot 检测绕过 |

#### 核心功能

- **本地主机测试**: Localhost 测试
- **截图捕获**: UI 交互截图
- **UI 交互**: 模拟真实用户操作
- **反检测**: Patchright 绕过检测

### 3.3 Go Playwright

| 项目 | 说明 |
|-----|------|
| **技能** | go-playwright |
| **来源** | Antigravity Awesome Skills |
| **特点** | Go 语言 Playwright 绑定 |

#### 核心功能

- **类型安全**: Go 类型系统保证
- **并发测试**: 高效并发测试支持
- **性能测试**: 性能基准测试

### 3.4 E2E 测试模式

| 技能 | 来源 | 功能 |
|-----|------|------|
| **e2e-testing** | Antigravity | 端到端测试基础 |
| **e2e-testing-patterns** | Antigravity | E2E 测试模式 |
| **webapp-testing** | Antigravity | Web 应用测试 |

### 3.5 Azure Playwright 测试

| 技能 | 来源 | 平台 |
|-----|------|------|
| **azure-microsoft-playwright-testing-ts** | Antigravity | Azure + TypeScript |
| **azure-resource-manager-playwright-dotnet** | Antigravity | Azure + .NET |

### 3.6 Unity 测试

#### Unity Test Framework Skill

| 项目 | 说明 |
|-----|------|
| **来源** | cc-plugin-unity-gamedev |
| **功能** | Unity 单元测试 |

#### 测试类型

| 类型 | 说明 | 适用场景 |
|-----|------|---------|
| **单元测试** | 测试单个类/方法 | 游戏逻辑验证 |
| **集成测试** | 测试多个组件交互 | 系统功能验证 |
| **UI 测试** | 测试 UI 交互 | 界面功能验证 |
| **性能测试** | 测试性能指标 | 性能优化验证 |

### 3.7 游戏自动化测试技能汇总

| 方向 | 推荐技能 | Star | 特点 |
|-----|---------|------|------|
| **Web 测试** | playwright-skill | ⭐1.8k | 主流浏览器自动化 |
| **反检测** | playwright-undetected | ⭐4 | Bot 绕过测试 |
| **Go 测试** | go-playwright | - | Go 语言绑定 |
| **Azure** | azure-playwright-testing | - | 云端测试 |
| **Unity 测试** | Unity Test Framework | - | 单元/集成测试 |
| **E2E 测试** | Claude Code Agents | ⭐10 | 端到端测试 |

---

## 四、其他开发者工具 (更新)

### 4.1 Composio 插件集合 (⭐ 推荐)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [ComposioHQ/awesome-claude-plugins](https://github.com/ComposioHQ/awesome-claude-plugins) |
| **特点** | 50+ 生产级插件 |
| **覆盖** | 前端、设计、Git、测试、后端、DevOps |

#### 核心插件列表

| 插件 | 功能 | 场景 |
|-----|------|------|
| **connect-apps** | 连接 500+ 应用 | 跨平台自动化 |
| **frontend-design** | 专业前端设计 | UI/UX 创建 |
| **test-writer-fixer** | 自动测试编写 | Jest/Vitest/Pytest |
| **code-review** | 代码审查 | 质量改进 |
| **debugger** | 高级调试 | Bug 追踪 |
| **security-guidance** | 安全指导 | OWASP 合规 |
| **changelog-generator** | 更新日志生成 | 版本发布 |
| **ship** | 完整发布流程 | CI/CD |

### 4.2 Antigravity Awesome Skills (⭐⭐⭐⭐⭐)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [sickn33/antigravity-awesome-skills](https://github.com/sickn33/antigravity-awesome-skills) |
| **Star** | ⭐ 活跃 |
| **技能数量** | 970+ |
| **覆盖** | 全栈开发、安全、测试、运维 |

#### 技能分类

| 分类 | 技能数量 | 示例 |
|-----|---------|------|
| **Architecture** | 20+ | architecture, c4-context, senior-architect |
| **Business** | 30+ | copywriting, pricing-strategy, seo-audit |
| **Data & AI** | 50+ | rag-engineer, prompt-engineer, langgraph |
| **Development** | 100+ | typescript-expert, python-patterns |
| **Security** | 40+ | api-security, sql-injection-testing |
| **Testing** | 30+ | test-driven-development, testing-patterns |
| **Infrastructure** | 50+ | docker-expert, aws-serverless |

#### 安装方式

```bash
# 默认安装 (Antigravity)
npx antigravity-awesome-skills

# Claude Code
npx antigravity-awesome-skills --claude

# Gemini CLI
npx antigravity-awesome-skills --gemini

# Codex CLI
npx antigravity-awesome-skills --codex
```

### 4.3 开发者工具技能汇总

| 方向 | 推荐技能 | Star | 特点 |
|-----|---------|------|------|
| **全能** | Antigravity Awesome Skills | 970+ | 全栈覆盖 |
| **插件集合** | Composio Plugins | 50+ | 生产级 |
| **代码审查** | code-review | - | 质量保证 |
| **测试** | test-writer-fixer | - | 自动测试 |
| **安全** | security-guidance | - | OWASP |

---

## 五、推荐技能组合

### 5.1 游戏开发推荐

```
Claude Code Game Studios + Unity 技能集 + Playwright
```

### 5.2 Python 开发推荐

```
Python Patterns + Pydantic AI + read-only-postgres + AWS
```

### 5.3 自动化测试推荐

```
Playwright + test-writer-fixer + Claude Code Agents
```

### 5.4 全栈开发推荐

```
Antigravity (970+ 技能) + Composio Plugins
```

---

## 六、总结

本期调研新增以下亮点：

1. **游戏开发**: Claude Code Game Studios (48 代理) + Unity AI Workflow
2. **Python Pydantic AI**: 集成 + AWS MCP Server
3. **测试**: Playwright 反检测 + Unity Test Framework
4. **工具**: Antigravity 970+ 技能全面更新

---

## 📚 参考链接

- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
- [Antigravity Awesome Skills](https://github.com/sickn33/antigravity-awesome-skills)
- [Composio Plugins](https://github.com/ComposioHQ/awesome-claude-plugins)
- [Claude Code Game Studios](https://github.com/Donchitos/Claude-Code-Game-Studios)
- [Unity AI Workflow](https://github.com/David-GD13/unity-ai-workflow)
