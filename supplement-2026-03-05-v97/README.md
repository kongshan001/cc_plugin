# 补充调研 v97 - Claude Code 热门插件最新调研

> 更新日期: 2026-03-05
> 调研方向: 游戏客户端开发 | Python 开发 | 游戏客户端自动化测试 | 其他开发者工具

---

## 📋 调研概述

本次调研继续深入分析 Claude Code 热门插件，聚焦以下四个方向：
1. **游戏客户端开发** - Unity、Unreal、Godot 游戏引擎集成
2. **Python 开发** - Python 项目模板、Django/Flask 开发、代码重构
3. **游戏客户端自动化测试** - 浏览器自动化、游戏测试工具、QA 工作流
4. **其他开发者工具** - 调试工具、协作平台、工程工作流、MCP 服务器

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

### 1.2 mcp-unity (CoderGamester/mcp-unity)

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

**优缺点分析**:
| 优点 | 缺点 |
|------ 官方维护|------|
|活跃 | 需要 Unity Editor |
| 功能全面 | 配置复杂 |

---

### 1.3 OH-Unity-GameDev-Skills (OstrichHermit/OH-Unity-GameDev-Skills)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 6 |
| **Forks** | 1 |
| **Language** | Python |
| **License** | MIT |

**描述**: 符合 Claude Code Skills 规范的 Unity 游戏开发代理技能集合。

**核心功能**:
- Unity 引擎集成
- C# 脚本开发
- 资源管理
- 构建配置

**部署方式**:
```bash
git clone https://github.com/OstrichHermit/OH-Unity-GameDev-Skills ~/.claude/plugins/
```

---

### 1.4 unity-ai-workflow (David-GD13/unity-ai-workflow)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 4 |
| **Forks** | - |
| **Language** | - |

**描述**: AI-first Unity 6.2+ 游戏开发工作流 — 规则、代理、技能和斜杠命令。

**核心功能**:
- Unity 6.2+ 支持
- AI 驱动开发工作流
- Claude Code 集成
- Antigravity 支持

**部署方式**:
```bash
git clone https://github.com/David-GD13/unity-ai-workflow ~/.claude/plugins/
```

---

### 1.5 unreal-engine-skills (quodsoler/unreal-engine-skills)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 1 |
| **Forks** | 0 |
| **Language** | - |
| **License** | MIT |

**描述**: Unreal Engine C++ 技能，面向 AI 编码代理。27 个技能覆盖游戏玩法、渲染、网络、动画等。

**核心功能**:
- Unreal Engine C++ 开发
- 游戏玩法编程
- 渲染系统
- 网络编程
- 动画系统

**部署方式**:
```bash
git clone https://github.com/quodsoler/unreal-engine-skills ~/.claude/plugins/
```

---

### 1.6 godot-development

**描述**: Godot 游戏开发技能集合。

**核心功能**:
- Godot 引擎集成
- GDScript 脚本编写
- 2D/3D 游戏开发
- 场景和节点操作

---

### 1.7 claudeforge

**描述**: CLAUDE.md 生成和维护工具。

**核心功能**:
- 自动生成项目文档
- 维护代码库知识
- 上下文管理

---

### 1.8 gamemaker-skills (leihaht/gamemaker-skills)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 2 |
| **Forks** | - |

**描述**: GameMaker Studio 2 和 GML 开发的 Claude Code 技能。全面覆盖对象创建、GML 语法、着色器、网络、优化等。

**核心功能**:
- GameMaker Studio 2 集成
- GML 脚本开发
- 着色器编写
- 网络功能
- 性能优化

---

## 🐍 二、Python 开发相关插件

### 2.1 pydantic-ai-skills (DougTrajano/pydantic-ai-skills)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 140 |
| **Forks** | 14 |
| **Language** | Python |
| **License** | MIT |

**描述**: 实现 Agent Skills 规范，支持 Pydantic AI 的渐进式披露。支持文件系统和程序化技能。

**核心功能**:
- Pydantic AI 集成
- 渐进式技能披露
- 文件系统技能
- 程序化技能

