# Claude Code 插件调研报告 - 2026年3月 (补充-第五期)

> 持续跟踪 Claude Code 生态热门插件，聚焦游戏开发、Python 开发、自动化测试、开发者工具方向

---

## 📋 调研概要

| 维度 | 统计 |
|-----|------|
| **调研时间** | 2026-03-04 |
| **覆盖方向** | 游戏开发、Python开发、自动化测试、开发者工具 |
| **技能总数** | 150+ 精选 |
| **数据来源** | awesome-claude-code, GitHub trending, Claude Official |

---

## 一、游戏客户端开发技能 (更新)

### 1.1 Claude Code Game Studios ⭐ 主流

| 项目 | 说明 |
|-----|------|
| **GitHub** | [Donchitos/Claude-Code-Game-Studios](https://github.com/Donchitos/Claude-Code-Game-Studios) |
| **Star** | ⭐ 26 |
| **更新** | 3天前 |
| **特点** | 48个AI代理 + 36个工作流技能 + 完整协调系统 |

#### 核心能力

- **48个专业AI代理**: 覆盖游戏开发全流程
- **36个工作流技能**: 完整游戏开发管线
- **工作室协调系统**: 模拟真实游戏工作室工作流
- **多引擎支持**: Unity, Unreal, Godot, WebGL

#### 适用场景

- 大型游戏项目开发
- 游戏工作室工作流自动化
- 跨团队协作开发
- 全栈游戏开发

### 1.2 Unity 开发技能

| 技能 | GitHub | Star | 特点 |
|-----|--------|------|------|
| **cc-plugin-unity-gamedev** | tjboudreaux/cc-plugin-unity-gamedev | ⭐1 | 21个专业技能，完整覆盖Unity开发栈 |
| **OH-Unity-GameDev-Skills** | OstrichHermit/OH-Unity-GameDev-Skills | ⭐6 | Unity基础开发+DoTween+MediaPipe |
| **unity-ai-workflow** | David-GD13/unity-ai-workflow | ⭐4 | Unity 6.2+ AI-first工作流 |
| **solana-game-skill** | solanabr/solana-game-skill | ⭐5 | Solana区块链游戏开发 |

#### Unity 技能核心分类

| 分类 | 技能 |
|-----|------|
| **工具类** | Addressables, MemoryPack, ScriptableObjects, Profiling |
| **动画/物理** | Animation, Physics, NavMesh, Object Pooling, State Machine |
| **AI/行为** | Behavior Designer, GAS (Gameplay Ability System) |
| **音视频** | Wwise音频, Cinemachine相机 |
| **UI** | UGUI, Mobile Optimization |
| **测试** | Unity Test Framework |
| **DI/异步** | VContainer, UniTask |

### 1.3 Unity AI Workflow (2026 新增)

#### 项目地址
- **GitHub**: [David-GD13/unity-ai-workflow](https://github.com/David-GD13/unity-ai-workflow)
- **Star**: ⭐ 4
- **特点**: 专为 Unity 6.2+ 设计的 AI-first 开发工作流

#### Dev Modes (三种开发模式)

| 模式 | 角色 | 适用场景 |
|------|------|---------|
| Assistant | 你构建，AI 辅助文档和解释 | 学习、创意控制 |
| Mix (默认) | 协作模式，AI 建议，你确认 | 大多数项目 |
| Automatic | AI 构建，短的 onboarding Q&A | 快速原型、游戏 jam |

#### 核心哲学: Game Feel 不是可选的

- 每项功能使用 /implement-feature 完整构建
- AI 在写代码前询问 VFX、SFX、相机反馈和触觉
- 迭代打磨，不是单独阶段

#### 技术架构

- **TCREI Prompting**: Task-Context-References-Evaluate-Iterate 方法论
- **验证系统**: 每个 AI 推荐标记 [VERIFIED]/[SYNTHESIZED]/[UNVERIFIED]
- **专家 Skills**: UI Toolkit、ScriptableObject、Netcode、game feel、测试、调试

### 1.4 游戏引擎选择决策树

```
什么类型的游戏?
│
├── 2D 游戏
│   ├── 需要完整引擎功能? → Phaser 4
│   └── 需要原始渲染能力? → PixiJS 8
│
├── 3D 游戏
│   ├── 需要完整引擎(物理、XR)? → Babylon.js 7
│   └── 专注渲染? → Three.js
│
└── 混合/Canvas
    └── 自定义 → 原始 Canvas/WebGL
```

### 1.5 游戏开发技能汇总

| 方向 | 推荐技能 | Star | 特点 |
|-----|---------|------|------|
| **Unity 完整开发** | Claude-Code-Game-Studios | ⭐26 | 48代理全栈覆盖 |
| **Unity 基础** | cc-plugin-unity-gamedev | ⭐1 | 21技能专业栈 |
| **Unity AI工作流** | unity-ai-workflow | ⭐4 | Unity 6.2+ |
| **Godot** | claude-resources | ⭐3 | 开源游戏引擎 |
| **GameMaker** | gamemaker-skills | ⭐2 | 2D游戏专用 |
| **Solana链游** | solana-game-skill | ⭐5 | 区块链游戏 |

---

## 二、Python 开发技能 (更新)

### 2.1 数据库集成

| 技能 | GitHub | 功能 | 安全性 |
|-----|--------|------|--------|
| **read-only-postgres** | jawwadfirdousi/agent-skills | PostgreSQL只读查询 | ⭐⭐⭐⭐⭐ |
| **postgres** | sanjay3290/ai-skills | PostgreSQL完整集成 | ⭐⭐⭐ |

#### read-only-postgres 核心特性

```sql
-- 支持的查询类型
SELECT * FROM users WHERE id = 1;
SHOW max_connections;
EXPLAIN ANALYZE SELECT * FROM orders;
WITH recent AS (...) SELECT * FROM recent;
```

#### 安全特性

| 特性 | 描述 |
|-----|------|
| **只读查询** | 仅支持 SELECT/SHOW/EXPLAIN/WITH |
| **超时限制** | 防止长时间运行查询 |
| **行数限制** | 防止大数据集返回 |
| **多连接** | 支持配置多个数据库连接 |

### 2.2 AWS 云服务集成

#### AWS MCP Server

| 项目 | 说明 |
|-----|------|
| **GitHub** | [alexei-led/aws-mcp-server](https://github.com/alexei-led/aws-mcp-server) |
| **语言** | Python |
| **特点** | AWS CLI 集成，多环境支持 |

#### 支持的服务

| 服务类别 | 支持内容 |
|---------|---------|
| **计算** | EC2, Lambda, ECS, EKS |
| **存储** | S3, EBS, EFS |
| **数据库** | RDS, DynamoDB, ElastiCache |
| **网络** | VPC, CloudFront, Route53 |
| **安全** | IAM, Secrets Manager |

### 2.3 Pydantic AI 深度集成

#### pydantic-ai-skills

| 项目 | 说明 |
|-----|------|
| **GitHub** | [DougTrajano/pydantic-ai-skills](https://github.com/DougTrajano/pydantic-ai-skills) |
| **Star** | ⭐ 136 |
| **语言** | Python |
| **特点** | Agent Skills 支持 Pydantic AI |

#### 核心功能

- **类型安全**: Pydantic 模型强制类型检查
- **渐进式提示**: 按需披露信息
- **AI 集成**: 与主流 LLM 无缝集成
- **验证系统**: 内置强大的数据验证

### 2.4 Developer Kit ⭐ NEW

| 项目 | 说明 |
|-----|------|
| **GitHub** | [giuseppe-trisciuoglio/developer-kit](https://github.com/giuseppe-trisciuoglio/developer-kit) |
| **Star** | ⭐ 128 |
| **特点** | 模块化插件系统，覆盖多技术栈 |

#### 技术栈覆盖

| 分类 | 技术栈 | 功能 |
|-----|--------|------|
| **Java** | Spring Boot, LangChain4J | 企业级 AI 开发 |
| **前端** | TypeScript, NestJS, React | 全栈开发 |
| **Python** | Python | 通用开发 |
| **PHP** | WordPress | CMS 开发 |
| **云** | AWS CloudFormation | 基础设施即代码 |
| **AI** | AI Patterns | AI 集成模式 |

### 2.5 Claude Code Tools (会话连续性)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [pchalasani/claude-code-tools](https://github.com/pchalasani/claude-code-tools) |
| **功能** | 会话连续性工具集 |
| **特点** | 避免上下文压缩，保持会话记忆 |

#### 核心功能

- **上下文保持**: 避免长时间会话的上下文压缩
- **跨代理切换**: Claude Code 与 Codex CLI 之间的上下文传递
- **会话搜索**: 基于 Tantivy 的全文搜索
- **Tmux 集成**: 与 tmux 无缝协作

### 2.6 Claudekit - CLI 工具包

| 项目 | 说明 |
|-----|------|
| **GitHub** | [carlrannaberg/claudekit](https://github.com/carlrannaberg/claudekit) |
| **功能** | CLI 工具包，20+ 子代理 |

#### 子代理列表

| 代理 | 功能 |
|-----|------|
| **oracle** | GPT-5 集成 |
| **code-reviewer** | 6方面深度分析 |
| **typescript-expert** | TypeScript 专家 |
| **ai-sdk-expert** | Vercel AI SDK |

### 2.7 Python 测试技能

#### pytest 最佳实践

```bash
# 运行所有测试
pytest

# 运行带标记的测试
pytest -m "unit"

# 生成覆盖率报告
pytest --cov=src --cov-report=html
```

#### TDD 开发流程

```
红色 (Red) → 编写失败的测试
   ↓
绿色 (Green) → 实现最小代码通过测试
   ↓
重构 (Refactor)→ 重构代码保持测试通过
```

### 2.8 Python 开发技能汇总

| 方向 | 推荐技能 | Star | 特点 |
|-----|---------|------|------|
| **数据库** | read-only-postgres | ⭐10 | 安全只读查询 |
| **云服务** | AWS MCP Server | ⭐活跃 | AWS 全服务支持 |
| **AI 框架** | pydantic-ai-skills | ⭐136 | 类型安全 AI 开发 |
| **开发者工具** | developer-kit | ⭐128 | 多技术栈覆盖 |
| **会话连续性** | claude-code-tools | - | 上下文保持 |
| **CLI 工具** | claudekit | - | 20+ 子代理 |

---

## 三、游戏客户端自动化测试 (更新)

### 3.1 浏览器自动化测试 - Playwright

#### Playwright Skill (核心)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [lackeyjb/playwright-skill](https://github.com/lackeyjb/playwright-skill) |
| **Star** | ⭐ 1.8k |
| **功能** | Playwright 浏览器自动化 |
| **特点** | 模型调用的 Playwright 自动化 |

#### 核心功能

- **Web 应用测试**: 自动化测试 Web 应用功能
- **UI 验证**: 验证前端功能和行为
- **截图捕获**: 自动截图记录测试状态
- **调试支持**: 辅助调试 UI 行为
- **Bot 检测绕过**: Patchright 支持反检测

### 3.2 Playwright Bot Bypass ⭐ NEW

| 项目 | 说明 |
|-----|------|
| **GitHub** | [greekr4/playwright-bot-bypass](https://github.com/greekr4/playwright-bot-bypass) |
| **特点** | Bot 检测绕过 (Google CAPTCHA 等) |

#### 核心功能

- **反检测**: 绕过机器人检测
- **CAPTCHA 处理**: Google CAPTCHA 绕过
- **Stealth 模式**: 隐匿浏览
- **多种网站**: 支持主流网站自动化

### 3.3 Playwright Undetected Skill

| 项目 | 说明 |
|-----|------|
| **GitHub** | [dalbit-mir/playwright-undetected-skill](https://github.com/dalbit-mir/playwright-undetected-skill) |
| **Star** | ⭐ 4 |
| **特点** | Bot 检测绕过 |

### 3.4 Unity 测试框架

#### Unity Test Framework Skill

| 项目 | 说明 |
|-----|------|
| **来源** | cc-plugin-unity-gamedev |
| **功能** | Unity 单元测试 |

#### 测试类型

| 类型 | 说明 | 适用场景 |
|-----|------|---------|
| **EditMode** | 编辑器环境测试 | 工具类、辅助功能 |
| **PlayMode** | 运行时测试 | 游戏逻辑、UI |
| **Performance** | 性能测试 | 性能优化 |

### 3.5 ADB 移动端测试

#### Android 测试技能

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

#### iOS 模拟器测试

| 项目 | 说明 |
|-----|------|
| **GitHub** | [conorluddy/ios-simulator-skill](https://github.com/conorluddy/ios-simulator-skill) |
| **Star** | ⭐ 557 |
| **平台** | macOS |

#### 核心功能

- 模拟器控制 (启动/停止)
- 应用安装
- UI 交互自动化
- 截图捕获

### 3.6 测试命令 Slash Commands

| 命令 | 来源 | 功能 |
|-----|------|------|
| **/tdd** | zscott/pane | TDD开发流程 |
| **/tdd-implement** | jerseycheese/Narraitor | TDD实现 |
| **/repro-issue** | rzykov/metabase | 可复现测试用例 |
| **/check** | rygwdn/slack-tools | 代码质量检查 |

### 3.7 游戏自动化测试汇总

| 方向 | 推荐技能 | Star | 特点 |
|-----|---------|------|------|
| **Web 测试** | playwright-skill | ⭐1.8k | 主流浏览器自动化 |
| **反检测** | playwright-bot-bypass | ⭐NEW | Bot 绕过测试 |
| **Unity 测试** | Unity Test Framework | - | 单元/集成测试 |
| **移动端** | ADB/iOS Simulator | - | 移动设备测试 |
| **TDD** | /tdd-implement | - | 测试驱动开发 |

---

## 四、其他开发者工具 (更新)

### 4.1 Agent 编排工具

#### Claude Squad - 多代理管理

| 项目 | 说明 |
|-----|------|
| **GitHub** | [smtg-ai/claude-squad](https://github.com/smtg-ai/claude-squad) |
| **功能** | 终端应用管理多个 Claude Code、Codex 等代理 |

#### Claude Swarm - 代理群体

| 项目 | 说明 |
|-----|------|
| **GitHub** | [parruda/claude-swarm](https://github.com/parruda/claude-swarm) |
| **功能** | 连接 Claude Code 到代理群体 |

#### sudocode - 轻量级编排

| 项目 | 说明 |
|-----|------|
| **GitHub** | [sudocode-ai/sudocode](https://github.com/sudocode-ai/sudocode) |
| **功能** | 轻量级 agent 编排开发工具，集成规范框架 |

### 4.2 项目管理集成

#### JIRA Skill ⭐ NEW

| 项目 | 说明 |
|-----|------|
| **GitHub** | [netresearch/jira-skill](https://github.com/netresearch/jira-skill) |
| **特点** | 智能 JIRA 集成，支持 MCP 配置 |

#### Claude Code PM

| 项目 | 说明 |
|-----|------|
| **GitHub** | [automazeio/ccpm](https://github.com/automazeio/ccpm) |
| **功能** | 综合性项目管理 workflow |

### 4.3 记忆与上下文

#### HAM 记忆系统 ⭐ NEW

| 项目 | 说明 |
|-----|------|
| **GitHub** | [kromahlusenii-ops/ham](https://github.com/kromahlusenii-ops/ham) |
| **特点** | AI 记忆系统，减少 50% token 使用 |

#### Claude Mem

| 项目 |说明 |
|-----|------|
| **GitHub** | [thedotmack/claude-mem](https://github.com/thedotmack/claude-mem) |
| **功能** | 自动捕获编码会话，压缩并注入未来会话 |

### 4.4 安全工具

#### Trail of Bits Security Skills

| 项目 | 说明 |
|-----|------|
| **GitHub** | [trailofbits/skills](https://github.com/trailofbits/skills) |
| **特点** | 安全专家团队开发，CodeQL/Semgrep 集成 |

#### 安全技能分类

| 技能 | 功能 |
|-----|------|
| **static-analysis** | 静态分析 |
| **codeql** | CodeQL 漏洞检测 |
| **semgrep** | Semgrep 模式匹配 |
| **variant-analysis** | 变体分析 |

#### parry - 提示注入扫描

| 项目 | 说明 |
|-----|------|
| **GitHub** | [vaporif/parry](https://github.com/vaporif/parry) |
| **特点** | 提示注入扫描器，扫描工具输入/输出 |

#### Dippy - AST 安全批准

| 项目 | 说明 |
|-----|------|
| **GitHub** | [ldayton/Dippy](https://github.com/ldayton/Dippy) |
| **特点** | AST 自动批准安全命令，提示危险操作 |

### 4.5 开发环境

#### Claude Code Templates

| 项目 | 说明 |
|-----|------|
| **GitHub** | [davila7/claude-code-templates](https://github.com/davila7/claude-code-templates) |
| **功能** | CLI 工具配置和监控 Claude Code |

#### Claude Hub

| 项目 | 说明 |
|-----|------|
| **GitHub** | [claude-did-this/claude-hub](https://github.com/claude-did-this/claude-hub) |
| **功能** | Webhook 服务连接 Claude Code 到 GitHub 仓库 |

### 4.6 Hook 系统

| 技能 | GitHub | 语言 |
|-----|--------|------|
| **claude-hooks** | johnlindquist/claude-hooks | TypeScript |
| **cchooks** | GowayLee/cchooks | Python |
| **claude-code-hooks-sdk** | beyondcode/claude-hooks-sdk | PHP |

### 4.7 使用监控

#### CC Usage

| 项目 | 说明 |
|-----|------|
| **GitHub** | [ryoppippi/ccusage](https://github.com/ryoppippi/ccusage) |
| **功能** | CLI 工具管理和分析 Claude Code 使用情况 |

#### ccflare - Web 仪表盘

| 项目 | 说明 |
|-----|------|
| **GitHub** | [snipeship/ccflare](https://github.com/snipeship/ccflare) |
| **功能** | Web UI 使用仪表盘 |

#### better-ccflare

| 项目 | 说明 |
|-----|------|
| **GitHub** | [tombii/better-ccflare](https://github.com/tombii/better-ccflare/) |
| **功能** | ccflare 增强分支，Docker 部署支持 |

### 4.8 IDE 集成

| 工具 | GitHub | 平台 |
|-----|--------|------|
| **claude-code.nvim** | greggh/claude-code.nvim | Neovim |
| **claude-code.el** | stevemolitor/claude-code.el | Emacs |
| **Claude Code Chat** | andrepimenta/claude-code-chat | VS Code |
| **Claudix** | Haleclipse/Claudix | VS Code |

### 4.9 开发者工具汇总

| 方向 | 推荐技能 | 特点 |
|-----|---------|------|
| **代理编排** | Claude Squad / Claude Swarm | 多代理管理 |
| **项目管理** | jira-skill / Claude Code PM | JIRA 集成 |
| **记忆系统** | HAM / Claude Mem | Token 优化 |
| **安全审计** | trailofbits-skills / parry | 安全检测 |
| **开发环境** | Claude Code Templates | 配置管理 |
| **Hook 系统** | claude-hooks / cchooks | 生命周期钩子 |
| **使用监控** | ccflare | 使用分析 |
| **IDE 集成** | claude-code.nvim | Neovim/Emacs/VSCode |

---

## 五、推荐技能组合

### 5.1 游戏开发组合

```
Claude Code Game Studios + Unity 技能集 + Playwright
```

### 5.2 Python 开发组合

```
Python Patterns + Pydantic AI + read-only-postgres + developer-kit + claude-code-tools
```

### 5.3 自动化测试组合

```
Playwright + playwright-bot-bypass + Unity Test Framework + ADB
```

### 5.4 团队协作组合

```
Claude Code PM + jira-skill + HAM + Claude Hub
```

### 5.5 安全优先组合

```
trailofbits-skills + parry + Dippy
```

---

## 六、趋势分析

### 技术趋势

| 方向 | 趋势 | 说明 |
|-----|------|------|
| **Agent工作流** | ⬆️ 上升 | agentsys, Claude Code Flow |
| **安全审计** | ⬆️ 上升 | trailofbits-skills, parry, Dippy |
| **游戏开发** | ⬆️ 上升 | Claude Code Game Studios 全栈覆盖 |
| **测试自动化** | ⬆️ 上升 | Playwright 主导 |
| **Hook 生态** | ⬆️ 上升 | 多语言 SDK |

### 技术栈分布

- **TypeScript**: 35+ 技能
- **Python**: 25+ 技能
- **Go**: 5+ 技能 (cc-tools, ccexp)
- **PHP**: 2+ 技能 (claude-hooks-sdk)

---

## 七、总结

本期调研亮点：

1. **游戏开发**: Claude Code Game Studios (48 代理) + Unity AI Workflow
2. **Python Developer Kit**: 覆盖 Java/Spring Boot, TypeScript/NestJS/React, Python, PHP/WordPress, AWS CloudFormation
3. **会话连续性**: claude-code-tools 解决上下文压缩问题
4. **团队协作**: Claude Squad/Claude Swarm 多代理管理
5. **安全增强**: parry 提示注入扫描 + Dippy AST 安全批准
6. **记忆优化**: HAM 减少 50% token 使用

---

## 📚 参考链接

- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
- [awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills)
- [Claude Code Handbook](https://nikiforovall.blog/claude-code-rules/)
- [Claude Code Ultimate Guide](https://github.com/FlorianBruniaux/claude-code-ultimate-guide)
- [Claude Code Game Studios](https://github.com/Donchitos/Claude-Code-Game-Studios)
- [Unity AI Workflow](https://github.com/David-GD13/unity-ai-workflow)
- [Developer Kit](https://github.com/giuseppe-trisciuoglio/developer-kit)
- [Playwright Skill](https://github.com/lackeyjb/playwright-skill)
- [Trail of Bits Skills](https://github.com/trailofbits/skills)
- [Claude Code Tools](https://github.com/pchalasani/claude-code-tools)

---

*持续更新中，欢迎提交 PR 补充更多技能*
