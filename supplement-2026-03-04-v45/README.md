# Claude Code 插件调研 - 第四十五期

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

## 一、本期新增热门插件 (精选)

### 1.1 科学研究技能集

#### Claude Scientific Skills ⭐⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [K-Dense-AI/claude-scientific-skills](https://github.com/K-Dense-AI/claude-scientific-skills) |
| **维护** | K-Dense AI |
| **评价** | "这是 GitHub 上最好的技能仓库之一" - awesome-claude-code |

**核心能力:**
- 研究技能
- 科学分析技能
- 工程技能
- 金融分析技能
- 写作技能

**适用场景:**
| 场景 | 适用性 |
|------|--------|
| 学术研究 | ✅ 非常适合 |
| 数据分析 | ✅ 非常适合 |
| 工程计算 | ✅ 适合 |
| 金融建模 | ✅ 适合 |
| 技术写作 | ✅ 适合 |

**安装:**
```bash
git clone https://github.com/K-Dense-AI/claude-scientific-skills ~/.claude/plugins/scientific
```

---

### 1.2 安全与权限管理

#### parry (提示注入扫描器) ⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [vaporif/parry](https://github.com/vaporif/parry) |
| **作者** | @Dmytro Onypko |
| **功能** | 提示注入攻击检测 |

**核心功能:**
- 扫描工具输入/输出中的注入攻击
- 敏感信息检测
- 数据泄露防护
- Claude Code Hook 集成

**安全场景:**
| 功能 | 描述 |
|------|------|
| 提示注入检测 | 识别恶意指令注入 |
| 密钥扫描 | 检测意外泄露的 API 密钥 |
| 数据外泄防护 | 阻止敏感信息输出 |

**注意:** 早期开发阶段，值得关注。

#### Dippy (智能命令批准) ⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [ldayton/Dippy](https://github.com/ldayton/Dippy) |
| **作者** | @Lily Dayton |
| **功能** | AST 解析自动批准安全命令 |

**核心功能:**
- AST-based 解析，智能识别安全命令
- 自动批准安全 bash 命令
- 危险操作提示确认
- 支持 Claude Code、Gemini CLI、Cursor

**解决的问题:**
- 权限疲劳 (permission fatigue)
- 不禁用安全检查的前提下提高效率

**安装:**
```bash
# 安装 Dippy
npm install -g dippy

# 配置 Hook
# 在 ~/.claude/settings.json 中配置
```

---

### 1.3 开发工具增强

#### sudocode ⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [sudocode-ai/sudocode](https://github.com/sudocode-ai/sudocode) |
| **作者** | @ssh-randy |
| **类型** | 轻量级 Agent 编排开发工具 |

**核心功能:**
- 集成多种规范框架
- 类似 Jira 的任务管理
- 轻量级工作流编排
- 仓库内直接运行

**适用场景:**
- 小型团队项目管理
- 敏捷开发流程
- 任务拆分与追踪

#### claude-tmux ⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [nielsgroen/claude-tmux](https://github.com/nielsgroen/claude-tmux) |
| **作者** | @Niels Groeneveld |
| **功能** | tmux 中的 Claude Code 管理 |

**核心功能:**
- tmux 弹出窗口显示所有 Claude Code 实例
- 快速切换
- 状态监控
- 会话生命周期管理
- Git worktree 和 PR 支持

**使用场景:**
```bash
# 在 tmux 中使用
Ctrl+b :new-session -s claude
claude-tmux list
```

#### claude-esp ⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [phiat/claude-esp](https://github.com/phiat/claude-esp) |
| **作者** | @phiat |
| **类型** | Go-based TUI |

**核心功能:**
- 流式输出 Claude Code 隐藏内容 (thinking、tool calls、subagents)
- 同时监控多个会话
- 按内容类型过滤
- 后台任务跟踪

**适用场景:**
- 调试 agent 行为
- 理解 Claude 幕后工作
- 不干扰主会话的情况下监控

