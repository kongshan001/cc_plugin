# Claude Code 插件调研报告 - 2026年3月 (补充-第七期)

> 持续跟踪 Claude Code 生态热门插件，聚焦游戏开发、Python 开发、自动化测试、开发者工具方向

---

## 📋 调研概要

| 维度 | 统计 |
|-----|------|
| **调研时间** | 2026-03-04 |
| **覆盖方向** | 游戏开发、Python开发、自动化测试、开发者工具 |
| **技能总数** | 150+ 精选 |
| **数据来源** | awesome-claude-code, GitHub trending, Antigravity Skills |

---

## 一、游戏客户端开发技能 (补充)

### 1.1 Antigravity Game Development Skills 完整矩阵

#### 游戏开发技能分类

| 分类 | 技能 ID | 名称 | 核心能力 |
|-----|---------|------|---------|
| **2D游戏** | 2d-games | 2D游戏开发 | Sprite、TileMap、物理、相机 |
| **3D游戏** | 3d-games | 3D游戏开发 | 渲染、Shader、物理、相机 |
| **PC/Console** | pc-games | PC/主机游戏开发 | 引擎选择、平台特性、优化 |
| **移动游戏** | mobile-games | 移动游戏开发 | iOS/Android 发布、优化 |
| **网页游戏** | web-games | 网页游戏开发 | WebGL、Canvas、性能 |
| **多人游戏** | multiplayer | 多人游戏开发 | 网络同步、 matchmaking |
| **VR/AR** | vr-ar | VR/AR游戏开发 | XR 交互、空间计算 |
| **游戏美术** | game-art | 游戏美术制作 | 资产管线、工具集成 |
| **游戏音频** | game-audio | 游戏音频系统 | Wwise、FMOD、空间音频 |
| **游戏设计** | game-design | 游戏设计 | 玩法设计、关卡设计 |

#### PC/Console 游戏开发决策树

```
什么类型的游戏?
│
├── 2D 游戏
│   ├── 开源重要? → Godot
│   └── 大团队/资源多? → Unity
│
├── 3D 游戏
│   ├── AAA 画质? → Unreal
│   └── 跨平台优先? → Unity
│   └── 独立/开源? → Godot 4
│
└── 特定需求
    ├── DOTS 性能? → Unity
    ├── Nanite/Lumen? → Unreal
    └── 轻量级? → Godot
```

### 1.2 Unity 开发技能深度分析

#### Unity 技能推荐矩阵

| 技能 | 来源 | Star | 核心能力 | 适用场景 |
|-----|------|------|---------|---------|
| **unity-developer** | Antigravity | - | Unity 6 LTS 专家 | 通用Unity开发 |
| **unity-ecs-patterns** | Antigravity | - | DOTS/ECS架构 | 性能优化项目 |
| **cc-plugin-unity-gamedev** | tjboudreaux | ⭐1 | 21专业技能 | 完整开发栈 |
| **OH-Unity-GameDev-Skills** | OstrichHermit | ⭐6 | Unity+DoTween+MediaPipe | 动画/视觉项目 |
| **unity-ai-workflow** | David-GD13 | ⭐4 | Unity 6.2+ AI工作流 | AI辅助开发 |

#### Unity 技能分类详解

| 类别 | 技能 | 说明 |
|-----|------|------|
| **资源管理** | Addressables | 异步加载、内存管理 |
| **数据序列化** | MemoryPack, ScriptableObjects | 高效数据存储 |
| **动画系统** | PrimeTween, DoTween | 高性能动画 |
| **物理系统** | Physics, NavMesh, Object Pooling | 物理模拟、寻路 |
| **AI行为** | Behavior Designer, GAS | 状态机、技能系统 |
| **音视频** | Wwise, Cinemachine | 音频、相机控制 |
| **UI** | UGUI, Mobile Optimization | 移动端UI优化 |
| **DI/异步** | VContainer, UniTask | 依赖注入、异步编程 |

### 1.3 Godot 游戏开发

#### Godot 4.x 技能

| 技能 ID | 名称 | 核心能力 |
|---------|------|---------|
| **godot-gdscript-patterns** | Godot 4 专家 | GDScript 2.0、信号系统 |
| **claude-resources** | Godot 资源 | 自定义代理和技能 |

#### Godot 4.x GDScript 示例

