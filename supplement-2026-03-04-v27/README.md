# Claude Code 热门插件补充调研 (第二十七期)

> 调研时间: 2026-03-04 | 数据来源: awesome-claude-code, GitHub trending, 技能市场分析

---

## 一、游戏客户端开发技能 (深度更新)

### 1.1 Claude Code Game Studios ⭐⭐ 强烈推荐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [Donchitos/Claude-Code-Game-Studios](https://github.com/Donchitos/Claude-Code-Game-Studios) |
| **Star** | ⭐ 28 (持续增长) |
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

### 1.2 Unity 开发技能矩阵 (2026 更新)

| 技能 | GitHub | Star | 核心领域 |
|-----|--------|------|---------|
| **cc-plugin-unity-gamedev** | tjboudreaux/cc-plugin-unity-gamedev | ⭐1 | 21个专业技能 |
| **OH-Unity-GameDev-Skills** | OstrichHermit/OH-Unity-GameDev-Skills | ⭐6 | DoTween, MediaPipe |
| **unity-ai-workflow** | David-GD13/unity-ai-workflow | ⭐4 | Unity 6.2+ AI工作流 |
| **Claude-Code-Skills-For-Unity** | flashwade03/Claude-Code-Skills-For-Unity | NEW | 知名Unity资产集成 |

#### Unity 技能深度分类

| 分类 | 包含技能 | 适用场景 |
|------|---------|---------|
| **资源管理** | Addressables, MemoryPack, ScriptableObjects | 资源加载优化 |
| **动画系统** | Animation, Timeline, Cinemachine | 过场动画、相机控制 |
| **物理系统** | Physics, NavMesh, Object Pooling | AI寻路、性能优化 |
| **游戏逻辑** | State Machine, Behavior Designer | AI行为树 |
| **能力系统** | GAS (Gameplay Ability System) | RPG/ARPG技能系统 |
| **音频** | Wwise音频集成 | 专业音频管理 |
| **UI** | UGUI, UI Toolkit | 跨平台UI |
| **DI** | VContainer | 依赖注入 |
| **异步** | UniTask | 异步编程 |
| **测试** | Unity Test Framework | 单元/集成测试 |

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
| **Star** | ⭐ 137 (持续增长) |
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
| **joshuaramkissoon/claude-skills** | joshuaramkissoon/claude-skills | NEW | Swift/SwiftUI + Python/FastAPI |
| **security-antipatterns-python** | subhashdasyam/security-antipatterns-python | ⭐3 | Python安全最佳实践 |

#### Beagle 代码审查技能

```markdown
支持框架:
├── Python: FastAPI, Django, Flask
├── Go: Gin, Echo
├── JavaScript: React, Next.js
└── AI: Pydantic AI, LangChain
```

### 2.3 数据库与云服务

| 技能 | GitHub | 功能 |
|-----|--------|------|
| **read-only-postgres** | jawwadfirdousi/agent-skills | PostgreSQL只读查询 |
| **aws-mcp-server** | alexei-led/aws-mcp-server | AWS CLI集成 |

#### AWS MCP Server 完整支持列表

| 类别 | 服务 |
|------|------|
| **计算** | EC2, Lambda, ECS, EKS |
| **存储** | S3, EBS, EFS |
| **数据库** | RDS, DynamoDB, ElastiCache |
| **网络** | VPC, CloudFront, Route53 |
| **安全** | IAM, Secrets Manager |

### 2.4 Python 测试技能

| 技能 | GitHub | 功能 |
|-----|--------|------|
| **pytest** | - | 标准测试框架 |
| **/tdd** | zscott/pane | TDD开发流程 |
| **/tdd-implement** | jerseycheese/Narraitor | TDD实现辅助 |
| **/repro-issue** | rzykov/metabase | 创建可复现测试用例 |

### 2.5 uv - Python 包管理器 (2025最快)

| 指标 | uv | pip |
|------|-----|-----|
| **安装速度** | 10-100x | 1x |
| **依赖解析** | Rust实现 | Python实现 |
| **磁盘IO** | 优化 | 标准 |

```bash
# 安装
curl -LsSf https://astral.sh/uv/install.sh | sh

# 项目初始化
uv init my-project
uv venv
uv pip install -r requirements.txt

# 运行脚本
uv run main.py
```

---

## 三、游戏客户端自动化测试 (重点更新)

### 3.1 Playwright 浏览器自动化 ⭐⭐⭐

| 技能 | GitHub | Star | 特点 |
|-----|--------|------|------|
| **playwright-skill** | lackeyjb/playwright-skill | ⭐1.8k | 主流浏览器自动化 |
| **playwright-undetected-skill** | dalbit-mir/playwright-undetected-skill | ⭐4 | Bot检测绕过 |
| **wico** | willcoliveira/qualiow-playwright-skills | ⭐4 | E2E测试可复用技能 |
| **playwright-cli-agents** | yusuftayman/playwright-cli-agents | ⭐11 | Page Object Model |

