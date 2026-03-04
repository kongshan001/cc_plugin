# Claude Code 热门插件补充调研 (v71)

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

### 5.3 最新热门插件推荐

#### 5.3.1 Claude Scientific Skills

| 项目 | 详情 |
|-----|------|
| Stars | 2.26.0+ |
| 功能 | 科研、工程、分析、金融、写作用于一体 |
| 特点 | 被评价为"最佳技能仓库之一" |

#### 5.3.2 Claude Codex Settings

| 项目 | 详情 |
|-----|------|
| Stars | 2.1.0+ |
| 功能 | 核心开发者活动覆盖 |
| 特点 | 覆盖 GitHub、Azure、MongoDB、Playwright 等 |

#### 5.3.3 Fullstack Dev Skills

| 项目 | 详情 |
|-----|------|
| 技能数量 | 65+ |
| 功能 | 全栈开发 |
| 特点 | 9 个项目工作流命令，Jira/Confluence 集成 |

### 5.4 工作流与知识指南

#### 5.4.1 Ralph Orchestrator

- **功能**: 自主 AI 开发框架
- **特点**: 
  - 智能退出检测
  - 速率限制
  - 电路中断模式
  - 全面安全防护

#### 5.4.2 AgentSys

- **功能**: 工作流自动化系统
- **特点**:
  - 任务到生产工作流自动化
  - PR 管理
  - 代码清理
  - 性能调查
  - 多代理代码审查

---

## 六、总结与建议

### 6.1 游戏客户端开发推荐

| 优先级 | 技能包 | 适用场景 |
|--------|--------|----------|
| ⭐⭐⭐ | Claude-Code-Game-Studios | 多引擎全栈开发 |
| ⭐⭐⭐ | cc-plugin-unity-gamedev | Unity 专项开发 |
| ⭐⭐ | godot-development | Godot 专项开发 |
| ⭐ | Unreal-MCP | Unreal 早期支持 |

### 6.2 Python 开发推荐

| 优先级 | 技能包 | 适用场景 |
|--------|--------|----------|
| ⭐⭐⭐ | pydantic-ai-skills | AI Agent 开发 |
| ⭐⭐⭐ | FastAPI-MCP | API 开发 |
| ⭐⭐ | read-only-postgres | 安全数据库操作 |
| ⭐⭐ | aws-mcp-server | 云服务集成 |

### 6.3 自动化测试推荐

| 优先级 | 技能包 | 适用场景 |
|--------|--------|----------|
| ⭐⭐⭐ | playwright-mcp | Web/H5 游戏测试 |
| ⭐⭐⭐ | Unity Test Framework | Unity 客户端测试 |
| ⭐⭐ | ADB Skills | Android 游戏测试 |
| ⭐⭐ | Appium | 跨平台测试 |

### 6.4 开发者工具推荐

| 优先级 | 技能包 | 适用场景 |
|--------|--------|----------|
| ⭐⭐⭐ | Superpowers | 核心工程能力 |
| ⭐⭐⭐ | Parry | 高安全环境 |
| ⭐⭐ | Dippy | 权限管理优化 |
| ⭐⭐ | AgentSys | 工作流自动化 |

---

## 七、附录：资源链接

### 7.1 官方资源

- [awesome-claude-code](https://github.com/anthropics/awesome-claude-code)
- [Claude Code 官方文档](https://docs.anthropic.com/en/docs/claude-code)
- [MCP 官方注册表](https://modelcontextprotocol.io/)

### 7.2 社区资源

- [Claude Code Skills Marketplace](https://claude.com/marketplace)
- [GitHub Trending](https://github.com/trending)

---

> 本文档最后更新于 2026年3月5日