```gdscript
extends Node

@export var speed: float = 100.0
@onready var sprite: Sprite2D = $Sprite2D

func _physics_process(delta: float) -> void:
    var direction := Input.get_axis("move_left", "move_right")
    position.x += direction * speed * delta

# 信号系统
signal health_changed(new_value: int)

@export var max_health: int = 100
var current_health: int = max_health:
    set(value):
        current_health = value
        health_changed.emit(value)
```

### 1.4 多人游戏与网络同步

#### 网络同步技术对比

| 技术 | 特点 | 适用场景 |
|------|------|---------|
| **帧同步** | 相同输入→相同输出，确定性 | 竞技游戏、动作游戏 |
| **状态同步** | 服务器权威，状态差异同步 | RPG、MMO |
| **延迟补偿** | Jitter: 0-200ms, 丢包: 5%-20% | FPS、射击游戏 |
| **客户端预测** | 本地先行，回滚机制 | 实时对战 |

---

## 二、Python 开发技能 (补充)

### 2.1 Python Skills 完整列表

| Skill ID | 名称 | 核心能力 | 评分 |
|----------|------|---------|------|
| python-pro | Python 3.12+ 专家 | 现代特性、生产级实践 | ⭐⭐⭐⭐⭐ |
| python-fastapi-development | FastAPI 开发 | SQLAlchemy、Pydantic | ⭐⭐⭐⭐⭐ |
| async-python-patterns | 异步编程 | asyncio、高并发 | ⭐⭐⭐⭐ |
| python-patterns | 设计模式 | 类型提示、最佳实践 | ⭐⭐⭐⭐ |
| python-performance-optimization | 性能优化 | cProfile、py-spy | ⭐⭐⭐⭐ |
| python-testing-patterns | 测试模式 | pytest、fixtures、TDD | ⭐⭐⭐⭐⭐ |
| python-packaging | PyPI 发布 | 包管理、版本控制 | ⭐⭐⭐⭐ |
| python-development-python-scaffold | 项目脚手架 | uv 工具链 | ⭐⭐⭐⭐ |

### 2.2 Modern Python 工具链

| 工具 | 用途 | 性能 |
|------|------|------|
| **uv** | 包管理器 | 10-100x pip |
| **ruff** | 格式化/lint | 替代 black/isort/flake8 |
| **mypy/pyright** | 类型检查 | 严格模式 |
| **pyproject.toml** | 项目配置 | 现代标准 |

#### uv 安装与使用

```bash
# 安装
curl -LsSf https://astral.sh/uv/install.sh | sh

# 项目初始化
uv init my-project
uv venv
uv pip install -r requirements.txt

# 运行脚本
uv run script.py

# 同步依赖
uv lock
uv sync
```

#### ruff 配置

```toml
[tool.ruff]
line-length = 100
target-version = "py312"

[tool.ruff.lint]
select = ["E", "F", "I", "N", "W", "UP"]
ignore = ["E501"]

[tool.ruff.format]
quote-style = "double"
```

### 2.3 FastAPI 高级特性

| 特性 | 说明 | 版本要求 |
|------|------|---------|
| Pydantic V2 | 数据验证 | FastAPI 0.100+ |
| SQLAlchemy 2.0+ | 异步ORM | FastAPI 0.100+ |
| WebSocket | 实时通信 | 全版本支持 |
| BackgroundTasks | 后台任务 | 全版本支持 |
| 依赖注入 | 灵活架构 | 全版本支持 |

#### FastAPI 异步示例

```python
from fastapi import FastAPI, Depends
from sqlalchemy.ext.asyncio import AsyncSession
from sqlalchemy import select

app = FastAPI()

async def get_db():
    async with async_session_maker() as session:
        yield session

@app.get("/users/{user_id}")
async def get_user(user_id: int, db: AsyncSession = Depends(get_db)):
    result = await db.execute(
        select(User).where(User.id == user_id)
    )
    return result.scalar_one_or_none()
```

### 2.4 AWS 云服务集成

#### AWS MCP Server 详细功能

| 服务类别 | 支持内容 | 功能 |
|---------|---------|------|
| **计算** | EC2, Lambda, ECS, EKS | 实例管理、容器部署 |
| **存储** | S3, EBS, EFS | 文件存储、备份 |
| **数据库** | RDS, DynamoDB, ElastiCache | 关系型/NoSQL/缓存 |
| **网络** | VPC, CloudFront, Route53 | 网络配置、CDN |
| **安全** | IAM, Secrets Manager | 权限管理、密钥管理 |

---