#### Playwright 核心功能

```python
# 典型测试用例
async def test_game_login():
    # 导航到游戏
    await page.goto("https://game.example.com")
    
    # 截图记录状态
    await page.screenshot(path="game-home.png")
    
    # 点击登录
    await page.click("#login-btn")
    
    # 输入凭证
    await page.fill("#username", "testuser")
    await page.fill("#password", "password123")
    
    # 提交并验证
    await page.click("#submit")
    assert await page.is_visible("#game-dashboard")
```

### 3.2 移动端游戏测试

#### iOS 模拟器测试 ⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [conorluddy/ios-simulator-skill](https://github.com/conorluddy/ios-simulator-skill) |
| **Star** | ⭐ 558 |
| **平台** | macOS |

**核心功能:**
- 模拟器启动/停止
- 应用安装
- UI 交互自动化
- 截图捕获

```bash
# 安装技能
claude install https://github.com/conorluddy/ios-simulator-skill

# 使用示例
/simulator list-devices
/simulator boot "iPhone 16 Pro"
/simulator install ~/Downloads/mygame.app
/simulator launch mygame
```

#### Android UI 测试

```bash
# 设备校准
adb shell wm size

# UI 检查
adb shell uiautomator dump /sdcard/view.xml

# 交互操作
adb shell input tap <x> <y>
adb shell input swipe <x1> <y1> <x2> <y2> <duration_ms>
adb shell input text "Hello"

# 截图
adb shell screencap -p /sdcard/screen.png
adb pull /sdcard/screen.png
```

### 3.3 Unity 测试框架

| 测试类型 | 说明 | 适用场景 |
|---------|------|---------|
| **EditMode** | 编辑器环境测试 | 工具类、辅助功能 |
| **PlayMode** | 运行时测试 | 游戏逻辑、UI |
| **Performance** | 性能测试 | 帧率、内存优化 |

```csharp
// Unity 单元测试示例
[Test]
public void TestPlayerHealthInitialization()
{
    var player = new GameObject("Player");
    var health = player.AddComponent<PlayerHealth>();
    
    Assert.AreEqual(100, health.MaxHealth);
    Assert.AreEqual(100, health.CurrentHealth);
}

[Test]
public void TestPlayerTakeDamage()
{
    var player = new GameObject("Player");
    var health = player.AddComponent<PlayerHealth>();
    
    health.TakeDamage(30);
    
    Assert.AreEqual(70, health.CurrentHealth);
}
```

### 3.4 QA Skills Directory

