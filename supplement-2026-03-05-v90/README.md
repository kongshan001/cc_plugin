# 补充调研 v90 - Claude Code 热门插件最新调研

> 更新日期: 2026-03-05
> 调研方向: 游戏客户端开发 | Python 开发 | 游戏客户端自动化测试 | 其他开发者工具

---

## 📋 调研概述

本次调研继续深入分析 Claude Code 热门插件，聚焦以下四个方向：
1. **游戏客户端开发** - Unity、Unreal、Godot 游戏引擎集成
2. **Python 开发** - Python 项目模板、Django/Flask 开发
3. **游戏客户端自动化测试** - 浏览器自动化、游戏测试工具
4. **其他开发者工具** - 调试工具、协作平台、工程工作流

---

## 🎮 一、游戏客户端开发相关插件

### 1.1 claude-code-game-studios (The1Studio/claude-code-game-studios)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 26-30 |
| **Forks** | - |
| **Language** | - |
| **更新** | 持续更新 |

**描述**: 48 个 AI 代理 + 36 个工作流技能的全栈游戏开发系统。

**核心功能**:
- Director → Lead → Specialist 三层架构
- 48 个专业 AI 代理
- 36 个工作流技能
- 支持 Unity/Unreal/Godot/WebGL

**部署方式**:
```bash
git clone https://github.com/The1Studio/claude-code-game-studios ~/.claude/plugins/
```

**优缺点分析**:
| 优点 | 缺点 |
|------|------|
| 完整团队模拟 | 资源消耗大 |
| 工作流自动化 | 复杂度高 |

---

### 1.2 cc-plugin-unity-gamedev

**描述**: 21 个专业 Unity 技能集合。

**核心功能**:
- Unity 游戏开发技能
- 场景管理
- 资源优化
- 调试和性能分析

---

### 1.3 godot-development

**描述**: Godot 游戏开发技能集合。

**核心功能**:
- Godot 引擎集成
- GDScript 脚本编写
- 2D/3D 游戏开发
- 场景和节点操作

**部署方式**:
```bash
git clone https://github.com/xxx/godot-development ~/.claude/plugins/
```

---