## 三、游戏客户端自动化测试 (补充)

### 3.1 浏览器自动化测试 - Playwright

#### Playwright Skill 核心功能

| 功能 | 说明 | 适用场景 |
|------|------|---------|
| **Web 应用测试** | 自动化测试 Web 应用功能 | 功能测试、回归测试 |
| **UI 验证** | 验证前端功能和行为 | 交互测试 |
| **截图捕获** | 自动截图记录测试状态 | 视觉回归测试 |
| **调试支持** | 辅助调试 UI 行为 | 问题定位 |
| **Bot 检测绕过** | Patchright 支持反检测 | 复杂场景测试 |

#### Playwright 测试示例

```python
from playwright.sync_api import sync_playwright

def test_login_flow():
    with sync_playwright() as p:
        browser = p.chromium.launch()
        page = browser.new_page()
        
        page.goto("https://game.example.com")
        page.click("#login-btn")
        page.fill("#username", "testuser")
        page.fill("#password", "password123")
        page.click("#submit")
        
        # 验证登录成功
        assert page.is_visible("#dashboard")
        
        # 截图记录
        page.screenshot(path="login_success.png")
        
        browser.close()
```

### 3.2 游戏客户端测试方案

| 测试类型 | 工具 | 适用场景 |
|---------|------|---------|
| **单元测试** | Unity Test Framework, pytest | 游戏逻辑验证 |
| **集成测试** | Playwright, Selenium | 客户端与服务端交互 |
| **UI测试** | Playwright, Appium | 游戏UI交互 |
| **性能测试** | Unity Profiler, RenderDoc | 帧率、内存测试 |
| **回归测试** | CI/CD + Playwright | 版本发布验证 |

#### Unity Test Framework

| 测试类型 | 说明 | 适用场景 |
|---------|------|---------|
| **EditMode** | 编辑器环境测试 | 工具类、辅助功能 |
| **PlayMode** | 运行时测试 | 游戏逻辑、UI |
| **Performance** | 性能测试 | 性能优化 |

### 3.3 移动端游戏测试

#### Android UI 测试 (android_ui_verification)

```bash
# 设备校准 - 获取屏幕分辨率
adb shell wm size

# UI 检查 - 获取元素信息
adb shell uiautomator dump /sdcard/view.xml

# 交互操作
adb shell input tap <x> <y>
adb shell input swipe <x1> <y1> <x2> <y2> <duration_ms>
adb shell input text "Hello"

# 截图验证
adb shell screencap -p /sdcard/screen.png
```

#### iOS 模拟器测试 (ios-simulator-skill)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [conorluddy/ios-simulator-skill](https://github.com/conorluddy/ios-simulator-skill) |
| **Star** | ⭐ 557 |
| **平台** | macOS |

**核心功能:**
- 模拟器控制 (启动/停止)
- 应用安装
- UI 交互自动化
- 截图捕获

### 3.4 TDD 开发流程

| 阶段 | 动作 | 必须执行 |
|------|------|---------|
| RED | 写失败的测试 | ✅ |
| VERIFY | 验证失败原因 | ✅ |
| GREEN | 最小代码通过 | ✅ |
| VERIFY | 验证测试通过 | ✅ |
| REFACTOR | 重构改进 | 可选 |

**TDD 铁律**: NO PRODUCTION CODE WITHOUT A FAILING TEST FIRST

---

## 四、其他开发者工具 (补充)

### 4.1 Agent 编排工具

| 项目 | GitHub | 功能 | 特点 |
|------|--------|------|------|
| **Claude Squad** | smtg-ai/claude-squad | 多工作区管理 | 同时管理多个项目 |
| **Claude Swarm** | parruda/claude-swarm | 多代理协同 | 连接 Claude Code 到代理群体 |
| **sudocode** | sudocode-ai/sudocode | 轻量级编排 | 轻量级 agent 编排开发工具 |
| **Auto-Claude** | AndyMik90/Auto-Claude | 自主多代理 | SDLC 全流程 |
| **Claude Code Flow** | ruvnet/claude-code-flow | 代码优先编排 | 递归代理循环 |

### 4.2 IDE 集成

| 工具 | GitHub | 平台 | 功能 |
|-----|--------|------|------|
| **claude-code.nvim** | greggh/claude-code.nvim | Neovim | 无缝集成 |
| **claude-code.el** | stevemolitor/claude-code.el | Emacs | Emacs 接口 |
| **Claude Code Chat** | andrepimenta/claude-code-chat | VS Code | 聊天界面 |
| **Claudix** | Haleclipse/Claudix | VS Code | 交互式聊天 |
| **claude-code-ide.el** | manzaltu/claude-code-ide.el | Emacs 增强 | LSP 集成 |

