# 补充调研 v91 - Claude Code 热门插件最新调研

> 更新日期: 2026-03-05
> 调研方向: 游戏客户端开发 | Python 开发 | 游戏客户端自动化测试 | 其他开发者工具

---

## 📋 调研概述

本次调研继续深入分析 Claude Code 热门插件，聚焦以下四个方向：
1. **游戏客户端开发** - Unity、Unreal、Godot 游戏引擎 MCP 集成
2. **Python 开发** - Python MCP 服务器、项目开发工具
3. **游戏客户端自动化测试** - 浏览器自动化、游戏测试工具
4. **其他开发者工具** - 自动化工作流、代码管理、工程工具

---

## 🎮 一、游戏客户端开发相关插件

### 1.1 mcp-unity (CoderGamester/mcp-unity)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 1,382 |
| **Forks** | 170 |
| **Language** | TypeScript |
| **更新** | 2026-03-04 |

**描述**: 主流 Unity MCP 集成方案，连接 LLMs 和高级 AI 代理到 Unity Editor。

**核心功能**:
- 场景操作与对象控制
- 资源管理和导入
- 脚本编辑和生成
- 构建自动化
- 调试和错误修复

**部署方式**:
```bash
npm install -g mcp-unity

# Claude Code 配置
{
  "mcpServers": {
    "unity": {
      "command": "npx",
      "args": ["-y", "mcp-unity"]
    }
  }
}
```

---

### 1.2 Unity-MCP (IvanMurzak/Unity-MCP)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 1,174 |
| **Forks** | 123 |
| **Language** | C# |
| **更新** | 2026-03-04 |

**描述**: AI-powered bridge connecting LLMs to Unity Editor via MCP.

**核心功能**:
- 完整的 Unity API 访问
- 场景图操作
- 组件管理
- 蓝图/脚本生成

---

### 1.3 mcp-unreal (remiphilippe/mcp-unreal)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 200+ |
| **Forks** | - |
| **Language** | Python |
| **更新** | 2026-02-23 |

**描述**: MCP server that gives AI coding agents (Claude Code, Cursor, etc.) full control over Unreal Engine 5.7 projects.

**核心功能**:
- 头无构建和测试
- Blueprint 编辑
- Actor 操作
- 程序化网格生成
- UE API 文档查询

**部署方式**:
```bash
pip install mcp-unreal
```

---

### 1.4 radial-hks/MCP-Unreal-Server

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 80+ |
| **Forks** | - |
| **Language** | Python |
| **更新** | 2026-01-29 |

**描述**: MCP Server implementation for interacting with Unreal Engine instances through remote Python execution.

**核心功能**:
- 远程 Unreal Engine 控制
- Python 执行集成
- 自动化构建流程

---

### 1.5 py-mcp-unreal (hannesdelbeke/py-mcp-unreal)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 50+ |
| **Forks** | - |
| **Language** | Python |
| **更新** | 2026-02-25 |

**描述**: MCP to let your AI run python code in Unreal.

**核心功能**:
- Unreal 内 Python 执行
- 自动化脚本运行
- 数据交换

---

### 1.6 mcp_godot_rag (weekitmo/mcp_godot_rag)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 40+ |
| **Forks** | - |
| **Language** | Python |
| **更新** | 2026-02-07 |

**描述**: This MCP server is used to provide Godot documentation to the Godot RAG model.

**核心功能**:
- Godot 文档 RAG
- API 查询
- 代码补全

---

### 1.7 MCP-Godot-sdk (SleeeepyZhou/MCP-Godot-sdk)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 30+ |
| **Forks** | - |
| **Language** | - |
| **更新** | 2025-07-28 |

**描述**: Used for rapid development of MCP applications in Godot.

---

## 🐍 二、Python 开发相关插件

### 2.1 mcp-python-interpreter (yzfly/mcp-python-interpreter)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 800+ |
| **Forks** | - |
| **Language** | Python |
| **更新** | 2026-02-05 |

**描述**: MCP Python Interpreter: run python code. Python-mcp-server, mcp-python-server, Code Executor.

**核心功能**:
- 动态 Python 代码执行
- 沙箱环境
- 数据处理
- 快速原型开发

