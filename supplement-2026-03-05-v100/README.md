# Claude Code 热门插件补充调研 v100

> 游戏客户端开发 / Python 开发 / 自动化测试 / 开发者工具

## 📋 调研概述

本次调研覆盖以下方向：
1. 游戏客户端开发相关插件
2. Python 开发相关插件
3. 游戏客户端自动化测试相关插件
4. 其他开发者工具

---

## 🎮 一、游戏客户端开发相关插件

### 1.1 pixel-plugin (像素画插件)

- **Stars**: ⭐ 56
- **仓库**: willibrandon/pixel-plugin
- **描述**: Claude Code 插件，通过自然语言创建像素艺术，支持动画、复古调色板、抖动和游戏引擎导出
- **功能**:
  - Aseprite 集成
  - 自然语言生成像素画
  - 动画支持
  - 复古游戏调色板
  - 游戏引擎导出
- **语言**: Shell
- **部署**: `git clone https://github.com/willibrandon/pixel-plugin ~/.claude/plugins/`

### 1.2 claude-code-game-studios (游戏工作室)

- **Stars**: ⭐ 26-30
- **仓库**: The1Studio/claude-code-game-studios
- **描述**: 48 个 AI 代理 + 36 个工作流技能的全栈游戏开发系统
- **架构**:
  - Director → Lead → Specialist 三层架构
  - 48 个专业 AI 代理
  - 36 个工作流技能
  - 支持 Unity/Unreal/Godot/WebGL

### 1.3 cc-plugin-unity-gamedev (Unity 游戏开发)

- **Stars**: ⭐ 21
- **描述**: 21 个专业 Unity 技能

### 1.4 Godot 开发相关

- **godot-development**: Godot 游戏开发技能

### 1.5 Unreal MCP

- **unreal-mcp**: Unreal Engine MCP 服务器

---

## 🐍 二、Python 开发相关插件

### 2.1 developer-kit (开发者工具包)

- **Stars**: ⭐ 134
- **仓库**: giuseppe-trisciuoglio/developer-kit
- **描述**: Claude Code 开发者工具包 - 模块化插件系统，提供可复用的技能、代理和命令
- **覆盖范围**:
  - Java/Spring Boot/LangChain4J
  - TypeScript/NestJS/React
  - Python
  - PHP/WordPress
  - AWS CloudFormation
  - AI 模式
- **特点**: 多 CLI 支持

### 2.2 axon (代码智能引擎)

- **Stars**: ⭐ 466
- **仓库**: harshkedia177/axon
- **描述**: 图形驱动的代码智能引擎 - 将代码库索引为知识图谱，通过 MCP 工具暴露给 AI 代理
- **功能**:
  - 代码库索引
  - 知识图谱构建
  - 死代码检测
  - 静态分析
  - Tree-sitter 集成
- **语言**: Python
- **主题**: claude-code, code-analysis, knowledge-graph, mcp, python, static-analysis

### 2.3 claude-arsenal (武器库)

- **Stars**: ⭐ 9
- **描述**: 39+ 经过验证的 Claude Code 技能和 9 个专业代理

### 2.4 popkit-claude

- **Stars**: ⭐ 4
- **仓库**: jrc1883/popkit-claude
- **描述**: AI 驱动的 Claude Code 开发工作流自动化 - 23 个命令，38 个技能，22 个专业代理

### 2.5 claude-skills-collection-2026

- **Stars**: ⭐ 23
- **仓库**: inollp7855/claude-skills-collection-2026
- **描述**: 2026 年完整的 Claude Skills 集合 - 100+ 生产就绪技能

### 2.6 darrenoakey/claude-skill-python

- **描述**: Claude Code 技能，执行严格的 Python 开发标准，零虚构测试

### 2.7 spoon-awesome-skill

- **Stars**: ⭐ 12
- **描述**: 57 个 Python 脚本，跨 19 个技能 - SpoonOS 开发和 Web3 集成

---

## 🧪 三、自动化测试相关插件

### 3.1 claude-code-playwright-mcp-test (Playwright 测试框架)

- **Stars**: ⭐ 164
- **仓库**: terryso/claude-code-playwright-mcp-test
- **描述**: 基于 YAML 的 Playwright MCP 自动化测试框架，专为 Claude Code 设计
- **功能**:
  - YAML 配置文件
  - Playwright 集成
  - 自动化测试
  - MCP 协议支持
- **语言**: JavaScript
- **创建时间**: 2025-06-15
- **主题**: claudecode, playwright

### 3.2 unibrowse (高级浏览器自动化)

- **Stars**: ⭐ 4
- **仓库**: sackio/unibrowse
- **描述**: Claude Code 高级浏览器自动化插件 - 5 个专业子代理，57+ 宏，智能委托
- **功能**:
  - Web 抓取
  - 表单填写
  - 电商自动化
  - QA 测试
  - 无障碍测试
- **语言**: JavaScript
- **主题**: accessibility-testing, browser-automation, chrome-extension, claude-code, e-commerce, mcp

### 3.3 ai-testing-mcp

- **Stars**: ⭐ 6
- **仓库**: Twisted66/ai-testing-mcp
- **描述**: AI 驱动的测试自动化 MCP 服务器 - TestSprite 替代方案

### 3.4 local-testing-agent (多语言测试自动化)

- **Stars**: ⭐ 0
- **仓库**: marcelkurvers/local-testing-agent
- **描述**: Claude Code 和 AI 助手的多语言测试自动化 MCP 服务器
- **支持语言**:
  - Python
  - JavaScript/TypeScript
  - Go
  - Rust
  - Java
  - Ruby
