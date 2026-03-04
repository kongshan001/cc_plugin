# Claude Code 插件调研 - 第四十一期

> 深度调研：游戏客户端开发、Python开发、自动化测试、开发者工具

## 调研时间
2026-03-04

## 数据来源
- awesome-claude-code (hesreallyhim)
- ComposioHQ/awesome-claude-skills (100+技能)
- VoltAgent/awesome-agent-skills (500+技能)
- GitHub Topics: claude-code-skills

---

## 一、游戏客户端开发技能 (深度)

### 1.1 官方游戏开发技能 (Anthropic)

#### web-artifacts-builder

| 项目 | 说明 |
|-----|------|
| **GitHub** | [anthropics/skills/web-artifacts-builder](https://github.com/anthropics/skills/tree/main/skills/web-artifacts-builder) |
| **官方** | ✅ Anthropic |
| **技术栈** | React + Tailwind CSS + shadcn/ui |

**核心能力:**
- 多组件 HTML artifacts 构建
- 现代前端技术栈
- 游戏UI界面生成
- 响应式设计

**适用场景:**
- ✅ WebGL 游戏界面
- ✅ HTML5 游戏开发
- ✅ 游戏官网/落地页
- ✅ 游戏配置工具

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

#### canvas-design

| 项目 | 说明 |
|-----|------|
| **GitHub** | [anthropics/skills/canvas-design](https://github.com/anthropics/skills/tree/main/skills/canvas-design) |
| **输出** | PNG + PDF |

**游戏相关用途:**
- 游戏海报设计
- UI元素设计
- 图标/Logo设计
- 宣传物料制作

---

### 1.2 社区游戏开发技能

#### iOS Simulator Skill

| 项目 | 说明 |
|-----|------|
| **GitHub** | [conorluddy/ios-simulator-skill](https://github.com/conorluddy/ios-simulator-skill) |
| **作者** | @conorluddy |
| **功能** | iOS模拟器交互 |

**游戏开发用途:**
- iOS游戏测试
- 手游UI调试
- 触控交互验证
- 设备适配测试

#### Move Code Quality Skill

| 项目 | 说明 |
|-----|------|
| **GitHub** | [1NickPappas/move-code-quality-skill](https://github.com/1NickPappas/move-code-quality-skill) |
| **语言** | Move (Sui/Aptos) |
| **用途** | 链游开发 |

**功能:**
- Move 代码质量分析
- Move 2024 Edition 合规检查
- 最佳实践验证

---

### 1.3 游戏开发推荐技能组合

```
游戏客户端开发技能栈:

Unity 开发:
├── cc-plugin-unity-gamedev (21技能)
├── OH-Unity-GameDev-Skills (DoTween/MediaPipe)
└── unity-ai-workflow (Unity 6.2+)

Unreal 开发:
├── 官方文档 + CLAUDE.md
└── C++最佳实践技能

WebGL/HTML5:
├── web-artifacts-builder (官方)
├── Playwright Browser Automation
└── webapp-testing (官方)

移动端:
├── iOS Simulator Skill
├── react-native-skills (Vercel)
└── Mobile Optimization

区块链游戏:
├── Move Code Quality Skill
├── solana-game-skill
└── Smart Contract 审计技能
```

---

## 二、Python 开发技能 (深度)

### 2.1 官方Python技能

#### MCP Builder

| 项目 | 说明 |
|-----|------|
| **GitHub** | [anthropics/skills/mcp-builder](https://github.com/anthropics/skills/tree/main/skills/mcp-builder) |
| **语言** | Python / TypeScript |
| **功能** | MCP服务器创建指南 |

**核心能力:**
- 外部API集成
- 服务连接指导
- 高质量MCP服务器开发
- 工具定义最佳实践

**安装使用:**
```bash
# 复制技能到本地
cp -r mcp-builder ~/.claude/skills/

# 在Claude Code中调用
/mcp-builder
```

#### postgres (只读查询)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [sanjay3290/ai-skills/postgres](https://github.com/sanjay3290/ai-skills/tree/main/skills/postgres) |
| **作者** | @sanjay3290 |
| **安全** | 只读操作 |

**功能:**
- 安全的SQL查询执行
- 多连接支持
- 深度防御安全机制
- 数据库探索

---

### 2.2 Python测试技能

#### test-driven-development (Superpowers)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [obra/superpowers/tdd](https://github.com/obra/superpowers/tree/main/skills/test-driven-development) |
| **维护** | Jesse Vincent |
| **Star** | ⭐ 4100+ |

**TDD流程:**
1. 编写失败测试 (Red)
2. 最小实现 (Green)
3. 重构优化 (Refactor)

**使用场景:**
- 任何功能实现前
- Bug修复前
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

---

### 2.3 Python开发工具

#### LangSmith Fetch

| 项目 | 说明 |
|-----|------|
| **GitHub** | [ComposioHQ/awesome-claude-skills/langsmith-fetch](https://github.com/ComposioHQ/awesome-claude-skills/blob/master/langsmith-fetch) |
| **作者** | @OthmanAdi |
| **特点** | 首个AI可观测性技能 |

**功能:**
- LangChain/LangGraph 调试
- 执行追踪获取
- LangSmith Studio 集成
- Agent性能分析

#### finishing-a-development-branch

| 项目 | 说明 |
|-----|------|
| **GitHub** | [obra/superpowers/finishing-branch](https://github.com/obra/superpowers/tree/main/skills/finishing-a-development-branch) |
| **功能** | 开发分支完成指南 |

**流程:**
1. 呈现清晰选项
2. 处理选定工作流
3. 代码审查准备
4. 合并前检查

---

### 2.4 Python推荐技能组合

```
Python开发技能栈:

基础开发:
├── python-mcp-server (官方)
├── aws-mcp-server (含Python规范)
└── MCP Builder (服务集成)

测试开发:
├── test-driven-development
├── pypict-claude-skill (组合测试)
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

## 三、游戏客户端自动化测试 (深度)

### 3.1 官方测试技能

#### webapp-testing (Anthropic)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [anthropics/skills/webapp-testing](https://github.com/anthropics/skills/tree/main/skills/webapp-testing) |
| **官方** | ✅ Anthropic |
| **技术** | Playwright |

**核心功能:**
- 本地Web应用测试
- 前端功能验证
- UI行为调试
- 截图捕获

**游戏测试场景:**
- WebGL游戏功能测试
- HTML5游戏兼容性
- 游戏内嵌Web视图
- 游戏官网测试

**使用示例:**
```bash
# 安装技能
git clone https://github.com/anthropics/skills.git
cp -r skills/webapp-testing ~/.claude/skills/

# 在Claude Code中使用
/webapp-testing http://localhost:3000
```

#### Playwright Browser Automation

| 项目 | 说明 |
|-----|------|
| **GitHub** | [lackeyjb/playwright-skill](https://github.com/lackeyjb/playwright-skill) |
| **作者** | @lackeyjb |
| **类型** | 模型调用自动化 |

**功能:**
- 模型触发的Playwright自动化
- Web应用测试验证
- 浏览器交互模拟

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

---

### 3.3 游戏测试框架建议

```
游戏客户端自动化测试框架:

Web游戏测试:
├── webapp-testing (官方Playwright)
├── playwright-mcp (MCP服务器)
├── Playwright Browser Automation
└── 截图对比工具

Unity测试:
├── Unity Test Framework (内置)
├── cc-plugin-unity-gamedev 测试技能
└── 性能分析工具

iOS游戏测试:
├── iOS Simulator Skill
├── XCUITest 集成
└── 设备农场集成

Android游戏测试:
├── Android Emulator 集成
├── Espresso UI测试
└── 设备兼容性测试

测试辅助:
├── test-driven-development
├── pypict-claude-skill (组合测试)
├── test-fixing (失败修复)
└── review-implementing (评审)
```

---

## 四、开发者工具技能 (深度)

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
- Anthropic最佳实践
- Agent说服原则
- 提示模式库
- 上下文优化

---

### 4.2 Git/版本控制技能

#### using-git-worktrees

| 项目 | 说明 |
|-----|------|
| **GitHub** | [obra/superpowers/git-worktrees](https://github.com/obra/superpowers/blob/main/skills/using-git-worktrees/) |
| **功能** | Git worktree管理 |

**功能:**
- 隔离git worktree创建
- 智能目录选择
- 安全验证
- 多分支并行开发

#### git-pushing

| 项目 | 说明 |
|-----|------|
| **GitHub** | [mhattingpete/claude-skills-marketplace/git-pushing](https://github.com/mhattingpete/claude-skills-marketplace/tree/main/engineering-workflow-plugin/skills/git-pushing) |
| **功能** | Git操作自动化 |

**功能:**
- 自动化git操作
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

#### FFUF Web Fuzzing

| 项目 | 说明 |
|-----|------|
| **GitHub** | [jthack/ffuf_claude_skill](https://github.com/jthack/ffuf_claude_skill) |
| **作者** | @jthack |
| **工具** | ffuf fuzzer |

**功能:**
- Web模糊测试集成
- 漏洞扫描
- 结果分析

#### threat-hunting-with-sigma-rules

| 项目 | 说明 |
|-----|------|
| **GitHub** | [jthack/threat-hunting-with-sigma-rules-skill](https://github.com/jthack/threat-hunting-with-sigma-rules-skill) |
| **功能** | Sigma规则威胁狩猎 |

**功能:**
- Sigma检测规则应用
- 威胁分析
- 安全事件调查

#### Computer Forensics Skills

| 项目 | 说明 |
|-----|------|
| **GitHub** | [mhattingpete/claude-skills-marketplace/computer-forensics](https://github.com/mhattingpete/claude-skills-marketplace/tree/main/computer-forensics-skills) |
| **技能数** | 3个 |

**技能列表:**
1. **computer-forensics** - 数字取证分析
2. **file-deletion** - 安全文件删除
3. **metadata-extraction** - 元数据提取分析

---

### 4.5 集成/自动化技能

#### Connect (Composio 1000+应用)

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
# 输入API密钥
```

#### jules (Google Jules集成)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [sanjay3290/ai-skills/jules](https://github.com/sanjay3290/ai-skills/tree/main/skills/jules) |
| **作者** | @sanjay3290 |
| **功能** | 任务委托给Google Jules |

**功能:**
- 异步Bug修复
- 文档生成
- 测试编写
- 功能实现

#### n8n-skills

| 项目 | 说明 |
|-----|------|
| **GitHub** | [haunchen/n8n-skills](https://github.com/haunchen/n8n-skills) |
| **功能** | n8n工作流操作 |

**功能:**
- AI理解n8n工作流
- 直接操作工作流
- 自动化集成

---

## 五、SaaS应用自动化技能

### 5.1 CRM & 销售

| 技能 | 功能 |
|-----|------|
| **Close Automation** | 线索、联系人、商机、活动 |
| **HubSpot Automation** | 联系人、交易、公司、工单 |
| **Pipedrive Automation** | 交易、联系人、组织、活动 |
| **Salesforce Automation** | 对象、记录、SOQL查询 |
| **Zoho CRM Automation** | 线索、联系人、交易、账户 |

### 5.2 项目管理

| 技能 | 功能 |
|-----|------|
| **Asana Automation** | 任务、项目、分区、分配 |
| **Basecamp Automation** | 待办列表、消息、人员 |
| **ClickUp Automation** | 任务、列表、空间、目标 |
| **Jira Automation** | 问题、项目、看板、冲刺 |
| **Linear Automation** | 问题、项目、团队、周期 |

### 5.3 开发工具

| 技能 | 功能 |
|-----|------|
| **GitHub Automation** | 仓库、Issue、PR、Actions |
| **GitLab Automation** | 项目、MR、Pipeline |
| **Bitbucket Automation** | 仓库、PR、Pipeline |

---

## 六、技能安装指南

### 6.1 通用安装方法

```bash
# 方法1: 直接克隆
git clone https://github.com/<org>/<repo>.git ~/.claude/skills/<name>

# 方法2: 复制单个技能
cp -r /path/to/skill ~/.claude/skills/

# 方法3: 使用符号链接
ln -s /path/to/skill ~/.claude/skills/<name>
```

### 6.2 MCP服务器安装

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

# 在Claude Code中测试
claude
> /<skill-name>
```

---

## 七、总结与推荐

### 7.1 技能推荐 (按优先级)

| 优先级 | 技能 | 用途 |
|--------|------|------|
| ⭐⭐⭐⭐⭐ | Superpowers | 核心工程技能 |
| ⭐⭐⭐⭐⭐ | python-mcp-server | Python开发 |
| ⭐⭐⭐⭐⭐ | webapp-testing | Web测试 |
| ⭐⭐⭐⭐⭐ | Connect (Composio) | 应用集成 |
| ⭐⭐⭐⭐ | Claude Code Game Studios | 游戏开发 |
| ⭐⭐⭐⭐ | test-driven-development | TDD |
| ⭐⭐⭐⭐ | Trail of Bits | 安全审计 |
| ⭐⭐⭐ | subagent-driven-development | 高级开发 |
| ⭐⭐⭐ | software-architecture | 架构设计 |

### 7.2 学习路径

```
入门 (第1周):
├── Superpowers 基础技能
├── python-mcp-server 安装
└── webapp-testing 体验

进阶 (第2-3周):
├── TDD 实践
├── Git worktrees 使用
├── Connect 应用集成
└── 游戏开发技能 (如需要)

高级 (第4周+):
├── subagent-driven-development
├── software-architecture
├── 自定义技能开发
└── MCP服务器开发
```

### 7.3 注意事项

1. **安全审查**: 第三方技能需检查代码
2. **版本兼容**: 确认Claude Code版本
3. **依赖管理**: 注意技能依赖项
4. **社区活跃度**: 优先选择活跃项目

---

## 参考链接

- [anthropics/skills](https://github.com/anthropics/skills) - 官方技能库
- [ComposioHQ/awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills)
- [VoltAgent/awesome-agent-skills](https://github.com/VoltAgent/awesome-agent-skills)
- [NeoLabHQ/context-engineering-kit](https://github.com/NeoLabHQ/context-engineering-kit)
- [obra/superpowers](https://github.com/obra/superpowers)
