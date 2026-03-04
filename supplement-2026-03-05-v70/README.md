# Claude Code 热门插件补充调研 (v70)

> 2026年3月5日 游戏客户端/Python/自动化测试/开发者工具 - 最新热门插件深度调研

---

## 一、本期调研概述

### 1.1 调研背景

本次调研继续深入分析 Claude Code 热门插件，聚焦以下四个方向：

1. **游戏客户端开发** - Unity、Godot、Unreal 等主流游戏引擎
2. **Python 开发** - Web 框架、数据处理、AI 集成
3. **游戏客户端自动化测试** - 跨平台测试方案
4. **其他开发者工具** - 安全、编排、记忆等工具

### 1.2 数据来源

- awesome-claude-code 官方列表 (最新更新)
- GitHub Trending
- Claude Code Skills Marketplace
- MCP 官方注册表

---

## 二、游戏客户端开发插件深度分析

### 2.1 Unity 开发技能矩阵

#### 2.1.1 主流 Unity 技能包对比

| 技能包 | Stars | 技能数量 | 维护状态 | 核心优势 |
|--------|-------|---------|---------|---------|
| Claude-Code-Game-Studios | 28+ | 48+ | 活跃 | AI 代理工作室模式，支持多引擎 |
| cc-plugin-unity-gamedev | 1+ | 21 | 活跃 | 完整覆盖 Unity 开发栈 |
| OH-Unity-GameDev-Skills | 6+ | 15+ | 持续更新级 + 现代化 | 轻量 |
| unity-ai-workflow | 4+ | 多 | 新兴 | Unity 6.2+ 专用 |

#### 2.1.2 Claude-Code-Game-Studios 深度分析

**架构设计**:
```
┌─────────────────────────────────────────────────────────────────┐
│              Claude-Code-Game-Studios 架构                      │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│   ┌─────────────────────────────────────────────────────────┐  │
│   │                    AI 代理层 (48 agents)                  │  │
│   ├─────────────────────────────────────────────────────────┤  │
│   │  Design    │  Code     │  Test    │  Deploy  │ Art    │  │
│   │  (12)      │  (15)     │  (8)      │  (5)     │  (8)   │  │
│   └─────────────────────────────────────────────────────────┘  │
│                              │                                  │
│   ┌─────────────────────────────────────────────────────────┐  │
│   │                   工作流技能层 (36 skills)                │  │
│   ├─────────────────────────────────────────────────────────┤  │
│   │  Unity    │  Godot   │  Unreal  │  General  │  Tools  │  │
│   └─────────────────────────────────────────────────────────┘  │
│                              │                                  │
│   ┌─────────────────────────────────────────────────────────┐  │
│   │                    引擎集成层                            │  │
│   ├─────────────────────────────────────────────────────────┤  │
│   │  Unity 2021+ │  Godot 4.x │  Unreal Engine 5.x        │  │
│   └─────────────────────────────────────────────────────────┘  │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

**核心 AI 代理分类**:

1. **设计代理 (12)**
   - Game Mechanics Designer
   - Level Designer
   - Narrative Designer
   - UI/UX Designer
   - Sound Designer
   - 等

2. **编码代理 (15)**
   - Systems Architect
   - Gameplay Programmer
   - AI Behavior Programmer
   - Network Programmer
   - Tools Developer
   - 等

3. **测试代理 (8)**
   - QA Automation Engineer
   - Performance Tester
   - Compatibility Tester
   - Security Tester
   - 等

4. **部署代理 (5)**
   - Build Engineer
   - Release Manager
   - CI/CD Specialist
   - 等

5. **美术代理 (8)**
   - 3D Artist
   - 2D Artist
   - VFX Artist
   - 等

#### 2.1.3 cc-plugin-unity-gamedev 技能体系

**技能分类**:

```
┌─────────────────────────────────────────────────────────────┐
│              cc-plugin-unity-gamedev 技能体系                │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  工具类 (8)                                                  │
│  ├── Addressables - 资源异步加载                            │
│  ├── MemoryPack - 序列化                                    │
│  ├── ScriptableObjects - 数据资产                           │
│  ├── Profiling - 性能分析                                   │
│  ├── Package Manager - 包管理                               │
│  ├── Version Control - 版本控制                             │
│  ├── Debugging - 调试技巧                                   │
│  └── Asset Pipeline - 资源管线                              │
│                                                             │
│  动画/物理 (5)                                               │
│  ├── Animation - 动画系统                                    │
│  ├── Physics - 物理引擎                                      │
│  ├── NavMesh - 导航网格                                      │
│  ├── Object Pooling - 对象池                                 │
│  └── State Machine - 状态机                                 │
│                                                             │
│  AI/行为 (2)                                                 │
│  ├── Behavior Designer - 行为树                            │
│  └── GAS - Gameplay Ability System                         │
│                                                             │
│  音视频 (2)                                                  │
│  ├── Wwise Audio - 音频系统                                 │
│  └── Cinemachine - 相机系统                                  │
│                                                             │
│  UI (2)                                                      │
│  ├── UGUI - Unity UI                                        │
│  └── Mobile Optimization - 移动端优化                       │
│                                                             │
│  测试 (1)                                                    │
│  └── Test Framework - 单元测试                              │
│                                                             │
│  架构 (1)                                                    │
│  ├── VContainer - 依赖注入                                   │
│  └── UniTask - 异步编程                                      │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