- **功能**:
  - 自动化测试发现
  - 测试执行
- **语言**: Python

### 3.5 mcp-chromium-arm64

- **Stars**: ⭐ 4
- **仓库**: nfodor/mcp-chromium-arm64
- **描述**: ARM64 浏览器自动化 - 80 美元树莓派预算的 SaaS 测试

### 3.6 claude-playwright

- **Stars**: ⭐ 2
- **仓库**: smartlabsAT/claude-playwright
- **描述**: Claude Code ↔ Playwright 无缝集成，智能缓存，AI 感知的选择器解析

---

## 🛠️ 四、其他开发者工具

### 4.1 awesome-claude-code-toolkit (最全工具包)

- **Stars**: ⭐ 639
- **仓库**: rohitg00/awesome-claude-code-toolkit
- **描述**: Claude Code 最全面的工具包
- **包含**:
  - 135 个代理
  - 35 个精选技能 (+15,000 via SkillKit)
  - 42 个命令
  - 120 个插件
  - 19 个钩子
  - 15 个规则
  - 7 个模板
  - 6 个 MCP 配置

### 4.2 claudex (自定义 Claude Code UI)

- **Stars**: ⭐ 224
- **仓库**: Mng-dev-ai/claudex
- **描述**: 你自己的 Claude Code UI、沙箱、浏览器内 VS Code、终端、多提供商支持
- **功能**:
  - 自定义 UI
  - 沙箱环境
  - 浏览器内 VS Code
  - 终端
  - 多提供商支持 (Anthropic, OpenAI, GitHub Copilot, OpenRouter)
  - 自定义技能
  - MCP 服务器
- **语言**: TypeScript

### 4.3 miro-ai (Miro AI 开发者工具)

- **Stars**: ⭐ 67
- **仓库**: miroapp/miro-ai
- **描述**: 官方 Miro AI 开发者工具和集成

### 4.4 recallium (本地 AI 记忆系统)

- **Stars**: ⭐ 17
- **仓库**: recallium-ai/recallium
- **描述**: 本地自托管通用 AI 记忆系统，为开发者工具提供持久知识层
- **功能**:
  - 消除"AI 健忘症"
  - 自动捕获和聚类决策
  - 跨项目模式识别
  - MCP 通用兼容

### 4.5 claude-chrome-mcp

- **Stars**: ⭐ 7
- **仓库**: durapensa/claude-chrome-mcp
- **描述**: 开发者工具套件，使 Claude Desktop、Claude Code 和其他 MCP 主机能够与 Chrome 浏览器交互

### 4.6 web-developer-mcp

- **Stars**: ⭐ 6
- **仓库**: Artmann/web-developer-mcp
- **描述**: Web 开发工具 MCP 服务器
- **功能**:
  - 浏览器自动化
  - DOM 检查
  - 网络监控
  - 控制台分析

### 4.7 codebase-curator

- **Stars**: ⭐ 6
- **仓库**: RLabs-Inc/codebase-curator
- **描述**: 智能代码库工具 - smartgrep 使用代码库的语义索引

### 4.8 beagle (代码审查技能)

- **Stars**: ⭐ 37
- **仓库**: existential-birds/beagle
- **描述**: Claude Code 代码审查技能和验证工作流
- **覆盖**: Python, Go, React, FastAPI, BubbleTea, AI 框架 (Pydantic AI, LangGraph, Vercel AI SDK)

### 4.9 claude-code-sub-agents

- **Stars**: ⭐ 30
- **仓库**: charles-adedotun/claude-code-sub-agents
- **描述**: 最小化 AI 代理系统 - 一个代理统治所有

### 4.10 skillnote

- **Stars**: ⭐ 5
- **仓库**: luna-prompts/skillnote
- **描述**: AI 编码代理的开源技能注册表

---

## 📊 热门插件排行榜

| 排名 | 插件名称 | Stars | 方向 |
|------|----------|-------|------|
| 1 | awesome-claude-code | 26,355 | 汇总 |
| 2 | awesome-claude-code-subagents | 12,555 | 子代理 |
| 3 | awesome-claude-skills | 8,246 | 技能 |
| 4 | axon | 466 | Python/代码分析 |
| 5 | awesome-claude-code-toolkit | 639 | 开发者工具 |
| 6 | claudex | 224 | UI/多提供商 |
| 7 | claude-code-playwright-mcp-test | 164 | 测试 |
| 8 | miro-ai | 67 | 集成 |
| 9 | pixel-plugin | 56 | 游戏/像素画 |
| 10 | beagle | 37 | 代码审查 |

---

## 🔧 安装与使用

### 通用安装方式

```bash
# 克隆到插件目录
git clone https://github.com/{owner}/{repo} ~/.claude/plugins/
```

### 技能使用

```bash
# 查看可用技能
claude --list-skills

# 使用特定技能
claude /skill {skill-name}
```

---

## 📝 总结

### 游戏客户端开发
- 像素画插件、游戏工作室、Unity/Godot/Unreal 集成
- 生态相对较小但有专业方向

### Python 开发
- 代码智能 (axon) 是亮点，466 Stars
- developer-kit (134 Stars) 提供全栈支持
- Pydantic AI、FastAPI 等框架有专门技能

### 自动化测试
- Playwright 测试框架最成熟 (164 Stars)
- 多语言测试支持逐渐增加
- 浏览器自动化是核心能力

### 开发者工具
- awesome 列表生态丰富
- claudex 提供 UI 定制
- 代码审查和知识图谱是热门方向