**部署方式**:
```bash
pip install mcp-python-interpreter
```

---

### 2.2 dedalus-mcp-python (dedalus-labs/dedalus-mcp-python)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 600+ |
| **Forks** | - |
| **Language** | Python |
| **更新** | 2026-03-03 |

**描述**: A simple and performant Model Context Protocol framework for Python.

**核心功能**:
- 高性能 MCP 框架
- Python 原生支持
- 快速开发 MCP 服务

---

### 2.3 claude-code-skills (Ricko12vPL/claude-code-skills)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 500+ |
| **Forks** | - |
| **Language** | Python |
| **更新** | 2026-03-01 |

**描述**: Claude Code Skills - Python, Software Engineering, ML, Quantitative Finance.

**核心功能**:
- Python 开发技能
- 机器学习技能
- 量化金融技能
- 软件工程技能

---

### 2.4 hdresearch/mcp-python

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 100+ |
| **Forks** | - |
| **Language** | Python |
| **更新** | 2026-02-26 |

**描述**: A python repl for MCP.

**核心功能**:
- Python REPL 集成
- 交互式代码执行
- 调试支持

---

### 2.5 SamMorrowDrums/mcp-python-starter

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 80+ |
| **Forks** | - |
| **Language** | Python |
| **更新** | 2026-03-04 |

**描述**: A starter MCP server in Python.

**核心功能**:
- MCP 服务器模板
- 快速启动
- 最佳实践

---

### 2.6 mssql-mcp-python (lorenzouriel/mssql-mcp-python)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 70+ |
| **Forks** | - |
| **Language** | Python |
| **更新** | 2026-03-03 |

**描述**: MCP that provides controlled and secure SQL Server database access for LLM applications.

**核心功能**:
- SQL Server 集成
- 安全查询
- 数据库操作

---

### 2.7 cohere-ai/north-mcp-python-sdk

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 50+ |
| **Forks** | - |
| **Language** | Python |
| **更新** | 2026-03-04 |

**描述**: An SDK for creating MCP Servers with north.

**核心功能**:
- MCP SDK
- North 框架集成
- 快速构建 MCP

---

## 🧪 三、游戏客户端自动化测试相关插件

### 3.1 playwright-mcp

| 项目 | 详情 |
|------|------|
| **评分** | ⭐ 3.581 |
| **Language** | TypeScript |

**描述**: Playwright MCP 服务器，浏览器自动化测试工具。

**核心功能**:
- 浏览器自动化
- UI 测试
- 截图和录像
- 性能监控
- 游戏客户端测试

**部署方式**:
```bash
npm install -g @anthropic-ai/playwright-mcp
```

---

### 3.2 mcp-test-automation-poc (QAkarotto/mcp-test-automation-poc)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 50+ |
| **Forks** | - |
| **Language** | - |
| **更新** | 2025-08-05 |

**描述**: MCP test automation proof of concept.

**核心功能**:
- 自动化测试框架
- 测试用例生成
- 报告生成

---

### 3.3 Webapp Testing

**描述**: Tests local web applications using Playwright。

**核心功能**:
- 本地 Web 应用测试
- 前端功能验证
- UI 行为调试
- 截图功能

---

### 3.4 browserwing

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 100+ |
| **Language** | JavaScript |
| **更新** | 2026-03-05 |

**描述**: BrowserWing turns your browser actions into MCP commands or Claude Skill, allowing AI agents to control browsers efficiently and reliably.

**核心功能**:
- 浏览器操作 MCP
- 高效控制
- 自动化工作流

---

### 3.5 dev-browser (SawyerHood/dev-browser)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 200+ |
| **Language** | - |
| **更新** | 2026-03-05 |

**描述**: A Claude Skill to give your agent the ability to use a web browser.

**核心功能**:
- 浏览器控制
- 自动化测试
- 网页交互

---

## 🛠️ 四、其他开发者工具

### 4.1 awesome-claude-skills (ComposioHQ/awesome-claude-skills)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 40,814 |
| **Language** | Python |
| **更新** | 2026-03-05 |

