# Claude Code 热门插件补充调研 (第三十期)

> 调研时间: 2026-03-04 | 数据来源: awesome-claude-code, GitHub trending, Antigravity Skills

---

## 一、游戏客户端开发技能 (深度更新)

### 1.1 Claude Code Game Studios ⭐⭐ 强烈推荐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [Donchitos/Claude-Code-Game-Studios](https://github.com/Donchitos/Claude-Code-Game-Studios) |
| **Star** | ⭐ 30 (持续增长) |
| **更新** | 3天前 |
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

### 1.3 Unity AI Workflow (2026 新推荐)

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

### 1.4 Web/H5 游戏开发技能

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

#### WebGPU 支持情况

| 浏览器 | 支持版本 | 全球支持率 |
|--------|---------|-----------|
| Chrome | v113+ | ✅ |
| Edge | v113+ | ✅ |
| Firefox | v131+ | ✅ |
| Safari | 18.0+ | ✅ |
| **总体** | - | **~73%** |

---

## 二、Python 开发技能 (全面更新)

### 2.1 Pydantic AI 技能 ⭐ 重点推荐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [DougTrajano/pydantic-ai-skills](https://github.com/DougTrajano/pydantic-ai-skills) |
| **Star** | ⭐ 140 (持续增长) |
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
            return {"usage": self.get_usage()}
        else:
            return {"full": self.get_full_docs()}
```

### 2.2 Python Web 框架技能

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **beagle** | existential-birds/beagle | ⭐34 | 代码审查 + 验证工作流 |
| **claude-skills** | joshuaramkissoon/claude-skills | NEW | Swift/SwiftUI + Python/FastAPI |
| **security-antipatterns-python** | subhashdasyam/security-antipatterns-python | ⭐3 | Python安全最佳实践 |

#### Beagle 代码审查技能

```markdown
支持框架:
├── Python: FastAPI, Django, Flask
├── Go: Gin, Echo
├── JavaScript: React, Next.js
└── AI: Pydantic AI, LangChain
```

### 2.3 Modern Python 技能 (Trail of Bits)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [trailofbits/skills (modern-python)](https://github.com/trailofbits/skills) |
| **特点** | uv, ruff, pytest 最佳实践 |

#### 核心能力

```bash
# 安装
/plugin marketplace add trailofbits/skills
/plugin install modern-python@trailofbits

# 核心工具
├── uv: 10-100x faster than pip
├── ruff: 超快 Python linter
└── pytest: 完整测试框架
```

### 2.4 Python 开发技能汇总

| Skill 名称 | 核心能力 | 适用场景 |
|------------|---------|---------|
| python-pro | Python 3.12+ 全栈指南 | 通用 Python 开发 |
| python-patterns | 开发原则和决策 | 架构设计 |
| python-fastapi-development | FastAPI 后端开发 | API 服务 |
| python-testing-patterns | pytest/测试策略 | 质量保证 |
| async-python-patterns | asyncio 异步编程 | 高并发 |
| temporal-python-pro | Temporal 工作流 | 分布式事务 |

---

## 三、游戏客户端自动化测试技能

### 3.1 Web/H5 游戏测试 ⭐ 推荐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [lackeyjb/playwright-skill](https://github.com/lackeyjb/playwright-skill) |
| **Star** | ⭐ 1.8k |
| **功能** | Playwright 浏览器自动化 |

#### 核心特性

```markdown
### 功能
├── 通用浏览器自动化: 自定义 Playwright 代码
├── 可见浏览器: headless: false 默认
├── 渐进式披露: 按需加载 API 文档
├── 安全清理: 智能临时文件管理
└── 综合助手: 常用工具函数

### 安装
/plugin marketplace add lackeyjb/playwright-skill
/plugin install playwright-skill@playwright-skill
cd ~/.claude/plugins/marketplaces/playwright-skill/skills/playwright-skill
npm run setup
```

#### 使用示例

```markdown
# 功能测试
"Test the homepage"
"Check if the contact form works"
"Verify the signup flow"

