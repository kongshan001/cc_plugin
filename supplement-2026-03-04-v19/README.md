# Claude Code 插件调研补充文档 v19

> 调研日期: 2026-03-04
> 调研方向: 游戏客户端开发 / Python 开发 / 游戏客户端自动化测试 / 其他开发者工具

---

## 目录

1. [游戏客户端开发](#1-游戏客户端开发)
2. [Python 开发](#2-python-开发)
3. [游戏客户端自动化测试](#3-游戏客户端自动化测试)
4. [其他开发者工具](#4-其他开发者工具)
5. [热门 MCP 服务器汇总](#5-热门-mcp-服务器汇总)
6. [快速推荐](#6-快速推荐)

---

## 1. 游戏客户端开发

### 1.1 lazy-bird ⭐⭐⭐⭐⭐
- **GitHub**: https://github.com/yusufkaraaslan/lazy-bird
- **Stars**: 210 | **语言**: Python
- **描述**: 通用开发自动化工具，支持 ANY 项目。Claude Code 可自主实现功能、运行测试、创建 PR。支持 15+ 框架预设，包括 **Godot 游戏开发框架**。
- **核心功能**:
  - Issue 驱动的自动开发
  - 支持 Godot、React、Django、Node.js、Rust 等框架
  - 自动运行测试并创建 PR
  - 安全、可扩展
- **适用场景**: 游戏客户端功能迭代、Bug 修复、自动化 PR
- **安装**: `pip install lazy-bird`

### 1.2 Godot MCP Server (通过 lazy-bird)
- **关联项目**: lazy-bird 内置 Godot 支持
- **功能**: Godot 项目代码生成、场景管理、GDScript 辅助
- **适用**: 2D/3D 游戏客户端开发

### 1.3 mcp-unity (Unity 集成)
- **描述**: Unity 游戏引擎 MCP 服务器集成
- **功能**: Unity 项目代码辅助、资源管理、场景操作
- **状态**: 社区维护

### 1.4 game-dev-skill
- **描述**: Claude Code 游戏开发技能包
- **功能**:
  - 游戏架构设计
  - 性能优化建议
  - 跨平台开发辅助
- **适用**: 多游戏引擎通用

---

## 2. Python 开发

### 2.1 Serena ⭐⭐⭐⭐⭐
- **GitHub**: https://github.com/oraios/serena
- **Stars**: 20,941 | **语言**: Python
- **描述**: 强大的编程代理工具包，提供语义检索和编辑能力（MCP 服务器及其他集成）
- **核心功能**:
  - 语义代码检索
  - 智能代码编辑
  - 语言服务器协议支持
  - MCP 服务器集成
- **官网**: https://oraios.github.io/serena
- **适用场景**: 大型 Python 项目重构、代码理解、智能编辑

### 2.2 PAL MCP Server ⭐⭐⭐⭐⭐
- **GitHub**: https://github.com/BeehiveInnovations/pal-mcp-server
- **Stars**: 11,180 | **语言**: Python
- **描述**: 多模型协作 MCP 服务器，支持 Claude Code / GeminiCLI / CodexCLI + Gemini / OpenAI / OpenRouter / Azure / Grok / Ollama
- **核心功能**:
  - 多 AI 模型协同工作
  - 模型切换和负载均衡
  - 自定义模型支持
- **适用场景**: Python 开发中需要多模型协作的场景

### 2.3 claud-skills ⭐⭐⭐⭐
- **GitHub**: https://github.com/Interstellar-code/claud-skills
- **Stars**: 11 | **语言**: Python
- **描述**: 生产级 Claude Code 框架，包含 13 个代理、9 个技能，支持自动生成文档
- **支持语言**: JavaScript, TypeScript, PHP, Laravel, React, **Python**
- **核心功能**:
  - 13 个专用代理
  - 9 个开发技能
  - 自动文档生成
  - Playwright 测试集成
- **适用场景**: Python Web 开发、API 开发

### 2.4 claude-arsenal ⭐⭐⭐⭐
- **GitHub**: https://github.com/majiayu000/claude-arsenal
- **Stars**: 9 | **语言**: Python
- **描述**: 39+ 实战级 Claude Code 技能 + 9 个专业代理，专业软件开发综合技能库
- **核心功能**:
  - 39+ 技能覆盖
  - DevOps 工具链
  - 多语言支持（Python, TypeScript）
- **适用场景**: Python 全栈开发、DevOps

### 2.5 koder ⭐⭐⭐⭐
- **GitHub**: https://github.com/feiskyer/koder
- **Stars**: 80 | **语言**: Python
- **描述**: 直观的 AI 编程助手和交互式 CLI 工具，通过智能自动化和上下文感知支持提升开发者生产力
- **核心功能**:
  - 智能代码补全
  - 上下文感知
  - 交互式 CLI
- **适用场景**: Python 日常开发

### 2.6 mcp-wireshark ⭐⭐⭐
- **GitHub**: https://github.com/khuynh22/mcp-wireshark
- **Stars**: 23 | **语言**: Python
- **描述**: Wireshark/tshark 与 AI 工具和 IDE 集成的 MCP 服务器
- **核心功能**:
  - 实时流量捕获
  - .pcap 文件解析
  - 显示过滤器应用
  - 流跟踪和 JSON 导出
- **适用场景**: Python 网络编程调试、协议分析

---

## 3. 游戏客户端自动化测试

### 3.1 playwright-skill ⭐⭐⭐⭐⭐
- **GitHub**: https://github.com/lackeyjb/playwright-skill
- **Stars**: 1,844 | **语言**: JavaScript
- **描述**: Claude Code 的 Playwright 浏览器自动化技能。模型调用式 - Claude 自主编写和执行自定义自动化测试和验证
- **核心功能**:
  - 模型调用式自动化（Claude 自主编写测试）
  - E2E 测试自动化
  - Web 测试验证
  - 无需手动编写测试脚本
- **适用场景**: 
  - 游戏 Web 客户端测试
  - 游戏官网/登录系统测试
  - 游戏内嵌 Web 页面测试
- **安装**: 复制到 `.claude/skills/` 目录

### 3.2 claude-code-playwright-mcp-test ⭐⭐⭐⭐
- **GitHub**: https://github.com/terryso/claude-code-playwright-mcp-test
- **Stars**: 164 | **语言**: JavaScript
- **描述**: 基于 YAML 的 Playwright MCP 自动化测试框架，专为 Claude Code 设计
- **核心功能**:
  - YAML 配置驱动测试
  - MCP 协议集成
  - Claude Code 原生支持
- **文档**: https://terryso.github.io/blog/yaml-playwright-testing-revolution
- **适用场景**: 低代码测试编写、游戏客户端 UI 自动化

### 3.3 playwright-bot-bypass ⭐⭐⭐
- **GitHub**: https://github.com/greekr4/playwright-bot-bypass
- **Stars**: 127 | **语言**: JavaScript
- **描述**: Claude Code 技能，用于绕过机器人检测（如 Google CAPTCHA）
- **核心功能**:
  - 反爬虫检测绕过
  - CAPTCHA 处理
  - 隐身浏览
- **适用场景**: 
  - 游戏客户端自动化测试（绕过反作弊）
  - 游戏数据采集
- **注意**: 仅用于合法测试目的

### 3.4 claude-cli-advanced-starter-pack ⭐⭐⭐
- **GitHub**: https://github.com/evan043/claude-cli-advanced-starter-pack
- **Stars**: 55 | **语言**: JavaScript
- **描述**: 高级 Claude Code CLI 工具包 - 代理、钩子、技能、MCP 服务器、分阶段开发、站点智能 dev-scan、GitHub 集成
- **核心功能**:
  - Playwright 集成
  - 站点智能扫描
  - 自动化测试工具链
- **适用场景**: 游戏客户端完整测试流程

---

## 4. 其他开发者工具

### 4.1 GitMCP ⭐⭐⭐⭐⭐
- **GitHub**: https://github.com/idosal/git-mcp
- **Stars**: 7,691 | **语言**: TypeScript
- **描述**: 终结代码幻觉！GitMCP 是免费开源的远程 MCP 服务器，适用于任何 GitHub 项目
- **核心功能**:
  - GitHub 项目代码检索
  - 代码上下文理解
  - 防止 AI 生成幻觉代码
- **官网**: https://gitmcp.io
- **适用场景**: 所有开发场景

### 4.2 DevDocs ⭐⭐⭐⭐⭐
- **GitHub**: https://github.com/cyberagiinc/DevDocs
- **Stars**: 2,037 | **语言**: TypeScript
- **描述**: 完全免费、私有的 UI 技术文档 MCP 服务器，专为程序员设计
- **核心功能**:
  - 技术文档聚合
  - 私有部署
  - UI 界面管理
  - 支持 Cursor, Windsurf, Cline, Roo Code, Claude Desktop
- **官网**: https://www.cyberagi.ai
- **适用场景**: 多框架/语言开发文档查询

### 4.3 pg-aiguide ⭐⭐⭐⭐
- **GitHub**: https://github.com/timescale/pg-aiguide
- **描述**: PostgreSQL 技能和文档的 MCP 服务器及 Claude 插件，帮助 AI 编程工具生成更好的 PostgreSQL 代码
- **核心功能**:
  - PostgreSQL 最佳实践
  - SQL 优化建议
  - TimescaleDB 支持
- **适用场景**: 游戏后端数据库开发

### 4.4 LLMDog ⭐⭐⭐
- **GitHub**: https://github.com/doganarif/LLMDog
- **Stars**: 78 | **语言**: Go
- **描述**: 命令行工具，帮助开发者与 Claude 和 ChatGPT 等大语言模型分享代码
- **核心功能**:
  - 代码片段分享
  - LLM 友好格式
  - 快速上下文构建
- **官网**: https://llmdog.arif.sh
- **适用场景**: 代码审查、问题诊断

### 4.5 miro-ai ⭐⭐⭐
- **GitHub**: https://github.com/miroapp/miro-ai
- **Stars**: 66 | **语言**: TypeScript
- **描述**: 官方 Miro AI 开发者工具和集成，包含 MCP 服务器配置、Claude Code 技能
- **核心功能**:
  - Miro 看板集成
  - 可视化协作
  - AI 辅助设计
- **适用场景**: 项目规划、团队协作

### 4.6 awesome-claude-code (jqueryscript) ⭐⭐⭐⭐
- **GitHub**: https://github.com/jqueryscript/awesome-claude-code
- **Stars**: 162
- **描述**: Claude Code 工具、IDE 集成、框架和资源的精选列表
- **官网**: https://www.scriptbyai.com/claude-code-resource-list/
- **适用场景**: 发现更多 Claude Code 工具

### 4.7 Useful-Skills-from-lyfX ⭐⭐⭐
- **GitHub**: https://github.com/andremoreira73/Useful-Skills-from-lyfX
- **描述**: lyfX.ai 实战级 Claude Code 技能 - 市场研究、LinkedIn 帖子、企业设计
- **核心功能**:
  - 市场研究自动化
  - 社交媒体内容生成
  - 企业级设计模板
- **适用场景**: 商业开发、市场分析

---

## 5. 热门 MCP 服务器汇总

| 名称 | Stars | 语言 | 用途 | 推荐度 |
|------|-------|------|------|--------|
| Serena | 20,941 | Python | 语义代码检索与编辑 | ⭐⭐⭐⭐⭐ |
| PAL MCP Server | 11,180 | Python | 多模型协作 | ⭐⭐⭐⭐⭐ |
| GitMCP | 7,691 | TypeScript | GitHub 项目代码检索 | ⭐⭐⭐⭐⭐ |
| DevDocs | 2,037 | TypeScript | 技术文档聚合 | ⭐⭐⭐⭐⭐ |
| playwright-skill | 1,844 | JavaScript | 浏览器自动化测试 | ⭐⭐⭐⭐⭐ |
| lazy-bird | 210 | Python | 通用开发自动化 | ⭐⭐⭐⭐⭐ |
| mcp-wireshark | 23 | Python | 网络流量分析 | ⭐⭐⭐ |

---

## 6. 快速推荐

### 游戏客户端开发推荐
1. **lazy-bird** - 支持 Godot，自动化功能开发
2. **Serena** - 大型项目代码理解和重构
3. **GitMCP** - GitHub 项目代码检索

### Python 开发推荐
1. **Serena** - 语义代码检索和编辑
2. **PAL MCP Server** - 多模型协作
3. **claude-arsenal** - 39+ 技能综合库
4. **koder** - 智能编程助手

### 游戏客户端自动化测试推荐
1. **playwright-skill** - 模型调用式 E2E 测试（强烈推荐）
2. **claude-code-playwright-mcp-test** - YAML 驱动测试框架
3. **playwright-bot-bypass** - 绕过机器人检测

### 通用开发者工具推荐
1. **GitMCP** - 防止代码幻觉
2. **DevDocs** - 技术文档聚合
3. **pg-aiguide** - PostgreSQL 开发辅助

---

## 安装指南

### MCP 服务器安装
```bash
# 大多数 MCP 服务器通过 npm 或 pip 安装
npm install -g @anthropic/mcp-server-name
# 或
pip install mcp-server-name
```

### Claude Code Skill 安装
```bash
# 克隆技能仓库
git clone https://github.com/xxx/skill-name.git

# 复制到 Claude Code 技能目录
cp -r skill-name ~/.claude/skills/
```

### Playwright Skill 安装
```bash
git clone https://github.com/lackeyjb/playwright-skill.git
cp -r playwright-skill ~/.claude/skills/playwright
```

---

## 相关资源

- [awesome-claude-code (hesreallyhim)](https://github.com/hesreallyhim/awesome-claude-code) - 最全 Claude Code 资源列表
- [awesome-claude-code (jqueryscript)](https://github.com/jqueryscript/awesome-claude-code) - 工具和集成列表
- [ClawHub](https://clawhub.com) - Agent Skills 发现平台
- [OpenClaw Docs](https://docs.openclaw.ai) - OpenClaw 文档

---

*文档生成时间: 2026-03-04 04:57 Asia/Shanghai*
