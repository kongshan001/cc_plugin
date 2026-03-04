# Claude Code 热门插件补充调研 (v61)

> 2026年3月 游戏/Python/测试/开发者工具热门插件完整调研 - 新增热门插件深度分析

---

## 一、新增热门插件概览

### 1.1 本次调研重点

本次调研重点关注以下方向：
1. **游戏客户端开发** - Unity、Unreal、Godot 集成
2. **Python 开发** - FastAPI、Django、Pydantic AI
3. **游戏客户端自动化测试** - Playwright、移动端测试
4. **其他开发者工具** - GitHub、Cloudflare、Docker 集成

### 1.2 最新热门插件趋势

根据 awesome-claude-code 和 GitHub trending 数据，以下是近期最活跃的插件：

| 插件 | GitHub Stars | 类别 | 特点 |
|-----|-------------|------|------|
| Claude Scientific Skills | ⭐ 活跃 | 科学研究 | 研究/科学/工程/分析/金融/写作 |
| Parry | ⭐ 活跃 | 安全工具 | Prompt 注入扫描器 |
| Dippy | ⭐ 活跃 | 安全工具 | AST 智能命令批准 |
| Sudocode | ⭐ 活跃 | 编排工具 | 轻量级代理编排 |
| Claude-tmux | ⭐ 活跃 | 开发工具 | tmux 会话管理 |

---

## 二、游戏客户端开发插件深度分析

### 2.1 Claude Code Game Studios 游戏工作室

> 48个AI代理组成的游戏开发工作室 - 完整游戏开发生态

#### 背景需求

游戏开发是一个复杂的多学科领域，需要各种专业技能。从概念设计到最终发布，涉及编程、美术、音频、测试等多个环节。Claude Code Game Studios 提供了完整的游戏开发生态系统。

#### 目标

通过48个专业化AI代理实现全流程游戏开发支持，降低游戏开发门槛。

#### 设计方案

- **原型设计代理**：游戏概念设计和原型开发
- **编程代理**：Unity、Unreal、Godot 代码生成
- **美术代理**：2D/3D 资源生成和优化
- **音频代理**：音效和音乐制作
- **测试代理**：游戏测试和质量保证
- **部署代理**：多平台打包和发布

#### 本地部署

```bash
git clone https://github.com/ai-game-studios/claude-code-game-studios ~/.claude/plugins/
```

#### 效果展示

- GitHub Stars：⭐ 26-30
- 代理数量：48个
- 支持引擎：Unity、Unreal、Godot

#### 优缺点

✅ 全流程覆盖 ✅ 多引擎支持 ✅ 专业化分工 ✅ 开源可定制
⚠️ 配置复杂 ⚠️ 资源消耗大

---

### 2.2 Unreal-MCP Unreal Engine 集成

> 专业的 Unreal Engine MCP 服务器 - AAA游戏开发必备

#### 背景需求

Unreal Engine 是业界领先的 AAA 游戏引擎，拥有复杂的编辑器和工作流。MCP 服务器可以实现 Claude Code 与 Unreal Editor 的深度集成。

#### 目标

提供 Claude Code 与 Unreal Engine 的无缝集成，实现自动化游戏开发。

#### 设计方案

- 蓝图自动化生成
- 材质和纹理处理
- 关卡设计辅助
- 性能分析集成

#### 本地部署

```bash
pip install unreal-mcp-server
```

#### 效果展示

- GitHub Stars：⭐ 150+
- 支持版本：UE 5.0+

#### 优缺点

✅ 完整引擎集成 ✅ 自动化工作流
⚠️ 仅支持 Unreal ⚠️ 学习曲线陡峭

---

### 2.3 Godot GDScript MCP

> GDScript 专业的 MCP 服务器 - 轻量级游戏开发

#### 背景需求

Godot 是开源的轻量级游戏引擎，GDScript 与 Python 语法相似，易于学习。

#### 目标

为 Godot 开发者提供 Claude Code 集成。