**部署方式**:
```bash
pip install pydantic-ai-skills
```

**优缺点分析**:
| 优点 | 缺点 |
|------|------|
| Python 生态完整 | 需要 Pydantic AI |
| 活跃维护 | 学习曲线 |

---

### 2.2 developer-kit (giuseppe-trisciuoglio/developer-kit)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 133 |
| **Forks** | 9 |
| **Language** | Python |
| **License** | Apache 2.0 |

**描述**: Claude Code 开发者工具包 — 模块化插件系统，提供可重用的技能、代理和命令来自动化开发任务。

**核心功能**:
- Java/Spring Boot/LangChain4J
- TypeScript/NestJS/React
- Python
- PHP/WordPress
- AWS CloudFormation
- AI 模式

**部署方式**:
```bash
git clone https://github.com/giuseppe-trisciuoglio/developer-kit ~/.claude/plugins/
```

---

### 2.3 python-rope-refactor (brian-yu/python-rope-refactor)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 36 |
| **Forks** | 2 |
| **Language** | Python |

**描述**: 教 LLM 代理如何使用 rope 进行 Python 代码库重构的技能。

**核心功能**:
- Python 代码重构
- rope 库集成
- 批量重命名
- 提取方法

**部署方式**:
```bash
git clone https://github.com/brian-yu/python-rope-refactor ~/.claude/plugins/
```

---

### 2.4 otel-instrumentation-mcp (liatrio-labs/otel-instrumentation-mcp)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 18 |
| **Forks** | - |
| **Language** | Python |

**描述**: Python MCP 服务器，为 AI 编码助手提供 OpenTelemetry 文档、示例和仪器化指导。

**核心功能**:
- OpenTelemetry 文档
- 代码仪器化
- 性能监控
- 分布式追踪

**部署方式**:
```bash
pip install otel-instrumentation-mcp
```

---

### 2.5 mcp-server-code-execution-mode (elusznik/mcp-server-code-execution-mode)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 318 |
| **Forks** | - |
| **Language** | Python |

**描述**: 在隔离的无 root 容器中执行 Python 代码的 MCP 服务器，可选 MCP 服务器代理。实现 Anthropic 和 Cloudflare 的想法以减少 MCP 工具定义的上下文膨胀。

**核心功能**:
- 沙箱代码执行
- 隔离环境
- 减少上下文膨胀
- 安全隔离

**部署方式**:
```bash
pip install mcp-server-code-execution-mode
```

---

### 2.6 fastapi-development

**描述**: FastAPI 开发技能集合。

**核心功能**:
- FastAPI 项目创建
- API 路由开发
- 数据库集成
- 认证和授权

---

## 🧪 三、游戏客户端自动化测试相关插件

### 3.1 playwright-skill (lackeyjb/playwright-skill)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 1,869 |
| **Forks** | 105 |
| **Language** | JavaScript |
| **License** | MIT |

**描述**: 用于 Playwright 浏览器自动化的 Claude Code 技能。模型调用 — Claude 自主编写和执行自定义自动化进行测试和验证。

**核心功能**:
- 浏览器自动化
- E2E 测试
- 网页抓取
- UI 交互
- 表单填写

**部署方式**:
```bash
git clone https://github.com/lackeyjb/playwright-skill ~/.claude/plugins/
```

**优缺点分析**:
| 优点 | 缺点 |
|------|------|
| 活跃维护 (2026-03-05 更新) | 需要 Playwright |
| 功能全面 | 学习曲线 |
| 1,869 Stars 高热度 | |

---

### 3.2 playwright-undetected-skill (dalbit-mir/playwright-undetected-skill)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 4 |
| **Forks** | - |

**描述**: 用于绕过机器人检测的浏览器自动化的 Claude Code 技能。本地主机测试、截图、UI 交互。基于 Patchright 的 undetected Playwright。

**核心功能**:
- 绕过机器人检测
- 本地测试
- 截图功能
- UI 交互

**部署方式**:
```bash
git clone https://github.com/dalbit-mir/playwright-undetected-skill ~/.claude/plugins/
```

