# Claude Code 插件补充调研 v94

> 游戏客户端 / Python 开发 / 自动化测试 / 开发者工具

## 调研概述

本次调研继续聚焦以下方向：
1. 游戏客户端开发
2. Python 开发
3. 游戏客户端自动化测试
4. 其他开发者工具

## 一、游戏客户端开发相关插件

### 1.1 Claude-Code-Game-Studios

- **GitHub**: Donchitos/Claude-Code-Game-Studios
- **Stars**: 30
- **功能**: 将 Claude Code 转变为完整游戏开发工作室 - 48 个 AI 代理、36 个工作流技能和完整的协调系统，模拟真实工作室层级
- **特点**:
  - 48 个专业 AI 代理
  - 36 个游戏开发工作流技能
  - 完整的工作室协调系统
- **适用场景**: 独立游戏开发、游戏原型设计

### 1.2 Claude-Resources (Godot)

- **GitHub**: kwhitejr/claude-resources
- **Stars**: 3
- **功能**: 自定义 Claude Code 代理和技能，用于 Godot 游戏开发工作流
- **特点**: 专注于 Godot 引擎的 AI 辅助开发

## 二、Python 开发相关插件

### 2.1 Developer-Kit (已调研 ✅)

- **Stars**: 133
- **功能**: Claude Code 模块化插件系统，提供可重用的技能、代理和命令

### 2.2 FastMCP (已调研 ✅)

- **Stars**: 23,383
- **功能**: Pythonic MCP 框架

## 三、自动化测试相关插件

### 3.1 MCP Inspector (官方热门 ⭐ 8,900)

- **GitHub**: modelcontextprotocol/inspector
- **Stars**: 8,900
- **功能**: MCP 服务器的可视化测试工具
- **特点**:
  - 官方维护的 MCP 测试工具
  - 可视化界面
  - 支持所有 MCP 协议测试
- **部署**:
```bash
npm install -g @modelcontextprotocol/inspector
mcp-inspector
```

### 3.2 MCPJam Inspector

- **GitHub**: MCPJam/inspector
- **Stars**: 1,782
- **功能**: MCP 服务器测试和调试工具，ChatGPT 应用和 MCP 应用测试
- **特点**:
  - 支持 MCP 服务器调试
  - ChatGPT 应用测试
  - MCP 应用测试
- **部署**:
```bash
npm install -g @mcpjam/inspector
```

### 3.3 Vibetest-Use

- **GitHub**: browser-use/vibetest-use
- **Stars**: 771
- **功能**: 使用 Browser-Use 代理的自动化 QA 测试
- **特点**:
  - 自动化浏览器测试
  - AI 驱动的测试生成
  - 视觉回归测试支持

### 3.4 SkUnit (AI 单元测试)

- **GitHub**: mehrandvd/skunit
- **Stars**: 171
- **功能**: AI 单元测试工具，支持 IChatClient、MCP 服务器和代理的测试
- **特点**:
  - 专门针对 AI 组件的测试框架
  - 支持 MCP 服务器测试
  - 代理行为验证

### 3.5 Claude-Code-Playwright-MCP-Test

- **GitHub**: terryso/claude-code-playwright-mcp-test
- **Stars**: 164
- **功能**: 基于 YAML 的 Playwright MCP 自动化测试框架，专为 Claude Code 设计
- **特点**:
  - YAML 配置驱动
  - Playwright 集成
  - 专为 Claude Code 优化

### 3.6 MCP-Universe

- **GitHub**: SalesforceAIResearch/MCP-Universe
- **Stars**: 566
- **功能**: 开发和测试 AI 代理的综合框架，专注于代理基准测试
- **特点**:
  - 代理能力评估
  - 真实世界场景测试
  - 基准测试框架

## 四、其他开发者工具

### 4.1 Fast-Agent

- **GitHub**: evalstate/fast-agent
- **Stars**: 3,694
- **功能**: 定义、提示和测试 MCP 启用代理和工作流
- **特点**:
  - 工作流定义
  - 代理测试
  - MCP 集成
