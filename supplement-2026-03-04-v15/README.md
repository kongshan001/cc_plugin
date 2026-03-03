# Claude Code 插件调研报告 - 2026年3月 (补充-第五期)

> 持续跟踪 Claude Code 生态热门插件，聚焦游戏开发、Python 开发、自动化测试、开发者工具方向

---

## 📋 调研概要

| 维度 | 统计 |
|-----|------|
| **调研时间** | 2026-03-04 |
| **覆盖方向** | 游戏开发、Python开发、自动化测试、开发者工具 |
| **技能总数** | 970+ (Antigravity Awesome Skills) |
| **数据来源** | awesome-claude-code, GitHub trending, Antigravity Skills |

---

## 一、最新添加插件 (Latest Additions)

### 1.1 Claude Scientific Skills ⭐⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [K-Dense-AI/claude-scientific-skills](https://github.com/K-Dense-AI/claude-scientific-skills) |
| **Star** | ⭐ 活跃 |
| **更新** | 持续更新 |
| **特点** | 科研/工程/分析/金融/写作全能技能集 |

#### 核心功能

- **研究技能**: 文献检索、学术写作、研究方法
- **科学计算**: 数据分析、模型构建、实验设计
- **工程分析**: 结构分析、仿真、计算
- **金融分析**: 量化分析、风险评估、投资策略
- **写作技能**: 技术文档、论文撰写、内容创作

#### 适用场景

- 学术研究
- 工程计算
- 金融建模
- 数据分析
- 技术写作

### 1.2 parry - 提示注入扫描器