---

### 3.3 Qa-WorkFlow (islam-mamdouh/Qa-WorkFlow)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 2 |
| **Forks** | 1 |
| **Language** | Shell |

**描述**: 使用 Claude Code 技能的 AI 驱动的 QA 自动化框架。自动化完整 QA 生命周期：故事验证 (INVEST)、IEEE 829 测试计划、测试用例生成、缺陷报告和 Figma 设计验证。为多平台和多语言测试构建，集成 Jira 和 Figma。

**核心功能**:
- INVEST 故事验证
- IEEE 829 测试计划
- 测试用例生成
- 缺陷报告
- Figma 设计验证
- Jira 集成
- Figma 集成

**部署方式**:
```bash
git clone https://github.com/islam-mamdouh/Qa-WorkFlow ~/.claude/plugins/
```

---

### 3.4 qa-test-automation-skill (lify0921/qa-test-automation-skill)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 1 |
| **Forks** | - |

**描述**: Claude Code 的 QA 测试自动化技能 — 从规格和源代码自动生成测试计划、测试设计和测试用例。

**核心功能**:
- 测试计划生成
- 测试设计
- 测试用例生成
- 规格分析

**部署方式**:
```bash
git clone https://github.com/lify0921/qa-test-automation-skill ~/.claude/plugins/
```

---

### 3.5 casely-qa-skill (JohnWayneeee/casely-qa-skill)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 2 |

**描述**: 🚀 Casely 1.5.0: PDF 需求文档 → 8 分钟内 47 个 TestRail 就绪的 Excel 测试用例。免费的 Cursor/Antigravity/CloudCode QA 自动化技能。解析文档 → 需求 → 测试计划 → 生成 → 导出 = 5 分钟内 + 100 个测试用例（手动和自动）

**核心功能**:
- PDF 需求解析
- TestRail 导出
- 测试计划生成
- 批量测试用例生成

---

### 3.6 playwright-py-skill (akaihola/playwright-py-skill)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 1 |

**描述**: 用于 Playwright 浏览器自动化的 Claude Code 技能。模型调用 — Claude 自主编写和执行自定义自动化进行测试和验证。

**核心功能**:
- Python Playwright 集成
- 浏览器自动化
- 测试自动化

---

## 🛠️ 四、其他开发者工具

### 4.1 awesome-claude-code (hesreallyhim/awesome-claude-code)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 26,329 |
| **Forks** | 1,650 |
| **Language** | Python |
| **License** | Other |

**描述**: Claude Code awesome 列表精选 — 技能、钩子、斜杠命令、代理编排器、应用程序和插件。

**核心内容**:
- 500+ 精选技能
- 100+ 代理编排器
- MCP 服务器
- 开发工具

**部署方式**:
```bash
git clone https://github.com/hesreallyhim/awesome-claude-code ~/.claude/plugins/
```

**优缺点分析**:
| 优点 | 缺点 |
|------|------|
| 26,329 Stars 超高热度 | 内容过多需要筛选 |
| 全面覆盖 | 更新频繁 |

---

### 4.2 awesome-claude-code-subagents (VoltAgent/awesome-claude-code-subagents)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 12,540 |
| **Forks** | 1,352 |
| **Language** | Shell |
| **License** | MIT |

**描述**: 100+ 专业 Claude Code 子代理集合，涵盖广泛的开发用例。

**核心功能**:
- 代码审查子代理
- 测试子代理
- 文档子代理
- 部署子代理
- 安全子代理

**部署方式**:
```bash
git clone https://github.com/VoltAgent/awesome-claude-code-subagents ~/.claude/plugins/
```

---

### 4.3 awesome-claude-code-toolkit (rohitg00/awesome-claude-code-toolkit)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 638 |
| **Forks** | 104 |
| **Language** | JavaScript |
| **License** | Apache 2.0 |

**描述**: Claude Code 最全面的工具包 — 135 个代理、35 个精选技能（+15,000 通过 SkillKit）、42 个命令、120 个插件、19 个钩子、15 个规则、7 个模板、6 个 MCP 配置。

