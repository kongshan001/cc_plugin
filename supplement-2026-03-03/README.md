# Claude Code 插件补充调研 - 2026年3月3日

## 📋 调研背景

本期调研聚焦于 GitHub trending 和 awesome-claude-code 中的热门插件，重点关注：
1. 游戏客户端开发 (Unity、Web/H5)
2. Python 开发
3. 游戏客户端自动化测试
4. 其他开发者工具

---

## 一、新增热门插件汇总

### 1.1 游戏开发方向 ⭐

| 插件 | GitHub | Star | 新增时间 | 特点 |
|-----|--------|------|---------|------|
| **Claude-Code-Game-Studios** | Donchitos/Claude-Code-Game-Studios | ⭐26 | 3天前 | 48 AI代理 + 36工作流技能 |
| **solana-game-skill** | solanabr/solana-game-skill | ⭐5 | Jan 30 | Solana区块链游戏 |

### 1.2 开发者工具方向 ⭐

| 插件 | GitHub | Star | 特点 |
|-----|--------|------|------|
| **sudocode** | sudocode-ai/sudocode | 新兴 | 轻量级agent编排工具 |
| **claude-tmux** | nielsgroen/claude-tmux | ⭐活跃 | tmux会话管理 |
| **claude-esp** | phiat/claude-esp | 新兴 | 隐藏输出流式传输 |

---

## 二、Claude-Code-Game-Studios 深度分析

### 2.1 概述

**Claude-Code-Game-Studios** 是一个将 Claude Code 转变为完整游戏开发工作室的插件，包含48个AI代理和36个工作流技能。

### 2.2 核心架构

```
┌─────────────────────────────────────────────┐
│         Claude Code Game Studios            │
├─────────────────────────────────────────────┤
│  ┌─────────┐  ┌─────────┐  ┌─────────┐    │
│  │  48 AI  │  │  36工作流 │  │  协调   │    │
│  │  代理    │  │  技能    │  │  系统   │    │
│  └─────────┘  └─────────┘  └─────────┘    │
├─────────────────────────────────────────────┤
│  支持引擎: Unity, Unreal, Godot, WebGL     │
└─────────────────────────────────────────────┘
```

### 2.3 适用场景

| 场景 | 推荐理由 |
|-----|---------|
| **大型游戏项目** | 48个专业代理覆盖全流程 |
| **工作室工作流** | 模拟真实游戏开发团队 |
| **跨平台开发** | Unity/Unreal/Godot/WebGL |
| **快速原型** | 36个工作流技能加速开发 |

### 2.4 安装

```bash
git clone https://github.com/Donchitos/Claude-Code-Game-Studios.git
cp -r Claude-Code-Game-Studios ~/.claude/skills/
```

---

## 三、游戏客户端测试方案详解

### 3.1 Unity 游戏测试

#### Unity Test Framework

| 测试类型 | 说明 | 适用场景 |
|---------|------|---------|
| **EditMode** | 编辑器环境测试 | 工具类、辅助功能 |
| **PlayMode** | 运行时测试 | 游戏逻辑、UI |
| **Performance** | 性能测试 | 性能优化 |

#### 测试示例

```csharp
// 单元测试
[Test]
public void TestPlayerHealth() {
    var player = new Player();
    Assert.AreEqual(100, player.Health);
    
    player.TakeDamage(30);
    Assert.AreEqual(70, player.Health);
}

// 集成测试
[UnityTest]
public IEnumerator TestPlayerMovement() {
    var player = new GameObject("Player");
    var movement = player.AddComponent<PlayerMovement>();
    
    movement.Move(Vector2.right);
    yield return new WaitForSeconds(0.1f);
    
    Assert.IsTrue(player.transform.position.x > 0);
}
```

### 3.2 Web/H5 游戏测试

#### Playwright 测试方案

```python
from playwright.sync_api import sync_playwright

def test_web_game():
    with sync_playwright() as p:
        browser = p.chromium.launch()
        page = browser.new_page()
        
        # 加载游戏
        page.goto("http://localhost:3000/game")
        
        # 模拟用户交互
        page.click("#start-button")
        page.wait_for_selector("#game-canvas")
        
        # 验证游戏加载
        assert page.is_visible("#game-canvas")
        
        # 截图记录
        page.screenshot(path="game_start.png")
        
        browser.close()
```

#### 反检测测试

```python
# 使用 playwright-undetected-skill
from patchright.sync_api import sync_playwright

def test_undetected():
    with sync_playwright() as p:
        browser = p.chromium.launch(
            args=['--disable-blink-features=AutomationControlled']
        )
        # 绕过bot检测
        page = browser.new_page()
        # ... 测试代码
```

### 3.3 移动端游戏测试

#### Android 测试 (ADB)

```bash
# 1. 连接设备
adb devices

# 2. 获取屏幕分辨率
adb shell wm size

# 3. 安装游戏
adb install game.apk

# 4. 启动游戏
adb shell am start -n com.game.package/.MainActivity

# 5. UI交互
adb shell input tap 500 500
adb shell input swipe 100 500 400 500 300

# 6. 截图验证
adb shell screencap -p /sdcard/screen.png
adb pull /sdcard/screen.png ./test_result.png
```

#### iOS 测试 (ios-simulator-skill)