| 项目 | 说明 |
|-----|------|
| **GitHub** | [PramodDutta/qaskills](https://github.com/PramodDutta/qaskills) |
| **Star** | ⭐ 71 |
| **特点** | AI编码代理测试技能精选目录 |

#### 涵盖方向

- 自动化测试
- 性能测试
- 安全测试
- 代码审查

---

## 四、开发者工具技能 (更新)

### 4.1 编排与工作流

| 技能 | GitHub | 特点 |
|-----|--------|------|
| **agentsys** | avifenesh/agentsys | 生产级工作流自动化 |
| **superpowers** | obra/superpowers | 核心工程技能集 |
| **claude-code-agents** | undeadlist/claude-code-agents | E2E开发工作流 |
| **sudocode** | sudocode-ai/sudocode | 轻量级agent编排 |

#### AgentSys 核心特性

```markdown
功能矩阵:
├── 任务自动化: task-to-production
├── PR管理: 自动创建/审查PR
├── 代码清理: 自动清理死代码
├── 性能调查: 性能瓶颈分析
├── 漂移检测: 配置漂移检测
└── 多代理审查: 并行代码审查
```

### 4.2 安全审计

| 技能 | GitHub | 特点 |
|-----|--------|------|
| **trailofbits-skills** | trailofbits/skills | CodeQL/Semgrep集成 |
| **parry** | vaporif/parry | 提示注入扫描器 |
| **Dippy** | ldayton/Dippy | AST自动批准安全命令 |

### 4.3 会话管理工具

| 技能 | GitHub | 功能 |
|-----|--------|------|
| **claude-tmux** | nielsgroen/claude-tmux | tmux会话管理 |
| **claude-esp** | phiat/claude-esp | 隐藏输出流式传输 |
| **claude-code-tools** | pchalasani/claude-code-tools | 会话连续性 |
| **recall** | zippoxer/recall | 会话全文搜索 |

### 4.4 Claude Code 增强工具

| 工具 | GitHub | 功能 |
|-----|--------|------|
| **claudekit** | carlrannaberg/claudekit | 20+子代理 |
| **ContextKit** | FlineDev/ContextKit | 4阶段规划 |
| **Claude Hub** | claude-did-this/claude-hub | GitHub集成 |
| **Rulesync** | dyoshikawa/rulesync | 配置同步 |

### 4.5 Hooks 生态系统

| 技能 | GitHub | 语言 |
|-----|--------|------|
| **claude-hooks** | johnlindquist/claude-hooks | TypeScript |
| **cchooks** | GowayLee/cchooks | Python |
| **claude-hooks-sdk** | beyondcode/claude-hooks-sdk | PHP |

---

## 五、热门技能推荐 (按场景)

### 5.1 游戏开发推荐

| 场景 | 首推技能 | 备选 |
|-----|---------|------|
| **Unity完整开发** | Claude-Code-Game-Studios | Claude-Code-Game-Studios |
| **Unity快速上手** | unity-ai-workflow | cc-plugin-unity-gamedev |
| **Godot开发** | claude-resources | - |
| **Web/H5游戏** | playwright-skill | - |
| **链游开发** | solana-game-skill | - |

### 5.2 Python 开发推荐

| 场景 | 首推技能 | 备选 |
|-----|---------|------|
| **AI应用开发** | pydantic-ai-skills | - |
| **Web后端** | FastAPI + beagle | - |
| **数据库** | read-only-postgres | - |
| **云服务** | aws-mcp-server | - |
| **测试** | pytest + /tdd | - |

### 5.3 测试自动化推荐

| 场景 | 首推技能 | 备选 |
|-----|---------|------|
| **Web测试** | playwright-skill | wico |
| **反检测测试** | playwright-undetected | - |
| **iOS测试** | ios-simulator-skill | - |
| **Android测试** | ADB + uiautomator | - |
| **Unity测试** | Unity Test Framework | - |

### 5.4 开发者效率推荐

| 场景 | 首推技能 | 备选 |
|-----|---------|------|
| **全栈开发** | superpowers | fullstack-dev-skills |
| **DevOps** | cc-devops-skills | Container Use |
| **安全审计** | trailofbits-skills | parry |
| **代码审查** | beagle | agentsys |

---

## 六、技能选择决策树

### 6.1 游戏客户端开发

```
游戏客户端开发?
├─ Unity → Claude-Code-Game-Studios
│           └─ Unity 6.2+ → unity-ai-workflow
├─ Godot → claude-resources
├─ GameMaker → gamemaker-skills
├─ Web/H5 → playwright-skill
└─ 区块链 → solana-game-skill
```

### 6.2 Python 开发

```
Python 开发?
├─ AI应用 → pydantic-ai-skills
├─ Web框架 → beagle (代码审查)
├─ 数据库 → read-only-postgres
├─ 云服务 → aws-mcp-server
└─ 测试 → pytest + /tdd
```

### 6.3 自动化测试

```
自动化测试?
├─ Web/H5游戏 → playwright-skill
├─ 反检测 → playwright-undetected
├─ iOS → ios-simulator-skill
├─ Android → ADB + uiautomator
└─ Unity → Unity Test Framework
```

---

## 七、安装与配置

### 7.1 快速安装

```bash
# 克隆安装
git clone https://github.com/用户名/技能名.git
cp -r 技能名 ~/.claude/skills/

# 或使用 claude install 命令
claude install https://github.com/Donchitos/Claude-Code-Game-Studios
claude install https://github.com/DougTrajano/pydantic-ai-skills
claude install https://github.com/lackeyjb/playwright-skill
```

### 7.2 验证安装

```bash
# 列出已安装技能
claude --list-skills

# 或在 Claude Code 中
/skill list
```

---

## 八、趋势总结

### 8.1 本期重点

1. **Claude Code Game Studios**: 游戏开发领域首个完整工作室级解决方案
2. **Unity AI Workflow**: 专为 Unity 6.2+ 设计的 AI-first 开发范式
3. **pydantic-ai-skills**: Python AI 开发类型安全标杆
4. **playwright-skill**: Web/H5 游戏测试首选方案
5. **ios-simulator-skill**: iOS 游戏测试必备工具

### 8.2 发展趋势

| 方向 | 趋势 | 说明 |
|-----|------|------|
| **多代理协作** | ⬆️ 上升 | 工作室级开发流程 |
| **AI-first工作流** | ⬆️ 上升 | 专为AI设计的工作流 |
| **安全审计** | ⬆️ 上升 | 提示注入防护 |
| **渐进式加载** | ⬆️ 上升 | token优化 |
| **跨平台测试** | ⬆️ 上升 | 移动端测试需求增加 |

---

*调研持续更新中，关注 [cc_plugin](https://github.com/kongshan001/cc_plugin) 获取最新资讯*