**核心功能**:
- 135 个代理
- 35 个精选技能
- 42 个命令
- 120 个插件
- 19 个钩子

**部署方式**:
```bash
git clone https://github.com/rohitg00/awesome-claude-code-toolkit ~/.claude/plugins/
```

---

### 4.4 beagle (existential-birds/beagle)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 37 |
| **Forks** | 5 |
| **Language** | Python |
| **License** | Apache 2.0 |

**描述**: 用于代码审查技能和验证工作流的 Claude Code 插件。支持 Python、Go、React、FastAPI、BubbleTea 和 AI 框架（Pydantic AI、LangGraph、Vercel AI SDK）。

**核心功能**:
- 代码审查
- 验证工作流
- Python 审查
- Go 审查
- React 审查
- FastAPI 审查

**部署方式**:
```bash
git clone https://github.com/existential-birds/beagle ~/.claude/plugins/
```

---

### 4.5 axon (harshkedia177/axon)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 466 |
| **Forks** | - |
| **Language** | - |

**描述**: 图形驱动的代码智能引擎 — 将代码库索引为知识图谱，通过 MCP 工具为 AI 代理暴露，并提供 CLI 给开发者。

**核心功能**:
- 代码索引
- 知识图谱
- MCP 工具
- 代码搜索

**部署方式**:
```bash
pip install axon
```

---

### 4.6 claudex (Mng-dev-ai/claudex)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 224 |
| **Forks** | - |

**描述**: 你自己的 Claude Code UI、沙箱、浏览器内 VS Code、终端、多提供商支持（Anthropic、OpenAI、GitHub Copilot、OpenRouter）、自定义技能和 MCP 服务器。

**核心功能**:
- 自定义 UI
- 沙箱环境
- 浏览器内 VS Code
- 多提供商支持
- MCP 服务器

**部署方式**:
```bash
npm install -g claudex
```

---

### 4.7 claude-reflect-system (haddock-development/claude-reflect-system)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 72 |
| **Forks** | - |

**描述**: Claude Code 持续学习和自改进技能系统 — 从修正中学习，永不重复错误。

**核心功能**:
- 持续学习
- 错误修正
- 自改进
- 知识积累

**部署方式**:
```bash
git clone https://github.com/haddock-development/claude-reflect-system ~/.claude/plugins/
```

---

### 4.8 mcp-server-code-execution-mode (elusznik/mcp-server-code-execution-mode)

**详见 2.5 节**

---

### 4.9 claude-starter-kit (serpro69/claude-starter-kit)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 62 |
| **Forks** | - |

**描述**: 所有 Claude Code 需求的基础模板仓库：配置、技能、代理等。

**核心功能**:
- 配置模板
- 技能模板
- 代理模板

**部署方式**:
```bash
git clone https://github.com/serpro69/claude-starter-kit ~/.claude/plugins/
```

---

### 4.10 claude-skills-marketplace (mhattingpete/claude-skills-marketplace)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 433 |
| **Forks** | - |

**描述**: 软件工程工作流的 Claude Code 技能 — Git 自动化、测试和代码审查。

**核心功能**:
- Git 自动化
- 测试技能
- 代码审查

**部署方式**:
```bash
git clone https://github.com/mhattingpete/claude-skills-marketplace ~/.claude/plugins/
```

---

### 4.11 skillkit-proxy

**描述**: 超大规模代理技能集合。

**核心功能**:
- 15,000+ 技能
- 跨多个 AI 助手

---

## 📊 五、热门插件综合对比

### 5.1 按 Stars 排名 Top 15