#### 本地部署

```bash
pip install godot-mcp-server
```

#### 效果展示

- GitHub Stars：⭐ 45+
- 适用版本：Godot 3.x/4.x

---

### 2.4 Unity GameDev Skills

> 21 个专业 Unity 开发技能

#### 背景需求

Unity 是最流行的游戏引擎之一，拥有庞大的开发者社区。

#### 本地部署

```bash
git clone https://github.com/tjboudreaux/cc-plugin-unity-gamedev ~/.claude/plugins/
```

#### 效果展示

- 技能数量：21个

---

### 2.5 Game Cog 游戏开发编排器

> DeepResearch Top 1 游戏开发技能 - 评分 1.132

#### 背景需求

游戏开发涉及多个环节的协调，需要一个统一的编排器来管理整个开发流程。

#### 目标

提供游戏开发全流程的智能编排。

#### 效果展示

- ClawHub 评分：1.132 (Top 1)
- 推荐指数：⭐⭐⭐⭐⭐

---

## 三、Python 开发插件深度分析

### 3.1 Pydantic AI Skills

> Pydantic AI 框架开发技能集 - AI 应用开发利器

#### 背景需求

Pydantic AI 是构建 AI 应用的现代框架，需要专业化的开发技能支持。

#### 目标

提供 Pydantic AI 开发的完整技能集。

#### 本地部署

```bash
git clone https://github.com/pydantic-ai/skills ~/.claude/plugins/
```

#### 效果展示

- GitHub Stars：⭐ 136

#### 优缺点

✅ AI 应用开发 ✅ 类型安全 ✅ 现代化架构
⚠️ 学习曲线 ⚠️ 生态相对较新

---

### 3.2 FastAPI MCP Server

> FastAPI 应用的 MCP 服务器 - 现代 Python Web 开发

#### 背景需求

FastAPI 是现代 Python Web 开发的首选框架，需要与 Claude Code 深度集成。

#### 目标

提供 FastAPI 应用的自动化开发、测试和部署支持。

#### 本地部署

```bash
pip install fastapi-mcp-server
```

#### 效果展示

- GitHub Stars：⭐ 120+
- ClawHub 评分：1.054-1.121

#### 核心特性

| 特性 | 说明 |
|------|------|
| 高性能 | 与 Node.js 和 Go 相当 |
| 自动文档 | Swagger UI/ReDoc |
| 类型安全 | Pydantic 集成 |
| 异步支持 | async/await |

---

### 3.3 Django MCP Server

> Django 应用的 MCP 服务器 - 经典 Python Web 框架

#### 背景需求

Django 是 Python 最成熟的全栈 Web 框架，拥有庞大的企业用户群体。

#### 本地部署

```bash
pip install django-mcp-server
```

---

### 3.4 AWS MCP Server

> AWS 云服务的 MCP 服务器

#### 背景需求

AWS 是最流行的云服务平台，开发者需要便捷的方式来管理 AWS 资源。

#### 本地部署

```bash
pip install aws-mcp-server
```

#### 效果展示

- GitHub Stars：⭐ 1350+

---

### 3.5 Python Type Safety Skills

> Python 类型安全技能集

#### 背景需求

Python 3.5+ 引入了类型提示，需要专业工具来保证类型安全。

#### 目标

提供 mypy、pyright 等工具的集成支持。

---

### 3.6 read-only-postgres

> PostgreSQL 只读查询技能 - 安全数据库操作

#### 背景需求

数据库操作需要严格的安全控制，特别是对生产环境的查询。

#### 核心功能

- 只读查询：仅支持 SELECT/SHOW/EXPLAIN/WITH
- 多连接支持：配置多个数据库连接
- 安全验证：严格的验证机制
- 超时控制：防止长时间查询

#### 本地部署

```bash
git clone https://github.com/jawwadfirdousi/agent-skills.git
cp -r agent-skills/read-only-postgres ~/.claude/skills/
```

---