**典型使用场景代码**:

```csharp
// Addressables 异步加载
var handle = Addressables.LoadAssetAsync<GameObject>("Prefab");
var prefab = await handle.Task;

// GAS 技能定义
[CreateAssetMenu(fileName = "NewAbility", menuName = "Ability/Active")]
public class GameplayAbility : AbilitySystemComponent
{
    public GameplayEffectContainer EffectContainer;
    
    public override void ActivateAbility(
        GameplayAbilitySpecHandle handle,
        GameplayEventData eventData)
    {
        // 技能激活逻辑
    }
}

// PrimeTween 高性能动画
Tween.Sequence()
    .Append(transform.TweenPosition(targetPos, 0.5f))
    .Append(transform.TweenScale(Vector3.one * 1.2f, 0.3f))
    .SetLoops(-1);

// VContainer 依赖注入
public class GamePresenter : IPresenter
{
    [Inject] private IGameModel _model;
    [Inject] private IGameView _view;
    
    public void OnStart()
    {
        _model.ScoreChanged += OnScoreChanged;
    }
}
```

### 2.2 Godot 开发技能

#### 2.2.1 资源汇总

| 资源 | Stars | 特点 |
|-----|-------|------|
| claude-resources (kwhitejr) | 3+ | Godot 4.x 专用 |
| godot-development | - | 基础开发技能 |
| Claude-Code-Game-Studios | 28+ | 包含 Godot 支持 |

#### 2.2.2 Godot 4.x 技能列表

| 技能类别 | 功能描述 |
|---------|---------|
| GDScript 编程 | 脚本编写、最佳实践 |
| Shader 开发 | 着色器编写 (Visual/GLSL) |
| 场景管理 | 节点操作、场景切换 |
| 资源管理 | 动态加载、资源打包 |
| 扩展开发 | GDExtension C++ 扩展 |
| 信号系统 | 事件驱动编程 |
| 动画系统 | AnimationPlayer/Tree |
| 物理引擎 | 2D/3D 物理 |

#### 2.2.3 GDScript 最佳实践