# 响应式测试
"Take screenshots of the dashboard in mobile and desktop"
"Test responsive design across different viewports"

# 表单自动化
"Fill out the registration form and submit it"
"Click through the main navigation"
"Test the search functionality"

# 质量检查
"Check for broken links"
"Verify all images load"
"Test form validation"
```

### 3.2 Playwright 反检测技能

| 项目 | GitHub | Star | 功能 |
|------|--------|------|------|
| **playwright-undetected-skill** | dalbit-mir/playwright-undetected-skill | ⭐4 | Bot 检测绕过 |

### 3.3 移动端游戏测试

#### iOS 模拟器测试

| 项目 | 说明 |
|-----|------|
| **GitHub** | [conorluddy/ios-simulator-skill](https://github.com/conorluddy/ios-simulator-skill) |
| **Star** | ⭐ 557 |
| **平台** | macOS |

```bash
# 核心功能
├── 模拟器控制: 启动/停止
├── 应用安装: .app/.ipa
├── UI 交互: tap/swipe/drag
└── 截图捕获: 自动化验证
```

#### Android ADB 测试

```bash
# 设备校准
adb shell wm size

# UI 检查
adb shell uiautomator dump /sdcard/view.xml

# 交互操作
adb shell input tap <x> <y>
adb shell input swipe <x1> <y1> <x2> <y2> <duration_ms>
adb shell input text "Hello"

# 截图验证
adb shell screencap -p /sdcard/screen.png
```

### 3.4 Unity 游戏测试

#### Unity Test Framework

| 测试类型 | 说明 | 适用场景 |
|----------|------|---------|
| **EditMode** | 编辑器环境测试 | 工具类、辅助功能 |
| **PlayMode** | 运行时测试 | 游戏逻辑、UI |
| **Performance** | 性能测试 | 帧率、内存优化 |

### 3.5 测试技能汇总

| 用途 | 首推技能 | 备选 |
|------|---------|------|
| Web/H5游戏测试 | playwright-skill | playwright-undetected |
| Unity测试 | Unity Test Framework | - |
| 移动端测试(iOS) | ios-simulator-skill | - |
| 移动端测试(Android) | ADB + uiautomator | - |

---

## 四、开发者工具技能 (深度更新)

### 4.1 Superpowers ⭐⭐ 强烈推荐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [obra/superpowers](https://github.com/obra/superpowers) |
| **Star** | ⭐ 1.7k+ |
| **特点** | 完整软件开发工作流方法论 |

#### 核心工作流

```markdown
### 自动触发技能
├── brainstorming: 设计前头脑风暴
├── writing-plans: 实现计划编写
├── subagent-driven-development: 子代理驱动开发
├── test-driven-development: TDD 红绿重构
├── requesting-code-review: 代码审查
└── finishing-a-development-branch: 分支完成

### TDD 流程
红色 (Red) → 编写失败的测试
绿色 (Green) → 实现最小代码通过测试
重构 (Refactor)→ 重构代码保持测试通过
```

#### 安装

```bash
# Claude Code
/plugin marketplace add obra/superpowers-marketplace
/plugin install superpowers@superpowers-marketplace

# Cursor
/plugin-add superpowers
```

### 4.2 AgentSys ⭐ 生产级推荐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [avifenesh/agentsys](https://github.com/avifenesh/agentsys) |
| **特点** | 生产级工作流自动化 |

#### 核心能力

```markdown
### 功能
├── 任务到生产工作流自动化
├── PR 管理
├── 代码清理
├── 性能调查
├── 漂移检测
└── 多代理代码审查

