# Claude Code 热门插件补充调研 (第三十一期)

> 调研时间: 2026-03-04 | 数据来源: awesome-claude-code, GitHub trending, Antigravity Skills

---

## 一、游戏客户端开发技能 (持续更新)

### 1.1 Claude Code Game Studios ⭐⭐ 强烈推荐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [Donchitos/Claude-Code-Game-Studios](https://github.com/Donchitos/Claude-Code-Game-Studios) |
| **Star** | ⭐ 30+ (持续增长) |
| **更新** | 3天内 |
| **特点** | 48个AI代理 + 36个工作流技能 + 完整协调系统 |

#### 核心能力

```markdown
# 工作室层级架构
├── Tier 1: 决策层 (Opus)
│   ├── creative-director: 创意总监
│   ├── technical-director: 技术总监
│   └── producer: 制作人
│
├── Tier 2: 部门Lead (Sonnet)
│   ├── game-designer: 游戏设计师
│   ├── lead-programmer: 首席程序员
│   ├── art-director: 美术总监
│   └── qa-lead: QA负责人
│
└── Tier 3: 专家层 (Sonnet/Haiku)
    ├── gameplay-programmer: 游戏逻辑程序
    ├── ui-programmer: UI程序
    └── tools-programmer: 工具程序
```

#### 工作流命令

| 分类 | 命令 | 功能 |
|-----|------|------|
| **Reviews** | /design-review, /code-review, /balance-check | 设计/代码/平衡审查 |
| **Production** | /sprint-plan, /milestone-review, /estimate | 迭代计划/里程碑/估算 |
| **Release** | /release-checklist, /launch-checklist, /hotfix | 发布检查/热修复 |
| **Team** | /team-combat, /team-narrative, /team-ui | 团队协作 |

### 1.2 Unity 开发技能矩阵 (2026 更新)

| 技能 | GitHub | Star | 核心领域 |
|-----|--------|------|---------|
| **cc-plugin-unity-gamedev** | tjboudreaux/cc-plugin-unity-gamedev | ⭐1 | 21个专业技能 |
| **OH-Unity-GameDev-Skills** | OstrichHermit/OH-Unity-GameDev-Skills | ⭐6 | DoTween, MediaPipe |
| **unity-ai-workflow** | David-GD13/unity-ai-workflow | ⭐4 | Unity 6.2+ AI工作流 |
| **Claude-Code-Skills-For-Unity** | flashwade03/Claude-Code-Skills-For-Unity | NEW | 知名Unity资产集成 |

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

### 1.3 Web/H5 游戏开发技能

#### 引擎选择决策树

```
游戏类型?
│
├── 2D 游戏
│   ├── 完整引擎功能? → Phaser 4
│   └── 原始渲染? → PixiJS 8
│
├── 3D 游戏
│   ├── 需要物理/XR? → Babylon.js 7
│   └── 专注渲染? → Three.js
│
└── 混合/Canvas → 自定义 WebGL
```

---

## 二、Python 开发技能 (全面更新)

### 2.1 Pydantic AI 技能 ⭐ 重点推荐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [DougTrajano/pydantic-ai-skills](https://github.com/DougTrajano/pydantic-ai-skills) |
| **Star** | ⭐ 140+ (持续增长) |
| **特点** | Agent Skills 渐进式披露支持 |

#### 核心特性

```python
# 渐进式披露示例
@dataclass
class PydanticAISkill:
    name: str
    description: str
    progressive: bool = True  # 按需加载
    
    def get_context(self, depth: int = 0) -> dict:
        """根据深度返回不同级别的信息"""
        if depth == 0:
            return {"summary": self.description}
        elif depth == 1:
            return {"summary": self.description, "usage": self.usage}
        else:
            return {"full": self.__dict__}
```

### 2.2 Python 开发技能矩阵

| Skill | GitHub | Star | 核心能力 |
|-------|--------|------|---------|
| **python-pro** | 社区精选 | ⭐⭐⭐ | Python 3.12+ 全栈指南 |
| **python-patterns** | 社区精选 | ⭐⭐ | 开发原则和决策 |
| **python-fastapi-development** | 社区精选 | ⭐⭐⭐ | FastAPI 后端开发 |
| **python-testing-patterns** | 社区精选 | ⭐⭐ | pytest/测试策略 |
| **python-performance-optimization** | 社区精选 | ⭐⭐ | 性能分析和优化 |
| **async-python-patterns** | 社区精选 | ⭐⭐ | asyncio 异步编程 |