```bash
# 使用 ios-simulator-skill
claude --skill ios-simulator-skill

# 启动模拟器
/simulator launch "iPhone 15"

# 安装应用
/simulator install ./game.app

# 运行测试
/simulator test ./game-test.spec
```

### 3.4 测试工具对比

| 工具 | 平台 | 优点 | 缺点 |
|-----|------|------|------|
| **Playwright** | Web/H5 | 功能全面、生态好 | Web限定 |
| **Unity Test Framework** | Unity | 原生集成 | 引擎限定 |
| **ADB + uiautomator** | Android | 灵活强大 | 需要root |
| **ios-simulator-skill** | iOS | macOS原生 | 平台限定 |
| **Appium** | 跨平台 | 通用性强 | 配置复杂 |

---

## 四、Python 开发技能更新

### 4.1 数据库技能 (更新)

#### read-only-postgres 安全特性

| 特性 | 说明 |
|-----|------|
| **只读查询** | 仅支持 SELECT/SHOW/EXPLAIN/WITH |
| **超时控制** | 防止长时间查询 |
| **行数限制** | 防止大规模数据泄露 |
| **多连接** | 支持配置多个数据库 |

#### 使用示例

```python
# 配置多个数据库连接
{
    "databases": [
        {
            "name": "production",
            "host": "prod.db.example.com",
            "description": "生产数据库"
        },
        {
            "name": "analytics",
            "host": "analytics.db.example.com",
            "description": "分析数据库"
        }
    ]
}
```

### 4.2 AI 框架集成

#### pydantic-ai-skills

```python
from pydantic import BaseModel
from pydantic_ai import Agent

class User(BaseModel):
    id: int
    name: str
    email: str

agent = Agent(
    model='anthropic:claude-3-5-sonnet-20241022',
    result_type=User
)

# 使用技能
result = agent.run_sync("创建用户 John Doe")
print(result.data)  # User(id=1, name='John Doe', email='john@example.com')
```

### 4.3 测试开发

#### TDD 流程

```
┌──────────────────────────────────────┐
│           TDD 开发流程               │
├──────────────────────────────────────┤
│  1. 红色 (Red)                       │
│     └─ 编写失败的测试                │
│            ↓                         │
│  2. 绿色 (Green)                     │
│     └─ 实现最小代码通过测试           │
│            ↓                         │
│  3. 重构 (Refactor)                  │
│     └─ 重构代码保持测试通过           │
└──────────────────────────────────────┘
```

#### pytest 最佳实践

```bash
# 安装
pip install pytest pytest-cov pytest-asyncio

# 运行测试
pytest tests/ -v --cov=src --cov-report=html

# 标记分类
pytest -m "unit"      # 单元测试
pytest -m "integration"  # 集成测试
pytest -m "e2e"       # 端到端测试
```

---

## 五、开发者工具新增

### 5.1 编排工具

#### sudocode

| 项目 | 说明 |
|-----|------|
| **GitHub** | sudocode-ai/sudocode |
| **特点** | 轻量级agent编排工具 |

**核心功能:**
- 规范框架集成
- Jira 风格任务管理
- 工作流自动化
- 多代理协调

### 5.2 会话管理

#### claude-tmux

```bash
# 启动 tmux 会话
claude-tmux start

# 列出所有会话
claude-tmux list

# 切换会话
claude-tmux switch session_name

# 会话监控
claude-tmux status
```

### 5.3 输出流式传输

#### claude-esp

```
功能: 将 Claude Code 的隐藏输出流式传输到独立终端
用途: 调试/理解 Claude 行为
特点: 
  - 实时监控 thinking 过程
  - 查看 tool calls
  - 跟踪 subagents
  - 多会话同时监控
```

---

## 六、补充技能推荐

### 6.1 按场景推荐

| 场景 | 首推技能 | 安装命令 |
|-----|---------|---------|
| **Unity游戏开发** | Claude-Code-Game-Studios | gh-Donchitos-Claude-Code-Game-Studios |
| **Web游戏测试** | playwright-skill | gh-lackeyjb-playwright-skill |
| **反检测测试** | playwright-undetected-skill | gh-dalbit-mir-playwright-undetected-skill |
| **Python AI开发** | pydantic-ai-skills | gh-DougTrajano-pydantic-ai-skills |
| **数据库查询** | read-only-postgres | gh-jawwadfirdousi-read-only-postgres |
| **安全审计** | trailofbits-skills | gh-trailofbits-skills |

### 6.2 技能组合推荐

```
游戏开发组合:
Claude-Code-Game-Studios + Unity Test Framework + playwright-skill

Python开发组合:
pydantic-ai-skills + read-only-postgres + pytest + aws-mcp-server

测试自动化组合:
playwright-skill + fieldwork-skills + claude-skills-marketplace
```

---

## 📎 相关资源

- [Claude-Code-Game-Studios](https://github.com/Donchitos/Claude-Code-Game-Studios)
- [playwright-skill](https://github.com/lackeyjb/playwright-skill)
- [playwright-undetected-skill](https://github.com/dalbit-mir/playwright-undetected-skill)
- [pydantic-ai-skills](https://github.com/DougTrajano/pydantic-ai-skills)
- [read-only-postgres](https://github.com/jawwadfirdousi/agent-skills)
- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)

---

*补充调研完成 - 2026年3月3日*
