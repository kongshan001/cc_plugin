# Claude Code 插件调研 - 第四十四期

> 热门插件深度调研：游戏客户端开发、Python开发、自动化测试、开发者工具

## 调研时间
2026-03-04

## 数据来源
- awesome-claude-code (hesreallyhim/awesome-claude-code)
- ComposioHQ/awesome-claude-skills (100+ 技能)
- GitHub Topics: claude-code-skills
- 官方团队技能库 (Anthropic, Vercel, Cloudflare, Google, Microsoft 等)
- cc_plugin 仓库历史调研文档

---

## 一、游戏客户端开发技能 (深度调研)

### 1.1 官方 Web/游戏开发技能 (Anthropic)

#### web-artifacts-builder ⭐⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [anthropics/skills/web-artifacts-builder](https://github.com/anthropics/skills/tree/main/skills/web-artifacts-builder) |
| **官方** | ✅ Anthropic |
| **技术栈** | React + Tailwind CSS + shadcn/ui + TypeScript |

**核心能力:**
- 多组件 HTML artifacts 构建
- 现代前端技术栈完整支持
- WebGL 游戏界面生成
- 响应式设计系统
- 可交互 UI 组件

**游戏开发适用场景:**
| 场景 | 适用性 | 说明 |
|------|--------|------|
| WebGL 游戏界面开发 | ✅ 高度适合 | 完整的 React 组件生态 |
| HTML5 游戏原型 | ✅ 适合 | 快速原型开发 |
| 游戏官网/落地页 | ✅ 非常适合 | 现代前端技术栈 |
| 游戏内嵌 Web 视图 | ✅ 适合 | WebView 接口对接 |
| 游戏配置工具 | ✅ 非常适合 | 表单+数据管理 |

**安装使用:**
```bash
# 复制技能到本地
cp -r skills/web-artifacts-builder ~/.claude/skills/

# 在 Claude Code 中调用
/webartifacts
```

#### algorithmic-art ⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [anthropics/skills/algorithmic-art](https://github.com/anthropics/skills/tree/main/skills/algorithmic-art) |
| **官方** | ✅ Anthropic |
| **技术** | p5.js + Canvas API |

**游戏相关用途:**
- 程序化生成游戏图形/纹理
- 粒子效果设计与预览
- 视觉特效原型开发
- 着色器效果验证
- 随机地形/地图生成

#### canvas-design ⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [anthropics/skills/canvas-design](https://github.com/anthropics/skills/tree/main/skills/canvas-design) |
| **官方** | ✅ Anthropic |
| **输出** | PNG + PDF + SVG |

**游戏相关用途:**
- 游戏海报/宣传物料设计
- UI 元素设计输出
- 图标/Logo 设计
- 游戏截图美化与导出

---

### 1.2 Unity 开发技能

#### cc-plugin-unity-gamedev ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [tjboudreaux/cc-plugin-unity-gamedev](https://github.com/tjboudreaux/cc-plugin-unity-gamedev) |
| **技能数** | 21+ 专业 Unity 技能 |
| **功能** | Unity 完整开发工作流 |

**技能列表:**
- Unity 编辑器操作
- C# 脚本生成
- 组件系统使用
- 物理系统配置
- 动画状态机
- UI 系统开发
- 资源管理
- 构建优化

**安装:**
```bash
git clone https://github.com/tjboudreaux/cc-plugin-unity-gamedev ~/.claude/plugins/
```

#### OH-Unity-GameDev-Skills