**描述**: A curated list of awesome Claude Skills, resources, and tools for customizing Claude AI workflows.

**核心功能**:
- 40k+ Stars 超级集合
- 技能库索引
- 工作流模板

---

### 4.2 claude-scientific-skills (K-Dense-AI/claude-scientific-skills)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 12,905 |
| **Language** | Python |
| **更新** | 2026-03-05 |

**描述**: A set of ready-to-use Agent Skills for research, science, engineering, analysis, finance and writing.

**核心功能**:
- 科学研究技能
- 工程分析
- 金融分析
- 写作辅助

---

### 4.3 n8n-mcp (czlonkowski/n8n-mcp)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 14,341 |
| **Language** | TypeScript |
| **更新** | 2026-03-05 |

**描述**: n8n workflow automation with MCP.

**核心功能**:
- 工作流自动化
- n8n 集成
- 节点连接

---

### 4.4 pal-mcp-server (BeehiveInnovations/pal-mcp-server)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 11,189 |
| **Language** | Python |
| **更新** | 2026-03-05 |

**描述**: PAL (Personal AI Librarian) MCP Server.

**核心功能**:
- 个人 AI 助理
- 知识管理
- 文档处理

---

### 4.5 claude-code-toolkit (rohitg00/awesome-claude-code-toolkit)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 638 |
| **Language** | JavaScript |
| **更新** | 2026-03-05 |

**描述**: The most comprehensive toolkit for Claude Code -- 135 agents, 35 curated skills (+15,000 via SkillKit), 42 commands, 120 plugins, 19 hooks, 15 rules, 7 templates, 6 MCP configs.

**核心功能**:
- 135 代理
- 35 技能
- 42 命令
- 120 插件

---

### 4.6 antigravity-awesome-skills (sickn33/antigravity-awesome-skills)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 19,933 |
| **Language** | Python |
| **更新** | 2026-03-05 |

**描述**: 超大规模代理技能集合，978+ 技能跨 10+ AI 助手。

**核心功能**:
- 978+ 技能
- 10+ AI 助手支持
- 跨平台集成

---

### 4.7 Skill_Seekers (yusufkaraaslan/Skill_Seekers)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 10,213 |
| **Language** | Python |
| **更新** | 2026-03-05 |

**描述**: A comprehensive skill library for Claude Code.

**核心功能**:
- 多领域技能
- 自动化工作流
- 开发工具集

---

### 4.8 marketingskills (coreyhaines31/marketingskills)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 11,028 |
| **Language** | JavaScript |
| **更新** | 2026-03-05 |

**描述**: Marketing skills for Claude Code.

**核心功能**:
- 营销自动化
- 内容生成
- 社交媒体管理

---

### 4.9 claude-code-infrastructure-showcase (diet103/claude-code-infrastructure-showcase)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 9,151 |
| **Language** | Shell |
| **更新** | 2026-03-05 |

**描述**: Infrastructure as Code showcase for Claude Code.

**核心功能**:
- IaC 模板
- 基础设施自动化
- 云资源管理

---

### 4.10 Claudeception (blader/Claudeception)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 1,920 |
| **Language** | Shell |
| **更新** | 2026-03-05 |

**描述**: Claude Code within Claude Code - nested AI execution.

**核心功能**:
- 嵌套 AI 执行
- 多代理协作
- 任务分解

---

### 4.11 claude-esp (phiat/claude-esp)

**描述**: Go-based TUI streaming Claude Code's hidden output.

**核心功能**:
- 隐藏输出流
- 多会话监控
- 内容过滤
- 调试支持

---

### 4.12 claude-tmux (nielsgroen/claude-tmux)

**描述**: Manage Claude Code within tmux.

**核心功能**:
- tmux 集成
- 会话管理
- 状态监控
- 快速切换

---

### 4.13 parry (vaporif/parry)

**描述**: Prompt injection scanner for Claude Code hooks.

**核心功能**:
- 注入攻击检测
- 敏感信息扫描
- 数据泄露防护

---

### 4.14 Dippy (ldayton/Dippy)

**描述**: Auto-approve safe bash commands using AST-based parsing.

