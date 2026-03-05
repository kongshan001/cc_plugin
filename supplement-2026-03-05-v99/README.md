# Claude Code 插件调研补充 v99 - 游戏/ Python /测试/开发者工具

> 调研日期：2026-03-05
> 方向：游戏客户端开发 | Python 开发 | 游戏客户端自动化测试 | 其他开发者工具

---

## 📦 一、游戏客户端开发

### 1.1 MCP Unity - Unity 编辑器集成

| 项目 | 详情 |
|------|------|
| **仓库** | [CoderGamester/mcp-unity](https://github.com/CoderGamester/mcp-unity) |
| **描述** | Model Context Protocol (MCP) 插件，连接 Unity Editor，支持 Cursor、Claude Code、Codex、Windsurf 等 IDE |
| **功能** | 通过 MCP 协议让 AI 助手与 Unity 项目交互，提供场景管理、GameObject 操作、组件控制、材质管理、测试运行等 30+ 工具 |
| **工具列表** | execute_menu_item, select_gameobject, update_gameobject, update_component, add_package, run_tests, send_console_log, add_asset_to_scene, create_prefab, create_scene, load_scene, delete_scene, get_gameobject, get_console_logs, recompile_scripts, save_scene, get_scene_info, unload_scene, duplicate_gameobject, delete_gameobject, reparent_gameobject, move_gameobject, rotate_gameobject, scale_gameobject, set_transform, create_material, assign_material, modify_material, get_material_info, batch_execute |
| **示例** | "Execute the menu item 'GameObject/Create Empty' to create a new empty GameObject" |
| **依赖** | Unity 6+, Node.js 18+, npm 9+ |
| **安装方式** | Unity Package Manager 添加 git URL: https://github.com/CoderGamester/mcp-unity.git |

### 1.2 Unreal MCP - Unreal Engine 集成

| 项目 | 详情 |
|------|------|
| **仓库** | [AlbertUnreal/Unreal-MCP](https://github.com/AlbertUnreal/Unreal-MCP) |
| **描述** | 将 Unreal Engine 与 Claude Code、Cursor 等 AI 助手集成的 MCP 服务器 |
| **功能** | 蓝图操作、材质管理、场景控制、Actor 操作、UI 构建、测试执行 |
| **支持引擎** | Unreal Engine 5.0+ |

### 1.3 Godot Development Skill - Godot 游戏开发

| 项目 | 详情 |
|------|------|
| **仓库** | [not-napoleon/godot-claude](https://github.com/not-napoleon/godot-claude) |
| **描述** | Claude Code 的 Godot 游戏开发技能集 |
| **功能** | GDScript 编写、场景管理、节点操作、项目结构指导 |

---

## 🐍 二、Python 开发

### 2.1 Claude Code Python Skills - Python 开发技能集

| 项目 | 详情 |
|------|------|
| **仓库** | [anthropics/claude-cookbooks](https://github.com/anthropics/claude-cookbooks) |
| **描述** | Anthropic 官方的 Claude 食谱库，主要使用 Python 编写示例代码 |
| **内容** | 分类、检索增强生成、摘要、工具使用、向量数据库集成、视觉处理 |
| **核心notebook** | 客户代理、计算器集成、SQL 查询、RAG (Pinecone)、Wikipedia 搜索、网页读取、嵌入 (Voyage AI)、图像生成、子代理使用、PDF 上传、自动评估、JSON 模式、提示缓存 |

### 2.2 Python Patterns Skill - Python 设计模式

| 项目 | 详情 |
|------|------|
| **来源** | Antigravity Awesome Skills |
| **描述** | Python 设计模式和最佳实践技能 |
| **功能** | 常用设计模式指导、代码结构优化、Python 特定模式 |

### 2.3 FastAPI Development Skill - FastAPI 开发

| 项目 | 详情 |
|------|------|
| **仓库** | [本仓库已有文档](./fastapi-development.md) |
| **描述** | FastAPI 快速开发技能 |
| **功能** | API 设计、路由定义、依赖注入、数据库集成 |

---

## 🎮 三、游戏客户端自动化测试

### 3.1 Unity Test Runner 集成

| 项目 | 详情 |
|------|------|
| **来源** | MCP Unity 插件内置 |
| **功能** | run_tests 工具 - 使用 Unity Test Runner 执行测试 |
| **示例** | "Run all the EditMode tests in my project" |
| **支持模式** | EditMode, PlayMode |

### 3.2 Playwright MCP - 浏览器自动化测试

| 项目 | 详情 |
|------|------|
| **仓库** | [mrwhoknows55/playwright-mcp-server](https://github.com/mrwhoknows55/playwright-mcp-server) |
| **描述** | Playwright 浏览器自动化 MCP 服务器 |
| **功能** | 页面导航、元素交互、截图、PDF 生成、网络监控 |
| **评分** | 3.5/5 ⭐ |

### 3.3 Vibetest - 游戏测试工具

| 项目 | 详情 |
|------|------|
| **仓库** | [vibetest/vibetest](https://github.com/vibetest/vibetest) |
| **描述** | 游戏自动化测试工具 |
| **功能** | 游戏端到端测试、视觉回归测试、性能测试 |

---

## 🛠️ 四、其他开发者工具

### 4.1 Claude Code Templates - 开发者模板库

| 项目 | 详情 |
|------|------|
| **仓库** | [davila7/claude-code-templates](https://github.com/davila7/claude-code-templates) |
| **描述** | Claude Code 资源集合，提供优雅的 UI、仪表盘、分析功能 |
| **类别** | slash commands, hooks, agents, skills |
| **特性** | 使用情况仪表盘、分析、完整功能集 |

### 4.2 Claude Hub - GitHub 集成

| 项目 | 详情 |
|------|------|
| **仓库** | [Claude-Did-This/claude-hub](https://github.com/claude-did-this/claude-hub) |
| **描述** | Webhook 服务，将 Claude Code 连接到 GitHub 仓库 |
| **功能** | 通过 PR 和 Issues 实现 AI 驱动的代码辅助、代码库分析、技术问题解答 |

### 4.3 Claude Session Restore - 会话恢复

| 项目 | 详情 |
|------|------|
| **仓库** | [ZENG3LD/claude-session-restore](https://github.com/ZENG3LD/claude-session-restore) |
| **描述** | 高效恢复先前 Claude Code 会话的上下文 |
| **功能** | 分析会话文件和 git 历史、多因子数据收集、时间过滤、tail-based 解析处理大文件 (2GB)、CLI 工具 + Claude Code 技能 |

### 4.4 Claude Code Tools - 工具集

| 项目 | 详情 |
|------|------|
| **仓库** | [pchalasani/claude-code-tools](https://github.com/pchalasani/claude-code-tools) |
| **描述** | 会话连续性工具集 |
| **功能** | 避免 compaction 和跨会话恢复上下文 Claude Code 和 Codex CLI 之间的跨代理切换、Rust/Tantivy 全文搜索 (TUI for humans, skill/CLI for agents)、tmux-cli skill + command、与脚本和 CLI agents 交互、安全 hook 阻止危险命令 |

### 4.5 Claude Starter Kit - 启动模板

| 项目 | 详情 |
|------|------|
| **仓库** | [serpro69/claude-starter-kit](https://github.com/serpro69/claude-starter-kit) |
| **描述** | Claude Code 完整开发环境启动模板仓库 |
| **预配置** | Claude Code、MCP servers、工具用于 AI 驱动开发工作流 |
| **包含** | 配置模板 for 3 primary systems: Claude Code, Serena, Task Master |

### 4.6 Claudekit - CLI 工具包

| 项目 | 详情 |
|------|------|
| **仓库** | [carlrannaberg/claudekit](https://github.com/carlrannaberg/claudekit) |
| **描述** | Impressive CLI 工具包 |
| **功能** | auto-save checkpointing、code quality hooks、specification generation and execution、20+ specialized subagents (oracle(gpt-5), code-reviewer(6-aspect deep analysis), ai-sdk-expert(Vercel AI SDK), typescript-expert 等) |

### 4.7 cc-tools - Go 实现工具

| 项目 | 详情 |
|------|------|
| **仓库** | [Veraticus/cc-tools](https://github.com/Veraticus/cc-tools) |
| **描述** | 高性能 Go 实现的 Claude Code hooks 和工具 |
| **功能** | smart linting、testing、statusline generation、最小开销 |

### 4.8 ContextKit - 开发框架

| 项目 | 详情 |
|------|------|
| **仓库** | [FlineDev/ContextKit](https://github.com/FlineDev/ContextKit) |
| **描述** | 系统化开发框架，将 Claude Code 转变为主动开发伙伴 |
| **功能** | 4阶段规划方法论、 specialized quality agents、结构化工作流、帮助 AI 首次产出生产就绪代码 |

### 4.9 Claude Composer - 增强工具

| 项目 | 详情 |
|------|------|
| **仓库** | [possibilities/claude-composer](https://github.com/possibilities/claude-composer) |
| **描述** | 为 Claude Code 添加小增强的工具 |
| **作者** | Mike Bannister (Claude Code 作者之一) |

### 4.10 Vibe-Log - 会话分析

| 项目 | 详情 |
|------|------|
| **仓库** | [vibe-log/vibe-log-cli](https://github.com/vibe-log/vibe-log-cli) |
| **描述** | 本地分析 Claude Code 提示，提供智能会话分析和可操作战略指导 |
| **输出** | statusline 和漂亮的 HTML 报告 |

### 4.11 Rulesync - 配置同步

| 项目 | 详情 |
|------|------|
| **仓库** | [dyoshikawa/rulesync](https://github.com/dyoshikawa/rulesync) |
| **描述** | Node.js CLI 工具，自动生成各种 AI coding agents 的配置 (rules, ignore files, MCP servers, commands, subagents) |
| **功能** | Claude Code 和其他 AI agents 之间的双向配置转换 |

---

## 📊 总结

### 游戏客户端开发
- **MCP Unity** - 最完整的 Unity 集成方案，提供 30+ 工具
- **Unreal MCP** - Unreal Engine 集成
- **Godot Development** - Godot 游戏开发支持

### Python 开发
- **Claude Cookbooks** - 官方 Python 示例库
- **Python Patterns Skill** - 设计模式指导
- **FastAPI Development** - API 开发支持

### 游戏客户端自动化测试
- **Unity Test Runner** - MCP Unity 内置测试功能
- **Playwright MCP** - 浏览器自动化测试
- **Vibetest** - 游戏专用测试工具

### 其他开发者工具
- **Claude Code Templates** - 完整资源库
- **Claude Hub** - GitHub 集成
- **Session Restore** - 会话恢复
- **Claudekit** - 20+ 子代理工具包
- **ContextKit** - 主动开发框架

---

*文档生成时间：2026-03-05*
*来源：awesome-claude-code, GitHub, MCP 官方文档*
