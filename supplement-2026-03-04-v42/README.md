# Claude Code 插件调研 - 第四十二期

> 深度补充调研：游戏客户端开发、Python开发、自动化测试、开发者工具生态

## 调研时间
2026-03-04

## 数据来源
- awesome-claude-code (hesreallyhim)
- VoltAgent/awesome-agent-skills (500+ 官方技能)
- ComposioHQ/awesome-claude-skills (100+ 技能)
- GitHub Topics: claude-code-skills
- 官方团队技能库 (Anthropic, Vercel, Cloudflare, Google, Microsoft 等)

---

## 一、游戏客户端开发技能 (补充)

### 1.1 官方游戏相关技能 (Anthropic)

#### web-artifacts-builder (官方推荐)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [anthropics/skills/web-artifacts-builder](https://github.com/anthropics/skills/tree/main/skills/web-artifacts-builder) |
| **官方** | ✅ Anthropic |
| **技术栈** | React + Tailwind CSS + shadcn/ui |

**核心能力:**
- 多组件 HTML artifacts 构建
- 现代前端技术栈
- WebGL 游戏界面生成
- 响应式设计

**游戏开发适用场景:**
- ✅ WebGL 游戏界面开发
- ✅ HTML5 游戏原型
- ✅ 游戏官网/落地页
- ✅ 游戏配置工具
- ✅ 游戏内嵌 Web 视图

#### algorithmic-art