### 技术栈
├── agnix: Agent 配置 linting
├── 正则 + AST 确定性检测
└── LLM 判断提升效率
```

### 4.3 Trail of Bits 安全技能

| 技能 | GitHub | 功能 |
|------|--------|------|
| **static-analysis** | trailofbits/skills | CodeQL/Semgrep 静态分析 |
| **variant-analysis** | trailofbits/skills | 跨代码库漏洞发现 |
| **semgrep-rule-creator** | trailofbits/skills | Semgrep 规则创建 |
| **testing-handbook-skills** | trailofbits/skills | Fuzzing/测试手册 |

### 4.4 Claude Code Game Studios 工具链

#### Hook 系统

| Hook | 触发 | 功能 |
|------|------|------|
| validate-commit.sh | git commit | 硬编码/TODO/JSON 检查 |
| validate-push.sh | git push | 受保护分支警告 |
| validate-assets.sh | 资源写入 | 命名规范验证 |
| session-start.sh | 会话开始 | 加载迭代上下文 |
| detect-gaps.sh | 会话开始 | 检测缺失文档 |
| log-agent.sh | 代理启动 | 审计追踪 |

#### 权限规则

```json
{
  "allow": ["git status", "pytest", "npm test"],
  "deny": ["git force-push", "rm -rf", ".env reading"]
}
```

### 4.5 开发者工具汇总

| 分类 | 技能 | 特点 |
|------|------|------|
| **工作流** | Superpowers | TDD + 子代理开发 |
| **自动化** | AgentSys | 生产级工作流 |
| **安全** | trailofbits-skills | CodeQL/Semgrep |
| **游戏** | Claude-Code-Game-Studios | 48代理全栈 |
| **调试** | claude-tmux | tmux 会话管理 |

---

## 五、MCP 服务器技能

### 5.1 Playwright MCP

| 项目 | GitHub |
|------|--------|
| **playwright-mcp** | [metoro-io/playwright-mcp-server](https://github.com/metoro-io/playwright-mcp-server) |

### 5.2 AWS MCP

| 项目 | GitHub | 支持服务 |
|------|--------|---------|
| **aws-mcp-server** | [alexei-led/aws-mcp-server](https://github.com/alexei-led/aws-mcp-server) | EC2, Lambda, S3, RDS, VPC |

### 5.3 更多 MCP 服务器

| 服务 | 用途 |
|------|------|
| **filesystem** | 文件系统操作 |
| **memory** | 持久化记忆 |
| **github** | GitHub API 集成 |
| **slack** | Slack 消息 |

---

## 八、GitHub Trending 新发现插件 (补充)

### 7.1 开发框架类

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **orchestkit** | yonatangross/orchestkit | ⭐98 | 61技能 + 36代理 + FastAPI/React/LangGraph |
| **claude-arsenal** | majiayu000/claude-arsenal | ⭐9 | 39+技能 + 9专业代理 |
| **safeclaw** | ykdojo/safeclaw | ⭐115 | 多会话容器管理仪表板 |

#### orchestkit 核心特性

```markdown
### 技术栈覆盖
├── FastAPI: RESTful API 设计
├── React 19: 组件开发
├── LangGraph: Agent 工作流
└── Testing & Security
```

### 7.2 产品管理类

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **Product-Manager-Skills** | deanpeters/Product-Manager-Skills | ⭐802 | 产品管理框架 |
| **pm-ai-playbook** | fimoklei/pm-ai-playbook | ⭐8 | 产品经理 AI 手册 |

### 7.3 测试类 (新发现)

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **qaskills** | PramodDutta/qaskills | ⭐71 | QA 测试技能目录 |
| **playwright-cli-agents** | yusuftayman/playwright-cli-agents | ⭐11 | Playwright E2E 测试生成 |
| **cc-plugin-eval** | sjnims/cc-plugin-eval | ⭐13 | 4阶段评估框架 |
| **vibe-testing** | knot0-com/vibe-testing | ⭐14 | LLM 推理压力测试 |
| **tap-test-skill** | aviz85/tap-test-skill | ⭐8 | 真实 API 集成测试 |

### 7.4 安全类 (新发现)

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **supabase-pentest-skills** | yoanbernabeu/supabase-pentest-skills | ⭐31 | Supabase 安全审计 |
| **jeffreysprompts.com** | Dicklesworthstone/jeffreysprompts.com | ⭐86 | 精选提示词集合 |
| **rego-skill** | Void3110/rego-skill | ⭐10 | OPA Rego 策略测试 |

### 7.5 DevOps 类 (新发现)

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **agent-skills** | terramate-io/agent-skills | ⭐26 | Terraform/Terramate |
| **robotics-agent-skills** | arpitg1304/robotics-agent-skills | ⭐115 | ROS1/ROS2 机器人开发 |
| **power-platform-skills** | DanielKerridge/claude-code-power-platform-skills | ⭐8 | Power Apps/Dataverse |

---

## 九、热门技能排行榜 (2026年3月更新)

### 6.1 按 Star 数排序

| 排名 | 技能 | Star | 分类 |
|------|------|------|------|
| 1 | playwright-skill | ⭐ 1.8k | 测试 |
| 2 | Superpowers | ⭐ 1.7k+ | 工作流 |
| 3 | Antigravity Awesome Skills | ⭐ 900+ | 综合 |
| 4 | pydantic-ai-skills | ⭐ 140 | Python |
| 5 | developer-kit | ⭐ 128 | 开发工具 |
| 6 | Claude Code Game Studios | ⭐ 30 | 游戏 |
| 7 | beagle | ⭐ 34 | 代码审查 |
| 8 | ios-simulator-skill | ⭐ 557 | 移动测试 |
| 9 | trailofbits-skills | - | 安全 |
| 10 | AgentSys | - | 自动化 |

### 6.2 按分类推荐

#### 游戏开发
- ⭐⭐⭐ Claude-Code-Game-Studios (48代理)
- ⭐⭐ unity-ai-workflow (Unity 6.2+)
- ⭐ cc-plugin-unity-gamedev

#### Python 开发
- ⭐⭐⭐ pydantic-ai-skills
- ⭐⭐ modern-python (Trail of Bits)
- ⭐ python-fastapi-development

#### 自动化测试
- ⭐⭐⭐ playwright-skill (Web测试)
- ⭐⭐ ios-simulator-skill (iOS测试)
- ⭐ Unity Test Framework

#### 开发者工具
- ⭐⭐⭐ Superpowers (TDD工作流)
- ⭐⭐ AgentSys (生产自动化)
- ⭐ trailofbits-skills (安全)

---

## 九、安装指南

### 7.1 Claude Code 插件安装

```bash
# 方法1: 插件市场
/plugin marketplace add <owner>/<repo>
/plugin install <plugin-name>@<marketplace>

