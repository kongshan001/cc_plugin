# Claude Code 热门插件补充调研 v82

> 游戏客户端 / Python / 自动化测试 / 开发者工具

---

## 调研概述

本次调研继续关注 Claude Code 热门插件，涵盖以下方向：
1. 游戏客户端开发
2. Python 开发
3. 游戏客户端自动化测试
4. 其他开发者工具

---

## 一、游戏客户端开发相关插件

### 1.1 Unity MCP Server

**项目信息**
- **GitHub**: [CoplayDev/unity-mcp](https://github.com/CoplayDev/unity-mcp)
- **语言**: C#
- **最新更新**: 2026-03-03

**核心功能**
- AI 助手（Claude、Cursor）与 Unity Editor 之间的桥梁
- 提供工具让 LLM 管理资源、控制场景、编辑脚本
- 自动化 Unity 项目中的各种任务

**功能列表**
| 功能 | 说明 |
|------|------|
| 资产管理 | 创建、删除、查询 Unity 资源 |
| 场景控制 | 加载、保存、切换场景 |
| 脚本编辑 | 读取和修改 C# 脚本 |
| 任务自动化 | 自动执行重复性开发任务 |

**安装配置**
```bash
# 克隆仓库
git clone https://github.com/CoplayDev/unity-mcp.git

# 按照文档配置 MCP 服务器
# 需要在 Unity 中安装对应包
```

**应用场景**
- Unity 游戏自动化构建
- 资源批量处理
- 场景管理辅助

---

### 1.2 Claude Code Game Studios

**项目信息**
- **GitHub**: 多个相关项目
- **⭐**: 26-30
- **类别**: 游戏开发工作室

**核心功能**
- 48 个 AI 代理专注于游戏开发
- 支持 Godot 4、Unity、Unreal Engine 5
- 36 个工作流技能覆盖游戏开发全流程

**支持引擎**
- Godot 4.x
- Unity (C#)
- Unreal Engine 5 (C++)

---

## 二、Python 开发相关插件

### 2.1 Claude Scientific Skills

**项目信息**
- **GitHub**: [K-Dense-AI/claude-scientific-skills](https://github.com/K-Dense-AI/claude-scientific-skills)
- **开发者**: K-Dense

**核心功能**
- 科学研究、工程、分析、金融和写作的即用型代理技能
- 包含研究、科学、工程领域的专业技能集
- 可作为 AI 代理使用

**技能分类**
- 🔬 研究技能
- 📊 分析技能
- 💰 金融技能
- ✍️ 写作技能

**特点**
- 文档详尽，质量优秀
- 适合深度研究任务
- 可作为学习资源

---

### 2.2 FastMCP

**项目信息**
- **GitHub**: [PrefectHQ/fastmcp](https://github.com/PrefectHQ/fastmcp)
- **语言**: Python
- **最新更新**: 2026-03-04

**核心功能**
- 快速构建 MCP 服务器和客户端的 Pythonic 方式
- 简化的 MCP 协议实现
- 适合快速原型开发

**特点**
- 🚀 快速开发
- 📘 Pythonic API
- 🧪 测试友好

---

### 2.3 read-only-postgres

**项目信息**
- **GitHub**: [jawwadfirdousi/agent-skills](https://github.com/jawwadfirdousi/agent-skills)

**核心功能**
- Claude Code 的只读 PostgreSQL 查询技能
- 支持 SELECT/SHOW/EXPLAIN/WITH 查询
- 严格的验证和超时控制

**功能列表**
- 多数据库连接支持
- 行数限制保护
- 查询超时控制
- 数据库描述选择

---

## 三、自动化测试相关插件

### 3.1 Playwright MCP

**项目信息**
- **GitHub**: 官方 MCP 服务器
- **评分**: 3.581

**核心功能**
- 浏览器自动化测试
- 网页抓取和交互
- 跨浏览器测试支持

**应用场景**
- 游戏客户端 UI 自动化测试
- 网页游戏功能测试
- 回归测试

---

### 3.2 Claude Code Agents

**项目信息**
- **GitHub**: [undeadlist/claude-code-agents](https://github.com/undeadlist/claude-code-agents)
- **开发者**: Paul - UndeadList

**核心功能**
- 全面的 E2E 开发工作流
- 为独立开发者设计的 Claude Code 子代理提示
- 并行运行多个审计器

**功能列表**
- 多审计器并行执行
- 微检查点协议的自动化修复循环
- 基于浏览器的 QA
- 严格的协议防止 AI 失控

---

## 四、开发者工具相关插件

### 4.1 AgentSys

**项目信息**
- **GitHub**: [avifenesh/agentsys](https://github.com/avifenesh/agentsys)
- **特点**: 工作流自动化系统

**核心功能**
- 任务到生产工作流自动化
- PR 管理
- 代码清理
- 性能调查
- 漂移检测
- 多代理代码审查

**技术特点**
- 使用正则表达式和 AST 的确定性检测
- LLM 判断提高效率
- 包含 agnix 用于 linting 代理配置
- 经过数千行代码和数千测试验证
- 用于许多生产系统

---

### 4.2 Superpowers

**项目信息**
- **GitHub**: [obra/superpowers](https://github.com/obra/superpowers)
- **⭐**: 4.1k+
- **开发者**: Jesse Vincent

**核心功能**
- 软件工程核心能力集合
- 覆盖 SDLC 的大部分流程

**包含能力**
- 📋 规划
- 🔍 审查
- 🧪 测试
- 🐛 调试

**特点**
- 编写良好，组织良好
- 适应性强
- 工程最佳实践集合

---

### 4.3 cc-devops-skills

**项目信息**
- **GitHub**: [akin-ozer/cc-devops-skills](https://github.com/akin-ozer/cc-devops-skills)

**核心功能**
- DevOps 工程师的详细技能集
- 验证、生成器、Shell 脚本和 CLI 工具
- 为各种平台创建高质量 IaC 代码

**特点**
- 极其详细
- 适合任何需要部署代码的人
- 即使只作为文档来源也值得下载

---

### 4.4 Claude Code Templates

**项目信息**
- **GitHub**: [davila7/claude-code-templates](https://github.com/davila7/claude-code-templates)
- **开发者**: Daniel Avila

**核心功能**
- 令人难以置信的各类资源集合
- 精美的 UI 展示
- 使用仪表板和分析功能

**功能列表**
- Slash 命令
- Hooks
- Agents
- 使用情况仪表板

---

### 4.5 Fullstack Dev Skills

**项目信息**
- **GitHub**: [jeffallan/claude-skills](https://github.com/jeffallan/claude-skills)

**核心功能**
- 全面的 Claude Code 插件
- 65 个专业技能覆盖全栈开发
- 9 个项目工作流命令

**特点**
- 支持多种框架
- Jira/Confluence 集成
- 上下文工程方法
- `/common-ground` 命令揭示 Claude 的隐藏假设

---

### 4.6 Claude CodePro

**项目信息**
- **GitHub**: [maxritter/claude-codepro](https://github.com/maxritter/claude-codepro)
- **开发者**: Max Ritter

**核心功能**
- Claude Code 专业开发环境
- Spec 驱动工作流
- TDD 强制执行
- 跨会话内存

**功能列表**
- 语义搜索
- 质量 hooks
- 模块化规则集成

---

### 4.7 Context Engineering Kit

**项目信息**
- **GitHub**: [NeoLabHQ/context-engineering-kit](https://github.com/NeoLabHQ/context-engineering-kit)
- **开发者**: Vlad Goncharov

**核心功能**
- 高级上下文工程技术和模式
- 最小化 token 占用
- 专注于提高代理结果质量

**特点**
- 手工艺制作
- 极简 token 足迹
- 质量导向

---

### 4.8 Everything Claude Code

**项目信息**
- **GitHub**: [affaan-m/everything-claude-code](https://github.com/affaan-m/everything-claude-code)
- **开发者**: Affaan Mustafa
- **最新更新**: 2026-03-05

**核心功能**
- 涵盖核心工程领域的顶级资源
- 大多数资源有独立价值
- 涵盖几乎所有 Claude Code 功能

**特点**
- 编写优秀
- 独立资源有示例作用
- 可选择加入作者的工作流模式

---

### 4.9 Claude Code Settings

**项目信息**
- **GitHub**: [fcakyon/claude-codex-settings](https://github.com/fcakyon/claude-codex-settings)
- **开发者**: fatih akyon

**核心功能**
- 组织良好的插件集
- 涵盖核心开发者活动
- 支持常见云平台

**支持平台**
- GitHub
- Azure
- MongoDB
- Tavily
- Playwright

---

### 4.10 Trail of Bits Security Skills

**项目信息**
- **GitHub**: [trailofbits/skills](https://github.com/trailofbits/skills)
- **开发者**: Trail of Bits

**核心功能**
- 专业安全技能集
- 代码审计和漏洞检测
- 超过一打安全技能

**功能列表**
- CodeQL 静态分析
- Semgrep 集成
- 变体分析
- 修复验证
- 差异代码审查

---

## 五、MCP 服务器相关

### 5.1 MCP for Beginners

**项目信息**
- **GitHub**: [microsoft/mcp-for-beginners](https://github.com/microsoft/mcp-for-beginners)
- **开发者**: Microsoft
- **最新更新**: 2026-03-04

**核心功能**
- MCP 基础的开源课程
- 跨语言示例
- .NET, Java, TypeScript, JavaScript, Rust, Python

**特点**
- 实用的 AI 工作流构建技术
- 从会话设置到服务编排
- 适合开发者学习

---

### 5.2 MCP Use

**项目信息**
- **GitHub**: [mcp-use/mcp-use](https://github.com/mcp-use/mcp-use)
- **最新更新**: 2026-03-04
- **语言**: TypeScript

**核心功能**
- 全栈 MCP 框架
- 为 ChatGPT/Claude 开发 MCP 应用
- 为 AI Agents 开发 MCP 服务器

---

### 5.3 IBM MCP Context Forge

**项目信息**
- **GitHub**: [IBM/mcp-context-forge](https://github.com/IBM/mcp-context-forge)
- **最新更新**: 2026-03-05
- **语言**: Python

**核心功能**
- AI 网关、注册表和代理
- 位于任何 MCP、A2A 或 REST/gRPC API 前面
- 统一端点，集中发现、护栏和管理

---

### 5.4 Firecrawl MCP Server

**项目信息**
- **GitHub**: [firecrawl/firecrawl-mcp-server](https://github.com/firecrawl/firecrawl-mcp-server)
- **最新更新**: 2026-03-03
- **语言**: JavaScript

**核心功能**
- 官方 Firecrawl MCP 服务器
- 强大的网页抓取和搜索能力
- 支持 Cursor、Claude 和其他 LLM 客户端

---

### 5.5 Exa MCP Server

**项目信息**
- **GitHub**: [exa-labs/exa-mcp-server](https://github.com/exa-labs/exa-mcp-server)
- **语言**: TypeScript
- **最新更新**: 2026-03-04

**核心功能**
- 网页搜索和抓取
- AI 驱动的搜索能力

---

## 六、总结与推荐

### 6.1 游戏开发推荐

| 插件 | 适用场景 | 优先级 |
|------|----------|--------|
| Unity MCP | Unity 项目自动化 | ⭐⭐⭐⭐⭐ |
| Claude Code Game Studios | 多引擎游戏开发 | ⭐⭐⭐⭐ |
| Godot Development | Godot 项目开发 | ⭐⭐⭐⭐ |

### 6.2 Python 开发推荐

| 插件 | 适用场景 | 优先级 |
|------|----------|--------|
| FastMCP | 快速构建 MCP | ⭐⭐⭐⭐⭐ |
| Claude Scientific Skills | 科学研究 | ⭐⭐⭐⭐ |
| read-only-postgres | 数据库查询 | ⭐⭐⭐⭐ |

### 6.3 测试自动化推荐

| 插件 | 适用场景 | 优先级 |
|------|----------|--------|
| Playwright MCP | UI 自动化测试 | ⭐⭐⭐⭐⭐ |
| Claude Code Agents | E2E 测试 | ⭐⭐⭐⭐ |

### 6.4 开发者工具推荐

| 插件 | 适用场景 | 优先级 |
|------|----------|--------|
| Superpowers | 通用开发 | ⭐⭐⭐⭐⭐ |
| AgentSys | 工作流自动化 | ⭐⭐⭐⭐⭐ |
| Claude CodePro | 专业开发环境 | ⭐⭐⭐⭐ |
| Trail of Bits | 安全审计 | ⭐⭐⭐⭐ |

---

## 参考链接

- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
- [awesome-mcp-servers](https://github.com/appcypher/awesome-mcp-servers)
- [model-context-protocol](https://github.com/topics/model-context-protocol)

---

*调研时间: 2026-03-05*
*版本: v82*