| 项目 | 说明 |
|-----|------|
| **GitHub** | [anthropics/skills/algorithmic-art](https://github.com/anthropics/skills/tree/main/skills/algorithmic-art) |
| **技术** | p5.js |
| **特点** | 种子随机性 |

**游戏相关用途:**
- 程序化生成图形
- 游戏纹理生成
- 粒子效果设计
- 视觉特效原型
- 着色器效果预览

#### canvas-design

| 项目 | 说明 |
|-----|------|
| **GitHub** | [anthropics/skills/canvas-design](https://github.com/anthropics/skills/tree/main/skills/canvas-design) |
| **输出** | PNG + PDF |

**游戏相关用途:**
- 游戏海报设计
- UI 元素设计
- 图标/Logo 设计
- 宣传物料制作
- 游戏截图美化

#### frontend-design

| 项目 | 说明 |
|-----|------|
| **GitHub** | [anthropics/skills/frontend-design](https://github.com/anthropics/skills/tree/main/skills/frontend-design) |
| **功能** | UI/UX 开发工具 |

**游戏客户端用途:**
- 游戏 UI 系统设计
- 用户体验优化
- 交互原型设计

---

### 1.2 移动端游戏开发技能

#### iOS Simulator Skill

| 项目 | 说明 |
|-----|------|
| **GitHub** | [conorluddy/ios-simulator-skill](https://github.com/conorluddy/ios-simulator-skill) |
| **作者** | @conorluddy |
| **功能** | iOS 模拟器交互 |

**游戏开发用途:**
- iOS 游戏测试
- 手游 UI 调试
- 触控交互验证
- 设备适配测试
- 性能监控

#### React Native Skills (Vercel)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [vercel-labs/agent-skills/react-native-skills](https://github.com/vercel-labs/agent-skills/tree/main/skills/react-native-skills) |
| **官方** | ✅ Vercel |
| **功能** | React Native 最佳实践 |

**游戏开发用途:**
- 跨平台手游开发
- 原生模块集成
- 性能优化指南

#### CallStack React Native Skills

| 项目 | 说明 |
|-----|------|
| **GitHub** | [callstackincubator/agent-skills](https://github.com/callstackincubator/agent-skills) |
| **官方** | ✅ CallStack (React Native 核心团队) |

**技能列表:**
- **react-native-best-practices** - React Native 性能优化
- **upgrading-react-native** - React Native 升级工作流
- **github** - GitHub 工作流模式

---

### 1.3 区块链游戏开发技能

#### Move Code Quality Skill

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

#### Trail of Bits 智能合约安全技能

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

### 1.4 游戏开发完整技能组合

```
游戏客户端开发技能栈推荐:

Unity 开发:
├── cc-plugin-unity-gamedev (21 技能)
├── OH-Unity-GameDev-Skills (DoTween/MediaPipe)
├── unity-ai-workflow (Unity 6.2+)
└── web-artifacts-builder (WebGL 界面)

Unreal 开发:
├── 官方文档 + CLAUDE.md
└── C++ 最佳实践技能

WebGL/HTML5 游戏:
├── web-artifacts-builder (官方)
├── Playwright Browser Automation
├── webapp-testing (官方)
└── frontend-design (官方)

移动端游戏:
├── iOS Simulator Skill
├── React Native Skills (Vercel)
├── CallStack React Native Skills
└── Mobile Optimization

区块链游戏:
├── Move Code Quality Skill
├── building-secure-contracts
├── spec-to-code-compliance
└── Smart Contract 审计技能
```

---

## 二、Python 开发技能 (补充)

### 2.1 官方 Python 技能

#### MCP Builder (官方)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [anthropics/skills/mcp-builder](https://github.com/anthropics/skills/tree/main/skills/mcp-builder) |
| **官方** | ✅ Anthropic |
| **语言** | Python / TypeScript |

**核心能力:**
- 外部 API 集成
- 服务连接指导
- 高质量 MCP 服务器开发
- 工具定义最佳实践
- 错误处理模式

**安装使用:**
```bash
# 复制技能到本地
cp -r mcp-builder ~/.claude/skills/

# 在 Claude Code 中调用
/mcp-builder
```

#### Skill Creator (官方)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [anthropics/skills/skill-creator](https://github.com/anthropics/skills/tree/main/skills/skill-creator) |
| **官方** | ✅ Anthropic |

**功能:**
- 创建 Claude 技能指南
- 技能模板提供
- 最佳实践指导

---

### 2.2 Python 测试技能

#### test-driven-development (Superpowers)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [obra/superpowers/tdd](https://github.com/obra/superpowers/tree/main/skills/test-driven-development) |
| **维护** | Jesse Vincent |
| **Star** | ⭐ 4100+ |

**TDD 流程:**
1. **Red** - 编写失败测试
2. **Green** - 最小实现使测试通过
3. **Refactor** - 重构优化

**使用场景:**
- 任何功能实现前
- Bug 修复前
- 代码重构时

#### pypict-claude-skill (组合测试)

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

#### property-based-testing (Trail of Bits)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [trailofbits/skills/property-based-testing](https://github.com/trailofbits/skills/tree/main/plugins/property-based-testing) |
| **官方** | ✅ Trail of Bits |

**功能:**
- 多语言属性测试
- 智能合约测试
- 模糊测试集成

---

### 2.3 Python 开发工具

#### modern-python (Trail of Bits)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [trailofbits/skills/modern-python](https://github.com/trailofbits/skills/tree/main/plugins/modern-python) |
| **官方** | ✅ Trail of Bits |

**工具链:**
- **uv** - 快速包管理器
- **ruff** - 代码检查
- **ty** - 类型检查
- **pytest** - 测试框架

#### postgres (只读查询)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [sanjay3290/ai-skills/postgres](https://github.com/sanjay3290/ai-skills/tree/main/skills/postgres) |
| **作者** | @sanjay3290 |
| **安全** | 只读操作 |

**功能:**
- 安全的 SQL 查询执行
- 多连接支持
- 深度防御安全机制
- 数据库探索

#### LangSmith Fetch

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

---

### 2.4 Python 推荐技能组合

```
Python 开发技能栈:

基础开发:
├── python-mcp-server (官方)
├── aws-mcp-server (含 Python 规范)
├── MCP Builder (服务集成)
└── modern-python (工具链)

测试开发:
├── test-driven-development
├── pypict-claude-skill (组合测试)
├── property-based-testing
└── postgres (数据库测试)

高级工具:
├── LangSmith Fetch (可观测性)
├── subagent-driven-development
└── software-architecture

代码质量:
├── finishing-a-development-branch
├── root-cause-tracing
└── kaizen (持续改进)
```

---

## 三、游戏客户端自动化测试 (补充)

### 3.1 官方测试技能

#### webapp-testing (Anthropic)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [anthropics/skills/webapp-testing](https://github.com/anthropics/skills/tree/main/skills/webapp-testing) |
| **官方** | ✅ Anthropic |
| **技术** | Playwright |

**核心功能:**
- 本地 Web 应用测试
- 前端功能验证
- UI 行为调试
- 截图捕获

**游戏测试场景:**
- WebGL 游戏功能测试
- HTML5 游戏兼容性
- 游戏内嵌 Web 视图
- 游戏官网测试

**使用示例:**
```bash
# 安装技能
git clone https://github.com/anthropics/skills.git
cp -r skills/webapp-testing ~/.claude/skills/

# 在 Claude Code 中使用
/webapp-testing http://localhost:3000
```

#### Playwright Browser Automation

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

---

### 3.2 测试辅助技能

#### test-fixing

| 项目 | 说明 |
|-----|------|
| **GitHub** | [mhattingpete/claude-skills-marketplace/test-fixing](https://github.com/mhattingpete/claude-skills-marketplace/tree/main/engineering-workflow-plugin/skills/test-fixing) |
| **功能** | 测试失败修复 |

**流程:**
1. 检测失败测试
2. 分析失败原因
3. 提出修复补丁
4. 验证修复效果

#### review-implementing

| 项目 | 说明 |
|-----|------|
| **GitHub** | [mhattingpete/claude-skills-marketplace/review-implementing](https://github.com/mhattingpete/claude-skills-marketplace/tree/main/engineering-workflow-plugin/skills/review-implementing) |
| **功能** | 实现计划评审 |

**功能:**
- 代码实现计划评估
- 规格对齐验证
- 最佳实践检查

#### TDD Guard Hook

| 项目 | 说明 |
|-----|------|
| **GitHub** | [nizos/tdd-guard](https://github.com/nizos/tdd-guard) |
| **类型** | Hook |
| **功能** | 强制 TDD 原则 |

**功能:**
- 实时监控文件操作
- 阻止违反 TDD 原则的更改
- 测试先行强制执行

---

### 3.3 安全测试技能

#### FFUF Web Fuzzing

| 项目 | 说明 |
|-----|------|
| **GitHub** | [jthack/ffuf_claude_skill](https://github.com/jthack/ffuf_claude_skill) |
| **作者** | @jthack |
| **工具** | ffuf fuzzer |

**功能:**
- Web 模糊测试集成
- 漏洞扫描
- 结果分析

**游戏服务端测试:**
- API 接口模糊测试
- 参数注入测试
- 边界条件验证

#### threat-hunting-with-sigma-rules

| 项目 | 说明 |
|-----|------|
| **GitHub** | [jthack/threat-hunting-with-sigma-rules-skill](https://github.com/jthack/threat-hunting-with-sigma-rules-skill) |
| **功能** | Sigma 规则威胁狩猎 |

**功能:**
- Sigma 检测规则应用
- 威胁分析
- 安全事件调查

---

### 3.4 游戏测试框架建议

```
游戏客户端自动化测试框架:

Web 游戏测试:
├── webapp-testing (官方 Playwright)
├── playwright-mcp (MCP 服务器)
├── Playwright Browser Automation
├── FFUF Web Fuzzing (安全)
└── 截图对比工具

Unity 测试:
├── Unity Test Framework (内置)
├── cc-plugin-unity-gamedev 测试技能
├── 性能分析工具
└── 内存泄漏检测

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
├── review-implementing (评审)
└── TDD Guard (Hook 强制)
```

---

## 四、开发者工具技能 (补充)

### 4.1 开发工作流技能

#### subagent-driven-development

| 项目 | 说明 |
|-----|------|
| **GitHub** | [NeoLabHQ/context-engineering-kit/sadd](https://github.com/NeoLabHQ/context-engineering-kit/tree/master/plugins/sadd/skills/subagent-driven-development) |
| **特点** | 独立子代理调度 |

**核心能力:**
- 独立子代理任务分派
- 代码审查检查点
- 迭代间控制
- 快速受控开发

**适用场景:**
- 大型功能开发
- 多模块并行开发
- 复杂重构任务

#### software-architecture

| 项目 | 说明 |
|-----|------|
| **GitHub** | [NeoLabHQ/context-engineering-kit/ddd](https://github.com/NeoLabHQ/context-engineering-kit/tree/master/plugins/ddd/skills/software-architecture) |
| **模式** | Clean Architecture + SOLID |

**核心内容:**
- Clean Architecture 实现
- SOLID 原则应用
- 设计模式库
- 架构最佳实践

#### prompt-engineering

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

#### using-git-worktrees

| 项目 | 说明 |
|-----|------|
| **GitHub** | [obra/superpowers/git-worktrees](https://github.com/obra/superpowers/blob/main/skills/using-git-worktrees/) |
| **功能** | Git worktree 管理 |

**功能:**
- 隔离 git worktree 创建
- 智能目录选择
- 安全验证
- 多分支并行开发

#### git-pushing

| 项目 | 说明 |
|-----|------|
| **GitHub** | [mhattingpete/claude-skills-marketplace/git-pushing](https://github.com/mhattingpete/claude-skills-marketplace/tree/main/engineering-workflow-plugin/skills/git-pushing) |
| **功能** | Git 操作自动化 |

**功能:**
- 自动化 git 操作
- 仓库交互
- 提交规范

---

### 4.3 代码质量技能

#### root-cause-tracing

| 项目 | 说明 |
|-----|------|
| **GitHub** | [obra/superpowers/root-cause-tracing](https://github.com/obra/superpowers/tree/main/skills/root-cause-tracing) |
| **功能** | 根因追踪 |

**使用场景:**
- 深层执行错误
- 原始触发追踪
- 问题链分析

#### kaizen (持续改进)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [NeoLabHQ/context-engineering-kit/kaizen](https://github.com/NeoLabHQ/context-engineering-kit/tree/master/plugins/kaizen/skills/kaizen) |
| **理念** | 日本改善哲学 |

**核心内容:**
- 多分析方法论
- Lean 精益原则
- 持续改进流程

#### brainstorming

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

#### Computer Forensics Skills

| 项目 | 说明 |
|-----|------|
| **GitHub** | [mhattingpete/claude-skills-marketplace/computer-forensics](https://github.com/mhattingpete/claude-skills-marketplace/tree/main/computer-forensics-skills) |
| **技能数** | 3 个 |

**技能列表:**
1. **computer-forensics** - 数字取证分析
2. **file-deletion** - 安全文件删除
3. **metadata-extraction** - 元数据提取分析

#### Trail of Bits 安全技能集

| 项目 | 说明 |
|-----|------|
| **GitHub** | [trailofbits/skills](https://github.com/trailofbits/skills) |
| **官方** | ✅ Trail of Bits |
| **数量** | 20+ 安全技能 |

**核心技能:**
- **static-analysis** - CodeQL + Semgrep + SARIF
- **variant-analysis** - 漏洞变体分析
- **differential-review** - 差异代码审查
- **constant-time-analysis** - 时序侧信道检测
- **semgrep-rule-creator** - Semgrep 规则创建

---

### 4.5 集成/自动化技能

#### Connect (Composio 1000+ 应用)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [ComposioHQ/awesome-claude-skills/connect](https://github.com/ComposioHQ/awesome-claude-skills/blob/master/connect) |
| **应用数** | 1000+ |
| **功能** | 应用连接自动化 |

**支持应用:**
- Gmail, Slack, GitHub
- Notion, Jira, Linear
- Salesforce, HubSpot
- 更多企业应用

**安装:**
```bash
claude --plugin-dir ./connect-apps-plugin
/connect-apps:setup
# 输入 API 密钥
```

#### jules (Google Jules 集成)

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

#### n8n-skills

| 项目 | 说明 |
|-----|------|
| **GitHub** | [haunchen/n8n-skills](https://github.com/haunchen/n8n-skills) |
| **功能** | n8n 工作流操作 |

**功能:**
- AI 理解 n8n 工作流
- 直接操作工作流
- 自动化集成

---

## 五、官方团队技能汇总

### 5.1 Anthropic 官方技能

| 技能 | 功能 |
|-----|------|
| docx | Word 文档创建/编辑 |
| pptx | PowerPoint 演示文稿 |
| xlsx | Excel 电子表格 |
| pdf | PDF 处理 |
| web-artifacts-builder | HTML artifacts 构建 |
| webapp-testing | Web 应用测试 |
| mcp-builder | MCP 服务器开发 |
| skill-creator | 技能创建指南 |
| algorithmic-art | 生成式艺术 |
| canvas-design | 视觉设计 |
| frontend-design | 前端设计 |

### 5.2 Vercel 官方技能

| 技能 | 功能 |
|-----|------|
| react-best-practices | React 最佳实践 |
| next-best-practices | Next.js 最佳实践 |
| next-cache-components | Next.js 缓存组件 |
| next-upgrade | Next.js 升级指南 |
| react-native-skills | React Native 开发 |
| vercel-deploy-claimable | Vercel 部署 |
| web-design-guidelines | Web 设计指南 |
| composition-patterns | 组合模式 |

### 5.3 Cloudflare 官方技能

| 技能 | 功能 |
|-----|------|
| agents-sdk | AI Agent 开发 |
| building-mcp-server-on-cloudflare | MCP 服务器 |
| durable-objects | 有状态对象 |
| web-perf | Web 性能优化 |
| wrangler | Cloudflare Workers 部署 |

### 5.4 Google 官方技能

| 技能 | 功能 |
|-----|------|
| gemini-skills | Gemini API/SDK |
| design-md | DESIGN.md 管理 |
| enhance-prompt | 提示词增强 |
| react-components | React 组件转换 |
| shadcn-ui | UI 组件构建 |

### 5.5 Microsoft Azure 技能

| 技能 | 功能 |
|-----|------|
| azure-ai-agents-persistent | 持久化 AI Agent |
| azure-ai-openai | OpenAI 集成 |
| azure-cosmos | Cosmos DB |
| azure-eventhub | 事件流处理 |
| azure-identity | 身份认证 |

---

## 六、技能安装指南

### 6.1 通用安装方法

```bash
# 方法 1: 直接克隆
git clone https://github.com/<org>/<repo>.git ~/.claude/skills/<name>

# 方法 2: 复制单个技能
cp -r /path/to/skill ~/.claude/skills/

# 方法 3: 使用符号链接
ln -s /path/to/skill ~/.claude/skills/<name>
```

### 6.2 MCP 服务器安装

```bash
# 使用 npx
npx -y @anthropic-ai/mcp-server-<name>

# 使用 uvx
uvx mcp-server-<name>

# 配置 claude_desktop_config.json
{
  "mcpServers": {
    "<name>": {
      "command": "npx",
      "args": ["-y", "@anthropic-ai/mcp-server-<name>"]
    }
  }
}
```

### 6.3 技能验证

```bash
# 检查技能是否加载
ls ~/.claude/skills/

# 在 Claude Code 中测试
claude
> /<skill-name>
```

---

## 七、总结与推荐

### 7.1 技能推荐 (按优先级)

| 优先级 | 技能 | 用途 |
|--------|------|------|
| ⭐⭐⭐⭐⭐ | Superpowers | 核心工程技能 |
| ⭐⭐⭐⭐⭐ | python-mcp-server | Python 开发 |
| ⭐⭐⭐⭐⭐ | webapp-testing | Web 测试 |
| ⭐⭐⭐⭐⭐ | Connect (Composio) | 应用集成 |
| ⭐⭐⭐⭐⭐ | Claude Code Game Studios | 游戏开发 |
| ⭐⭐⭐⭐ | Trail of Bits | 安全审计 |
| ⭐⭐⭐⭐ | test-driven-development | TDD |
| ⭐⭐⭐ | subagent-driven-development | 高级开发 |
| ⭐⭐⭐ | software-architecture | 架构设计 |

### 7.2 学习路径

```
入门 (第 1 周):
├── Superpowers 基础技能
├── python-mcp-server 安装
└── webapp-testing 体验

进阶 (第 2-3 周):
├── TDD 实践
├── Git worktrees 使用
├── Connect 应用集成
└── 游戏开发技能 (如需要)

高级 (第 4 周+):
├── subagent-driven-development
├── software-architecture
├── 自定义技能开发
└── MCP 服务器开发
```

### 7.3 注意事项

1. **安全审查**: 第三方技能需检查代码
2. **版本兼容**: 确认 Claude Code 版本
3. **依赖管理**: 注意技能依赖项
4. **社区活跃度**: 优先选择活跃项目

---

## 参考链接

- [anthropics/skills](https://github.com/anthropics/skills) - 官方技能库
- [ComposioHQ/awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills)
- [VoltAgent/awesome-agent-skills](https://github.com/VoltAgent/awesome-agent-skills)
- [NeoLabHQ/context-engineering-kit](https://github.com/NeoLabHQ/context-engineering-kit)
- [obra/superpowers](https://github.com/obra/superpowers)
- [trailofbits/skills](https://github.com/trailofbits/skills)
- [vercel-labs/agent-skills](https://github.com/vercel-labs/agent-skills)