### 1.4 mcp-unity (CoderGamester/mcp-unity)

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
```

---

### 1.5 Unity-MCP (IvanMurzak/Unity-MCP)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 1,174 |
| **Forks** | 123 |
| **Language** | C# |
| **更新** | 2026-03-04 |

**描述**: AI-powered bridge connecting LLMs to Unity Editor via MCP.

---

### 1.6 unreal-mcp (codex精/unreal-mcp)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 245 |
| **Forks** | 28 |
| **Language** | Python |
| **更新** | 2026-03-03 |

**描述**: Unreal Engine MCP server。

---

## 🐍 二、Python 开发相关插件

### 2.1 pydantic-ai-skills

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 136 |

**描述**: Pydantic AI 开发技能集合。

**核心功能**:
- Pydantic 模型定义
- 数据验证
- API 开发
- 类型安全

---

### 2.2 fastapi-development

**描述**: FastAPI 开发技能集合。

**核心功能**:
- RESTful API 开发
- 异步编程
- 自动文档生成
- 中间件配置
- 依赖注入

---

### 2.3 pypict-claude-skill

**描述**: PICT 成对测试用例生成技能。

**核心功能**:
- 组合测试用例生成
- 正交测试设计
- 测试覆盖优化
- Python 项目测试

---

### 2.4 read-only-postgres

**描述**: Read-only PostgreSQL query skill for Claude Code。

**核心功能**:
- SELECT/SHOW/EXPLAIN/WITH 查询
- 多连接支持
- 安全验证
- 超时和行限制

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

### 3.2 playwright-skill

**描述**: Model-invoked Playwright automation for testing。

**核心功能**:
- 前端功能测试
- UI 行为验证
- 截图捕获
- 调试支持

---

### 3.3 Webapp Testing

**描述**: Tests local web applications using Playwright。

**核心功能**:
- 本地 Web 应用测试
- 前端功能验证
- UI 行为调试
- 截图功能

---

### 3.4 iOS Simulator

**描述**: Enables Claude to interact with iOS Simulator。

**核心功能**:
- iOS 模拟器交互
- 应用测试
- 调试支持

---

## 🛠️ 四、其他开发者工具

### 4.1 superpowers

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

### 4.2 cc-devops-skills

**描述**: DevOps 工程师技能集，IaC 自动化。

**核心功能**:
- 基础设施即代码
- 部署自动化
- 云平台集成
- CI/CD 流水线

---

### 4.3 pr-review-toolkit

**描述**: 官方 PR 审查工具包，6 专业代理。

**核心功能**:
- 代码审查
- 自动化检查
- 质量分析
- 安全扫描

---

### 4.4 security-guidance

**描述**: 官方安全提醒钩子，9 种安全模式。

**核心功能**:
- 安全模式检测
- 漏洞预防
- 安全最佳实践

---

### 4.5 claude-tmux

**描述**: Claude Code tmux 会话管理工具。

**核心功能**:
- tmux 集成
- 会话管理
- 状态监控
- 快速切换

**部署方式**:
```bash
git clone https://github.com/nielsgroen/claude-tmux ~/.claude/plugins/
```

---

### 4.6 claude-esp

**描述**: Go-based TUI streaming Claude Code's hidden output。

**核心功能**:
- 隐藏输出流
- 多会话监控
- 内容过滤
- 调试支持

---

### 4.7 AgentSys

**描述**: 工作流自动化系统。

**核心功能**:
- 任务到生产工作流
- PR 管理
- 代码清理
- 性能调查
- 多代理代码审查

---

### 4.8 sudocode

**描述**: 轻量级代理编排工具。

**核心功能**:
- 规范管理
- 任务编排
- Git 原生集成

---

### 4.9 parry

**描述**: 提示注入扫描器。

**核心功能**:
- 注入攻击检测
- 敏感信息扫描
- 数据泄露防护

---

### 4.10 Dippy

**描述**: Bash 命令过滤器。

**核心功能**:
- AST 解析
- 自动批准安全命令
- 危险操作提示
- 权限疲劳减少

---

### 4.11 context7-mcp-server

**描述**: Context7 MCP 服务器，50+ 框架支持。

**核心功能**:
- 上下文管理
- 框架集成
- 智能加载

---

### 4.12 claude-mem

**描述**: 智能记忆系统。

**核心功能**:
- 自动上下文捕获
- AI 压缩
- 会话记忆

---

### 4.13 agents-claude-code

**描述**: 100 超专业 AI 代理集合。

**核心功能**:
- 多代理协作
- 专业任务处理
- 工作流自动化

---

### 4.14 developer-kit

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 133 |

**描述**: 全栈开发工具包。

---

### 4.15 mcp-ssh-manager

**描述**: SSH 远程管理工具。

**核心功能**:
- 37 工具
- 远程连接
- 服务器管理

---

### 4.16 git-context-controller

**描述**: Git 风格上下文管理框架。

**核心功能**:
- 上下文切换
- 状态管理
- Git 集成

---

## 📊 五、热门插件汇总表

| 插件名称 | 方向 | Stars | 功能描述 |
|----------|------|-------|----------|
| mcp-unity | 游戏开发 | ⭐ 1,382 | Unity MCP 集成 |
| Unity-MCP | 游戏开发 | ⭐ 1,174 | Unity AI 桥接 |
| superpowers | 开发者工具 | ⭐ 4.1k+ | 核心工程技能 |
| cc-devops-skills | 开发者工具 | - | DevOps 自动化 |
| pydantic-ai-skills | Python | ⭐ 136 | Pydantic 开发 |
| playwright-mcp | 测试 | 3.581 | 浏览器自动化 |
| claude-code-game-studios | 游戏开发 | ⭐ 26-30 | 48 AI 代理游戏工作室 |
| claude-tmux | 开发者工具 | - | tmux 集成 |
| context7-mcp-server | 开发者工具 | - | 上下文管理 |
| antigravity-awesome-skills | 综合 | ⭐ 900+ | 978+ 超大技能集合 |

---

## 🎯 六、推荐插件

### 游戏开发推荐
1. **mcp-unity** - Unity 官方推荐集成
2. **claude-code-game-studios** - 全栈游戏开发团队

### Python 开发推荐
1. **pydantic-ai-skills** - Pydantic AI 开发
2. **fastapi-development** - FastAPI 开发

### 测试推荐
1. **playwright-mcp** - 浏览器自动化测试
2. **Webapp Testing** - Web 应用测试

### 开发者工具推荐
1. **superpowers** - 核心工程技能集
2. **cc-devops-skills** - DevOps 自动化
3. **claude-tmux** - tmux 会话管理

---

## 📝 总结

Claude Code 插件生态持续繁荣，本次调研发现以下趋势：

1. **游戏开发**: Unity MCP 最为成熟，1.3k+ Stars
2. **Python**: Pydantic AI 技能集关注度高
3. **测试**: Playwright 集成是主流选择
4. **开发者工具**: superpowers (4.1k+ Stars) 是最受欢迎的工程技能集

---

*文档生成时间: 2026-03-05*