| 排名 | 插件名称 | Stars | 方向 |
|------|----------|-------|------|
| 1 | awesome-claude-code | 26,329 | 开发者工具 |
| 2 | awesome-claude-code-subagents | 12,540 | 开发者工具 |
| 3 | playwright-skill | 1,869 | 测试自动化 |
| 4 | mcp-unity | 1,382 | 游戏开发 |
| 5 | awesome-claude-code-toolkit | 638 | 开发者工具 |
| 6 | developer-kit | 133 | Python 开发 |
| 7 | pydantic-ai-skills | 140 | Python 开发 |
| 8 | claude-skills-marketplace | 433 | 开发者工具 |
| 9 | mcp-server-code-execution-mode | 318 | Python 开发 |
| 10 | axon | 466 | 开发者工具 |
| 11 | claudex | 224 | 开发者工具 |
| 12 | beagle | 37 | 开发者工具 |
| 13 | python-rope-refactor | 36 | Python 开发 |
| 14 | claude-reflect-system | 72 | 开发者工具 |
| 15 | claude-starter-kit | 62 | 开发者工具 |

### 5.2 按方向分类

**🎮 游戏客户端开发**
- mcp-unity (1,382 ⭐)
- claude-code-game-studios (26-30 ⭐)
- OH-Unity-GameDev-Skills (6 ⭐)
- unity-ai-workflow (4 ⭐)
- unreal-engine-skills (1 ⭐)

**🐍 Python 开发**
- pydantic-ai-skills (140 ⭐)
- developer-kit (133 ⭐)
- python-rope-refactor (36 ⭐)
- otel-instrumentation-mcp (18 ⭐)
- mcp-server-code-execution-mode (318 ⭐)

**🧪 游戏客户端自动化测试**
- playwright-skill (1,869 ⭐)
- playwright-undetected-skill (4 ⭐)
- Qa-WorkFlow (2 ⭐)
- qa-test-automation-skill (1 ⭐)
- casely-qa-skill (2 ⭐)
- playwright-py-skill (1 ⭐)

**🛠️ 其他开发者工具**
- awesome-claude-code (26,329 ⭐)
- awesome-claude-code-subagents (12,540 ⭐)
- awesome-claude-code-toolkit (638 ⭐)
- claude-skills-marketplace (433 ⭐)
- axon (466 ⭐)

---

## 🎯 六、推荐插件

### 6.1 游戏客户端开发推荐

| 插件 | 推荐理由 |
|------|----------|
| **mcp-unity** | 1,382 Stars，主流 Unity 集成，活跃维护 |
| **unreal-engine-skills** | 27 个技能覆盖 UE 开发 |
| **godot-development** | Godot 官方支持 |

### 6.2 Python 开发推荐

| 插件 | 推荐理由 |
|------|----------|
| **pydantic-ai-skills** | 140 Stars，AI 框架集成 |
| **developer-kit** | 133 Stars，全栈开发 |
| **python-rope-refactor** | 36 Stars，代码重构 |
| **mcp-server-code-execution-mode** | 318 Stars，沙箱执行 |

### 6.3 自动化测试推荐

| 插件 | 推荐理由 |
|------|----------|
| **playwright-skill** | 1,869 Stars，最热门测试技能 |
| **Qa-WorkFlow** | 完整 QA 生命周期 |

### 6.4 开发者工具推荐

| 插件 | 推荐理由 |
|------|----------|
| **awesome-claude-code** | 26,329 Stars，入门必读 |
| **awesome-claude-code-subagents** | 12,540 Stars，100+ 子代理 |
| **awesome-claude-code-toolkit** | 638 Stars，最全工具包 |

---

## 📝 七、总结

本次调研完成了 Claude Code 热门插件的深度分析，涵盖：

1. **游戏客户端开发**: Unity、Unreal、Godot 等主流游戏引擎的 Claude Code 集成方案
2. **Python 开发**: Pydantic AI、FastAPI、Django 等 Python 生态的技能和 MCP 服务器
3. **游戏客户端自动化测试**: Playwright 为核心的浏览器自动化和 QA 工作流
4. **其他开发者工具**: 代码审查、知识图谱、持续学习等开发辅助工具

**关键发现**:
- playwright-skill (1,869 ⭐) 是测试自动化领域的热门插件
- mcp-unity (1,382 ⭐) 是游戏开发领域的热门插件
- awesome-claude-code (26,329 ⭐) 是开发者工具领域的入门必读资源

---

> 调研日期: 2026-03-05
> 调研工具: GitHub API + Claude Code 插件分析