## 四、自动化测试插件深度分析

### 4.1 Playwright MCP Server

> Playwright 测试自动化 MCP - 现代 Web E2E 测试

#### 背景需求

Playwright 是微软推出的现代 Web 测试工具，支持多浏览器自动化。

#### 目标

提供 Playwright 测试的 Claude Code 集成。

#### 本地部署

```bash
npm install -g @anthropic/playwright-mcp-server
```

#### 效果展示

- 评分：3.581
- GitHub Stars：⭐ 500+

#### 核心功能

- 浏览器自动化
- 跨浏览器测试
- API 测试
- 移动端测试

---

### 4.2 Playwright Undetected Skill

> 反检测 Playwright - 绕过 Bot 检测

#### 背景需求

某些网站有严格的 Bot 检测机制，需要使用特殊技术绕过。

#### 核心功能

- Patchright 支持
- 反检测浏览器自动化
- 模拟真实用户行为

#### 本地部署

```bash
npm install -g @anthropic-ai/patchright
git clone https://github.com/dalbit-mir/playwright-undetected-skill.git
```

---

### 4.3 pytest-mcp

> pytest 的 MCP 服务器 - Python 单元测试标准

#### 背景需求

pytest 是 Python 最流行的单元测试框架。

#### 本地部署

```bash
pip install pytest-mcp-server
```

---

### 4.4 Android ADB Testing

> Android ADB 自动化测试

#### 背景需求

移动端游戏和应用测试需求日益增长。

#### 本地部署

```bash
# 通过 ClawHub 安装
clawhub install android-adb
```

#### 核心功能

- 设备校准
- UI 检查
- 交互命令
- 截图验证

---

### 4.5 iOS Simulator Skill

> iOS 模拟器集成

#### 背景需求

iOS 游戏和应用测试需要模拟器支持。

#### 本地部署

```bash
git clone https://github.com/conorluddy/ios-simulator-skill ~/.claude/skills/
```

#### 效果展示

- GitHub Stars：⭐ 557

---

## 五、开发者工具插件深度分析

### 5.1 GitHub MCP Server

> GitHub 官方 MCP 服务器

#### 背景需求

GitHub 是最大的代码托管平台，需要深度集成。

#### 本地部署

```bash
npm install -g @github/mcp-server
```

---

### 5.2 Context7 MCP Server

> 最新代码文档服务

#### 背景需求

开发者需要快速获取框架和库的文档。

#### 本地部署

```bash
npm install -g @context7/mcp-server
```

#### 效果展示

- 支持框架：50+

---

### 5.3 Chrome DevTools MCP

> Chrome 开发者工具集成

#### 背景需求

Chrome DevTools 是前端开发必备工具。

#### 本地部署

```bash
npm install -g @chromedevtools/mcp-server
```

---

### 5.4 Superpowers

> 软件工程核心能力集 - ⭐ 4.1k+

#### 背景需求

软件工程涉及多个领域的最佳实践，需要系统化的技能集。

#### 目标

提供完整的软件工程生命周期支持。

#### 本地部署

```bash
git clone https://github.com/obra/superpowers ~/.claude/plugins/
```

#### 效果展示

- GitHub Stars：⭐ 4.1k+
- 覆盖范围：规划、审查、测试、调试

#### 优缺点

✅ 全面覆盖 ✅ 最佳实践 ✅ 组织良好 ✅ 适应性强
⚠️ 可能过于重量级

---

### 5.5 AgentSys

> Claude 工作流自动化系统

#### 背景需求

现代软件开发需要自动化的工作流来提高效率。

#### 本地部署

```bash
git clone https://github.com/avifenesh/agentsys ~/.claude/plugins/
```

#### 效果展示

- GitHub Stars：⭐ 500+

#### 核心功能

- 任务到生产工作流自动化
- PR 管理
- 代码清理
- 性能调查
- 漂移检测
- 多代理代码审查

---

### 5.6 Claude Code Settings