```gdscript
extends Node

# 信号定义
signal health_changed(new_health: int)
signal died

# 导出变量
@export var speed: float = 100.0
@export var max_health: int = 100

# 节点引用
@onready var sprite: Sprite2D = $Sprite2D
@onready var animation_player: AnimationPlayer = $AnimationPlayer

# 状态机
enum State { IDLE, RUN, JUMP, FALL }
var current_state: State = State.IDLE

func _ready() -> void:
    print("Node ready: ", name)

func _physics_process(delta: float) -> void:
    var direction := Input.get_axis("move_left", "move_right")
    position.x += direction * speed * delta
    
    # 状态转换
    match current_state:
        State.IDLE:
            if direction != 0:
                current_state = State.RUN
        State.RUN:
            if direction == 0:
                current_state = State.IDLE
```

### 2.3 Unreal Engine 现状

| 状态 | 说明 |
|-----|------|
| 技能数量 | 较少 |
| 成熟度 | 早期阶段 |
| 推荐方案 | 使用通用 C++/Blueprint 技能 + MCP |

#### 2.3.1 Unreal-MCP 最新动态

- UE 5.5+ 支持持续更新
- Blueprint 操作稳定性提升
- 社区贡献组件增加

#### 2.3.2 Unreal 开发建议

```
推荐工作流:
1. 使用 C++ 技能处理核心逻辑
2. 使用 Blueprint 技能处理可视化编程
3. 结合 Unreal-MCP 进行项目交互
4. 使用通用测试技能进行验证
```

### 2.4 其他游戏引擎

| 引擎 | 技能包 | Stars | 用途 |
|-----|--------|-------|------|
| GameMaker | gamemaker-skills | 2+ | 2D 游戏开发 |
| Space Engineers | se-dev-skills | 2+ | 游戏 Mod 开发 |
| Cocos | (建设中) | - | 跨平台游戏 |
| Defold | (社区) | - | 2D 游戏开发 |

---

## 三、Python 开发插件生态

### 3.1 Web 框架技能

#### 3.1.1 FastAPI-MCP 深度实践

| 项目 | 详情 |
|-----|------|
| 安装方式 | pip install fastapi-mcp |
| 功能 | API 开发 + 类型验证 + MCP 服务器 |
| 依赖 | FastAPI, pydantic, uvicorn |

**快速开始**:
```bash
# 安装
pip install fastapi-mcp

# 运行
uv run fastapi-mcp --app main:app --auth

# MCP 配置
{
  "mcpServers": {
    "my-api": {
      "command": "uv",
      "args": ["run", "fastapi-mcp", "--app", "main:app"]
    }
  }
}
```

**完整示例**:
```python
from fastapi import FastAPI
from pydantic import BaseModel
from fastapi_mcp import add_mcp_server

app = FastAPI(title="Game API")

class Player(BaseModel):
    id: int
    name: str
    score: int

players = {}

@app.post("/players")
def create_player(player: Player):
    players[player.id] = player
    return player

@app.get("/players/{player_id}")
def get_player(player_id: int):
    return players.get(player_id, {"error": "Not found"})

# 添加 MCP 路由
add_mcp_server(app, path="/mcp")
```

#### 3.1.2 Django 与 Flask 技能

| 框架 | 技能 | 特点 |
|-----|------|------|
| Django | django-skill | 全栈 Web 框架 + ORM |
| Flask | flask-skill | 轻量级 + 灵活性 |

### 3.2 Pydantic AI 技能

| 项目 | Stars | 功能 |
|-----|-------|------|
| pydantic-ai-skills | 138+ | Agent 开发 + 类型安全 |

#### 3.2.1 核心功能

- **类型安全**: Pydantic 模型强制类型检查
- **渐进式提示**: 按需披露信息
- **AI 集成**: 与主流 LLM 无缝集成
- **验证系统**: 内置强大的数据验证

#### 3.2.2 Pydantic AI 示例