| 项目 | 说明 |
|-----|------|
| **GitHub** | [OlegHahm/OH-Unity-GameDev-Skills](https://github.com/OlegHahm/OH-Unity-GameDev-Skills) |
| **技能** | DoTween + MediaPipe 集成 |

**功能:**
- 动画系统集成 (DoTween)
- 机器学习视觉 (MediaPipe)
- 手势识别交互
- 面部追踪功能

#### unity-ai-workflow

| 项目 | 说明 |
|-----|------|
| **版本** | Unity 6.2+ |
| **功能** | AI 驱动开发工作流 |

---

### 1.3 Unreal/其他游戏引擎

#### Unreal Engine C++ Skills

| 项目 | 说明 |
|-----|------|
| **官方文档** | [Unreal Engine Documentation](https://docs.unrealengine.com) |
| **语言** | C++ |
| **功能** | 完整游戏引擎开发 |

**Claude Code 集成方式:**
- 创建项目 CLAUDE.md
- 定义 C++ 代码规范
- 集成 Unreal Build System
- 配置Blueprint工作流

#### Godot GDScript Skills

| 项目 | 说明 |
|-----|------|
| **GitHub** | [Godot Engine](https://github.com/godotengine/godot) |
| **语言** | GDScript / C# |
| **功能** | 轻量级游戏引擎开发 |

---

### 1.4 移动端游戏开发技能

#### iOS Simulator Skill ⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [conorluddy/ios-simulator-skill](https://github.com/conorluddy/ios-simulator-skill) |
| **作者** | @conorluddy |
| **功能** | iOS 模拟器交互控制 |

**游戏开发用途:**
| 功能 | 描述 |
|------|------|
| iOS 游戏测试 | 模拟器内运行测试 |
| 手游 UI 调试 | 实时 UI 层级检查 |
| 触控交互验证 | 模拟各种触控手势 |
| 设备适配测试 | 多分辨率/设备模拟 |
| 性能监控 | FPS/内存实时监控 |

#### React Native Skills (Vercel) ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [vercel-labs/agent-skills/react-native-skills](https://github.com/vercel-labs/agent-skills/tree/main/skills/react-native-skills) |
| **官方** | ✅ Vercel |
| **功能** | React Native 最佳实践 |

**游戏开发用途:**
- 跨平台手游开发 (iOS + Android)
- 原生模块集成
- 性能优化指南
- 热更新实现

#### CallStack React Native Skills ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [callstackincubator/agent-skills](https://github.com/callstackincubator/agent-skills) |
| **官方** | ✅ CallStack (React Native 核心团队) |

**核心技能:**
- **react-native-best-practices** - React Native 性能优化圣典
- **upgrading-react-native** - React Native 升级工作流
- **github** - GitHub 工作流模式

---

### 1.5 区块链游戏开发技能

#### Move Code Quality Skill ⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [1NickPappas/move-code-quality-skill](https://github.com/1NickPappas/move-code-quality-skill) |
| **语言** | Move (Sui/Aptos) |
| **用途** | 链游智能合约开发 |

**功能:**
- Move 代码质量分析
- Move 2024 Edition 合规检查
- 最佳实践验证
- 安全漏洞检测
- 智能合约审计

#### Trail of Bits 智能合约安全技能 ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [trailofbits/skills/building-secure-contracts](https://github.com/trailofbits/skills/tree/main/plugins/building-secure-contracts) |
| **官方** | ✅ Trail of Bits (安全审计公司) |

**功能:**
- 智能合约安全工具包
- 6 种区块链漏洞扫描器
- 入口点分析
- 规格到代码合规检查

---

### 1.6 游戏开发技能推荐组合

```
🎮 游戏客户端开发技能栈推荐:

Unity 开发:
├── cc-plugin-unity-gamedev (21 技能)
├── OH-Unity-GameDev-Skills (DoTween/MediaPipe)
└── unity-ai-workflow (Unity 6.2+)

Unreal 开发:
├── 官方文档 + CLAUDE.md
└── C++ 最佳实践技能

WebGL/HTML5 游戏:
├── web-artifacts-builder (官方 ⭐⭐⭐⭐⭐)
├── Playwright Browser Automation
├── webapp-testing (官方)
└── frontend-design (官方)

移动端游戏:
├── iOS Simulator Skill
├── React Native Skills (Vercel ⭐⭐⭐⭐)
├── CallStack React Native Skills
└── Mobile Optimization

区块链游戏:
├── Move Code Quality Skill
├── building-secure-contracts
└── Smart Contract 审计技能
```

---

## 二、Python 开发技能 (深度调研)

### 2.1 官方 Python 技能

#### MCP Builder ⭐⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [anthropics/skills/mcp-builder](https://github.com/anthropics/skills/tree/main/skills/mcp-builder) |
| **官方** | ✅ Anthropic |
| **语言** | Python / TypeScript |

**核心能力:**
- 外部 API 集成开发
- 服务连接指导
- 高质量 MCP 服务器开发
- 工具定义最佳实践
- 错误处理模式
- 认证/授权实现

**安装使用:**
```bash
# 复制技能到本地
cp -r mcp-builder ~/.claude/skills/

# 在 Claude Code 中调用
/mcp-builder
```

#### Skill Creator ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [anthropics/skills/skill-creator](https://github.com/anthropics/skills/tree/main/skills/skill-creator) |
| **官方** | ✅ Anthropic |

**功能:**
- 创建 Claude 技能指南
- 技能模板提供
- 最佳实践指导
- 技能结构规范

---

### 2.2 Python 测试技能

#### test-driven-development (Superpowers) ⭐⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [obra/superpowers/tdd](https://github.com/obra/superpowers/tree/main/skills/test-driven-development) |
| **维护** | Jesse Vincent |
| **Star** | ⭐ 4100+ |

**TDD 流程:**
```
1. Red (红) - 编写失败测试
2. Green (绿) - 最小实现使测试通过
3. Refactor (重构) - 重构优化
```

**使用场景:**
- 任何功能实现前
- Bug 修复前
- 代码重构时
- Python 项目开发

#### pypict-claude-skill (组合测试) ⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [omkamal/pypict-claude-skill](https://github.com/omkamal/pypict-claude-skill) |
| **作者** | @omkamal |
| **技术** | PICT (Pairwise Testing) |

**功能:**
- 全面的测试用例设计
- 组合测试优化
- 配对覆盖生成
- 需求/代码分析

**游戏测试应用:**
- 游戏配置组合测试
- 设备/分辨率矩阵
- 本地化测试覆盖
- 多平台兼容性测试

#### property-based-testing (Trail of Bits) ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [trailofbits/skills/property-based-testing](https://github.com/trailofbits/skills/tree/main/plugins/property-based-testing) |
| **官方** | ✅ Trail of Bits |

**功能:**
- 多语言属性测试
- 智能合约测试
- 模糊测试集成
- Hypothesis 测试框架

---

### 2.3 Python 开发工具

#### modern-python (Trail of Bits) ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [trailofbits/skills/modern-python](https://github.com/trailofbits/skills/tree/main/plugins/modern-python) |
| **官方** | ✅ Trail of Bits |

**工具链:**
| 工具 | 用途 |
|------|------|
| **uv** | 快速包管理器 (Rust 实现) |
| **ruff** | 代码检查 (比 flake8 快 10-100x) |
| **ty** | 类型检查 (比 mypy 快) |
| **pytest** | 测试框架 |
| **coverage** | 覆盖率分析 |

**安装:**
```bash
# uv 安装
curl -LsSf https://astral.sh/uv/install.sh | sh

# ruff 安装
pip install ruff

# 工具链使用
uv pip install -r requirements.txt
ruff check .
ty check .
pytest --cov=.
```

#### read-only-postgres ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [jawwadfirdousi/agent-skills](https://github.com/jawwadfirdousi/agent-skills) |
| **作者** | @jawwadfirdousi |
| **安全** | 只读操作 ✅ |

**功能:**
- 安全的 SQL 查询执行 (SELECT/SHOW/EXPLAIN/WITH)
- 多连接支持
- 深度防御安全机制
- 数据库探索
- 查询超时保护
- 行数限制

**Python 数据库测试:**
```bash
# 安装技能
cp -r skills/postgres ~/.claude/skills/

# 使用技能
/postgres
# 显示所有可用连接
# 选择数据库并执行查询
```

#### LangSmith Fetch ⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [ComposioHQ/awesome-claude-skills/langsmith-fetch](https://github.com/ComposioHQ/awesome-claude-skills/blob/master/langsmith-fetch) |
| **作者** | @OthmanAdi |
| **特点** | 首个 AI 可观测性技能 |

**功能:**
- LangChain/LangGraph 调试
- 执行追踪获取
- LangSmith Studio 集成
- Agent 性能分析
- Token 消耗统计

---

### 2.4 Python 推荐技能组合

```
🐍 Python 开发技能栈:

基础开发:
├── python-mcp-server (官方)
├── MCP Builder (服务集成 ⭐⭐⭐⭐⭐)
├── Skill Creator (技能创建 ⭐⭐⭐⭐)
└── modern-python (工具链 ⭐⭐⭐⭐)

测试开发:
├── test-driven-development (TDD ⭐⭐⭐⭐⭐)
├── pypict-claude-skill (组合测试 ⭐⭐⭐)
├── property-based-testing (属性测试 ⭐⭐⭐⭐)
└── read-only-postgres (数据库测试 ⭐⭐⭐⭐)

高级工具:
├── LangSmith Fetch (可观测性 ⭐⭐⭐)
├── subagent-driven-development
└── software-architecture

代码质量:
├── finishing-a-development-branch
├── root-cause-tracing
└── kaizen (持续改进)
```

---

## 三、游戏客户端自动化测试 (深度调研)

### 3.1 官方测试技能

#### webapp-testing (Anthropic) ⭐⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [anthropics/skills/webapp-testing](https://github.com/anthropics/skills/tree/main/skills/webapp-testing) |
| **官方** | ✅ Anthropic |
| **技术** | Playwright |

**核心功能:**
- 本地 Web 应用测试
- 前端功能验证
- UI 行为调试
- 截图/视频捕获
- 跨浏览器测试
- API 集成测试

**游戏测试场景:**
| 场景 | 适用性 | 说明 |
|------|--------|------|
| WebGL 游戏功能测试 | ✅ 高度适合 | Playwright 支持 WebGL |
| HTML5 游戏兼容性 | ✅ 非常适合 | 多浏览器测试 |
| 游戏内嵌 Web 视图 | ✅ 适合 | WebView 测试 |
| 游戏官网测试 | ✅ 非常适合 | 完整 E2E |
| 游戏充值/支付流程 | ✅ 适合 | 自动化支付测试 |

**使用示例:**
```bash
# 安装技能
git clone https://github.com/anthropics/skills.git
cp -r skills/webapp-testing ~/.claude/skills/

# 在 Claude Code 中使用
/webapp-testing http://localhost:3000
# 或
/test-webapp
```

#### Playwright Browser Automation ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [lackeyjb/playwright-skill](https://github.com/lackeyjb/playwright-skill) |
| **作者** | @lackeyjb |
| **类型** | 模型调用自动化 |

**功能:**
- 模型触发的 Playwright 自动化
- Web 应用测试验证
- 浏览器交互模拟
- E2E 测试执行
- 视觉回归测试
- 性能指标收集

#### playwright-mcp

| 项目 | 说明 |
|-----|------|
| **GitHub** | [anonyco/playwright-mcp](https://github.com/anonyco/playwright-mcp) |
| **评分** | 3.581 |
| **功能** | Playwright MCP 服务器 |

---

### 3.2 游戏自动化测试框架

#### Unity Test Framework

| 项目 | 说明 |
|-----|------|
| **官方** | ✅ Unity Technologies |
| **类型** | 单元/集成测试 |
| **语言** | C# |

**测试类型:**
- 单元测试 ( NUnit )
- 集成测试
- 性能测试
- 编辑器测试
- PlayMode 测试

**游戏客户端测试场景:**
```
├── 游戏逻辑单元测试
├── AI 行为测试
├── 物理系统测试
├── 动画状态机测试
├── UI 交互测试
├── 网络同步测试
├── 存档/加载测试
└── 性能基准测试
```

#### 游戏自动化测试建议

```
🎮 游戏客户端自动化测试框架:

Web 游戏测试:
├── webapp-testing (官方 Playwright ⭐⭐⭐⭐⭐)
├── playwright-mcp (MCP 服务器)
├── Playwright Browser Automation
├── 截图对比工具
└── 视觉回归测试

Unity 测试:
├── Unity Test Framework (内置)
├── cc-plugin-unity-gamedev 测试技能
├── 性能分析工具 (Profiler)
└── 内存泄漏检测 (Memory Profiler)

iOS 游戏测试:
├── iOS Simulator Skill
├── XCUITest 集成
└── 设备农场集成

Android 游戏测试:
├── Android Emulator 集成
├── Espresso UI 测试
└── 设备兼容性测试

测试辅助:
├── test-driven-development
├── pypict-claude-skill (组合测试)
├── test-fixing (失败修复)
└── TDD Guard (Hook 强制)
```

---

### 3.3 测试辅助技能

#### test-fixing ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [mhattingpete/claude-skills-marketplace/test-fixing](https://github.com/mhattingpete/claude-skills-marketplace/tree/main/engineering-workflow-plugin/skills/test-fixing) |
| **功能** | 测试失败修复 |

**流程:**
1. 检测失败测试
2. 分析失败原因
3. 提出修复补丁
4. 验证修复效果

#### review-implementing ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [mhattingpete/claude-skills-marketplace/review-implementing](https://github.com/mhattingpete/claude-skills-marketplace/tree/main/engineering-workflow-plugin/skills/review-implementing) |
| **功能** | 实现计划评审 |

**功能:**
- 代码实现计划评估
- 规格对齐验证
- 最佳实践检查
- 潜在问题预警

#### TDD Guard Hook ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [nizos/tdd-guard](https://github.com/nizos/tdd-guard) |
| **类型** | Hook |
| **功能** | 强制 TDD 原则 |

**功能:**
- 实时监控文件操作
- 阻止违反 TDD 原则的更改
- 测试先行强制执行
- 代码覆盖检查

**安装配置:**
```json
// ~/.claude/settings.json
{
  "hooks": {
    "PreToolUse": ["tdd-guard"]
  }
}
```

---

### 3.4 安全测试技能

#### FFUF Web Fuzzing ⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [jthack/ffuf_claude_skill](https://github.com/jthack/ffuf_claude_skill) |
| **作者** | @jthack |
| **工具** | ffuf fuzzer |

**功能:**
- Web 模糊测试集成
- 漏洞扫描
- 结果分析
- 参数 fuzzing

**游戏服务端测试:**
- API 接口模糊测试
- 参数注入测试
- 边界条件验证
- DDoS 压力测试

#### threat-hunting-with-sigma-rules ⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [jthack/threat-hunting-with-sigma-rules-skill](https://github.com/jthack/threat-hunting-with-sigma-rules-skill) |
| **功能** | Sigma 规则威胁狩猎 |

**功能:**
- Sigma 检测规则应用
- 威胁分析
- 安全事件调查
- 日志分析

---

## 四、开发者工具技能 (深度调研)

### 4.1 开发工作流技能

#### subagent-driven-development ⭐⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [NeoLabHQ/context-engineering-kit/sadd](https://github.com/NeoLabHQ/context-engineering-kit/tree/master/plugins/sadd/skills/subagent-driven-development) |
| **特点** | 独立子代理调度 |

**核心能力:**
- 独立子代理任务分派
- 代码审查检查点
- 迭代间控制
- 快速受控开发
- 并行任务管理

**适用场景:**
- 大型功能开发
- 多模块并行开发
- 复杂重构任务
- 团队协作开发

#### software-architecture ⭐⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [NeoLabHQ/context-engineering-kit/ddd](https://github.com/NeoLabHQ/context-engineering-kit/tree/master/plugins/ddd/skills/software-architecture) |
| **模式** | Clean Architecture + SOLID |

**核心内容:**
- Clean Architecture 实现
- SOLID 原则应用
- 设计模式库
- 架构最佳实践
- DDD 领域驱动设计

#### prompt-engineering ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [NeoLabHQ/context-engineering-kit/prompt-eng](https://github.com/NeoLabHQ/context-engineering-kit/tree/master/plugins/customaize-agent/skills/prompt-engineering) |
| **内容** | 提示工程技巧 |

**核心内容:**
- Anthropic 最佳实践
- Agent 说服原则
- 提示模式库
- 上下文优化

---

### 4.2 Git/版本控制技能

#### using-git-worktrees ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [obra/superpowers/git-worktrees](https://github.com/obra/superpowers/blob/main/skills/using-git-worktrees/) |
| **功能** | Git worktree 管理 |

**功能:**
- 隔离 git worktree 创建
- 智能目录选择
- 安全验证
- 多分支并行开发
- PR 预览分支

**使用场景:**
```bash
# 在 Claude Code 中
/git-worktrees create feature-login
# 自动创建隔离的 worktree

/git-worktrees list
# 列出所有 worktree
```

#### git-pushing ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [mhattingpete/claude-skills-marketplace/git-pushing](https://github.com/mhattingpete/claude-skills-marketplace/tree/main/engineering-workflow-plugin/skills/git-pushing) |
| **功能** | Git 操作自动化 |

**功能:**
- 自动化 git 操作
- 仓库交互
- 提交规范
- 分支管理

---

### 4.3 代码质量技能

#### root-cause-tracing ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [obra/superpowers/root-cause-tracing](https://github.com/obra/superpowers/tree/main/skills/root-cause-tracing) |
| **功能** | 根因追踪 |

**使用场景:**
- 深层执行错误
- 原始触发追踪
- 问题链分析
- Bug 根源定位

#### kaizen (持续改进) ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [NeoLabHQ/context-engineering-kit/kaizen](https://github.com/NeoLabHQ/context-engineering-kit/tree/master/plugins/kaizen/skills/kaizen) |
| **理念** | 日本改善哲学 |

**核心内容:**
- 多分析方法论
- Lean 精益原则
- 持续改进流程
- 效率优化

#### brainstorming ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [obra/superpowers/brainstorming](https://github.com/obra/superpowers/tree/main/skills/brainstorming) |
| **功能** | 结构化头脑风暴 |

**流程:**
1. 粗略想法输入
2. 结构化提问
3. 方案探索
4. 完整设计输出

---

### 4.4 安全技能

#### Computer Forensics Skills ⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [mhattingpete/claude-skills-marketplace/computer-forensics](https://github.com/mhattingpete/claude-skills-marketplace/tree/main/computer-forensics-skills) |
| **技能数** | 3 个 |

**技能列表:**
1. **computer-forensics** - 数字取证分析
2. **file-deletion** - 安全文件删除
3. **metadata-extraction** - 元数据提取分析

#### Trail of Bits 安全技能集 ⭐⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [trailofbits/skills](https://github.com/trailofbits/skills) |
| **官方** | ✅ Trail of Bits |
| **数量** | 20+ 安全技能 |

**核心技能:**
| 技能 | 功能 |
|------|------|
| **static-analysis** | CodeQL + Semgrep + SARIF |
| **variant-analysis** | 漏洞变体分析 |
| **differential-review** | 差异代码审查 |
| **constant-time-analysis** | 时序侧信道检测 |
| **semgrep-rule-creator** | Semgrep 规则创建 |
| **building-secure-contracts** | 智能合约安全 |

---

### 4.5 集成/自动化技能

#### Connect (Composio 1000+ 应用) ⭐⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [ComposioHQ/awesome-claude-skills/connect](https://github.com/ComposioHQ/awesome-claude-skills/blob/master/connect) |
| **应用数** | 1000+ |
| **功能** | 应用连接自动化 |

**支持应用:**
- 📧 Gmail, 📬 Outlook
- 💬 Slack, Discord, Telegram
- 📋 GitHub, GitLab, Jira
- 📝 Notion, Confluence
- 📊 Salesforce, HubSpot
- ☁️ AWS, Azure, GCP
- 更多企业应用

**安装:**
```bash
claude --plugin-dir ./connect-apps-plugin
/connect-apps:setup
# 输入 API 密钥
```

#### jules (Google Jules 集成) ⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [sanjay3290/ai-skills/jules](https://github.com/sanjay3290/ai-skills/tree/main/skills/jules) |
| **作者** | @sanjay3290 |
| **功能** | 任务委托给 Google Jules |

**功能:**
- 异步 Bug 修复
- 文档生成
- 测试编写
- 功能实现
- 代码审查

#### n8n-skills ⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [haunchen/n8n-skills](https://github.com/haunchen/n8n-skills) |
| **功能** | n8n 工作流操作 |

**功能:**
- AI 理解 n8n 工作流
- 直接操作工作流
- 自动化集成
- 流程编排

---

### 4.6 开发者工具推荐组合

```
🔧 开发者工具技能栈:

开发工作流:
├── subagent-driven-development (子代理开发 ⭐⭐⭐⭐⭐)
├── software-architecture (架构设计 ⭐⭐⭐⭐⭐)
└── prompt-engineering (提示工程 ⭐⭐⭐⭐)

版本控制:
├── using-git-worktrees (Git Worktree ⭐⭐⭐⭐)
└── git-pushing (Git 操作 ⭐⭐⭐⭐)

代码质量:
├── root-cause-tracing (根因追踪 ⭐⭐⭐⭐)
├── kaizen (持续改进 ⭐⭐⭐⭐)
└── brainstorming (头脑风暴 ⭐⭐⭐⭐)

安全测试:
├── static-analysis (静态分析 ⭐⭐⭐⭐⭐)
├── property-based-testing (属性测试 ⭐⭐⭐⭐)
└── FFUF Web Fuzzing (模糊测试 ⭐⭐⭐)

集成自动化:
├── Connect (1000+ 应用集成 ⭐⭐⭐⭐⭐)
├── jules (Google Jules ⭐⭐⭐)
└── n8n-skills (工作流 ⭐⭐⭐)
```

---

## 五、总结与建议

### 5.1 调研结论

| 类别 | 推荐技能 | 优先级 |
|------|----------|--------|
| **游戏客户端开发** | web-artifacts-builder, cc-plugin-unity-gamedev, React Native Skills | ⭐⭐⭐⭐⭐ |
| **Python 开发** | MCP Builder, modern-python, test-driven-development | ⭐⭐⭐⭐⭐ |
| **自动化测试** | webapp-testing, Playwright MCP, test-fixing | ⭐⭐⭐⭐ |
| **开发者工具** | Superpowers, subagent-driven-development, Connect | ⭐⭐⭐⭐⭐ |

### 5.2 快速入门推荐

```bash
# 1. 官方核心技能
git clone https://github.com/anthropics/skills.git ~/.claude/skills/

# 2. Superpowers (开发工作流)
git clone https://github.com/obra/superpowers.git ~/.claude/plugins/superpowers

# 3. 游戏开发
git clone https://github.com/tjboudreaux/cc-plugin-unity-gamedev ~/.claude/plugins/

# 4. Python 开发工具链
git clone https://github.com/trailofbits/skills.git ~/.claude/plugins/trailofbits
```

### 5.3 下一步行动

1. **游戏客户端**: 重点关注 web-artifacts-builder + Unity 技能组合
2. **Python 开发**: 采用 modern-python 工具链 + TDD 开发模式
3. **测试**: 使用 webapp-testing + test-fixing 工作流
4. **效率提升**: 部署 Superpowers + subagent-driven-development

---

## 📚 参考资源

- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
- [awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills)
- [anthropics/skills](https://github.com/anthropics/skills)
- [trailofbits/skills](https://github.com/trailofbits/skills)
- [obra/superpowers](https://github.com/obra/superpowers)
- [cc_plugin 仓库](https://github.com/kongshan001/cc_plugin)