### 2.3 AWS MCP Server ⭐ 推荐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [alexei-led/aws-mcp-server](https://github.com/alexei-led/aws-mcp-server) |
| **Star** | ⭐ 官方维护 |
| **特点** | 多 Python 环境设置 + 详细代码风格指南 |

#### 核心能力

```markdown
### 环境配置
- virtualenv / conda / uv 多选项
- 多版本 Python 支持
- 依赖管理最佳实践

### 代码规范
- Black 代码格式化
- isort import 排序
- flake8 linting
- mypy 类型检查

### 安全考虑
- 凭证管理
- 最小权限原则
- 安全审计
```

---

## 三、游戏客户端自动化测试 (重点更新)

### 3.1 Playwright MCP Server ⭐⭐ 强烈推荐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers/tree/main/src/playwright) |
| **Star** | ⭐ 官方维护 |
| **状态** | ✅ 已调研 |
| **分类** | MCP Server / 浏览器自动化 / 测试工具 |

#### 核心架构

```
┌─────────────────────────────────────────────────────────────────┐
│                  Playwright MCP Server 架构                      │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│   ┌─────────────┐   ┌─────────────┐   ┌─────────────┐        │
│   │ Claude Code │◄──│   MCP       │◄──│  Playwright │        │
│   │   客户端    │   │   协议      │   │   浏览器    │        │
│   └─────────────┘   └──────┬──────┘   └─────────────┘        │
│                             │                                   │
│                             ▼                                   │
│                    ┌─────────────────┐                         │
│                    │  Playwright    │                         │
│                    │  MCP Server     │                         │
│                    └─────────────────┘                         │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

#### 核心能力

| 能力 | 说明 |
|------|------|
| **浏览器控制** | 启动、关闭浏览器 |
| **页面操作** | 导航、点击、输入 |
| **元素定位** | CSS、XPath、ARIA |
| **截图** | 页面截图、元素截图 |
| **PDF** | 生成 PDF |
| **网络拦截** | 模拟请求/响应 |

### 3.2 自动化测试技能矩阵

| Skill | 核心能力 | 适用场景 |
|-------|---------|---------|
| **test-automator** | AI 驱动测试自动化 | 智能测试生成 |
| **testing-qa** | 综合 QA 工作流 | 质量保证 |
| **e2e-testing-patterns** | Playwright/Cypress | 端到端测试 |
| **python-testing-patterns** | pytest 最佳实践 | Python 测试 |
| **testing-patterns** | Jest 测试模式 | JS/TS 测试 |
| **unit-testing-test-generate** | 单元测试生成 | 测试覆盖 |
| **test-driven-development** | TDD 开发流程 | 测试先行 |

### 3.3 游戏客户端测试特别技能

#### 自动化测试框架对比

| 框架 | 特点 | 适用场景 |
|------|------|---------|
| **Playwright** | 跨浏览器、API 丰富 | 现代 Web 游戏测试 |
| **Selenium** | 历史悠久、生态广 | 遗留游戏项目 |
| **Cypress** | 调试友好、实时重载 | 开发测试 |
| **Appium** | 移动端测试 | 手游测试 |

#### 游戏客户端测试关键点

```markdown
### UI 自动化测试
- 元素定位策略 (data-testid 推荐)
- 等待策略 (避免硬编码 sleep)
- 页面对象模式

### 性能测试
- 帧率监控
- 内存泄漏检测
- 加载时间测试

### 兼容性测试
- 多浏览器测试
- 分辨率适配
- 操作系统兼容
```

---

## 四、开发者工具 (持续更新)

### 4.1 Claude Starter Kit ⭐ 推荐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [serpro69/claude-starter-kit](https://github.com/serpro69/claude-starter-kit) |
| **Star** | ⭐ 官方维护 |
| **特点** | 预配置 MCP 服务器和工具 |

#### 核心能力

```markdown
### 预配置系统
├── Claude Code 配置
├── Serena 配置
└── Task Master 配置

### 功能特性
- AI 驱动开发工作流
- 快速项目初始化
- 标准化开发环境
- MCP 服务器集成
```

### 4.2 Rulesync ⭐ 推荐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [dyoshikawa/rulesync](https://github.com/dyoshikawa/rulesync) |
| **Star** | ⭐ 持续更新 (v7.12.1) |
| **特点** | AI 编码代理配置转换工具 |

#### 核心能力

```markdown
### 支持平台
├── Claude Code
├── Cursor
├── Windsurf
└── 其他 AI 代理