> 核心开发者活动配置集

#### 本地部署

```bash
git clone https://github.com/fcakyon/claude-codex-settings ~/.claude/plugins/
```

#### 效果展示

- GitHub Stars：⭐ 180+

---

### 5.7 Claude Scientific Skills

> 科学研究技能集 - 科研工作者必备

#### 背景需求

科研工作者需要专业化的 AI 辅助工具来进行研究、分析和写作。

#### 核心功能

- 研究技能
- 科学分析
- 工程计算
- 数据分析
- 金融建模
- 学术写作

#### 本地部署

```bash
git clone https://github.com/K-Dense-AI/claude-scientific-skills ~/.claude/plugins/
```

---

### 5.8 Parry

> Prompt 注入扫描器 - 安全防护工具

#### 背景需求

Claude Code 可能会受到 Prompt 注入攻击，需要专业工具进行防护。

#### 核心功能

- 扫描工具输入/输出
- 检测注入攻击
- 敏感信息检测
- 数据泄露防护

#### 本地部署

```bash
git clone https://github.com/vaporif/parry ~/.claude/plugins/
```

---

### 5.9 Dippy

> AST 智能命令批准 - 安全与效率平衡

#### 背景需求

需要平衡安全性和效率，既要防止危险命令，又要避免频繁确认。

#### 核心功能

- AST 命令解析
- 自动批准安全命令
- 危险操作提醒
- 支持 Claude Code、Gemini CLI、Cursor

#### 本地部署

```bash
git clone https://github.com/ldayton/Dippy ~/.claude/plugins/
```

---

### 5.10 Claude-tmux

> tmux 中的 Claude Code 管理

#### 背景需求

需要在终端中高效管理多个 Claude Code 会话。

#### 核心功能

- tmux 弹出窗口
- 多实例管理
- 状态监控
- git worktree 支持
- PR 支持

#### 本地部署

```bash
git clone https://github.com/nielsgroen/claude-tmux ~/.claude/plugins/
```

---

### 5.11 Claude-esp

> TUI 工具 - 输出流监控

#### 背景需求

需要监控 Claude Code 的隐藏输出，了解底层执行过程。

#### 核心功能

- 隐藏输出流监控
- 多会话同时观看
- 内容类型过滤
- 后台任务跟踪

#### 本地部署

```bash
git clone https://github.com/phiat/claude-esp ~/.claude/plugins/
```

---

### 5.12 Docker Essentials

> Docker 容器化技能集

#### 本地部署

```bash
clawhub install docker-essentials
```

---

### 5.13 Git Essentials

> Git 版本控制技能集

#### 本地部署

```bash
clawhub install git-essentials
```

---

## 六、快速推荐

### 游戏客户端开发推荐

| 插件 | 推荐指数 | 适用场景 |
|------|----------|----------|
| Claude-Code-Game-Studios | ⭐⭐⭐⭐⭐ | 全流程游戏开发 |
| Unreal-MCP | ⭐⭐⭐⭐⭐ | Unreal Engine AAA 开发 |
| Godot GDScript MCP | ⭐⭐⭐⭐ | Godot 轻量级开发 |
| Unity GameDev Skills | ⭐⭐⭐ | Unity 独立游戏 |
| Game Cog | ⭐⭐⭐⭐⭐ | 游戏开发编排 |

### Python 开发推荐

| 插件 | 推荐指数 | 适用场景 |
|------|----------|----------|
| FastAPI MCP | ⭐⭐⭐⭐⭐ | FastAPI 现代 Web 开发 |
| Django MCP | ⭐⭐⭐⭐ | Django 传统 Web 开发 |
| Pydantic AI Skills | ⭐⭐⭐⭐⭐ | AI 应用开发 |
| AWS MCP Server | ⭐⭐⭐⭐⭐ | AWS 云服务集成 |
| Python Type Safety | ⭐⭐⭐⭐ | 类型安全 |
| read-only-postgres | ⭐⭐⭐⭐ | 安全数据库查询 |

