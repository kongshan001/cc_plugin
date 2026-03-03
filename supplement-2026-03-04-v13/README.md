# Claude Code 热门插件补充调研 (2026-03-04)

## 📋 文档信息

- **调研日期**: 2026-03-04
- **分类**: 游戏客户端开发 / Python 开发 / 自动化测试 / 开发者工具
- **状态**: ✅ 补充调研
- **来源**: awesome-claude-code + GitHub 搜索

---

## 1. 游戏客户端开发技能补充

### 1.1 Unity 游戏开发补充技能

#### cc-plugin-unity-gamedev (推荐 ⭐⭐⭐⭐⭐)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [tjboudreaux/cc-plugin-unity-gamedev](https://github.com/tjboudreaux/cc-plugin-unity-gamedev) |
| **Star** | ⭐ 1 |
| **技能数量** | 21 个专业化技能 |
| **覆盖范围** | Unity 完整开发栈 |

**技能分类**:

| 类别 | 数量 | 包含内容 |
|-----|-----|---------|
| 工具类 | 8 | Addressables, MemoryPack, ScriptableObjects, Profiling, Package Manager, Version Control, Debugging, Asset Pipeline |
| 动画/物理 | 5 | Animation, Physics, NavMesh, Object Pooling, State Machine |
| AI/行为 | 2 | Behavior Designer, Gameplay Ability System (GAS) |
| 音视频 | 2 | Wwise 音频, Cinemachine 相机 |
| UI | 2 | UGUI, Mobile Optimization |
| 测试 | 1 | Test Framework |
| DI/异步 | 1 | VContainer, UniTask |

#### Unity 技能示例

```csharp
// Addressables 异步加载
var handle = Addressables.LoadAssetAsync<GameObject>("Prefab");
var prefab = await handle.Task;
Addressables.Release(handle);

// Gameplay Ability System
[CreateAssetMenu(fileName = "NewAbility", menuName = "Ability/Active")]
public class GameplayAbility : AbilitySystemComponent
{
    public override void ActivateAbility(
        GameplayAbilitySpecHandle handle,
        GameplayEventData eventData)
    {
        // 激活技能逻辑
    }
}
```

#### OH-Unity-GameDev-Skills

