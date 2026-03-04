# Claude Code 游戏开发插件调研 (补充)

> 2026年3月 新增热门游戏开发相关插件调研

## 1. Claude-Code-Game-Studios 全能游戏开发工作室

> 48个AI代理 + 36个工作流技能 + 完整协调系统

## 1.1 背景需求

游戏开发涉及多个专业领域，需要完整的开发工作室支持。

## 1.2 目标

将 Claude Code 打造成完整游戏开发工作室，模拟真实游戏工作室的协作流程。

## 1.3 设计方案

- **48个AI代理**：覆盖设计、编程、美术、音频、测试等
- **36个工作流技能**：项目管理、代码审查、测试自动化等
- **协调系统**：模拟真实工作室的团队协作流程
- 多代理并行工作，自动任务分配

## 1.4 本地部署

```bash
git clone https://github.com/Donchitos/Claude-Code-Game-Studios ~/.claude/plugins/
```

## 1.5 效果展示

- GitHub Stars：⭐ 28
- 更新频率：活跃（4天前更新）

## 1.6 优缺点

✅ 功能全面 ✅ 工作室级架构 ✅ 多代理协作  
⚠️ 学习曲线陡峭 ⚠️ 配置复杂

## 1.7 平替插件

| 插件 | 特点 |
|------|------|
| cc-plugin-unity-gamedev | Unity专用技能集 |
| Unity GameDev Skills | Unity专业开发 |

---

## 2. Unity GameDev Skills Unity专业开发技能

> 符合 Claude Code Skills 规范的 Unity 游戏开发技能集

## 2.1 背景需求

Unity 是最流行的游戏引擎，需要专门的开发技能支持。

## 2.2 目标

提供符合规范的 Unity 专业开发技能。

## 2.3 设计方案

- C# 编程技能
- Unity 组件开发
- 物理系统集成
- UI 系统构建
- 资源管理

## 2.4 本地部署

```bash
git clone https://github.com/OstrichHermit/OH-Unity-GameDev-Skills ~/.claude/plugins/
```

## 2.5 效果展示

- GitHub Stars：⭐ 6

## 2.6 优缺点

✅ 专注Unity ✅ 规范兼容  
⚠️ 规模较小

---

## 3. Godot Game Development Godot游戏开发

> Claude Code 自定义代理和技能，专用于 Godot 游戏开发工作流

## 3.1 背景需求

Godot 是开源游戏引擎，需要 Claude Code 集成支持。

## 3.2 目标

为 Godot 开发者提供完整的工作流自动化。

## 3.3 设计方案

- GDScript 编程技能
- Godot 节点系统
- 场景管理
- 2D/3D 开发支持

## 3.4 本地部署

```bash
git clone https://github.com/kwhitejr/claude-resources ~/.claude/plugins/
```

## 3.5 效果展示

- GitHub Stars：⭐ 3

---

## 4. GameMaker Studio 2 Skills GameMaker技能

> GameMaker Studio 2 和 GML 开发的 Claude Code 技能

## 4.1 背景需求

GameMaker 是流行的2D游戏开发工具。

## 4.2 目标

提供 GameMaker 专业开发支持。

## 4.3 设计方案

- GML 语法技能
- 对象创建
- 着色器开发
- 网络功能

## 4.4 本地部署

```bash
git clone https://github.com/leihaht/gamemaker-skills ~/.claude/plugins/
```

## 4.5 效果展示

- GitHub Stars：⭐ 2

---

## 5. Love2D Game Development Love2D游戏开发

> 使用 Claude Code 和 Love2D 技能"氛围编程" bomberman 克隆

## 5.1 背景需求

Love2D 是轻量级 Lua 游戏框架。

## 5.2 目标

展示 AI 驱动游戏原型开发。

## 5.3 设计方案

- Lua 编程
- 游戏逻辑
- 2D 渲染

## 5.4 本地部署

```bash
git clone https://github.com/chongdashu/love2d-pocket-bomber-game ~/.claude/plugins/
```

## 5.5 效果展示

- GitHub Stars：⭐ 11

---

## 6. Solana Game Skill 区块链游戏开发

> C#、Solana Unity SDK、Solana Mobile 的 Claude Code 技能

## 6.1 背景需求

区块链游戏需要与 Solana 生态集成。

## 6.2 目标

提供 Solana 区块链游戏开发支持。

## 6.3 设计方案

- Solana SDK 集成
- 移动端支持
- 钱包集成

## 6.4 本地部署

```bash
git clone https://github.com/solanabr/solana-game-skill ~/.claude/plugins/
```

## 6.5 效果展示

- GitHub Stars：⭐ 5

---

## 7. Game Cog 游戏开发认知框架

> 专门为游戏开发设计的 AI 认知框架

## 7.1 背景需求

游戏开发有独特的技术栈和开发流程。

## 7.2 目标

提供游戏开发专用的问题解决框架。

## 7.3 设计方案

- 游戏架构模式
- 性能优化技能
- 资源管理
- 跨平台部署

## 7.4 本地部署

```bash
# 参考 cc_skills_repo/game-dev-skills/game-cog.md
```

## 7.5 效果展示

- 专业游戏开发框架

---

## 总结：游戏开发插件生态

| 插件 | 方向 | Stars | 特点 |
|------|------|-------|------|
| Claude-Code-Game-Studios | 全栈 | 28 | 48代理+36技能 |
| cc-plugin-unity-gamedev | Unity | 1 | 21个专业技能 |
| OH-Unity-GameDev-Skills | Unity | 6 | 规范兼容 |
| Godot Development | Godot | 3 | 开源引擎 |
| GameMaker Skills | GML | 2 | 2D专用 |
| Love2D Games | Lua | 11 | 轻量原型 |
| Solana Game Skill | 区块链 | 5 | Web3集成 |

**推荐**：
- Unity开发 → Claude-Code-Game-Studios + Unity GameDev Skills
- 快速原型 → Love2D + Claude Code
- 区块链游戏 → Solana Game Skill