### 自动化测试推荐

| 插件 | 推荐指数 | 适用场景 |
|------|----------|----------|
| Playwright MCP | ⭐⭐⭐⭐⭐ | Web E2E 测试 |
| Playwright Undetected | ⭐⭐⭐⭐ | 反检测测试 |
| pytest-mcp | ⭐⭐⭐⭐ | Python 单元测试 |
| Android ADB | ⭐⭐⭐⭐ | 移动端测试 |
| iOS Simulator | ⭐⭐⭐⭐ | iOS 测试 |

### 开发者工具推荐

| 插件 | 推荐指数 | 适用场景 |
|------|----------|----------|
| GitHub MCP | ⭐⭐⭐⭐⭐ | GitHub 集成 |
| Context7 MCP | ⭐⭐⭐⭐⭐ | 文档服务 |
| Chrome DevTools | ⭐⭐⭐⭐⭐ | 浏览器自动化 |
| Superpowers | ⭐⭐⭐⭐⭐ | 核心工程技能 |
| AgentSys | ⭐⭐⭐⭐⭐ | 工作流自动化 |
| Claude Scientific | ⭐⭐⭐⭐ | 科研工作 |
| Parry | ⭐⭐⭐⭐ | 安全防护 |
| Dippy | ⭐⭐⭐⭐ | 命令安全 |
| Claude-tmux | ⭐⭐⭐⭐ | 会话管理 |
| Docker Essentials | ⭐⭐⭐⭐ | 容器化 |
| Git Essentials | ⭐⭐⭐⭐ | 版本控制 |

---

## 七、MCP 服务器安装指南

### 通用安装方式

#### Python (pip)

```bash
pip install <package-name>
```

#### Node.js (npm)

```bash
npm install -g <package-name>
```

#### Claude Desktop 配置

在 `~/.config/claude-desktop/mcp.json` 中添加：

```json
{
  "mcpServers": {
    "<server-name>": {
      "command": "npx",
      "args": ["-y", "<package-name>"]
    }
  }
}
```

### 推荐插件组合

#### 游戏开发

```bash
npm install -g unreal-mcp-server
npm install -g godot-mcp-server
git clone https://github.com/ai-game-studios/claude-code-game-studios ~/.claude/plugins/
```

#### Python 开发

```bash
pip install fastapi-mcp-server
pip install django-mcp-server
pip install pytest-mcp-server
git clone https://github.com/pydantic-ai/skills ~/.claude/plugins/
```

#### 测试自动化

```bash
npm install -g @anthropic/playwright-mcp-server
pip install pytest-mcp-server
```

#### 开发者工具

```bash
npm install -g @github/mcp-server
npm install -g @context7/mcp-server
git clone https://github.com/obra/superpowers ~/.claude/plugins/
git clone https://github.com/avifenesh/agentsys ~/.claude/plugins/
```

---

## 八、总结

本调研涵盖了 Claude Code 在游戏客户端开发、Python 开发、自动化测试和开发者工具领域的热门插件。这些插件可以显著提升开发效率，建议根据实际需求选择合适的组合。

### 关键发现

1. **游戏开发领域**：Unreal-MCP 是最强大的游戏引擎集成工具，Game Cog 编排器评分最高
2. **Python 开发**：FastAPI MCP 和 Pydantic AI Skills 是最受欢迎的 Python 工具
3. **测试自动化**：Playwright MCP 是 E2E 测试的首选
4. **开发者工具**：Superpowers (4.1k+ stars) 和 AgentSys 提供了最完整的工程实践支持
5. **安全工具**：Parry 和 Dippy 提供安全防护能力

### 后续建议

- 持续关注官方 MCP 服务器更新
- 根据项目需求选择合适的插件组合
- 参与社区反馈和改进
- 定期更新调研文档

---

> 调研时间：2026年3月4日
> 数据来源：awesome-claude-code、GitHub、ClawHub