```python
from pydantic import BaseModel, Field
from pydantic_ai import Agent

class GameResult(BaseModel):
    player_name: str = Field(..., description="Player name")
    score: int = Field(..., ge=0, le=100000)
    level: int = Field(..., ge=1, le=100)
    items_collected: list[str] = Field(default_factory=list)

# 创建 Agent
game_agent = Agent(
    model='openai:gpt-4',
    result_type=GameResult,
    system_prompt='You are a game score analyzer.'
)

# 使用
result = game_agent.run_sync("Player 'Hero123' scored 9500 points on level 5")
print(result.data)
# GameResult(player_name='Hero123', score=9500, level=5, items_collected=[])
```

### 3.3 数据库技能

| 技能 | 功能 | 安全特性 |
|-----|------|---------|
| read-only-postgres | PostgreSQL 只读查询 | 强制 SELECT/SHOW/EXPLAIN |
| postgres | 完整数据库操作 | 多连接 + 防御性安全 |
| memory-mcp-server | 记忆存储 | 本地持久化 |
| sqlite-mcp | SQLite 操作 | 轻量级数据库 |

#### 3.3.1 Read-Only PostgreSQL 技能

```python
# 配置
export POSTGRES_HOST=localhost
export POSTGRES_USER=your_user
export POSTGRES_PASSWORD=your_password

# 安全查询示例 (只允许 SELECT)
SELECT * FROM players WHERE score > 1000 ORDER BY score DESC LIMIT 10;

-- 允许的操作
SELECT, SHOW, EXPLAIN, WITH (CTE)

-- 禁止的操作
INSERT, UPDATE, DELETE, DROP, CREATE, ALTER, TRUNCATE
```

### 3.4 AWS 云服务集成

| MCP | Stars | 功能 |
|-----|-------|------|
| aws-mcp-server | 1350+ | EC2/Lambda/S3/RDS/VPC |
| aws-services | 社区版 | 更多 AWS 服务 |

#### 3.4.1 AWS MCP 配置

```json
{
  "mcpServers": {
    "aws": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-aws"],
      "env": {
        "AWS_ACCESS_KEY_ID": "${AWS_ACCESS_KEY_ID}",
        "AWS_SECRET_ACCESS_KEY": "${AWS_SECRET_ACCESS_KEY}",
        "AWS_DEFAULT_REGION": "us-east-1"
      }
    }
  }
}
```

### 3.5 Python 测试技能

| 技能 | 来源 | 功能 |
|-----|------|------|
| test-driven-development | superpowers | TDD 开发流程 |
| test-fixing | marketplace | 测试修复 |
| test-writing | marketplace | 测试编写 |
| pytest | 官方 | 单元测试框架 |
| pytest-mcp | 社区 | Pytest MCP 服务器 |

#### 3.5.1 Pytest 最佳实践

```python
import pytest
from unittest.mock import Mock, patch

class TestGameLogic:
    @pytest.fixture
    def player(self):
        return Player(name="TestPlayer", health=100)
    
    def test_take_damage(self, player):
        player.take_damage(30)
        assert player.health == 70
    
    def test_heal(self, player):
        player.take_damage(50)
        player.heal(20)
        assert player.health == 70
    
    @pytest.mark.asyncio
    async def test_async_save(self, player):
        await player.save_async()
        # 验证保存逻辑
    
    def test_mock_external_api(self):
        with patch('game.api.get_player_data') as mock_get:
            mock_get.return_value = {"id": 1, "name": "Test"}
            # 测试逻辑
```

---

## 四、游戏客户端自动化测试方案

### 4.1 测试类型与技术选型