- **部署**:
```bash
pip install fast-agent
```

### 4.2 McpHub Neovim

- **GitHub**: ravitemer/mcphub.nvim
- **Stars**: 1,739
- **功能**: Neovim MCP 客户端，无缝集成 MCP 服务器到编辑工作流
- **特点**:
  - Neovim 原生集成
  - MCP 服务器管理
  - 直观界面

### 4.3 LitterBox (安全测试)

- **GitHub**: BlackSnufkin/LitterBox
- **Stars**: 1,316
- **功能**: 恶意软件开发者和红队的安全沙箱环境，用于在部署前测试有效载荷
- **特点**:
  - 恶意软件分析
  - 检测机制测试
  - MCP 集成

### 4.4 MCP-For-Security

- **GitHub**: cyproxio/mcp-for-security
- **Stars**: 559
- **功能**: 安全工具的 MCP 集合：SQLMap、FFUF、NMAP、Masscan 等
- **特点**:
  - 渗透测试集成
  - 漏洞扫描
  - AI 安全工作流

### 4.5 Awesome-MCP-Devtools

- **GitHub**: punkpeye/awesome-mcp-devtools
- **Stars**: 428
- **功能**: MCP 服务器开发的开发者工具、SDK、库和测试工具精选列表
- **特点**:
  - 开发工具集合
  - 测试工具
  - 最佳实践

### 4.6 MCPMark

- **GitHub**: eval-sys/mcpmark
- **Stars**: 389
- **功能**: 综合压力测试 MCP 基准，用于评估模型和代理在真实世界 MCP 使用中的能力
- **特点**:
  - 压力测试
  - 代理能力评估
  - 性能基准

### 4.7 KMCP (Kubernetes)

- **GitHub**: kagent-dev/kmcp
- **Stars**: 434
- **功能**: 用于构建、测试和部署 MCP 服务器的 CLI 工具和 Kubernetes 控制器
- **特点**:
  - Kubernetes 集成
  - CLI 工具
  - 自动化部署

### 4.8 SecOps-MCP

- **GitHub**: securityfortech/secops-mcp
- **Stars**: 184
- **功能**: 一体化安全测试工具箱，通过单一 MCP 接口整合流行开源工具
- **特点**:
  - 渗透测试
  - 漏洞赏金
  - 威胁狩猎

## 五、热门插件排行榜

| 排名 | 插件名称 | Stars | 类别 |
|------|----------|-------|------|
| 1 | MCP Inspector | 8,900 | 测试工具 |
| 2 | Fast-Agent | 3,694 | 工作流 |
| 3 | MCPJam Inspector | 1,782 | 测试工具 |
| 4 | McpHub Neovim | 1,739 | 编辑器集成 |
| 5 | LitterBox | 1,316 | 安全测试 |
| 6 | Vibetest-Use | 771 | QA测试 |
| 7 | MCP-Universe | 566 | 基准测试 |
| 8 | MCP-For-Security | 559 | 安全工具 |
| 9 | Awesome-MCP-Devtools | 428 | 开发工具 |
| 10 | KMCP | 434 | K8s工具 |

## 六、部署建议

### 游戏开发
- 推荐: Claude-Code-Game-Studios + Claude-Resources (Godot)

### Python 开发
- 推荐: FastMCP + Developer-Kit

### 自动化测试
- 推荐: MCP Inspector + Playwright-MCP + Vibetest-Use

### 开发者工具
- 推荐: Fast-Agent + McpHub + Awesome-MCP-Devtools

## 七、总结

本次调研发现以下趋势：

1. **MCP Inspector** (8900 stars) 成为 MCP 测试工具的黄金标准
2. **Fast-Agent** (3694 stars) 提供强大的工作流定义和测试能力
3. 安全相关 MCP 工具正在快速增长 (LitterBox, MCP-For-Security)
4. 编辑器集成 (Neovim) 生态日益丰富
5. AI 代理基准测试框架 (MCP-Universe, MCPMark) 开始兴起

---
调研时间: 2026-03-05