### 功能特性
- 配置自动生成
- 规则文件转换
- MCP 服务器配置
- 命令和子代理管理
```

### 4.3 AgentSys ⭐⭐ 强烈推荐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [avifenesh/agentsys](https://github.com/avifenesh/agentsys) |
| **Star** | ⭐ 140+ (v5.3.7) |
| **特点** | 工作流自动化系统 |

#### 核心能力

```markdown
### 自动化能力
├── 任务到生产工作流
├── PR 管理
├── 代码清理
├── 性能调查
├── 漂移检测
└── 多代理代码审查

### 技术特点
- 确定式检测 (regex, AST)
- LLM 判断效率优化
- 生产系统验证
- 数千行代码 + 数千测试
```

### 4.4 Superpowers ⭐⭐ 强烈推荐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [obra/superpowers](https://github.com/obra/superpowers) |
| **Star** | ⭐ 知名 (v4.1.1) |
| **特点** | 软件工程核心能力捆绑 |

#### 核心能力

```markdown
### 覆盖范围
├── 规划 (Planning)
├── 审查 (Reviewing)
├── 测试 (Testing)
├── 调试 (Debugging)
└── SDLC 大部分阶段

### 特点
- 工程最佳实践整合
- 良好组织结构
- 适应性强的设计
- 被作者称为"superpowers"
```

### 4.5 开发者工具技能矩阵

| Skill | GitHub | Star | 核心能力 |
|-------|--------|------|---------|
| **browser-automation** | 社区精选 | ⭐⭐⭐ | 浏览器自动化 |
| **github** | 社区精选 | ⭐⭐⭐ | GitHub 基础操作 |
| **docker-essentials** | 社区精选 | ⭐⭐ | Docker 基础 |
| **docker** | 社区精选 | ⭐⭐ | Docker 完整版 |
| **docker-compose** | 社区精选 | ⭐⭐ | 多容器编排 |
| **github-workflow-automation** | 社区精选 | ⭐⭐ | GitHub Actions |
| **cli-tool-development** | 社区精选 | ⭐⭐ | CLI 工具开发 |

---

## 五、MCP 服务器生态 (持续更新)

### 5.1 MCP 服务器概览

| 服务器 | 功能 | 适用场景 |
|--------|------|---------|
| **AWS MCP Server** | AWS 资源管理 | 云服务集成 |
| **Playwright MCP** | 浏览器自动化 | Web 测试/爬虫 |
| **stt-mcp-server-linux** | 语音转文字 | Linux 语音输入 |
| **VoiceMode MCP** | 语音模式 | 自然对话 |
| **Basic Memory** | 记忆管理 | 项目知识管理 |
| **Perplexity MCP** | 搜索集成 | 研究辅助 |

### 5.2 MCP 服务器安装方式

#### 方式 1: npm 安装

```bash
# 安装 MCP 服务器
npm install -g @modelcontextprotocol/server-playwright

# 配置 Claude Code
# 在 claude.json 中添加服务器配置
```

#### 方式 2: Docker 部署

```bash
# 拉取镜像
docker pull mcp/server-playwright

# 运行容器
docker run -d --name playwright-mcp \
  -p 3100:3100 \
  mcp/server-playwright
```

---

## 六、调研总结

### 6.1 本期重点

| 方向 | 重点插件 | 推荐指数 |
|------|---------|---------|
| **游戏开发** | Claude Code Game Studios | ⭐⭐⭐ |
| **Python 开发** | Pydantic AI Skills, AWS MCP Server | ⭐⭐⭐ |
| **自动化测试** | Playwright MCP Server, Test Automator | ⭐⭐⭐ |
| **开发者工具** | AgentSys, Superpowers, Rulesync | ⭐⭐⭐ |

### 6.2 趋势分析

```markdown
### 2026 年趋势
1. MCP 协议成为 AI 编程助手标配
2. 游戏工作室级 AI 代理系统兴起
3. AI 驱动测试自动化成熟
4. 跨平台开发工具整合加速

### 技术亮点
- 渐进式技能披露
- 多代理协作系统
- 自愈测试技术
- 游戏 feel 优先开发
```

### 6.3 下期预告

- 更多 Unity 2026 新特性
- Unreal Engine 5 AI 开发
- Godot 4 MCP 集成
- 游戏 AI 行为树自动化

---

## 📚 参考资源

- [awesome-claude-code](https://github.com/anthropics/awesome-claude-code)
- [Antigravity Awesome Skills](https://github.com/anthropics/antigravity)
- [Model Context Protocol Servers](https://github.com/modelcontextprotocol/servers)
- [Claude Code 官方文档](https://docs.anthropic.com/en/docs/claude-code)

---

> 调研日期: 2026-03-04 | 持续更新中...