---

### 1.4 代码生成与分析

#### Codex Skill ⭐⭐⭐⭐

| 项目 |说明 |
|-----|------|
| **GitHub** | [skills-directory/skill-codex](https://github.com/skills-directory/skill-codex) |
| **作者** | @klaudworks |

**核心功能:**
- 从 Claude Code 调用 Codex
- 自动推断模型参数
- 推理 effort 参数
- 沙箱配置
- 简化会话继续

**与 MCP 区别:**
- 比原始 Codex MCP 服务器更智能
- 自动参数推断
- 更简洁的会话管理

#### Claude Code Agents ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [undeadlist/claude-code-agents](https://github.com/undeadlist/claude-code-agents) |
| **作者** | @Paul - UndeadList |
| **类型** | 全栈 E2E 开发工作流 |

**核心功能:**
- 多个审计器并行运行
- 微检查点协议自动化修复循环
- 基于浏览器的 QA
- 严格协议防止 AI 失控

**适用场景:**
- Solo 开发者
- 小团队开发
- 代码质量保证

---

### 1.5 全栈开发

#### Fullstack Dev Skills ⭐⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [jeffallan/claude-skills](https://github.com/jeffallan/claude-skills) |
| **技能数** | 65+ 专业技能 |
| **特点** | 9 个项目工作流命令 |

**技能覆盖:**
| 类别 | 技能数 |
|------|--------|
| 前端框架 | 15+ |
| 后端框架 | 15+ |
| 数据库 | 10+ |
| DevOps | 10+ |
| 测试 | 10+ |
| 其他 | 5+ |

**工作流命令:**
- Jira 集成
- Confluence 集成
- /common-ground 命令 (上下文假设可视化)

**安装:**
```bash
git clone https://github.com/jeffallan/claude-skills ~/.claude/plugins/fullstack
```

#### cc-devops-skills ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [akin-ozer/cc-devops-skills](https://github.com/akin-ozer/cc-devops-skills) |
| **作者** | @akin-ozer |
| **类型** | DevOps 工程师技能集 |

**核心功能:**
- 验证器
- 生成器
- Shell 脚本
- CLI 工具

**支持平台:**
- AWS
- Azure
- GCP
- Kubernetes
- Docker
- 更多云平台

**特点:**
- 即使只作为文档参考也值得下载
- 极其详细的 IaC 代码生成

---

## 二、Python 开发补充技能

### 2.1 数据库技能

#### read-only-postgres (补充) ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [jawwadfirdousi/agent-skills](https://github.com/jawwadfirdousi/agent-skills) |
| **安全** | 只读操作 ✅ |

**高级功能:**
- 多连接支持
- 深度防御安全机制
- 查询超时保护
- 行数限制
- EXPLAIN 分析

**Python 测试应用:**
```python
# 在 Python 测试中使用
SELECT * FROM users WHERE id = 1;
EXPLAIN ANALYZE SELECT * FROM orders WHERE status = 'pending';
```

---

### 2.2 现代化 Python 工具链

#### modern-python (Trail of Bits) ⭐⭐⭐⭐

**补充工具:**

| 工具 | 用途 | 速度 |
|------|------|------|
| **uv** | 包管理器 (Rust) | 比 pip 快 10-100x |
| **ruff** | 代码检查 | 比 flake8 快 10-100x |
| **ty** | 类型检查 | 比 mypy 快 |
| **pytest** | 测试 | 标准 |
| **coverage** | 覆盖率 | 标准 |

**安装:**
```bash
# uv (极速包管理)
curl -LsSf https://astral.sh/uv/install.sh | sh

# ruff (极速检查)
pip install ruff

# ty (极速类型检查)
pip install ty

# 使用示例
uv pip install -r requirements.txt
ruff check .
ty check .
pytest --cov=.
```

---

## 三、游戏客户端开发补充

### 3.1 Web 游戏开发

#### web-artifacts-builder (补充) ⭐⭐⭐⭐⭐

**游戏开发高级场景:**

| 场景 | 适用性 | 详细说明 |
|------|--------|----------|
| WebGL 游戏界面 | ✅ 高度适合 | React 组件生态完整 |
| HTML5 游戏原型 | ✅ 适合 | 快速迭代 |
| 游戏官网/落地页 | ✅ 非常适合 | 现代前端技术栈 |
| 游戏内嵌 Web 视图 | ✅ 适合 | WebView 对接 |
| 游戏配置工具 | ✅ 非常适合 | 表单+数据管理 |
| 游戏商城/商店 | ✅ 非常适合 | 电商功能 |
| 多人游戏大厅 | ✅ 适合 | 实时通信 |

**高级功能:**
- 多组件 artifacts 构建
- 现代前端技术栈完整支持
- WebGL 游戏界面生成
- 响应式设计系统
- 可交互 UI 组件

---

### 3.2 移动游戏开发补充

#### iOS Simulator Skill (补充) ⭐⭐⭐

**游戏测试高级功能:**

| 功能 | 描述 |
|------|------|
| iOS 游戏测试 | 模拟器内运行测试 |
| 手游 UI 调试 | 实时 UI 层级检查 |
| 触控交互验证 | 模拟各种触控手势 |
| 设备适配测试 | 多分辨率/设备模拟 |
| 性能监控 | FPS/内存实时监控 |
| 截图/录屏 | 游戏表现记录 |

**使用示例:**
```bash
# 安装技能
git clone https://github.com/conorluddy/ios-simulator-skill ~/.claude/skills/

# 使用
/ios-simulator list-devices
/ios-simulator launch "MyGame.app"
/ios-simulator capture-screenshot
```

---

## 四、开发者工具补充

### 4.1 编排与自动化

#### AgentSys (补充) ⭐⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [avifenesh/agentsys](https://github.com/avifenesh/agentsys) |
| **代码行数** | 数千行 |
| **测试数** | 数千个 |

**补充功能:**
- 任务到生产工作流自动化
- PR 管理
- 代码清理
- 性能调查
- 漂移检测
- 多代理代码审查

**技术特点:**
- 确定式检测 (regex、AST)
- LLM 判断提高效率
- 生产系统验证

#### Agentic Workflow Patterns ⭐⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [ThibautMelen/agentic-workflow-patterns](https://github.com/ThibautMelen/agentic-workflow-patterns) |

**模式库:**
- Subagent 编排
- Progressive Skills
- Parallel Tool Calling
- Master-Clone 架构
- Wizard 工作流

**特点:**
- Anthropic 文档模式集合
- Mermaid 图表
- 代码示例
- 其他 provider 兼容

---

### 4.2 项目管理

#### Claude Code PM ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [automazeio/ccpm](https://github.com/ranaroussi/ccpm) |
| **作者** | @Ran Aroussi |
| **类型** | 项目管理综合工作流 |

**功能:**
- 多个专业代理
- 强 slash 命令
- 完整文档

#### Simone ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [Helmi/claude-simone](https://github.com/Helmi/claude-simone) |
| **类型** | 广义项目管理 |

**包含:**
- 命令集
- 文档
- 指南
- 流程

---

### 4.3 Claude Code 增强工具

#### Claude Code Tips ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [ykdojo/claude-code-tips](https://github.com/ykdojo/claude-code-tips) |
| **技巧数** | 35+ |

**技巧类别:**
- 语音输入
- System prompt 补丁
- 容器工作流
- 会话克隆
- 多模型编排
- 更多

**亮点:**
- 演示示例
- 工作脚本
- 插件

#### claude-code-docs ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [costiash/claude-code-docs](https://github.com/costiash/claude-code-docs) |
| **功能** | Anthropic 文档镜像 + 增强 |

**增强功能:**
- 全文搜索
- 查询时更新
- 完整索引

---

## 五、本期推荐技能组合

### 5.1 游戏开发推荐

```
🎮 游戏客户端开发完整技能栈:

Web/HTML5 游戏:
├── web-artifacts-builder (官方 ⭐⭐⭐⭐⭐)
├── Playwright Browser Automation
├── webapp-testing (官方)
└── frontend-design (官方)

Unity 开发:
├── cc-plugin-unity-gamedev (21 技能)
├── Unity Test Framework
└── 性能分析工具

移动端游戏:
├── iOS Simulator Skill
├── React Native Skills (Vercel)
└── Android Emulator 集成

区块链游戏:
├── Move Code Quality Skill
└── building-secure-contracts
```

### 5.2 Python 开发推荐

```
🐍 Python 开发完整技能栈:

基础开发:
├── Claude Scientific Skills (⭐⭐⭐⭐⭐)
├── modern-python (工具链 ⭐⭐⭐⭐)
└── MCP Builder (服务集成)

测试:
├── test-driven-development (TDD ⭐⭐⭐⭐⭐)
├── pypict-claude-skill (组合测试)
└── property-based-testing (属性测试)

数据库:
├── read-only-postgres (只读查询)
└── PostgreSQL 测试技能
```

### 5.3 开发者工具推荐

```
🔧 开发者工具完整技能栈:

开发工作流:
├── AgentSys (工作流自动化 ⭐⭐⭐⭐⭐)
├── Agentic Workflow Patterns (模式库 ⭐⭐⭐⭐⭐)
├── Claude Code Agents (E2E 开发)
└── Fullstack Dev Skills (65+ 技能)

效率提升:
├── claude-tmux (tmux 集成)
├── claude-esp (TUI 监控)
├── Dippy (安全命令批准)
└── sudocode (任务管理)

项目管理:
├── Claude Code PM
└── Simone

安全:
├── parry (提示注入检测 ⭐⭐⭐)
└── Trail of Bits 安全技能
```

---

## 六、总结

### 6.1 本期亮点

| 类别 | 新增插件 | 评价 |
|------|----------|------|
| **科学研究** | Claude Scientific Skills | ⭐⭐⭐⭐⭐ 强烈推荐 |
| **安全** | parry, Dippy | ⭐⭐⭐ 新兴工具 |
| **开发工具** | claude-tmux, claude-esp | ⭐⭐⭐ 高效增强 |
| **全栈** | Fullstack Dev Skills | ⭐⭐⭐⭐⭐ 65+ 技能 |
| **DevOps** | cc-devops-skills | ⭐⭐⭐⭐ 详细文档 |

### 6.2 快速入门

```bash
# 1. 科学研究技能
git clone https://github.com/K-Dense-AI/claude-scientific-skills ~/.claude/plugins/scientific

# 2. 全栈开发 (65+ 技能)
git clone https://github.com/jeffallan/claude-skills ~/.claude/plugins/fullstack

# 3. DevOps 技能
git clone https://github.com/akin-ozer/cc-devops-skills ~/.claude/plugins/devops

# 4. 工作流编排
git clone https://github.com/avifenesh/agentsys ~/.claude/plugins/agentsys
```

### 6.3 下一步行动

1. **科学研究**: 部署 Claude Scientific Skills 用于研究和分析
2. **安全增强**: 评估 parry 和 Dippy
3. **效率提升**: 集成 claude-tmux 和 claude-esp
4. **全栈开发**: 使用 Fullstack Dev Skills 的 65+ 技能

---

## 📚 参考资源

- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
- [awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills)
- [anthropics/skills](https://github.com/anthropics/skills)
- [trailofbits/skills](https://github.com/trailofbits/skills)
- [obra/superpowers](https://github.com/obra/superpowers)
- [cc_plugin 仓库](https://github.com/kongshan001/cc_plugin)