### 4.3 Hook 系统

| 技能 | GitHub | 语言 | 功能 |
|-----|--------|------|------|
| **claude-hooks** | johnlindquist/claude-hooks | TypeScript | TypeScript Hook 系统 |
| **cchooks** | GowayLee/cchooks | Python | Python Hook SDK |
| **claude-code-hooks-sdk** | beyondcode/claude-code-hooks-sdk | PHP | PHP Hook SDK |
| **parry** | vaporif/parry | - | 提示注入扫描器 |
| **Dippy** | ldayton/Dippy | - | AST 自动批准安全命令 |

### 4.4 使用监控

| 项目 | GitHub | 功能 |
|------|--------|------|
| **CC Usage** | ryoppippi/ccusage | CLI 工具分析使用情况 |
| **ccflare** | snipeship/ccflare | Web UI 仪表盘 |
| **better-ccflare** | tombii/better-ccflare | ccflare 分支增强版 |
| **Claudex** | kunwar-shah/claudex | Web 浏览器探索会话历史 |

### 4.5 Claude Code Pro

| 技能 | GitHub | 特点 |
|-----|--------|------|
| **Claude CodePro** | maxritter/claude-codepro | TDD强制执行，质量挂钩 |

### 4.6 DevOps 工具

| 技能 | GitHub | 特点 |
|-----|--------|------|
| **cc-devops-skills** | akin-ozer/cc-devops-skills | IaC代码生成 |
| **ContextKit** | FlineDev/ContextKit | 4阶段规划方法论 |

---

## 五、技能选择决策树

### 5.1 游戏开发选择

```
游戏客户端开发?
├─ Unity → cc-plugin-unity-gamedev
├─ Godot → godot-gdscript-patterns
├─ 2D游戏 → 2d-games (Antigravity)
├─ 3D游戏 → 3d-games (Antigravity)
├─ PC/Console → pc-games (Antigravity)
├─ 多人游戏 → multiplayer (Antigravity)
└─ 通用 → Claude-Code-Game-Studios
```

### 5.2 Python 开发选择

```
Python 开发?
├─ Web框架 → python-fastapi-development
├─ 数据库 → read-only-postgres
├─ 云服务 → aws-mcp-server
├─ 测试 → python-testing-patterns
├─ 性能优化 → python-performance-optimization
└─ 包管理 → uv
```

### 5.3 自动化测试选择

```
自动化测试?
├─ 浏览器 → playwright-skill
├─ 单元测试 → Unity Test Framework / pytest
├─ 代码质量 → /check, /clean
├─ TDD → /tdd-implement
└─ 移动端 → ios-simulator-skill / android_ui_verification
```

---

## 六、趋势分析

### 6.1 热门方向

| 方向 | 趋势 | 说明 |
|-----|------|------|
| **Agent工作流** | ⬆️ 上升 | agentsys, claude-code-agents, Claude Code Flow |
| **安全审计** | ⬆️ 上升 | trailofbits-skills, parry, Dippy |
| **游戏开发** | ⬆️ 上升 | Claude-Code-Game-Studios 全栈覆盖 |
| **测试自动化** | ⬆️ 上升 | Playwright主导，TDD命令丰富 |
| **Hook 生态** | ⬆️ 上升 | 多语言 SDK (Python, PHP, TypeScript) |

### 6.2 技术栈分布

```
编程语言:
├── TypeScript: 35+ 技能
├── Python: 25+ 技能
├── Go: 5+ 技能 (cc-tools, ccexp)
└── PHP: 2+ 技能 (claude-hooks-sdk)

测试框架:
├── Playwright: 主导
├── Unity Test Framework: 游戏
├── pytest: Python
└── Vitest: 前端
```

---

## 📎 相关资源

- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
- [awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills)
- [Antigravity Awesome Skills](https://github.com/chrish不要再信息泄漏/antigravity-awesome-skills)
- [Claude Code Handbook](https://nikiforovall.blog/claude-code-rules/)
- [Claude Code Ultimate Guide](https://github.com/FlorianBruniaux/claude-code-ultimate-guide)

---

*持续更新中，欢迎提交 PR 补充更多技能*
