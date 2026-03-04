# Claude Code 热门插件补充调研 (v69)

> 2026年3月5日 游戏客户端/Python/自动化测试/开发者工具 - 最新热门插件完整调研

---

## 一、本期调研概述

### 1.1 调研背景

本次调研继续深入分析 Claude Code 热门插件，聚焦以下四个方向：

1. **游戏客户端开发** - Unity、Godot、Unreal 等主流游戏引擎
2. **Python 开发** - Web 框架、数据处理、AI 集成
3. **游戏客户端自动化测试** - 跨平台测试方案
4. **其他开发者工具** - 安全、编排、记忆等工具

### 1.2 数据来源

- awesome-claude-code 官方列表 (已更新至最新)
- GitHub Trending
- Claude Code Skills Marketplace
- MCP 官方注册表

---

## 二、游戏客户端开发插件深度分析

### 2.1 Unity 开发技能矩阵

| 技能包 | Stars | 技能数量 | 维护状态 | 核心优势 |
|--------|-------|---------|---------|---------|
| cc-plugin-unity-gamedev | 1+ | 21 | 活跃 | 完整覆盖 Unity 开发栈 |
| Claude-Code-Game-Studios | 28+ | 48+ | 活跃 | AI 代理工作室模式 |
| OH-Unity-GameDev-Skills | 6+ | 15+ | 持续更新 | 轻量级 + 现代化 |
| unity-ai-workflow | 4+ | 多 | 新兴 | Unity 6.2+ 专用 |

#### cc-plugin-unity-gamedev 详细分析

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

**典型使用场景**:

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
```

### 2.2 Godot 开发技能

| 资源 | Stars | 特点 |
|-----|-------|------|
| claude-resources (kwhitejr) | 3+ | Godot 4.x 专用 |
| godot-development | - | 基础开发技能 |

**GDScript 示例**:
```gdscript
extends Node

@export var speed: float = 100.0
@onready var sprite: Sprite2D = $Sprite2D

func _physics_process(delta: float) -> void:
    var direction := Input.get_axis("move_left", "move_right")
    position.x += direction * speed * delta
```

### 2.3 Unreal Engine 现状

| 状态 | 说明 |
|-----|------|
| 技能数量 | 较少 |
| 成熟度 | 早期阶段 |
| 推荐方案 | 使用通用 C++/Blueprint 技能 + MCP |

**Unreal-MCP 最新动态**:
- UE 5.5+ 支持持续更新
- Blueprint 操作稳定性提升
- 社区贡献组件增加

### 2.4 其他游戏引擎

| 引擎 | 技能包 | Stars | 用途 |
|-----|--------|-------|------|
| GameMaker | gamemaker-skills | 2+ | 2D 游戏开发 |
| Space Engineers | se-dev-skills | 2+ | 游戏 Mod 开发 |
| Cocos | (建设中) | - | 跨平台游戏 |

---

## 三、Python 开发插件生态

### 3.1 Web 框架技能

| 框架 | MCP/技能 | 功能 |
|-----|---------|------|
| **FastAPI** | fastapi-mcp | API 开发 + 类型验证 |
| **Django** | django-skill | 全栈 Web 框架 |
| **Flask** | flask-skill | 轻量级 Web 框架 |

#### FastAPI-MCP 实践

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

### 3.2 Pydantic AI 技能

| 项目 | Stars | 功能 |
|-----|-------|------|
| pydantic-ai-skills | 138+ | Agent 开发 + 类型安全 |

**核心功能**:
- 类型安全：Pydantic 模型强制类型检查
- 渐进式提示：按需披露信息
- AI 集成：与主流 LLM 无缝集成
- 验证系统：内置强大的数据验证

### 3.3 数据库技能

| 技能 | 功能 | 安全特性 |
|-----|------|---------|
| read-only-postgres | PostgreSQL 只读查询 | 强制 SELECT/SHOW/EXPLAIN |
| postgres | 完整数据库操作 | 多连接 + 防御性安全 |
| memory-mcp-server | 记忆存储 | 本地持久化 |

### 3.4 AWS 云服务集成

| MCP | Stars | 功能 |
|-----|-------|------|
| aws-mcp-server | 1350+ | EC2/Lambda/S3/RDS/VPC |

### 3.5 Python 测试技能

| 技能 | 来源 | 功能 |
|-----|------|------|
| test-driven-development | superpowers | TDD 开发流程 |
| test-fixing | marketplace | 测试修复 |
| test-writing | marketplace | 测试编写 |
| pytest | 官方 | 单元测试框架 |

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

**核心功能**:
- Web 应用自动化测试
- UI 交互验证
- 截图捕获
- 登录流程测试
- 反检测能力 (Patchright)

### 4.3 Unity 测试框架

| 测试类型 | 工具 | 适用场景 |
|---------|------|---------|
| EditMode | Unity Test Framework | 工具类测试 |
| PlayMode | Unity PlayMode | 游戏逻辑测试 |
| 性能测试 | Unity Profiler | 性能优化 |

```csharp
// EditMode 测试
[Test]
public void TestEditMode() { 
    Assert.AreEqual(1 + 1, 2);
}

// PlayMode 测试
[UnityTest]
public IEnumerator TestPlayMode() {
    var go = new GameObject("Test");
    yield return null;
    Assert.IsNotNull(go);
}

// 异步测试
[UnityTest]
public IEnumerator TestAsync() {
    var task = LoadAssetAsync();
    yield return new WaitUntil(() => task.IsCompleted);
    Assert.IsTrue(task.IsCompleted);
}
```

### 4.4 移动端游戏测试

#### Android 测试

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
```

#### iOS 测试

| 工具 | 功能 |
|-----|------|
| ios-simulator-skill | iOS 模拟器集成 |
| Xcode | 调试和性能分析 |

### 4.5 视觉回归测试

```python
# Playwright 截图对比
from playwright.sync_api import sync_playwright

def test_visual_regression(page):
    page.goto("http://localhost:3000")
    page.screenshot(path="baseline.png")
    
    # 比较截图
    assert compare_images("screenshot.png", "baseline.png")
```

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

#### Parry 提示注入扫描器

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

#### Dippy Bash 命令过滤器

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
```

### 5.2 编排工具

| 工具 | 特点 | Stars |
|------|------|-------|
| **Sudocode** | Git 原生 + 规范管理 | 新兴 |
| **Claude Squad** | 多会话管理 | - |
| **Nelson** | 海军指挥架构 | - |

#### Sudocode 深度分析

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

*文档版本: v69 - 2026-03-05*

*持续更新中，关注 GitHub 仓库获取最新调研报告*