# 方法2: 手动安装
git clone https://github.com/<owner>/<repo>.git ~/.claude/skills/<skill-name>

# 方法3: 项目内安装
mkdir -p .claude/skills
git clone https://github.com/<owner>/<repo>.git .claude/skills/<skill-name>
```

### 7.2 技能使用

```markdown
# 自动触发
直接描述需求，Claude 会自动选择合适的技能

# 手动触发
/skill-name [参数]

# 查看帮助
/help
```

---

## 十、总结与建议

### 8.1 技能选择建议

| 场景 | 推荐技能 |
|------|---------|
| 大型游戏项目 | Claude-Code-Game-Studios |
| Unity 开发 | unity-ai-workflow + cc-plugin-unity-gamedev |
| Python API 开发 | pydantic-ai-skills + python-fastapi-development |
| Web 游戏测试 | playwright-skill |
| 移动端游戏测试 | ios-simulator-skill / ADB |
| TDD 开发 | Superpowers |
| 安全审计 | trailofbits-skills |
| 生产级工作流 | AgentSys |

### 8.2 学习路径

```
初学者
├── 安装 Superpowers 体验完整工作流
├── 学习 playwright-skill 进行测试
└── 探索 pydantic-ai-skills

中级
├── 引入 Claude-Code-Game-Studios 开发游戏
├── 使用 trailofbits-skills 进行安全审计
└── 配置 AgentSys 自动化工作流

高级
├── 自定义 48 代理游戏开发系统
├── 构建企业级 MCP 服务器
└── 开发自定义 Skills
```

---

*文档更新时间: 2026-03-04*
*数据来源: awesome-claude-code, GitHub trending, Antigravity Skills*