```
┌─────────────────────────────────────────────────────────────┐
│              游戏客户端测试技术选型                           │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  ┌─────────────────┐    ┌─────────────────┐               │
│  │   Web/H5 游戏   │    │  原生游戏客户端  │               │
│  ├─────────────────┤    ├─────────────────┤               │
│  │  Playwright     │    │  Unity Test     │               │
│  │  Puppeteer     │    │  Framework      │               │
│  │  Selenium      │    │  PlayMode       │               │
│  └────────┬────────┘    └────────┬────────┘               │
│           │                      │                         │
│           ▼                      ▼                         │
│  ┌─────────────────────────────────────────────────┐       │
│  │              移动端游戏测试                        │       │
│  ├─────────────────────────────────────────────────┤       │
│  │  Android: ADB + android_ui_verification         │       │
│  │  iOS: ios-simulator-skill                       │       │
│  │  跨平台: Appium                                  │       │
│  └─────────────────────────────────────────────────┘       │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

### 4.2 Playwright 系列技能

| 技能 | Stars | 特点 |
|-----|-------|------|
| playwright-skill | 1.8k+ | 官方推荐 |
| playwright-undetected-skill | 4+ | Bot 检测绕过 |
| playwright-mcp | - | MCP 服务器 |
| patchright | - | 反检测浏览器自动化 |

#### 4.2.1 Playwright 核心功能

- Web 应用自动化测试
- UI 交互验证
- 截图捕获
- 登录流程测试
- 反检测能力 (Patchright)

#### 4.2.2 Playwright 游戏测试示例

```python
from playwright.sync_api import sync_playwright

def test_game_ui():
    with sync_playwright() as p:
        browser = p.chromium.launch(headless=True)
        page = browser.new_page()
        
        # 加载游戏
        page.goto("http://localhost:3000/game")
        
        # 等待游戏初始化
        page.wait_for_selector("#game-canvas", timeout=10000)
        
        # 测试 UI 交互
        page.click("#start-button")
        page.wait_for_selector("#game-started")
        
        # 验证分数显示
        score = page.inner_text("#score")
        assert score == "0"
        
        # 截图
        page.screenshot(path="game_start.png")
        
        browser.close()

def test_visual_regression(page):
    """视觉回归测试"""
    page.goto("http://localhost:3000")
    
    # 基准截图
    if not os.path.exists("baseline.png"):
        page.screenshot(path="baseline.png")
    
    # 当前截图对比
    page.screenshot(path="current.png")
    assert compare_images("current.png", "baseline.png") < 0.1
```

### 4.3 Unity 测试框架

#### 4.3.1 Unity 测试类型

| 测试类型 | 工具 | 适用场景 |
|---------|------|---------|
| EditMode | Unity Test Framework | 工具类测试 |
| PlayMode | Unity PlayMode | 游戏逻辑测试 |
| 性能测试 | Unity Profiler | 性能优化 |
| 集成测试 | Unity Test Framework | 模块交互 |

#### 4.3.2 Unity 测试示例

```csharp
// EditMode 测试
using NUnit.Framework;

[Test]
public void TestEditMode()
{ 
    Assert.AreEqual(1 + 1, 2);
}

[TestCase(2, 2, 4)]
[TestCase(0, 0, 0)]
public void TestAddition(int a, int b, int expected)
{
    Assert.AreEqual(expected, a + b);
}

// PlayMode 测试
using UnityEngine.TestTools;
using System.Collections;

[TestFixture]
public class GameTests
{
    [UnityTest]
    public IEnumerator TestPlayMode()
    {
        var go = new GameObject("Test");
        yield return null;
        Assert.IsNotNull(go);
    }
    
    [UnityTest]
    public IEnumerator TestAsync()
    {
        var task = LoadAssetAsync();
        yield return new WaitUntil(() => task.IsCompleted);
        Assert.IsTrue(task.IsCompleted);
    }
    
    [UnityTest]
    public IEnumerator TestPlayerMovement()
    {
        // 创建测试玩家
        var player = new GameObject("Player");
        var movement = player.AddComponent<PlayerMovement>();
        
        // 模拟输入
        Input.SetAxis("Horizontal", 1);
        
        // 等待物理更新
        yield return new WaitForFixedUpdate();
        
        // 验证移动
        Assert.Greater(player.transform.position.x, 0);
    }
}
```

### 4.4 移动端游戏测试

#### 4.4.1 Android 测试

| 工具 | 功能 |
|-----|------|
| android_ui_verification | ADB 自动化 UI 测试 |
| ADB | 设备控制、截图、日志 |
| Unity Profiler | 性能分析 |

**工作流程**:
```bash
# 1. 设备校准
adb shell wm size