**核心功能**:
- AST 解析
- 自动批准安全命令
- 危险操作提示

---

### 4.15 mcp-ssh-manager

**描述**: SSH 远程管理工具。

**核心功能**:
- 37 工具
- 远程连接
- 服务器管理

---

### 4.16 superpowers

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 4.1k+ |

**描述**: 核心工程技能集，SDLC 全流程覆盖。

**核心功能**:
- 规划、审查、测试、调试
- Git 工作流
- 代码质量
- 文档生成

---

## 📊 五、热门插件汇总表

| 插件名称 | 方向 | Stars | 功能描述 |
|----------|------|-------|----------|
| awesome-claude-skills | 综合 | ⭐ 40,814 | 超大技能集合 |
| claude-scientific-skills | 科学研究 | ⭐ 12,905 | 科研分析技能 |
| n8n-mcp | 开发者工具 | ⭐ 14,341 | 工作流自动化 |
| pal-mcp-server | 开发者工具 | ⭐ 11,189 | AI 知识管理 |
| mcp-unity | 游戏开发 | ⭐ 1,382 | Unity MCP 集成 |
| Unity-MCP | 游戏开发 | ⭐ 1,174 | Unity AI 桥接 |
| marketingskills | 营销 | ⭐ 11,028 | 营销自动化 |
| Skill_Seekers | 综合 | ⭐ 10,213 | 多领域技能 |
| claude-code-infrastructure-showcase | DevOps | ⭐ 9,151 | IaC 模板 |
| mcp-python-interpreter | Python | ⭐ 800+ | Python 代码执行 |
| mcp-unreal | 游戏开发 | ⭐ 200+ | Unreal MCP |
| superpowers | 开发者工具 | ⭐ 4.1k+ | 核心工程技能 |
| dev-browser | 测试 | ⭐ 200+ | 浏览器控制 |
| pydantic-ai-skills | Python | ⭐ 136 | Pydantic 开发 |
| playwright-mcp | 测试 | 3.581 | 浏览器自动化 |

---

## 🎯 六、推荐插件

### 游戏开发推荐
1. **mcp-unity** - Unity 官方推荐集成 (1.3k+ Stars)
2. **Unity-MCP** - 完整 Unity API 访问 (1.1k+ Stars)
3. **mcp-unreal** - Unreal Engine 5.7 完整控制

### Python 开发推荐
1. **mcp-python-interpreter** - Python 代码执行器
2. **dedalus-mcp-python** - 高性能 MCP 框架
3. **claude-code-skills** - Python/ML/金融技能

### 测试推荐
1. **playwright-mcp** - 浏览器自动化测试
2. **dev-browser** - Claude 浏览器控制技能
3. **browserwing** - 浏览器操作 MCP

### 开发者工具推荐
1. **awesome-claude-skills** - 40k+ Stars 超级集合
2. **n8n-mcp** - 工作流自动化 (14k+ Stars)
3. **superpowers** - 核心工程技能集 (4.1k+ Stars)
4. **antigravity-awesome-skills** - 978+ 超大技能集合

---

## 📝 总结

Claude Code 插件生态持续繁荣，本次调研发现以下趋势：

1. **游戏开发**: 
   - Unity MCP 最为成熟 (1.3k+ Stars)
   - Unreal MCP 快速发展
   - Godot MCP 开始出现

2. **Python**: 
   - mcp-python-interpreter 受关注
   - MCP Python SDK 框架涌现
   - 数据库集成 MCP 增加

3. **测试**: 
   - Playwright 集成是主流选择
   - 浏览器控制技能多样化
   - 自动化测试 MCP 出现

4. **开发者工具**: 
   - awesome-claude-skills 达到 40k+ Stars
   - n8n-mcp 工作流集成 (14k+ Stars)
   - 专业化技能集合增多

---

## 🔗 相关链接

- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
- [awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills)
- [mcp-unity](https://github.com/CoderGamester/mcp-unity)
- [mcp-unreal](https://github.com/remiphilippe/mcp-unreal)
- [mcp-python-interpreter](https://github.com/yzfly/mcp-python-interpreter)

---

*文档生成时间: 2026-03-05*
