# Claude Code 热门插件补充调研 v84

> 游戏客户端 / Python / 自动化测试 / 开发者工具

---

## 调研概述

本次调研继续关注 Claude Code 热门插件，补充以下方向：
1. 游戏客户端开发
2. Python 开发
3. 游戏客户端自动化测试
4. 其他开发者工具

---

## 一、游戏客户端开发相关插件

### 1.1 MCP Unity - 主流 Unity MCP 集成方案

**项目信息**
- **GitHub**: [CoderGamester/mcp-unity](https://github.com/CoderGamester/mcp-unity)
- **⭐**: 1,382 | **Fork**: 170
- **语言**: C#
- **License**: MIT
- **创建时间**: 2025-03-13
- **最新更新**: 2026-03-04
- **标签**: game-development, unity, mcp, cursor, claude-code, codex-cli, windsurf

**核心功能**
Model Context Protocol (MCP) 插件，连接 Unity Editor 与各种 AI 助手（Cursor、Claude Code、Codex、Windsurf 等）。

**功能列表**
| 功能 | 说明 |
|------|------|
| 场景操作 | 创建、加载、保存、切换 Unity 场景 |
| 资源管理 | 创建、删除、查询 Unity 资源 |
| 脚本编辑 | 读取、修改 C# 脚本 |
| 游戏对象控制 | 创建、修改、删除 GameObject |
| 属性检查器 | 读取和修改组件属性 |
| 构建自动化 | 触发 Unity 构建流程 |

**安装配置**
```bash
# 通过 npm 安装
npm install mcp-unity

# 或克隆仓库
git clone https://github.com/CoderGamester/mcp-unity.git

# 在 Claude Code 配置中添加
{
  "mcpServers": {
    "unity": {
      "command": "npx",
      "args": ["-y", "mcp-unity"]
    }
  }
}
```

**技术特点**
- 跨 IDE 支持（Cursor、Claude Code、Codex、Windsurf）
- 支持 Unity 2020+ 版本
- 提供完整的 Unity API 封装

**优缺点**
✅ 活跃度高，1.3k+ stars  
✅ 跨多 AI 助手支持  
✅ 完整 Unity 集成  
⚠️ 需要 Unity Editor 运行  
⚠️ 部分功能需要特定 Unity 包

---

### 1.2 UnityAgentClient - 通用 AI Agent Unity 集成

**项目信息**
- **GitHub**: [nuskey8/UnityAgentClient](https://github.com/nuskey8/UnityAgentClient)
- **⭐**: 242 | **Fork**: 19
- **语言**: C#
- **License**: MIT
- **创建时间**: 2025-11-05
- **最新更新**: 2026-03-03
- **标签**: agentclientprotocol, ai-agent, unity

**核心功能**
提供任何 AI Agent（Gemini CLI、Claude Code、Codex CLI 等）与 Unity 编辑器的集成，使用 Agent Client Protocol。

**功能列表**
| 功能 | 说明 |
|------|------|
| Agent 协议支持 | 标准化 AI Agent 通信 |
| Unity 集成 | 与 Unity Editor 无缝连接 |
| 多 Agent 支持 | 支持各类主流 AI Agent |
| 命令执行 | 执行 Unity 控制台命令 |

**安装配置**
```bash
git clone https://github.com/nuskey8/UnityAgentClient.git
# 按照 Unity 包管理器导入
```

**应用场景**
- Unity 项目自动化
- AI 辅助游戏开发
- 批量处理 Unity 资源

**优缺点**
✅ 支持多 AI Agent  
✅ 标准化协议  
⚠️ 文档相对简略  
⚠️ 生态较小

---

### 1.3 Claude Code Game Studios - 48 AI 代理游戏工作室

**项目信息**
- **GitHub**: [Donchitos/Claude-Code-Game-Studios](https://github.com/Donchitos/Claude-Code-Game-Studios)
- **⭐**: 30 | **Fork**: 8
- **语言**: Shell
- **License**: MIT
- **创建时间**: 2026-02-12
- **最新更新**: 2026-03-04
- **标签**: ai-agents, claude-code, game-development, godot, unity, unreal-engine

**核心功能**
将 Claude Code 转变为完整的游戏开发工作室 - 48 个 AI 代理、36 个工作流技能，完整协调系统模拟真实工作室层级。

**功能列表**
| 功能 | 说明 |
|------|------|
| 48 专业代理 | 覆盖游戏开发各领域 |
| 36 工作流技能 | 完整开发流程支持 |
| 多引擎支持 | Godot、Unity、Unreal |
| 工作室层级 | 模拟真实开发团队 |

**支持引擎**
- Godot 4.x
- Unity (C#)
- Unreal Engine 5 (C++)

**安装配置**
```bash
git clone https://github.com/Donchitos/Claude-Code-Game-Studios.git
# 阅读文档配置代理
```

**优缺点**
✅ 48 个专业代理  
✅ 多引擎支持  
⚠️ Star 较少  
⚠️ 配置相对复杂

---

### 1.4 Gamekit CLI - Unity 游戏开发 CLI

**项目信息**
- **GitHub**: [gamekit-agent/gamekit-cli](https://github.com/gamekit-agent/gamekit-cli)
- **⭐**: 44 | **Fork**: 4
- **语言**: TypeScript
- **License**: MIT
- **创建时间**: 2026-01-23
- **最新更新**: 2026-03-01

**核心功能**
开源命令行工具，使用 Claude Code 开发 Unity 游戏。

**功能列表**
| 功能 | 说明 |
|------|------|
| CLI 交互 | 命令行开发 Unity |
| AI 集成 | Claude Code 辅助开发 |
| 项目管理 | Unity 项目管理 |

**安装配置**
```bash
npm install -g gamekit-cli
gamekit init my-game
```

**优缺点**
✅ 轻量级 CLI  
✅ 易于集成  
⚠️ 功能有限  
⚠️ 社区较小

---

### 1.5 Unity Claude Bridge - 文件协议连接

**项目信息**
- **GitHub**: [ManageXR/claude-unity-bridge](https://github.com/ManageXR/claude-unity-bridge)
- **⭐**: 15
- **语言**: C#
- **License**: MIT

**核心功能**
基于文件的命令协议，使 Claude Code 能够触发 Unity Editor 操作，专为多 Agent 和高度并行化工作流设计。

**应用场景**
- 多 Agent 协作开发
- 并行化 Unity 工作流
- 自动化测试集成

**优缺点**
✅ 支持并行化  
✅ 文件协议简单  
⚠️ 功能有限  
⚠️ 生态较小

---

## 二、Python 开发相关插件

### 2.1 Developer Kit - 全栈开发工具包

**项目信息**
- **GitHub**: [giuseppe-trisciuoglio/developer-kit](https://github.com/giuseppe-trisciuoglio/developer-kit)
- **⭐**: 133 | **Fork**: 9
- **语言**: Python
- **License**: MIT
- **创建时间**: 2025-10-21
- **最新更新**: 2026-03-04
- **标签**: claude-code, python, typescript, java, spring-boot, aws, skills

**核心功能**
Claude Code 模块化插件系统，提供可重用的技能、Agent 和命令，自动化开发任务。涵盖 Java/Spring Boot/LangChain4J、TypeScript/NestJS/React、Python、PHP/WordPress、AWS CloudFormation 和 AI 模式。

**功能列表**
| 功能 | 说明 |
|------|------|
| Java/Spring 技能 | Spring Boot、LangChain4J 开发 |
| TypeScript 技能 | NestJS、React 开发 |
| Python 技能 | Python 开发自动化 |
| PHP/WordPress | WordPress 开发 |
| AWS CloudFormation | IaC 自动化 |
| AI 模式 | 常见 AI 开发模式 |

**安装配置**
```bash
git clone https://github.com/giuseppe-trisciuoglio/developer-kit.git
# 选择需要的技能目录
```

**优缺点**
✅ 多语言支持  
✅ 模块化设计  
✅ 持续更新  
⚠️ 配置复杂  
⚠️ 部分技能需要特定环境

---

### 2.2 Python Template for Claude Code

**项目信息**
- **GitHub**: [discus0434/python-template-for-claude-code](https://github.com/discus0434/python-template-for-claude-code)
- **⭐**: 145 | **Fork**: 11
- **语言**: Python
- **License**: MIT
- **创建时间**: 2025-06-14
- **最新更新**: 2026-01-15
- **标签**: claude-code

**核心功能**
以 Claude Code 为中心的 Python 项目模板。

**功能列表**
| 功能 | 说明 |
|------|------|
| 项目结构 | 标准 Python 项目布局 |
| CLAUDE.md | Claude Code 上下文配置 |
| 技能集成 | 预置开发技能 |
| 自动化脚本 | 常见开发任务自动化 |

**安装配置**
```bash
git clone https://github.com/discus0434/python-template-for-claude-code.git
python -m pip install -r requirements.txt
```

**优缺点**
✅ 开箱即用  
✅ 结构清晰  
⚠️ 功能有限  
⚠️ 更新不活跃

---

### 2.3 DevKit - 52 专业技能开发工具包

**项目信息**
- **GitHub**: [CuriousLearner/devkit](https://github.com/CuriousLearner/devkit)
- **⭐**: 22 | **Fork**: 4
- **语言**: Shell
- **License**: MIT
- **创建时间**: 2025-10-20
- **最新更新**: 2026-02-13

**核心功能**
综合开发工具包：52 个 Claude Code 专业技能，涵盖开发、代码质量、API、数据库、安全、DevOps、数据分析和协作。

**功能列表**
| 功能 | 说明 |
|------|------|
| 开发技能 | 常见开发任务 |
| 代码质量 | Linting、格式化 |
| API 开发 | REST、GraphQL |
| 数据库 | SQL、ORM |
| 安全审计 | 常见安全问题 |
| DevOps | CI/CD、部署 |
| 数据分析 | 数据处理 |

**安装配置**
```bash
git clone https://github.com/CuriousLearner/devkit.git
# 按需选择技能
```

**优缺点**
✅ 技能丰富  
✅ 覆盖全面  
⚠️ Star 少  
⚠️ 文档有限

---

## 三、自动化测试相关插件

### 3.1 Auto Review ClaudeMCP - Unity PR 自动化审查

**项目信息**
- **GitHub**: [IskanderAl/Auto-Review-ClaudeMCP](https://github.com/IskanderAl/Auto-Review-ClaudeMCP)
- **⭐**: 19 | **Fork**: 0
- **语言**: Python
- **License**: MIT
- **创建时间**: 2026-02-21
- **最新更新**: 2026-02-26

**核心功能**
Python MCP 服务器，将 Claude Desktop 连接到 GitHub Pull Requests。获取 PR diff，过滤二进制和资源文件（Unity `.meta`、图片、音频、Shader 等），只向 Claude 提供实际代码审查。作为 QA 自动化工具加速 PR 审查。

**功能列表**
| 功能 | 说明 |
|------|------|
| PR 获取 | 获取 GitHub PR diff |
| 智能过滤 | 过滤二进制/资源文件 |
| 代码审查 | AI 驱动代码审查 |
| Unity 优化 | 专门处理 Unity 资源 |

**过滤的文件类型**
- Unity `.meta` 文件
- 图片（.png、.jpg、.psd）
- 音频文件
- Shader 文件
- 二进制资源

**安装配置**
```bash
pip install auto-review-claude-mcp
# 配置 MCP 服务器
```

**应用场景**
- Unity 项目 PR 审查
- 自动化代码审查
- 游戏项目质量保证

**优缺点**
✅ 专为游戏项目优化  
✅ 过滤不必要文件  
⚠️ 新项目，生态小  
⚠️ 主要针对 Unity

---

### 3.2 Agents Claude Code - 100 超专业 AI 代理

**项目信息**
- **GitHub**: [lodetomasi/agents-claude-code](https://github.com/lodetomasi/agents-claude-code)
- **⭐**: 124 | **Fork**: 29
- **语言**: Null
- **License**: MIT
- **创建时间**: 2025-08-01
- **最新更新**: 2026-03-04
- **标签**: ai-agents, ai-assistant, developer-tools, devops, python

**核心功能**
100 个超专业化 Claude Code AI 代理，将 Claude 转变为个人技术团队，包含 React、AWS、Kubernetes、ML、安全等领域的专家。

**功能列表**
| 功能 | 说明 |
|------|------|
| React 专家 | 前端开发代理 |
| AWS 专家 | 云服务代理 |
| Kubernetes | 容器编排代理 |
| ML 专家 | 机器学习代理 |
| 安全专家 | 安全审计代理 |
| DevOps | 运维自动化代理 |

**安装配置**
```bash
git clone https://github.com/lodetomasi/agents-claude-code.git
# 按需选择代理
```

**优缺点**
✅ 100 个专业代理  
✅ 覆盖广泛  
✅ 持续更新  
⚠️ 配置复杂  
⚠️ 部分代理需要特定环境

---

## 四、其他开发者工具

### 4.1 MCP SSH Manager - SSH 远程管理

**项目信息**
- **GitHub**: [bvisible/mcp-ssh-manager](https://github.com/bvisible/mcp-ssh-manager)
- **⭐**: 63 | **Fork**: 16
- **语言**: JavaScript
- **License**: MIT
- **创建时间**: 2025-08-12
- **最新更新**: 2026-03-04
- **标签**: mcp, ssh, devops, automation, claude-code, database, monitoring, backup

**核心功能**
MCP SSH 服务器：37 个远程 SSH 管理工具，支持 Claude Code 和 OpenAI Codex，用于 DevOps 自动化、备份、数据库操作、健康监控。

**功能列表**
| 功能 | 说明 |
|------|------|
| SSH 连接 | 远程服务器连接 |
| 文件操作 | 远程文件管理 |
| 数据库操作 | 远程数据库管理 |
| 健康监控 | 服务器健康检查 |
| 备份管理 | 自动备份任务 |
| 部署自动化 | 一键部署 |

**工具数量**: 37 个专业工具

**安装配置**
```bash
npm install mcp-ssh-manager
# 配置 SSH 连接
```

**应用场景**
- 远程服务器管理
- DevOps 自动化
- 数据库运维
- 监控告警

**优缺点**
✅ 37 个工具  
✅ DevOps 全面支持  
✅ 数据库集成  
⚠️ 需要 SSH 权限  
⚠️ 安全考虑

---

### 4.2 Claude K8s Plugin - Kubernetes CRD 运算符

**项目信息**
- **GitHub**: [Sagart-cactus/claude-k8s-plugin](https://github.com/Sagart-cactus/claude-k8s-plugin)
- **⭐**: 32
- **语言**: Shell
- **License**: MIT

**核心功能**
Claude Code 插件，用于使用 Webhook 和 Tilt 快速开发循环构建 Kubernetes CRD 运算符。

**功能列表**
| 功能 | 说明 |
|------|------|
| CRD 开发 | 自定义资源定义 |
| Webhook 支持 | 动态 webhook 配置 |
| Tilt 集成 | 快速开发循环 |

**安装配置**
```bash
git clone https://github.com/Sagart-cactus/claude-k8s-plugin.git
```

**应用场景**
- Kubernetes 运算符开发
- 自定义资源管理

**优缺点**
✅ K8s 深度集成  
✅ 快速开发循环  
⚠️ 生态较小  
⚠️ 需要 K8s 知识

---

### 4.3 Kube Audit Kit - Kubernetes 安全审计

**项目信息**
- **GitHub**: [crazygit/kube-audit-kit](https://github.com/crazygit/kube-audit-kit)
- **⭐**: 27
- **语言**: Shell

**核心功能**
Claude Code 技能，用于非侵入式 Kubernetes 集群安全审计。

**功能列表**
| 功能 | 说明 |
|------|------|
| 安全扫描 | 集群安全检查 |
| 配置审计 | K8s 配置审查 |
| 风险评估 | 安全风险识别 |

**安装配置**
```bash
git clone https://github.com/crazygit/kube-audit-kit.git
```

**优缺点**
✅ 安全专注  
✅ 非侵入式  
⚠️ 功能有限  
⚠️ 社区较小

---

### 4.4 MCP LibSQL - 数据库 MCP 服务器

**项目信息**
- **GitHub**: [Xexr/mcp-libsql](https://github.com/Xexr/mcp-libsql)
- **⭐**: 19
- **语言**: TypeScript

**核心功能**
面向 LibSQL 数据库的安全 MCP 服务器，提供全面工具、连接池和事务支持。为 Claude Desktop、Claude Code、Cursor 等 MCP 客户端构建。

**功能列表**
| 功能 | 说明 |
|------|------|
| 数据库操作 | CRUD 操作 |
| 连接池 | 高效连接管理 |
| 事务支持 | 原子操作 |
| 安全防护 | SQL 注入防护 |

**安装配置**
```bash
npm install mcp-libsql
```

**优缺点**
✅ 轻量级数据库  
✅ 安全防护  
⚠️ LibSQL 生态小  
⚠️ 功能有限

---

### 4.5 MCP Interactive Terminal - 交互式终端

**项目信息**
- **GitHub**: [amol21p/mcp-interactive-terminal](https://github.com/amol21p/mcp-interactive-terminal)
- **⭐**: 12

**核心功能**
MCP 服务器，为 AI Agent（Claude Code、Cursor、Windsurf）提供真实的交互式终端会话 - REPL、SSH、数据库、Docker 和任何交互式 CLI。

**功能列表**
| 功能 | 说明 |
|------|------|
| REPL 支持 | 交互式解释器 |
| SSH 会话 | 远程终端 |
| 数据库终端 | SQL REPL |
| Docker CLI | 容器交互 |
| 通用 CLI | 任何交互式命令 |

**安装配置**
```bash
npm install mcp-interactive-terminal
```

**应用场景**
- 交互式开发
- 远程运维
- 容器管理

**优缺点**
✅ 通用性强  
✅ 多场景支持  
⚠️ 安全性考虑  
⚠️ 配置复杂

---

## 五、热门插件对比分析

### 5.1 游戏开发插件对比

| 插件 | Stars | 特点 | 适用场景 |
|------|-------|------|----------|
| mcp-unity | 1,382 | 主流 Unity 集成 | Unity 项目必选 |
| UnityAgentClient | 242 | 通用 Agent 协议 | 多 Agent 协作 |
| Game Studios | 30 | 48 代理工作室 | 大型游戏团队 |
| gamekit-cli | 44 | 轻量 CLI | 快速开发 |

### 5.2 Python 开发插件对比

| 插件 | Stars | 特点 | 适用场景 |
|------|-------|------|----------|
| developer-kit | 133 | 全栈工具包 | 多语言项目 |
| python-template | 145 | 项目模板 | 新项目启动 |
| devkit | 22 | 52 技能 | 综合开发 |

### 5.3 自动化测试插件对比

| 插件 | Stars | 特点 | 适用场景 |
|------|-------|------|----------|
| Auto Review MCP | 19 | Unity PR 审查 | 游戏项目 |
| agents-claude-code | 124 | 100 代理 | 大型项目 |

---

## 六、总结与建议

### 本次调研发现

1. **游戏客户端开发**: mcp-unity 是最成熟的 Unity 集成方案，拥有 1.3k+ stars 和活跃的社区
2. **Python 开发**: developer-kit 提供全面的多语言支持，python-template 适合快速启动
3. **自动化测试**: Auto Review MCP 专注游戏项目 PR 审查
4. **开发者工具**: MCP SSH Manager (37 工具) 和 agents-claude-code (100 代理) 提供强大能力

### 推荐插件

| 类别 | 推荐插件 | 理由 |
|------|----------|------|
| 游戏开发 | mcp-unity | 最成熟，Stars 最高 |
| Python 开发 | developer-kit | 功能最全面 |
| 自动化测试 | Auto-Review-ClaudeMCP | 专注游戏项目 |
| DevOps | mcp-ssh-manager | 37 工具全覆盖 |

---

## 参考链接

- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
- [mcp-unity](https://github.com/CoderGamester/mcp-unity)
- [developer-kit](https://github.com/giuseppe-trisciuoglio/developer-kit)
- [mcp-ssh-manager](https://github.com/bvisible/mcp-ssh-manager)

---

*调研时间: 2026-03-05*
*版本: v84*