# 2. UI 检查
adb shell uiautomator dump /sdcard/view.xml

# 3. 交互操作
adb shell input tap <x> <y>
adb shell input swipe <x1> <y1> <x2> <y2>

# 4. 截图验证
adb shell screencap -p /sdcard/screen.png
adb pull /sdcard/screen.png

# 5. 日志分析
adb logcat -d > game_log.txt
```

#### 4.4.2 iOS 测试

| 工具 | 功能 |
|-----|------|
| ios-simulator-skill | iOS 模拟器集成 |
| Xcode | 调试和性能分析 |
| xcrun simctl | 模拟器控制 |

**xcrun simctl 命令**:
```bash
# 启动模拟器
xcrun simctl boot "iPhone 15 Pro"

# 安装应用
xcrun simctl install booted /path/to/game.app

# 启动应用
xcrun simctl launch booted com.game.app

# 截图
xcrun simctl screenshot /tmp/game_screen.png

# 关闭应用
xcrun simctl terminate booted com.game.app
```

### 4.5 跨平台测试框架

| 框架 | 适用平台 | 特点 |
|-----|---------|------|
| Appium | iOS/Android/Web | 跨平台自动化 |
| Detox | React Native | 灰盒测试 |
| EarlGrey | iOS | Google 出品 |
| Espresso | Android | Google 出品 |

### 4.6 测试金字塔实践

```
        /\
       /  \      E2E 测试 (少量) - 端到端场景
      /----\    
     /      \   集成测试 (中量) - 模块交互
    /--------\  
   /          \ 单元测试 (大量) - 核心逻辑
  --------------
```

---

## 五、开发者工具深度分析

### 5.1 安全工具对比

| 工具 | 功能 | Stars | 适用场景 |
|------|------|-------|---------|
| **Parry** | 提示注入扫描器 | 新兴 | 高安全环境 |
| **Dippy** | Bash 命令过滤 | 新兴 | 权限管理 |
| **Snyk Agent Scan** | 漏洞扫描 | - | 依赖安全 |
| **Trail of Bits** | 安全审计 | 专业 | 代码审计 |
| **Britfix** | 英式英语转换 | - | 文档规范化 |

#### 5.1.1 Parry 提示注入扫描器

**安全架构**:
```
PreToolUse Hook (5层防护)
├── Taint Enforcement (污染 enforcement)
├── CLAUDE.md Scanning (配置扫描)
├── Exfil Blocking (数据外泄阻止)
├── Sensitive Path Blocking (敏感路径阻止)
└── Input Content Injection (输入内容注入检测)

PostToolUse Hook
└── 扫描工具输出中的注入/秘密

UserPromptSubmit Hook
└── 审计 .claude/ 目录权限
```

**检测能力**:
- ML 模型检测 (DeBERTa v3 / Llama Prompt Guard 2)
- 模式匹配 (40+ 凭证模式)
- AST 分析 (Tree-sitter 驱动)

#### 5.1.2 Dippy Bash 命令过滤器

**工作原理**:
```
Claude Code → Bash Command → Dippy Hook → AST 解析
                                              ↓
                        ┌──────────────────────┐
                        │     决策结果          │
                        ├──────────────────────┤
                        │ Safe  → Auto Approve  │
                        │ Unsafe → Prompt User │
                        └──────────────────────┘
```

**自动批准的命令类型**:
```bash
# 复杂管道
ps aux | grep python | awk '{print $2}'

# 链式读取
git status && git log --oneline -5

# 云检查
aws ec2 describe-instances --filters