| 项目 | 说明 |
|-----|------|
| **GitHub** | [vaporif/parry](https://github.com/vaporif/parry) |
| **Star** | ⭐ 新兴 |
| **状态** | 🔶 早期开发 |
| **功能** | Claude Code Hooks 提示注入扫描 |

#### 核心功能

- **注入攻击检测**: 扫描工具输入/输出中的提示注入
- **敏感信息检测**: 检测可能的敏感数据泄露
- **数据外泄防护**: 阻止数据外泄尝试
- **双向扫描**: 输入和输出同时监控

#### ⚠️ 注意事项

> 早期开发阶段，但值得关注。安全敏感场景建议谨慎使用。

### 1.3 Dippy - 智能命令批准

| 项目 | 说明 |
|-----|------|
| **GitHub** | [ldayton/Dippy](https://github.com/ldayton/Dippy) |
| **Star** | ⭐ 新兴 |
| **支持平台** | Claude Code, Gemini CLI, Cursor |

#### 核心功能

- **AST 解析**: 使用 AST 分析 Bash 命令安全性
- **智能批准**: 自动批准安全命令
- **危险命令提示**: 危险操作才请求确认
- **零权限疲劳**: 解决频繁授权问题

#### 工作原理

```
Bash 命令 → AST 解析 → 安全性评估
                ↓
        ┌───────┴───────┐
        ↓               ↓
    安全命令         危险命令
    (自动批准)      (请求确认)
```

### 1.4 sudocode - 轻量级编排工具

| 项目 | 说明 |
|-----|------|
| **GitHub** | [sudocode-ai/sudocode](https://github.com/sudocode-ai/sudocode) |
| **Star** | ⭐ 新兴 |
| **特点** | 轻量级代理编排开发工具 |

#### 核心功能

- **规范框架集成**: 支持多种规范框架
- **Jira 集成**: 类似 Jira 的任务管理
- **repo 内运行**: 直接在项目中运行
- **轻量级**: 极简依赖，快速启动

### 1.5 claude-tmux - Tmux 管理

| 项目 | 说明 |
|-----|------|
| **GitHub** | [nielsgroen/claude-tmux](https://github.com/nielsgroen/claude-tmux) |
| **Star** | ⭐ 新兴 |
| **功能** | 在 Tmux 中管理 Claude Code |

#### 核心功能

- **Tmux 弹出**: 显示所有 Claude Code 实例
- **快速切换**: 实例间快速切换
- **状态监控**: 实时状态监控
- **会话管理**: 完整生命周期管理
- **Git Worktree 支持**: Git Worktree 和 PR 支持

### 1.6 claude-esp - 输出流式传输

| 项目 | 说明 |
|-----|------|
| **GitHub** | [phiat/claude-esp](https://github.com/phiat/claude-esp) |
| **语言** | Go |
| **功能** | 将 Claude Code 隐藏输出流式传输到独立终端 |

#### 核心功能

- **多会话监控**: 同时监控多个会话
- **内容过滤**: 按内容类型过滤
- **后台任务追踪**: 跟踪后台任务
- **调试支持**: 理解 Claude 底层行为

#### 适用场景

- 调试 Claude 行为
- 理解 Claude 思考过程
- 监控子代理活动
- 学习 Claude 工作原理

---

## 二、Hooks 插件 (安全与自动化)

### 2.1 Hooks 概述

Hooks 是 Claude Code 强大的 API，允许在 Claude 生命周期中的不同点激活命令和运行脚本。

### 2.2 安全相关 Hooks

#### Britfix - 英式英语转换

| 项目 | 说明 |
|-----|------|
| **GitHub** | [Talieisin/britfix](https://github.com/Talieisin/britfix) |
| **功能** | 自动转换美式英语到英式英语 |

#### 智能转换

- **代码感知**: 只转换注释和文档字符串
- **标识符保护**: 不转换代码标识符
- **字符串字面量保护**: 不转换字符串内容

#### parry - 提示注入扫描 (见 1.2)

#### Dippy - 自动批准安全命令 (见 1.3)

### 2.3 开发效率 Hooks

#### TDD Guard

| 项目 | 说明 |
|-----|------|
| **GitHub** | [nizos/tdd-guard](https://github.com/nizos/tdd-guard) |
| **功能** | 实时监控文件操作，阻止违反 TDD 原则的更改 |

#### TypeScript Quality Hooks

| 项目 | 说明 |
|-----|------|
| **GitHub** | [bartolli/claude-code-typescript-hooks](https://github.com/bartolli/claude-code-typescript-hooks) |
| **功能** | TypeScript 项目质量检查 |
| **性能** | SHA256 配置缓存，<5ms 验证 |

#### CC Notify - 桌面通知

| 项目 | 说明 |
|-----|------|
| **GitHub** | [dazuiba/CCNotify](https://github.com/dazuiba/CCNotify) |
| **功能** | Claude Code 桌面通知 |

### 2.4 Hooks 开发工具

#### cchooks - Python SDK

| 项目 | 说明 |
|-----|------|
| **GitHub** | [GowayLee/cchooks](https://github.com/GowayLee/cchooks) |
| **语言** | Python |
| **特点** | 轻量级 Python SDK，简洁 API |

#### claude-code-hooks-sdk - PHP SDK

| 项目 | 说明 |
|-----|------|
| **GitHub** | [beyondcode/claude-hooks-sdk](https://github.com/beyondcode/claude-hooks-sdk) |
| **语言** | PHP |
| **特点** | Laravel 风格 PHP SDK |

#### claude-hooks - TypeScript 系统

| 项目 | 说明 |
|-----|------|
| **GitHub** | [johnlindquist/claude-hooks](https://github.com/johnlindquist/claude-hooks) |
| **语言** | TypeScript |
| **特点** | 强大灵活的 Hooks 配置系统 |

### 2.5 Claudio - 系统音效

| 项目 | 说明 |
|-----|------|
| **GitHub** | [ctoth/claudio](https://github.com/ctoth/claudio) |
| **功能** | 通过 Hooks 添加系统原生音效 |

---

## 三、IDE 集成

### 3.1 VS Code 集成

#### Claude Code Chat

| 项目 | 说明 |
|-----|------|
| **市场** | [VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=AndrePimenta.claude-code-chat) |
| **作者** | andrepimenta |
| **功能** | 优雅的 Claude Code 聊天界面 |

#### Claudix - Claude Code for VSCode

| 项目 | 说明 |
|-----|------|
| **GitHub** | [Haleclipse/Claudix](https://github.com/Haleclipse/Claudix) |
| **技术栈** | Vue 3 + TypeScript |
| **功能** | 直接在编辑器中使用 Claude Code |

#### 核心功能

- 交互式聊天界面
- 会话管理
- 智能文件操作
- 终端执行
- 实时流式响应

### 3.2 Emacs 集成

#### claude-code.el

| 项目 | 说明 |
|-----|------|
| **GitHub** | [stevemolitor/claude-code.el](https://github.com/stevemolitor/claude-code.el) |
| **功能** | Emacs 接口 for Claude Code CLI |

#### claude-code-ide.el

| 项目 | 说明 |
|-----|------|
| **GitHub** | [manzaltu/claude-code-ide.el](https://github.com/manzaltu/claude-code-ide.el) |
| **功能** | 高级 Emacs 集成 |

#### 核心功能

- Ediff 风格的代码建议
- LSP/flymake/flycheck 诊断
- 缓冲区上下文跟踪
- 符号引用/定义 MCP 工具支持
- Tree-sitter AST 查询

### 3.3 Neovim 集成

#### claude-code.nvim

| 项目 | 说明 |
|-----|------|
| **GitHub** | [greggh/claude-code.nvim](https://github.com/greggh/claude-code.nvim) |
| **功能** | Claude Code 与 Neovim 无缝集成 |

---

## 四、使用监控工具

### 4.1 CLI 工具

#### CC Usage

| 项目 | 说明 |
|-----|------|
| **GitHub** | [ryoppippi/ccusage](https://github.com/ryoppippi/ccusage) |
| **功能** | 管理和分析 Claude Code 使用情况 |
| **特点** | 基于本地日志分析 |

#### 核心功能

- 成本信息仪表盘
- Token 消耗分析
- 使用趋势可视化

### 4.2 Web 仪表盘

#### ccflare

| 项目 | 说明 |
|-----|------|
| **GitHub** | [snipeship/ccflare](https://github.com/snipeship/ccflare) |
| **特点** | Web UI 仪表盘，功能全面 |

#### better-ccflare

| 项目 | 说明 |
|-----|------|
| **GitHub** | [tombii/better-ccflare](https://github.com/tombii/better-ccflare) |
| **来源** | ccflare 分支 |
| **特点** | 性能增强、扩展支持、Docker 部署 |

#### 增强功能

- 性能优化
- 更多提供商支持
- Bug 修复
- Docker 部署支持

#### Claude Code Usage Monitor

| 项目 | 说明 |
|-----|------|
| **GitHub** | [Maciek-roboblog/Claude-Code-Usage-Monitor](https://github.com/Maciek-roboblog/Claude-Code-Usage-Monitor) |
| **特点** | 实时终端工具 |

#### 核心功能

- 实时 Token 消耗显示
- 消耗速率
- Token 耗尽预测
- 可视化进度条
- 会话分析
- 多订阅计划支持

### 4.3 会话浏览器

#### Claudex

| 项目 | 说明 |
|-----|------|
| **GitHub** | [kunwar-shah/claudex](https://github.com/kunwar-shah/claudex) |
| **功能** | Web 会话浏览器 |
| **特点** | 完全本地，无遥测 |

#### 核心功能

- 项目对话历史浏览
- 代码库全文搜索索引
- 易于导航的 UI
- 高级分析仪表盘
- 多种导出选项

### 4.4 社区排行榜

#### viberank

| 项目 | 说明 |
|-----|------|
| **GitHub** | [sculptdotfun/viberank](https://github.com/sculptdotfun/viberank) |
| **功能** | 社区驱动的使用统计排行榜 |

#### 核心功能

- 使用统计可视化
- GitHub OAuth
- 数据验证
- CLI/Web 提交方式

---

## 五、配置管理工具

### 5.1 claude-rules-doctor

| 项目 | 说明 |
|-----|------|
| **GitHub** | [nulone/claude-rules-doctor](https://github.com/nulone/claude-rules-doctor) |
| **功能** | 检测失效的 .claude/rules/ 文件 |

#### 核心功能

- **死规则检测**: 检查 paths: globs 是否匹配文件
- **CI 模式**: 失效规则退出码为 1
- **JSON 输出**: 程序化输出
- **详细模式**: 显示匹配的文件

#### 工作原理

```bash
# 检查规则
claude-rules-doctor

# CI 模式
claude-rules-doctor --ci

# 详细模式
claude-rules-doctor --verbose
```

### 5.2 ClaudeCTX

| 项目 | 说明 |
|-----|------|
| **GitHub** | [foxj77/claudectx](https://github.com/foxj77/claudectx) |
| **功能** | 一键切换整个 Claude Code 配置 |

#### 核心功能

- 配置文件快速切换
- 多环境支持
- 预设管理

---

## 六、状态栏工具 (Status Lines)

### 6.1 状态栏概述

状态栏配置和自定义 Claude Code 状态栏功能。

### 6.2 Rust 实现

#### CCometixLine

| 项目 | 说明 |
|-----|------|
| **GitHub** | [Haleclipse/CCometixLine](https://github.com/Haleclipse/CCometixLine) |
| **语言** | Rust |
| **特点** | 高性能，Git 集成，使用跟踪 |

#### claudia-statusline

| 项目 | 说明 |
|-----|------|
| **GitHub** | [hagan/claudia-statusline](https://github.com/hagan/claudia-statusline) |
| **语言** | Rust |
| **特点** | 高性能，持久统计，进度条 |

#### 核心功能

- SQLite 持久化
- Git 集成
- 上下文进度条
- 消耗速率计算
- XDG 合规
- 主题支持 (dark/light)

### 6.3 其他实现

#### ccstatusline

| 项目 | 说明 |
|-----|------|
| **GitHub** | [sirmalloc/ccstatusline]( |
| **功能** | 高可定制状态行格式化 |

#### claude-powerline

| 项目 | 说明 |
|-----|------|
| **GitHub** | [Owloops/claude-powerline]( |
| **风格** | Vim 风格 powerline |
| **功能** | 实时使用跟踪，Git 集成，自定义主题 |

#### claude-code-statusline

| 项目 | 说明 |
|-----|------|
| **GitHub** | [rz1989s/claude-code-statusline]( |
| **特点** | 增强的 4 行状态行，主题，成本跟踪 |

---

## 七、编排工具 (Orchestrators)

### 7.1 Auto-Claude

| 项目 | 说明 |
|-----|------|
| **GitHub** | [AndyMik90/Auto-Claude](https://github.com/AndyMik90/Auto-Claude) |
| **特点** | 多代理编排框架 |
| **UI** | Kanban 风格 |

#### 核心功能

- 完整 SDLC 集成
- 计划、构建、验证自动化
- 精心设计的代理编排

### 7.2 Claude Squad

| 项目 | 说明 |
|-----|------|
| **GitHub** | [smtg-ai/claude-squad](https://github.com/smtg-ai/claude-squad) |
| **功能** | 终端应用管理多个 Claude Code 实例 |

### 7.3 Claude Swarm

| 项目 | 说明 |
|-----|------|
| **GitHub** | [parruda/claude-swarm](https://github.com/parruda/claude-swarm) |
| **功能** | 连接到 Claude Code Agent 群组 |

### 7.4 Happy Coder

| 项目 | 说明 |
|-----|------|
| **GitHub** | [slopus/happy](https://github.com/slopus/happy) |
| **功能** | 并行运行多个 Claude Code |
| **通知** | 推送通知 |

### 7.5 TSK - AI Agent 任务管理器

| 项目 | 说明 |
|-----|------|
| **GitHub** | [dtormoen/tsk](https://github.com/dtormoen/tsk) |
| **语言** | Rust |
| **功能** | 沙箱 Docker 环境中的 AI 代理任务 |

---

## 八、工具类 (Tooling)

### 8.1 会话管理

#### Claude Session Restore

| 项目 | 说明 |
|-----|------|
| **GitHub** | [ZENG3LD/claude-session-restore](https://github.com/ZENG3LD/claude-session-restore) |
| **功能** | 从之前会话恢复上下文 |

#### cchistory

| 项目 | 说明 |
|-----|------|
| **GitHub** | [eckardt/cchistory](https://github.com/eckardt/cchistory) |
| **功能** | 列出会话中所有 Bash 命令 |

#### recall

| 项目 | 说明 |
|-----|------|
| **GitHub** | [zippoxer/recall](https://github.com/zippoxer/recall) |
| **功能** | 全文搜索 Claude Code 会话 |

### 8.2 配置工具

#### ccexp

| 项目 | 说明 |
|-----|------|
| **GitHub** | [nyatinte/ccexp](https://github.com/nyatinte/ccexp) |
| **功能** | 交互式 CLI 工具发现和管理配置文件 |
| **UI** | 精美终端 UI |

#### Claude Composer

| 项目 | 说明 |
|-----|------|
| **GitHub** | [possibilities/claude-composer](https://github.com/possibilities/claude-composer) |
| **功能** | 添加小增强到 Claude Code |

#### tweakcc

| 项目 | 说明 |
|-----|------|
| **GitHub** | [Piebald-AI/tweakcc](https://github.com/Piebald-AI/tweakcc) |
| **功能** | 命令行工具自定义样式 |

### 8.3 日志查看

#### cclogviewer

| 项目 | 说明 |
|-----|------|
| **GitHub** | [Brads3290/cclogviewer](https://github.com/Brads3290/cclogviewer) |
| **功能** | 查看 Claude Code .jsonl 对话文件 |

### 8.4 容器化

#### run-claude-docker

| 项目 | 说明 |
|-----|------|
| **GitHub** | [icanhasjonas/run-claude-docker](https://github.com/icanhasjonas/run-claude-docker) |
| **功能** | Docker 运行器转发工作区 |

#### viwo-cli

| 项目 | 说明 |
|-----|------|
| **GitHub** | [OverseedAI/viwo](https://github.com/OverseedAI/viwo) |
| **功能** | Docker 容器中运行 Claude Code |

---

## 九、技能汇总表

### 按类别分类

| 类别 | 推荐技能 | 特点 |
|-----|---------|------|
| **最新添加** | Claude Scientific Skills | 科研全能 |
| **安全 Hooks** | parry | 注入扫描 |
| **效率 Hooks** | Dippy | 智能批准 |
| **IDE 集成** | Claudix | VS Code 集成 |
| **使用监控** | better-ccflare | Web 仪表盘 |
| **配置管理** | claude-rules-doctor | 死规则检测 |
| **状态栏** | claudia-statusline | Rust 高性能 |
| **编排工具** | Auto-Claude | 多代理框架 |

---

## 十、安装指南

### 安装最新添加的插件

```bash
# Claude Scientific Skills
git clone https://github.com/K-Dense-AI/claude-scientific-skills.git
cp -r claude-scientific-skills ~/.claude/skills/

# parry - 提示注入扫描
git clone https://github.com/vaporif/parry.git
cp -r parry ~/.claude/hooks/

# Dippy - 智能命令批准
git clone https://github.com/ldayton/Dippy.git
cp -r Dippy ~/.claude/hooks/

# sudocode - 编排工具
git clone https://github.com/sudocode-ai/sudocode.git

# claude-tmux
git clone https://github.com/nielsgroen/claude-tmux.git
```

### 安装 IDE 集成

```bash
# VS Code - 从 Marketplace 安装
# Claude Code Chat
# Claudix

# Emacs
git clone https://github.com/stevemolitor/claude-code.el.git

# Neovim
git clone https://github.com/greggh/claude-code.nvim.git
```

### 安装监控工具

```bash
# CC Usage
cargo install ccusage

# better-ccflare
git clone https://github.com/tombii/better-ccflare.git
cd better-ccflare && docker-compose up -d
```

---

## 📚 参考链接

- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
- [parry - 提示注入扫描](https://github.com/vaporif/parry)
- [Dippy - 智能命令批准](https://github.com/ldayton/Dippy)
- [Claude Scientific Skills](https://github.com/K-Dense-AI/claude-scientific-skills)
- [Claudix VS Code](https://github.com/Haleclipse/Claudix)
- [better-ccflare](https://github.com/tombii/better-ccflare)

---

*持续更新中，关注 Claude Code 生态最新发展*