| 项目 | 说明 |
|-----|------|
| **GitHub** | [OstrichHermit/OH-Unity-GameDev-Skills](https://github.com/OstrichHermit/OH-Unity-GameDev-Skills) |
| **Star** | ⭐ 6 |
| **特点** | 符合 Claude Code Skills 规范 |

**包含技能**:
- claude_skill_unity - Unity 基础开发
- doTween-unity - DoTween 动画集成
- media-pipe-unity-skill - MediaPipe 机器视觉
- prime-tween-unity - PrimeTween 高性能动画
- skill-creator - 技能创建辅助

### 1.2 Godot 游戏开发

#### claude-resources (Godot)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [kwhitejr/claude-resources](https://github.com/kwhitejr/claude-resources) |
| **Star** | ⭐ 3 |
| **适用版本** | Godot 4.x |

**GDScript 示例**:
```gdscript
extends Node

@export var speed: float = 100.0
@onready var sprite: Sprite2D = $Sprite2D

func _physics_process(delta: float) -> void:
    var direction := Input.get_axis("move_left", "move_right")
    position.x += direction * speed * delta
```

### 1.3 GameMaker Studio 开发

#### gamemaker-skills

| 项目 | 说明 |
|-----|------|
| **GitHub** | [leihaht/gamemaker-skills](https://github.com/leihaht/gamemaker-skills) |
| **Star** | ⭐ 2 |
| **语言** | GML |

**核心功能**:
- 对象创建和管理
- GML 语法专家
- Shaders 着色器开发
- 多人游戏网络编程

### 1.4 其他游戏开发资源

#### Space Engineers 插件开发

| 项目 | 说明 |
|-----|------|
| **GitHub** | [viktor-ferenczi/se-dev-skills](https://github.com/viktor-ferenczi/se-dev-skills) |
| **Star** | ⭐ 2 |
| **用途** | Space Engineers Mod/插件开发 |

#### Game Opus - 游戏开发元技能

| 项目 | 说明 |
|-----|------|
| **GitHub** | [nightbs8/game-opus](https://github.com/nightbs8/game-opus) |
| **技能数量** | 14 个游戏开发 + 3 个 3D 技能 |

---

## 2. Python 开发技能补充

### 2.1 Python 类型安全

#### python-type-safety

| 项目 | 说明 |
|-----|------|
| **来源** | [skills.sh/wshobson/agents/python-type-safety](https://skills.sh/wshobson/agents/python-type-safety) |
| **定位** | Python 类型安全最佳实践 |

**核心概念**:

```python
# 类型注解
def get_user(user_id: str) -> User | None:
    """Return type makes 'might not exist' explicit."""
    ...

# 泛型
from typing import TypeVar, Generic
T = TypeVar("T")

class Result(Generic[T]):
    def __init__(self, value: T | None = None) -> None:
        self._value = value

# Protocols (结构化接口)
from typing import Protocol, runtime_checkable

@runtime_checkable
class Serializable(Protocol):
    def to_dict(self) -> dict: ...
    @classmethod
    def from_dict(cls, data: dict) -> "Serializable": ...

# 类型收窄
def process_user(user_id: str) -> UserData:
    user = find_user(user_id)
    if user is None:
        raise UserNotFoundError(f"User {user_id} not found")
    # Type checker knows user is User here
    return UserData(name=user.name, email=user.email)
```

**最佳实践**:
- 标注所有公共签名
- 使用 mypy 严格模式
- 使用 pydantic 进行运行时验证
- 使用 pyright 作为 LSP

### 2.2 Python Web 框架

#### Django/Flask/FastAPI Skills

| 框架 | 技能 | 说明 |
|-----|-----|------|
| Django | pytest-django | Django 测试客户端 |
| Flask | pytest-flask | Flask 测试客户端 |
| FastAPI | TestClient | 内置测试支持 |

**测试示例**:
```python
# FastAPI 测试
from fastapi.testclient import TestClient

def test_api_endpoint():
    client = TestClient(app)
    response = client.get("/api/users")
    assert response.status_code == 200
    assert len(response.json()) > 0
```

### 2.3 Python 测试开发

#### test-driven-development (superpowers)

| 项目 | 说明 |
|-----|------|
| **来源** | superpowers 技能集 |
| **流程** | 红色-绿色-重构 |

**TDD 循环**:
```
1. 编写失败测试 (红色)
2. 实现功能通过测试 (绿色)
3. 重构代码 (重构)
```

#### 测试修复技能

| 技能 | 功能 |
|-----|------|
| test-fixing | 测试修复 |
| test-writing | 测试编写 |
| test-running | 测试运行 |
| bug-finding | Bug 查找 |

### 2.4 AWS 云服务集成

#### aws-mcp-server

| 项目 | 说明 |
|-----|------|
| **GitHub** | [alexei-led/aws-mcp-server](https://github.com/alexei-led/aws-mcp-server) |
| **语言** | Python |
| **特点** | AWS CLI 集成，多环境支持 |

**支持的服务**:
- 计算: EC2, Lambda, ECS, EKS
- 存储: S3, EBS, EFS
- 数据库: RDS, DynamoDB, ElastiCache
- 网络: VPC, CloudFront, Route53
- 安全: IAM, Secrets Manager

### 2.5 Pydantic AI 集成

#### pydantic-ai-skills

| 项目 | 说明 |
|-----|------|
| **GitHub** | [DougTrajano/pydantic-ai-skills](https://github.com/DougTrajano/pydantic-ai-skills) |
| **Star** | ⭐ 136 |
| **特点** | Agent Skills 支持 Pydantic AI |

**核心功能**:
- 类型安全: Pydantic 模型强制类型检查
- 渐进式提示: 按需披露信息
- AI 集成: 与主流 LLM 无缝集成
- 验证系统: 内置强大的数据验证

---

## 3. 游戏客户端自动化测试补充

### 3.1 Unity Test Framework

| 项目 | 说明 |
|-----|------|
| **来源** | cc-plugin-unity-gamedev |
| **功能** | Unity 单元测试 |

**测试类型**:
- EditMode 测试: 编辑器模式，纯 C# 逻辑
- PlayMode 测试: 运行时，集成测试
- 异步测试: 协程测试

**测试示例**:
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

### 3.2 Playwright 浏览器测试

#### playwright-skill

| 项目 | 说明 |
|-----|------|
| **GitHub** | [lackeyjb/playwright-skill](https://github.com/lackeyjb/playwright-skill) |
| **Star** | ⭐ 1.8k |
| **特点** | 模型调用的 Playwright 自动化 |

**适用场景**:
- Web/H5 游戏测试
- UI 自动化验证
- 回归测试
- 登录流程测试

### 3.3 自动化测试技能汇总

| 测试类型 | 推荐方案 | 优点 | 局限 |
|---------|---------|------|------|
| Unity 单元测试 | Unity Test Framework | 专业集成 | 需 Unity 环境 |
| Unity 集成测试 | Unity PlayMode | 完整测试 | 性能较慢 |
| Web/H5 游戏 | Playwright | 功能强大 | 需 Web 环境 |
| iOS 游戏测试 | ios-simulator-skill | 原生模拟器 | macOS only |
| Android 游戏测试 | android_ui_verification | ADB 自动化 | 需 Android SDK |
| UI 交互测试 | Playwright + 截图 | 直观 | 维护成本高 |
| 性能测试 | Unity Profiler | 专业 | 学习曲线高 |

### 3.4 网络同步测试

#### 帧同步测试

- 确定性验证: 相同输入 → 相同输出
- 断线重连测试
- 录像回放验证

#### 状态同步测试

- 状态一致性验证
- 增量同步效率
- 预测回滚测试

#### 延迟模拟

- 网络抖动 (Jitter): 0-200ms 随机延迟
- 丢包模拟: 5%-20% 丢包率
- 高延迟环境: 200-500ms RTT

### 3.5 性能基准测试

| 指标 | 目标 | 测量工具 |
|-----|-----|---------|
| 帧率 | 60 FPS (16.67ms/帧) | Unity Profiler |
| 最低帧率 | 30 FPS (33.33ms/帧) | UnityFrameTimingManager |
| 内存 | 堆内存监控 | Unity Profiler |
| 加载时间 | 场景切换时间 | 计时器 |

---

## 4. 其他开发者工具补充

### 4.1 开发者工具包

#### developer-kit

| 项目 | 说明 |
|-----|------|
| **GitHub** | [giuseppe-trisciuoglio/developer-kit](https://github.com/giuseppe-trisciuoglio/developer-kit) |
| **Star** | ⭐ 128 |
| **语言** | Python |

**包含内容**:
- Skills: 可复用技能
- Agents: 自动化代理
- Commands: 快捷命令
- 自动化: 开发工作流自动化

#### claude-code-tools

| 项目 | 说明 |
|-----|------|
| **GitHub** | [pchalasani/claude-code-tools](功能) |
| **功能** | 会话连续性工具集 |

**核心功能**:
- 会话保持: 避免上下文压缩
- 跨代理切换: Claude Code ↔ Codex CLI
- 全文搜索: Rust/Titanic 全文索引
- TMux 集成: 终端会话管理

#### Claudekit

| 项目 | 说明 |
|-----|------|
| **GitHub** | [carlrannaberg/claudekit](https://github.com/carlrannaberg/claudekit) |
| **子代理数量** | 20+ |

**子代理列表**:

| 代理名称 | 功能 |
|---------|------|
| oracle | GPT-5 集成 |
| code-reviewer | 6 方面深度分析 |
| typescript-expert | TypeScript 专家 |
| ai-sdk-expert | Vercel AI SDK |

### 4.2 浏览器自动化

#### browser-automation

| Skill 名称 | 核心能力 |
|-----------|---------|
| browser-automation | 浏览器自动化 |

**工具对比**:

| 工具 | 特点 | 适用场景 |
|------|------|---------|
| Playwright | 跨浏览器、API 丰富 | 现代 Web 测试 |
| Puppeteer | Chrome 专用、轻量 | 爬虫/截图 |
| Selenium | 历史悠久、生态广 | 遗留项目 |
| Cypress | 调试友好、实时重载 | 开发测试 |

### 4.3 GitHub 自动化

#### github-automation

| Skill 名称 | 核心能力 |
|-----------|---------|
| github-automation | GitHub 自动化 |
| github-workflow-automation | GitHub Actions |

**核心功能**:
- Issue 管理: 创建/关闭/编辑/标签
- Pull Request: 创建/审查/自动合并
- Actions: 触发工作流/查看状态
- 仓库管理: 分支保护/权限配置

### 4.4 CI/CD 自动化

#### cicd-automation-workflow-automate

| 技能名称 | 功能 |
|---------|------|
| cicd-automation-workflow-automate | CI/CD 流水线自动化 |

**支持平台**:
- GitHub Actions
- GitLab CI
- Jenkins

**最佳实践**:
- 失败快速反馈
- 并行执行
- 缓存优化
- 安全扫描

### 4.5 AgentSys 工作流自动化

#### AgentSys

| 项目 | 说明 |
|-----|------|
| **GitHub** | [avifenesh/agentsys](https://github.com/avifenesh/agentsys) |
| **Star** | ⭐ 活跃 |
| **特点** | 完整的工作流自动化系统 |

**核心功能**:
- 任务到生产工作流自动化
- PR 管理
- 代码清理
- 性能调查
- 漂移检测
- 多代理代码审查

### 4.6 Superpowers 核心技能

#### Superpowers

| 项目 | 说明 |
|-----|------|
| **GitHub** | [obra/superpowers](https://github.com/obra/superpowers) |
| **Star** | ⭐ 活跃 |
| **作者** | Jesse Vincent |

**覆盖范围**:
- 规划 (Planning)
- 审查 (Reviewing)
- 测试 (Testing)
- 调试 (Debugging)
- SDLC 全流程

### 4.7 Claude Code Settings

#### claude-codex-settings

| 项目 | 说明 |
|-----|------|
| **GitHub** | [fcakyon/claude-codex-settings](https://github.com/fcakyon/claude-codex-settings) |
| **Star** | ⭐ 活跃 |
| **特点** | 核心开发者活动覆盖 |

**支持平台**:
- GitHub
- Azure
- MongoDB
- Tavily
- Playwright

### 4.8 cc-tools (Go 实现)

#### cc-tools

| 项目 | 说明 |
|-----|------|
| **GitHub** | [Veraticus/cc-tools](https://github.com/Veraticus/cc-tools) |
| **语言** | Go |
| **特点** | 高性能 hooks 和工具 |

**功能**:
- 智能 linting
- 测试
- 状态行生成

---

## 5. 安装指南

### 5.1 安装 Unity 技能

```bash
# 克隆 Unity 游戏开发技能
git clone https://github.com/tjboudreaux/cc-plugin-unity-gamedev.git

# 安装到 Claude Code
cp -r cc-plugin-unity-gamedev ~/.claude/

# 或使用技能安装命令
claude --install-skill gh-tjboudreaux-cc-plugin-unity-gamedev
```

### 5.2 安装 Python 类型安全技能

```bash
# 克隆仓库
git clone https://github.com/wshobson/agents.git

# 复制技能
cp -r python-type-safety ~/.claude/skills/
```

### 5.3 安装测试自动化技能

```bash
# 使用 Antigravity 安装
npx antigravity-awesome-skills --claude

# E2E 测试
>> /e2e-testing-patterns 帮助我设置 Playwright 测试

# TDD 开发
>> /test-driven-development 使用 TDD 开发这个功能
```

### 5.4 安装开发者工具

```bash
# 浏览器自动化
>> /browser-automation 帮助我自动化这个表单

# GitHub 自动化
>> /github-automation 创建一个 release 工作流

# CI/CD
>> /cicd-automation-workflow-automate 设置 CI 流水线
```

---

## 6. 技能选择建议

### 按用途选择

| 用途 | 推荐技能 |
|-----|---------|
| 大型 Unity 项目 | cc-plugin-unity-gamedev (21 技能) |
| 快速原型 | OH-Unity-GameDev-Skills |
| Python 类型安全 | python-type-safety |
| 企业级测试 | test-automator |
| Web E2E 测试 | e2e-testing-patterns |
| Python 测试 | python-testing-patterns |
| CI/CD 自动化 | github-workflow-automation |
| 工作流自动化 | AgentSys |
| 核心开发技能 | Superpowers |

---

## 7. 优缺点分析

### ✅ 优点

| 优点 | 说明 |
|-----|------|
| 引擎覆盖全面 | 支持 Unity/Godot/GameMaker |
| 技能专业化 | 针对不同系统有专门技能 |
| 测试支持完善 | Unity Test Framework + Playwright |
| Python 生态完整 | 类型安全到测试全覆盖 |
| 开发者工具全 | 从代码到部署全覆盖 |
| 社区活跃 | 持续更新维护 |

### ❌ 缺点

| 缺点 | 说明 |
|-----|------|
| Star 普遍较低 | 社区生态仍在早期 |
| Unreal 技能少 | Unreal Engine 支持有限 |
| 部分技能较新 | 稳定性有待验证 |
| 中文资料少 | 需要英文阅读能力 |

---

## 📎 相关链接

- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
- [awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills)
- [Antigravity Awesome Skills](https://github.com/sickn33/antigravity-awesome-skills)
- [cc-plugin-unity-gamedev](https://github.com/tjboudreaux/cc-plugin-unity-gamedev)
- [python-type-safety](https://skills.sh/wshobson/agents/python-type-safety)
- [AgentSys](https://github.com/avifenesh/agentsys)
- [Superpowers](https://github.com/obra/superpowers)

---

*持续更新中...*