# 构建命令
npm run build && npm run test
```

### 5.2 编排工具

| 工具 | 特点 | Stars |
|------|------|-------|
| **Sudocode** | Git 原生 + 规范管理 | 新兴 |
| **Claude Squad** | 多会话管理 | - |
| **Claude Swarm** | 多代理协作 | - |
| **Nelson** | 海军指挥架构 | - |
| **Auto-Claude** | 多代理框架 | - |

#### 5.2.1 Sudocode 深度分析

**核心概念**:
```
规范管理 (Specs) → 任务管理 (Issues) → 执行轨迹 (Executions)
       ↓                    ↓                    ↓
  .sudo/specs/        .sudo/issues/        .sudo/executions/
```

**功能特性**:
- 定义高级需求和意图
- 代理运行时上下文和计划
- 依赖图拓扑排序执行
- 临时分支/工作树累积变更

### 5.3 记忆/上下文工具

| 工具 | Token 减少 | 特点 |
|------|-----------|------|
| **HAM** | 50% | 记忆系统 |
| **Beads** | 30%+ | 分布式记忆 |
| **claude-mem** | - | 智能记忆系统 |
| **token-optimizer** | 10-20% | 幽灵 Token |
| **ContextKit** | - | 主动开发伙伴 |

### 5.4 Claude Scientific Skills

| 领域 | 功能 |
|-----|------|
| **Research** | 文献综述、元分析 |
| **Science** | 物理、化学、生物、地质 |
| **Engineering** | 硬件、CAD、固件、PCB |
| **Analysis** | 数据、统计、可视化、ML/AI |
| **Finance** | 量化交易、风险分析 |
| **Writing** | 学术写作、LaTeX |

### 5.5 开发者工具对比

| 类别 | 推荐工具 | 优先级 |
|------|---------|-------|
| **安全增强** | Parry + Dippy | ⭐⭐⭐⭐⭐ |
| **项目编排** | Sudocode | ⭐⭐⭐⭐ |
| **记忆系统** | claude-mem / Beads | ⭐⭐⭐⭐ |
| **科学研究** | Claude Scientific Skills | ⭐⭐⭐ |
| **会话管理** | Claude-tmux | ⭐⭐⭐ |
| **IDE 集成** | claude-code.nvim | ⭐⭐⭐ |

---

## 六、部署配置模板

### 6.1 安全增强配置

```bash
# ~/.config/claude-desktop/mcp.json
{
  "mcpServers": {
    "sudocode": {
      "command": "sudocode",
      "args": ["server"]
    },
    "aws": {
      "command": "aws-mcp-server",
      "args": []
    }
  }
}

# ~/.claude/settings.json
{
  "hooks": {
    "PreToolUse": [
      { "command": "parry hook", "timeout": 1000 },
      { "matcher": "Bash", "hooks": [{ "type": "command", "command": "dippy" }] }
    ],
    "PostToolUse": [{ "command": "parry hook", "timeout": 5000 }],
    "UserPromptSubmit": [{ "command": "parry hook", "timeout": 2000 }]
  }
}
```

### 6.2 游戏开发配置

```bash
# 安装 Unity 技能
git clone https://github.com/tjboudreaux/cc-plugin-unity-gamedev.git
cp -r cc-plugin-unity-gamedev ~/.claude/

# 安装 Godot 技能
git clone https://github.com/kwhitejr/claude-resources.git
cp -r claude-resources/godot ~/.claude/skills/

# 安装完整游戏工作室
git clone https://github.com/rdegges/claude-code-game-studios.git
cp -r claude-code-game-studios ~/.claude/
```

### 6.3 Python 开发配置

```bash
# 安装 FastAPI MCP
pip install fastapi-mcp

