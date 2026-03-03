# Claude Code 游戏客户端开发技能补充调研

## 📋 文档信息

- **调研日期**: 2026-03-03
- **分类**: 游戏开发 / 客户端开发 / Unity / Godot / GameMaker / Unreal
- **状态**: ✅ 补充调研

---

## 1. Unity 游戏开发技能 (重点)

### 1.1 cc-plugin-unity-gamedev (推荐)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [tjboudreaux/cc-plugin-unity-gamedev](https://github.com/tjboudreaux/cc-plugin-unity-gamedev) |
| **Star** | ⭐ 1 |
| **技能数量** | 21 个专业化技能 |
| **覆盖范围** | Unity 完整开发栈 |

### 技能分类详解

| 类别 | 技能数量 | 包含内容 |
|-----|---------|---------|
| **工具类** | 8 | Addressables, MemoryPack, ScriptableObjects, Profiling, Package Manager, Version Control, Debugging, Asset Pipeline |
| **动画/物理** | 5 | Animation, Physics, NavMesh, Object Pooling, State Machine |
| **AI/行为** | 2 | Behavior Designer, Gameplay Ability System (GAS) |
| **音视频** | 2 | Wwise 音频, Cinemachine 相机 |
| **UI** | 2 | UGUI, Mobile Optimization |
| **测试** | 1 | Test Framework |
| **DI/异步** | 1 | VContainer, UniTask |

### 核心技能详解

#### Addressables (资源管理系统)
```csharp
// 异步资源加载
var handle = Addressables.LoadAssetAsync<GameObject>("Prefab");
var prefab = await handle.Task;

// 内存管理
Addressables.Release(handle);

// 引用计数
using (var op = Addressables.LoadAssetAsync<TextAsset>("Data"))
{
    var data = await op.Task;
    // 使用数据
}
```

#### Gameplay Ability System (GAS)
```csharp
// Ability 定义
[CreateAssetMenu(fileName = "NewAbility", menuName = "Ability/Active")]
public class GameplayAbility : AbilitySystemComponent
{
    public GameplayEffectContainer EffectContainer;
    
    public override void ActivateAbility(
        GameplayAbilitySpecHandle handle,
        GameplayEventData eventData)
    {
        // 激活技能逻辑
    }
}
```

#### PrimeTween (高性能动画)
```csharp
// 动画序列
Tween.Sequence()
    .Append(transform.TweenPosition(targetPos, 0.5f))
    .Append(transform.TweenScale(Vector3.one * 1.2f, 0.3f))
    .SetLoops(-1);

// UI 动画
button.TweenScaleY(1.1f, 0.2f).SetEase(Ease.Back.Out);
```

### 1.2 OH-Unity-GameDev-Skills

