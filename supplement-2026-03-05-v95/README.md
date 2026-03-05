# Claude Code 插件补充调研 v95

> 游戏客户端 / Python 开发 / 自动化测试 / 开发者工具

## 调研概述

本次调研继续聚焦以下方向：
1. 游戏客户端开发
2. Python 开发
3. 游戏客户端自动化测试
4. 其他开发者工具

## 一、游戏客户端开发相关插件

### 1.1 Claude-Starter-Kit 全栈开发模板

- **GitHub**: serpro69/claude-starter-kit
- **功能**: Claude Code 全栈开发启动模板，提供开箱即用的开发环境配置
- **特点**:
  - 预配置 MCP 服务器：Context7、Serena、Task Master、Pal
  - 6 个专业开发技能：分析、实施、测试、文档、开发指南、代码审查
  - 3 个任务编排代理：任务编排器、任务执行器、任务检查器
  - 47+ slash 命令覆盖完整开发周期
  - GitHub Actions 模板同步和工作流
- **适用场景**: 全栈项目启动、团队协作开发环境

### 1.2 官方插件系统深度解析

Claude Code 官方提供 15+ 插件，涵盖：

| 插件名称 | 功能 | 场景 |
|---------|------|------|
| agent-sdk-dev | Agent SDK 开发套件 | SDK 开发 |
| code-review | PR 自动代码审查 | 代码质量 |
| feature-dev | 7 阶段功能开发工作流 | 功能开发 |
| frontend-design | 前端设计技能 | UI 开发 |
| pr-review-toolkit | 6 个专业审查代理 | PR 审查 |
| security-guidance | 9 种安全模式提醒 | 安全开发 |
| ralph-wiggum | 迭代式 AI 开发循环 | 自动化开发 |

## 二、Python 开发相关插件

### 2.1 FastMCP - Pythonic MCP 框架 ⭐ 23,383

- **功能**: 最流行的 Python MCP 框架
- **特点**:
  - 简洁的装饰器 API
  - 异步支持
  - 丰富的示例
- **安装**: `pip install fastmcp`

### 2.2 Claude-Starter-Kit Python 开发支持

- **MCP 服务器**:
  - Context7: 最新的 Python 库文档
  - Serena: Python 代码语义分析
  - Task Master: Python 项目任务管理
- **技能**:
  - solid-code-review: Python 专项代码审查
  - testing-process: Python 测试最佳实践

## 三、自动化测试相关插件

### 3.1 MCP Inspector ⭐ 8,900

- **功能**: 官方 MCP 可视化测试工具
- **特点**:
  - 支持所有 MCP 协议测试
  - 可视化界面
  - 实时调试
- **安装**:
```bash
npm install -g @modelcontextprotocol/inspector
mcp-inspector
```

### 3.2 Playwright-MCP (官方) ⭐ 3,581

- **功能**: 浏览器自动化和 Web 测试
- **特点**:
  - 跨浏览器测试
  - 视觉回归测试
  - API 测试
- **场景**: Web 应用测试、端到端测试

### 3.3 Vibetest-Use ⭐ 771

- **功能**: AI 驱动的自动化 QA 测试
- **特点**:
  - Browser-Use 代理集成
  - 智能测试生成
  - 视觉回归测试

## 四、其他开发者工具

### 4.1 Claude-Tmux - 会话管理

- **GitHub**: nielsgroen/claude-tmux
- **功能**: 在 tmux 中管理 Claude Code 会话
- **特点**:
  - tmux 弹出式界面
  - 多会话切换
  - 状态监控
  - Git worktree 支持
- **安装**:
```bash
git clone https://github.com/nielsgroen/claude-tmux ~/.claude/plugins/
```

### 4.2 Claude-ESP - 调试工具

- **GitHub**: phiat/claude-esp
- **功能**: Claude Code 隐藏输出流调试工具
- **特点**:
  - 实时流式输出
  - 多会话同时监控
  - 内容过滤
  - 后台任务跟踪
- **技术栈**: Go + TUI

### 4.3 Rulesync - 配置同步

- **功能**: AI 编码代理配置同步工具
- **特点**:
  - Claude Code ↔ 其他代理配置转换
  - 规则、忽略文件、MCP 服务器同步
  - 项目级配置管理

### 4.4 ContextKit - 开发框架

- **功能**: 系统化开发框架
- **特点**:
  - 4 阶段规划方法论
  - 专业质量代理
  - 结构化工作流

### 4.5 SuperClaude - 配置框架

- **功能**: Claude Code 增强配置框架
- **特点**:
  - 专业命令
  - 认知人格
  - 内省方法论

### 4.6 Claude-Code-Templates

- **GitHub**: davila7/claude-code-templates
- **功能**: Claude Code 资源大全
- **特点**:
  - 使用仪表盘
  - 分析功能
  - Slash 命令库
  - Hooks 集合

## 五、部署建议

### 游戏客户端开发
```
推荐插件组合:
- mcp-unity / mcp-unreal / mcp-godot
- Claude-Code-Game-Studios
- Claude-Tmux (调试)
```

### Python 开发
```
推荐插件组合:
- FastMCP
- Claude-Starter-Kit
- Context7 (Python 文档)
- solid-code-review
```

### 自动化测试
```
推荐插件组合:
- MCP Inspector (测试)
- Playwright-MCP (Web 测试)
- Vibetest-Use (QA)
- SkUnit (单元测试)
```

### 开发者工具
```
推荐插件组合:
- Claude-Starter-Kit (全栈)
- Claude-Tmux (会话管理)
- Claude-ESP (调试)
- Rulesync (配置)
```

## 六、总结

本次调研发现以下趋势：

1. **官方插件生态**日益完善，覆盖开发全流程
2. **MCP 测试工具**成为标配 (Inspector 8900 stars)
3. **会话管理工具**兴起 (Claude-Tmux, Claude-ESP)
4. **配置同步**需求增长 (Rulesync)
5. **启动模板**标准化 (Claude-Starter-Kit)

---
调研时间: 2026-03-05