# 配置 PostgreSQL 技能
export POSTGRES_HOST=localhost
export POSTGRES_USER=your_user
export POSTGRES_PASSWORD=your_password
```

---

## 七、插件选择指南

### 7.1 按场景推荐

| 场景 | 推荐插件组合 |
|------|------------|
| **Unity 游戏开发** | cc-plugin-unity-gamedev + Unity Test Framework |
| **Godot 游戏开发** | claude-resources + GDScript Skills |
| **Unreal 游戏开发** | Unreal-MCP + 通用 C++ 技能 |
| **Web/H5 游戏测试** | Playwright Skill + 反检测版本 |
| **Python API 开发** | FastAPI-MCP + pydantic-ai-skills |
| **数据库操作** | read-only-postgres (安全优先) |
| **高安全环境** | Parry + Dippy |
| **团队协作** | Sudocode + Claude-tmux |
| **科学研究** | Claude Scientific Skills |

### 7.2 学习路径

```
入门阶段:
├── 安装 Claude Code
├── 试用 Dippy 减少权限提示
└── 配置 Sudocode 管理项目

进阶阶段:
├── 集成 Parry 加强安全
├── 使用 Playwright 进行 Web 测试
├── 配置 Python 开发技能
└── 集成 Unity/Godot 开发技能

专家阶段:
├── 自定义安全规则
├── 开发 Sudocode 集成
├── 构建自动化工作流
└── 多代理系统编排
```

---

## 八、热门插件排行榜

### 8.1 游戏开发类

| 排名 | 插件 | Stars | 趋势 |
|-----|------|-------|------|
| 1 | Claude-Code-Game-Studios | 28+ | ↗ |
| 2 | OH-Unity-GameDev-Skills | 6+ | ↗ |
| 3 | cc-plugin-unity-gamedev | 1+ | → |
| 4 | gamemaker-skills | 2+ | → |
| 5 | godot-development | - | 新兴 |

### 8.2 Python 开发类

| 排名 | 插件 | Stars | 趋势 |
|-----|------|-------|------|
| 1 | pydantic-ai-skills | 138+ | ↗ |
| 2 | aws-mcp-server | 1350+ | ↗ |
| 3 | read-only-postgres | - | → |
| 4 | fastapi-mcp | - | ↗ |
| 5 | stt-mcp-server-linux | - | 新兴 |

### 8.3 测试类

| 排名 | 插件 | Stars | 趋势 |
|-----|------|-------|------|
| 1 | playwright-skill | 1.8k+ | ↗ |
| 2 | playwright-undetected-skill | 4+ | ↗ |
| 3 | ios-simulator-skill | 557+ | → |
| 4 | android_ui_verification | - | → |
| 5 | Unity Test Framework | 内置 | → |

### 8.4 开发者工具类

| 排名 | 插件 | Stars | 趋势 |
|-----|------|-------|------|
| 1 | superpowers | 4.1k+ | ↗ |
| 2 | Sudocode | 新兴 | ↗↗ |
| 3 | Parry | 新兴 | ↗↗ |
| 4 | Dippy | 新兴 | ↗↗ |
| 5 | claude-mem | - | → |

---

## 九、总结与建议

### 9.1 关键发现

1. **游戏开发**: Unity 技能最成熟，Godot 快速发展，Unreal 仍在早期
2. **Python 开发**: FastAPI-MCP 和 Pydantic AI 是热点
3. **自动化测试**: Playwright 生态最完善，移动端测试方案多样
4. **开发者工具**: 安全类工具(Sudocode/Parry/Dippy)正在崛起

### 9.2 趋势预测

| 方向 | 预测 |
|------|------|
| 游戏开发 | 更多专业引擎技能 (Unreal/Cocos) |
| Python | AI 集成技能持续增长 |
| 测试 | 跨平台统一测试框架 |
| 安全 | 提示注入防护成为标配 |

---

## 参考资源

- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
- [awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills)
- [MCP 官方文档](https://modelcontextprotocol.io)
- [Unity 官方文档](https://docs.unity3d.com/)
- [Godot 官方文档](https://docs.godotengine.org/)
- [Playwright 文档](https://playwright.dev/)

---

*文档版本: v70 - 2026-03-05*

*持续更新中，关注 GitHub 仓库获取最新调研报告*