| 项目 | 说明 |
|-----|------|
| **GitHub** | [OstrichHermit/OH-Unity-GameDev-Skills](https://github.com/OstrichHermit/OH-Unity-GameDev-Skills) |
| **Star** | ⭐ 6 |
| **语言** | Python |
| **特点** | 符合 Claude Code Skills 规范的 Unity 游戏开发技能集 |

### 技能列表

| 技能名称 | 功能描述 |
|---------|---------|
| **claude_skill_unity** | Unity 基础开发技能 |
| **doTween-unity** | DoTween 动画库集成 |
| **media-pipe-unity-skill** | MediaPipe 机器视觉集成 |
| **prime-tween-unity** | PrimeTween 高性能动画 |
| **skill-creator** | 技能创建辅助工具 |

### 适用场景

- Unity 游戏原型开发
- 动画系统实现
- 机器视觉游戏应用
- 性能优化

### 1.3 unity-ai-workflow

| 项目 | 说明 |
|-----|------|
| **GitHub** | [David-GD13/unity-ai-workflow](https://github.com/David-GD13/unity-ai-workflow) |
| **Star** | ⭐ 4 |
| **特点** | AI-first Unity 6.2+ 游戏开发工作流 |

### 包含内容

- **Rules**: 项目规则配置
- **Agents**: AI 代理配置
- **Skills**: Claude Code 技能集
- **Slash Commands**: 快捷命令

### 适用版本

- Unity 6.2+
- Claude Code
- Antigravity

### 1.4 Claude-Code-Skills-For-Unity-Game-Development

| 项目 | 说明 |
|-----|------|
| **GitHub** | [flashwade03/Claude-Code-Skills-For-Unity-Game-Development](https://github.com/flashwade03/Claude-Code-Skills-For-Unity-Game-Development) |
| **特点** | 知名 Unity 资产开发技能 |

---

## 2. Unreal Engine 开发技能

### 2.1 Unreal Engine 技能现状

| 状态 | 说明 |
|-----|------|
| **技能数量** | 较少 |
| **成熟度** | 早期阶段 |
| **推荐方案** | 使用通用 C++/Blueprint 技能 |

### 现有资源

- **CLAUDE.md 文件**: 多个 Unreal 项目包含 CLAUDE.md
- **Blueprint 支持**: 部分技能支持可视化脚本
- **插件开发**: 基本的插件开发指导

---

## 3. Godot 游戏开发技能

### 3.1 Claude Resources for Godot

| 项目 | 说明 |
|-----|------|
| **GitHub** | [kwhitejr/claude-resources](https://github.com/kwhitejr/claude-resources) |
| **Star** | ⭐ 3 |
| **特点** | Godot 游戏开发自定义代理和技能 |

### 适用场景

- Godot 4.x 项目开发
- GDScript 脚本编写
- 游戏工作流自动化

### 3.2 Godot 4.x 支持

```gdscript
# GDScript 示例
extends Node

@export var speed: float = 100.0
@onready var sprite: Sprite2D = $Sprite2D

func _physics_process(delta: float) -> void:
    var direction := Input.get_axis("move_left", "move_right")
    position.x += direction * speed * delta
```

---

## 4. GameMaker Studio 开发技能

### 4.1 GameMaker Skills

| 项目 | 说明 |
|-----|------|
| **GitHub** | [leihaht/gamemaker-skills](https://github.com/leihaht/gamemaker-skills) |
| **Star** | ⭐ 2 |
| **语言** | GML |

### 核心功能

- **对象创建**: GameMaker 对象创建和管理
- **GML 语法**: GML 语言专家
- **Shaders**: 着色器开发
- **网络功能**: 多人游戏网络编程

### 适用场景

- 2D 游戏开发
- 游戏原型快速开发
- 独立游戏制作

### 4.2 GML 示例

```gml
// 创建事件
function Create() {
    speed = 5;
    direction = 0;
}

// 步事件
function Step() {
    if (keyboard_check(vk_left)) {
        x -= speed;
    }
    if (keyboard_check(vk_right)) {
        x += speed;
    }
}
```

---

## 5. 其他游戏开发技能

### 5.1 Space Engineers 插件开发

| 项目 | 说明 |
|-----|------|
| **GitHub** | [viktor-ferenczi/se-dev-skills](https://github.com/viktor-ferenczi/se-dev-skills) |
| **Star** | ⭐ 2 |
| **语言** | Python |
| **用途** | Space Engineers 插件/Mod/游戏脚本开发 |

### 适用平台

- Space Engineers 游戏
- 插件开发
- 游戏内脚本编写

### 5.2 Game Opus - 终极游戏开发元技能

| 项目 | 说明 |
|-----|------|
| **GitHub** | [nightbs8/game-opus](https://github.com/nightbs8/game-opus) |
| **Star** | ⭐ 0 |
| **特点** | 激活 14 个游戏开发 + 3D 技能 |

### 技能数量

- **游戏开发技能**: 14 个
- **3D 技能**: 3 个

### 5.3 Cowork Skills

| 项目 | 说明 |
|-----|------|
| **GitHub** | [GrizzwaldHouse/cowork-skills](https://github.com/GrizzwaldHouse/cowork-skills) |
| **Star** | ⭐ 0 |
| **语言** | Python |

### 包含内容

- 设计技能
- 文档技能
- AI 工作流
- 游戏开发

---

## 6. 游戏客户端自动化测试

### 6.1 Unity Test Framework

| 项目 | 说明 |
|-----|------|
| **来源** | cc-plugin-unity-gamedev |
| **功能** | Unity 单元测试 |

### 核心功能

- **EditMode 测试**: 编辑器模式测试
- **PlayMode 测试**: 运行时测试
- **异步测试**: 异步代码测试
- **Mocking**: 测试模拟

### 测试示例

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

### 6.2 Playwright 浏览器测试

| 项目 | 说明 |
|-----|------|
| **GitHub** | [lackeyjb/playwright-skill](https://github.com/lackeyjb/playwright-skill) |
| **Star** | ⭐ 1.8k |
| **特点** | 模型调用的 Playwright 自动化 |

### 适用场景

- Web/H5 游戏测试
- UI 自动化验证
- 回归测试
- 登录流程测试

### 6.3 游戏测试方案对比

| 测试类型 | 推荐方案 | 优点 | 局限 |
|---------|---------|------|------|
| **Unity 单元测试** | Unity Test Framework | 专业集成 | 需 Unity 环境 |
| **Unity 集成测试** | Unity PlayMode | 完整测试 | 性能较慢 |
| **Web/H5 游戏** | Playwright | 功能强大 | 需 Web 环境 |
| **UI 交互测试** | Playwright + 截图 | 直观 | 维护成本高 |
| **性能测试** | Unity Profiler | 专业 | 学习曲线高 |

---

## 7. 部署指南

### 安装 Unity 技能

```bash
# 克隆 Unity 游戏开发技能
git clone https://github.com/tjboudreaux/cc-plugin-unity-gamedev.git

# 安装到 Claude Code
cp -r cc-plugin-unity-gamedev ~/.claude/

# 或使用技能安装命令
claude --install-skill gh-tjboudreaux-cc-plugin-unity-gamedev
```

### 安装 Godot 技能

```bash
# 克隆 Godot 开发资源
git clone https://github.com/kwhitejr/claude-resources.git

# 复制到技能目录
cp -r claude-resources/godot ~/.claude/skills/
```

### 安装 GameMaker 技能

```bash
# 克隆 GameMaker 技能
git clone https://github.com/leihaht/gamemaker-skills.git

# 复制到技能目录
cp -r gamemaker-skills ~/.claude/skills/
```

---

## 8. 技能选择建议

### 按游戏引擎选择

| 引擎 | 推荐技能 | 优先级 |
|-----|---------|-------|
| **Unity** | cc-plugin-unity-gamedev | ⭐⭐⭐⭐⭐ |
| **Unity** | OH-Unity-GameDev-Skills | ⭐⭐⭐⭐ |
| **Godot** | claude-resources | ⭐⭐⭐⭐ |
| **GameMaker** | gamemaker-skills | ⭐⭐⭐ |
| **Space Engineers** | se-dev-skills | ⭐⭐ |

### 按用途选择

| 用途 | 推荐技能 |
|-----|---------|
| **大型 Unity 项目** | cc-plugin-unity-gamedev (21 技能) |
| **快速原型** | OH-Unity-GameDev-Skills |
| **独立游戏** | gamemaker-skills |
| **Mod 开发** | se-dev-skills |
| **AI/机器学习** | media-pipe-unity-skill |
| **Web/H5 游戏** | playwright-skill |

---

## 9. 优缺点分析

### ✅ 优点

| 优点 | 说明 |
|-----|------|
| **引擎覆盖全面** | 支持 Unity/Godot/GameMaker 等主流引擎 |
| **技能专业化** | 针对不同 Unity 系统有专门技能 |
| **测试支持** | Unity Test Framework + Playwright |
| **开箱即用** | 安装配置简单 |
| **持续更新** | 社区活跃维护 |
| **文档完善** | 大部分有详细说明 |

### ❌ 缺点

| 缺点 | 说明 |
|-----|------|
| **Star 普遍较低** | 社区生态仍在早期 |
| **Unreal 技能少** | Unreal Engine 支持有限 |
| **部分技能较新** | 稳定性有待验证 |
| **中文资料少** | 需要英文阅读能力 |

---

## 10. 未来趋势

### 10.1 发展趋势

| 方向 | 预测 |
|-----|------|
| **Unity 技能** | 持续增长，更多专业系统技能 |
| **Unreal Engine** | 可能会出现更多 C++ 技能 |
| **跨平台测试** | 统一的测试框架技能 |
| **AI 集成** | 游戏 AI 开发技能增加 |

### 10.2 值得关注

- **Unity 6 新特性**: 关注新版本配套技能
- **GAS 深入**: Gameplay Ability System 技能完善
- **多引擎支持**: 跨引擎开发技能

---

## 📎 相关资源

- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
- [awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills)
- [Unity 官方文档](https://docs.unity3d.com/)
- [Godot 官方文档](https://docs.godotengine.org/)
- [GameMaker 文档](https://manual.yoyogames.com/)

---

*游戏开发技能集正在快速发展，建议关注社区更新。*
