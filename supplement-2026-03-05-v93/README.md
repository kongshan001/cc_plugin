# Claude Code 插件补充调研 v93

> 游戏客户端 / Python 开发 / 自动化测试 / 开发者工具

## 调研概述

本次调研继续聚焦以下方向：
1. 游戏客户端开发
2. Python 开发
3. 游戏客户端自动化测试
4. 其他开发者工具

## 一、游戏客户端开发相关插件

### 1.1 Unreal-MCP (热门趋势 ⭐ 1,504)

- **GitHub**: chongdashu/unreal-mcp
- **Stars**: 1,504
- **功能**: AI 助手与 Unreal Engine 5 的桥梁，支持蓝图生成、关卡编辑、资产操作
- **部署**: 
```bash
pip install unreal-mcp
# 配置 claude_desktop_config.json
```
- **状态**: ✅ 热门推荐

### 1.2 Unreal-Engine-MCP (新版)

- **GitHub**: flopperam/unreal-engine-mcp
- **Stars**: 增长中
- **功能**: UE 5.5+ 自然语言控制，3D 世界构建
- **特点**: 支持建筑场景生成、复杂结构创建

### 1.3 Unity-MCP (已调研 ✅)

- **Stars**: 1,382
- **功能**: Unity Editor 自动化

### 1.4 iOS-Simulator-Skill (移动端测试)

- **GitHub**: conorluddy/ios-simulator-skill
- **Stars**: 565
- **功能**: Claude Code iOS 模拟器技能，用于构建、运行和交互 iOS 应用
- **技术栈**: Python

## 二、Python 开发相关插件

### 2.1 FastMCP (⭐ 23,383 - 热门第一)

- **GitHub**: PrefectHQ/fastmcp
- **Stars**: 23,383
- **功能**: 快速构建 MCP 服务器和客户端的 Python 框架
- **特点**: 
  - Pythonic 方式构建 MCP
  - 与 Prefect 工作流集成
  - 高性能异步支持
- **安装**:
```bash
pip install fastmcp
```

### 2.2 Anthropic Python SDK (官方)

- **GitHub**: anthropics/anthropic-sdk-python
- **功能**: Claude API Python SDK
- **安装**:
```bash
pip install anthropic
```

### 2.3 Pydantic-AI-Skills (已调研 ✅)

- **Stars**: 136
- **功能**: 类型安全 AI 应用开发

## 三、自动化测试相关插件

### 3.1 Playwright-Skill (⭐ 1,864)

- **GitHub**: lackeyjb/playwright-skill
- **Stars**: 1,864
- **功能**: Claude Code 浏览器自动化技能，模型自主编写和执行自定义自动化测试
- **特点**: 
  - Model-invoked 模式
  - Claude 自主编写测试代码
  - E2E 测试支持
- **部署**: Claude Code Skills 标准安装

### 3.2 Claude-Skills-Marketplace

- **GitHub**: mhattingpete/claude-skills-marketplace
- **Stars**: 433
- **功能**: 软件工程工作流技能市场 - Git 自动化、测试、代码审查

### 3.3 ClaudeCode-Rule2Hook

- **GitHub**: zxdxjtu/claudecode-rule2hook
- **功能**: 将自然语言项目规则转换为 Claude Code 自动化钩子

## 四、其他开发者工具

### 4.1 Lazy-Bird (开发自动化)

- **GitHub**: yusufkaraaslan/lazy-bird
- **Stars**: 增长中
- **功能**: 通用开发自动化，支持 15+ 框架预设
- **特点**:
  - Issue 驱动开发
  - 安全可扩展
  - 节省 20-100 小时/月

### 4.2 Claude-Esp (调试工具)

- **功能**: Claude Code 隐藏输出流式传输工具
- **特点**: 
  - Go 实现的 TUI
  - 实时监控多个会话
  - 过滤和跟踪后台任务

## 五、热门插件排行榜

| 排名 | 插件名称 | Stars | 类别 |
|------|----------|-------|------|
| 1 | FastMCP | 23,383 | Python/MCP |
| 2 | Playwright-Skill | 1,864 | 测试自动化 |
| 3 | Unreal-MCP | 1,504 | 游戏开发 |
| 4 | iOS-Simulator-Skill | 565 | 移动测试 |
| 5 | Claude-Skills-Marketplace | 433 | 开发工具 |

## 六、部署建议

### 游戏开发
- 推荐: Unreal-MCP + Unity-MCP
- 测试: Playwright-Skill

### Python 开发
- 推荐: FastMCP + Anthropic SDK

### 自动化测试
- 推荐: Playwright-Skill + Claude-Skills-Marketplace

## 七、总结

本次调研发现了以下趋势：
1. **Unreal-MCP** 成为游戏开发新热门
2. **FastMCP** 以 23k+ Stars 领跑 Python MCP 框架
3. **Playwright-Skill** 是自动化测试的首选方案
4. iOS 模拟器技能填补了移动端测试空白

---
调研时间: 2026-03-05
