# 补充调研 v87 - Claude Code 热门插件最新调研

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
- 跨 AI 助手支持

**部署方式**:
```bash
# NPM 安装
npm install -g mcp-unity

# Claude Code 配置 (~/.claude.json)
{
  "mcpServers": {
    "unity": {
      "command": "npx",
      "args": ["-y", "mcp-unity"]
    }
  }
}
```

**优缺点分析**:
| 优点 | 缺点 |
|------|------|
| 1.3k+ Stars，最流行的 Unity MCP | 需要 Unity Editor 运行 |
| 持续活跃更新 | 部分功能需要特定 Unity 包 |
| 完整 Unity API 覆盖 | |
| 多 AI 助手支持 | |

---

### 1.2 Unity-MCP (IvanMurzak/Unity-MCP)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 1,174 |
| **Forks** | 123 |
| **Language** | C# |
| **更新** | 2026-03-04 |

**描述**: AI-powered bridge connecting LLMs and advanced AI agents to the Unity Editor via MCP.

**核心功能**:
- AI 驱动的代码生成
- 错误调试自动化
- 游戏开发任务自动化
- 自然语言交互

---

### 1.3 unreal-mcp (codex精/unreal-mcp)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 245 |
| **Forks** | 28 |
| **Language** | Python |
| **更新** | 2026-03-03 |

**描述**: Unreal Engine MCP server - Connect Claude Code to Unreal Engine for game development automation.

**核心功能**:
- Unreal Engine 集成
- 蓝图操作自动化
- 材质和纹理管理
- 关卡设计辅助
- C++ 代码生成

---

### 1.4 godot-development (GodotDevelopment/godot-development)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 128 |
| **Forks** | 12 |
| **Language** | Python |
| **更新** | 2026-03-03 |

**描述**: Claude Code skill for Godot game engine development with GDScript support.

**核心功能**:
- GDScript 代码生成
- Godot 引擎集成
- 游戏场景管理
- 节点系统支持

---

### 1.5 pixel-plugin (willibrandon/pixel-plugin)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 56 |
| **Forks** | 6 |
| **Language** | Shell |
| **更新** | 2026-03-04 |

**描述**: Claude Code plugin for creating pixel art with Aseprite through natural language.

**核心功能**:
- 像素艺术创作
- 动画支持
- 复古调色板
- 抖动效果 (Dithering)
- 游戏引擎导出

---

## 🐍 二、Python 开发相关插件

### 2.1 developer-kit (giuseppe-trisciuoglio/developer-kit)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 133 |
| **Forks** | 9 |
| **Language** | Python |
| **更新** | 2026-03-04 |

**描述**: 模块化插件系统，提供可重用的技能、代理和命令来自动化开发任务。

**支持领域**:

| 领域 | 技术栈 |
|------|--------|
| Java | Spring Boot、LangChain4J |
| TypeScript | NestJS、React |
| **Python** | **Python 开发、AWS Lambda** |
| PHP | WordPress |
| AWS | CloudFormation |

**核心命令**:
- `/devkit.brainstorm` - 头脑风暴和设计
- `/devkit.feature-development` - 功能开发
- `/devkit.refactor` - 代码重构
- `/devkit.fix-debugging` - 修复和调试

---

### 2.2 fastapi-development (lieroz/FastAPI-development)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ - |
| **Forks** | - |
| **Language** | Python |
| **更新** | 2026-03 |

**描述**: FastAPI 开发技能集，提供完整的 FastAPI 项目开发工作流。

**核心功能**:
- FastAPI 项目初始化
- API 路由设计
- 数据库集成
- 认证和授权
- 测试和部署

---

### 2.3 pydantic-ai-skills (nutlope/pydantic-ai-skills)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 136 |
| **Forks** | 19 |
| **Language** | Python |
| **更新** | 2026-03-04 |

**描述**: Pydantic AI 开发技能集，专注于 Pydantic AI 框架的开发。

**核心功能**:
- Pydantic AI 代理开发
- 数据验证
- 类型安全
- 模型集成

---

### 2.4 read-only-postgres (jawwadfirdousi/agent-skills)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ - |
| **Forks** | - |
| **Language** | Python |
| **更新** | 2026-03 |

**描述**: Read-only PostgreSQL query skill for Claude Code.

**核心功能**:
- SELECT/SHOW/EXPLAIN/WITH 查询
- 多数据库连接
- 严格验证和超时
- 行数限制

---

## 🧪 三、游戏客户端自动化测试相关插件

### 3.1 playwright-skill (lackeyjb/playwright-skill)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 1,863 |
| **Forks** | 105 |
| **Language** | JavaScript |
| **更新** | 2026-03-05 |

**描述**: Claude Code Skill for browser automation with Playwright. Model-invoked - Claude autonomously writes and executes custom automation for testing and validation.

**核心功能**:
- 浏览器自动化
- Playwright 集成
- E2E 测试
- 自定义代码生成
- 可视化执行

**使用示例**:
```
"Test the homepage"
"Check if the contact form works"
"Verify the signup flow"
"Take screenshots of the dashboard in mobile and desktop"
```

**特点**:
- 通用浏览器自动化
- 默认可见浏览器
- 零模块解析错误
- 渐进式披露

---

### 3.2 playwright-mcp (smykes/playwright-mcp)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ - |
| **Forks** | - |
| **Language** | TypeScript |
| **更新** | 2026-03 |

**描述**: Playwright MCP 服务器，提供浏览器自动化能力。

**核心功能**:
- 页面导航和交互
- 元素定位和操作
- 截图和录制
- 网络请求拦截

---

### 3.3 unibrowse (sackio/unibrowse)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 4 |
| **Forks** | 0 |
| **Language** | JavaScript |
| **更新** | 2026-01-30 |

**描述**: 🤨 Advanced browser automation plugin for Claude Code with 5 specialized sub-agents, 57+ macros.

**核心功能**:
- 5 个专业子代理
- 57+ 宏
- 智能委托
- Web 爬取
- 表单自动化
- 电商自动化
- QA 测试

---

### 3.4 local-testing-agent (marcelkurvers/local-testing-agent)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 0 |
| **Forks** | - |
| **Language** | - |
| **更新** | 2026-02 |

**描述**: Multi-language testing automation MCP server for Claude Code.

**支持语言**:
- Python
- JavaScript/TypeScript
- Go
- Rust
- Java
- Ruby

---

### 3.5 ai-testing-mcp (Twisted66/ai-testing-mcp)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 6 |
| **Forks** | - |
| **Language** | - |
| **更新** | 2026-02 |

**描述**: AI-powered testing automation MCP server - TestSprite alternative.

---

## 🛠️ 四、其他开发者工具

### 4.1 claude-tmux (nielsgroen/claude-tmux)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 新增 |
| **Forks** | - |
| **Language** | - |
| **更新** | 2026-03 |

**描述**: Manage Claude Code within tmux. A tmux popup of all your Claude Code instances.

**核心功能**:
- tmux 会话管理
- Claude Code 实例管理
- 快速切换
- 状态监控
- Git worktree 支持
- PR 支持

---

### 4.2 claude-esp (phiat/claude-esp)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 新增 |
| **Forks** | - |
| **Language** | Go |
| **更新** | 2026-03 |

**描述**: Go-based TUI that streams Claude Code's hidden output to a separate terminal.

**核心功能**:
- Claude Code 隐藏输出流
- 多会话同时监控
- 内容类型过滤
- 后台任务跟踪

---

### 4.3 claude-skills-marketplace (mhattingpete/claude-skills-marketplace)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 431 |
| **Forks** | 50 |
| **Language** | HTML |
| **更新** | 2026-03-04 |

**描述**: Claude Code Skills for software engineering workflows - Git automation, testing, and code review.

**核心功能**:
- Git 自动化
- 测试工作流
- 代码审查

---

### 4.4 superpowers (obra/superpowers)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ 4,100+ |
| **Forks** | - |
| **Language** | - |
| **更新** | 2026-03 |

**描述**: A strong bundle of core competencies for software engineering.

**核心功能**:
- 规划、审查、测试、调试
- 完整 SDLC 覆盖
- 工程最佳实践

---

### 4.5 agentsys (avifenesh/agentsys)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ - |
| **Forks** | - |
| **Language** | - |
| **更新** | 2026-03 |

**描述**: Workflow automation system for Claude with useful plugins, agents, and skills.

**核心功能**:
- 任务到生产工作流自动化
- PR 管理
- 代码清理
- 性能调查
- 多代理代码审查

---

### 4.6 ContextKit (FlineDev/ContextKit)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ - |
| **Forks** | - |
| **Language** | - |
| **更新** | 2026-03 |

**描述**: A systematic development framework that transforms Claude Code into a proactive development partner.

**核心功能**:
- 4 阶段规划方法论
- 专业化质量代理
- 结构化工作流

---

### 4.7 ClaudeHub (Claude-Did-This/claude-hub)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ - |
| **Forks** | - |
| **Language** | - |
| **更新** | 2026-03 |

**描述**: A webhook service that connects Claude Code to GitHub repositories.

**核心功能**:
- GitHub Webhook 集成
- PR 和 Issue AI 辅助
- 代码分析

---

### 4.8 cc-devops-skills (akin-ozer/cc-devops-skills)

| 项目 | 详情 |
|------|------|
| **Stars** | ⭐ - |
| **Forks** | - |
| **Language** | - |
| **更新** | 2026-03 |

**描述**: Immensely detailed set of skills for DevOps Engineers.

**核心功能**:
- 验证和生成器
- Shell 脚本
- CLI 工具
- 高质量 IaC 代码

---

## 📊 总结与建议

### 热门插件推荐

| 类别 | 推荐插件 | Stars | 特点 |
|------|---------|-------|------|
| 游戏开发 | mcp-unity | 1,382 | 主流 Unity 集成 |
| 游戏开发 | Unity-MCP | 1,174 | AI 驱动 Unity 集成 |
| 游戏开发 | unreal-mcp | 245 | Unreal Engine 集成 |
| Python 开发 | developer-kit | 133 | 模块化多语言支持 |
| Python 开发 | pydantic-ai-skills | 136 | Pydantic AI 开发 |
| 自动化测试 | playwright-skill | 1,863 | 最热门浏览器自动化 |
| 自动化测试 | unibrowse | 4 | 高级浏览器自动化 |
| 开发者工具 | superpowers | 4,100+ | 核心工程技能集 |
| 开发者工具 | claude-skills-marketplace | 431 | Git 自动化 |

### 调研发现

1. **游戏客户端开发**: 
   - Unity 相关的 MCP 解决方案最为成熟，Stars 达 1.1k-1.3k+
   - Unreal Engine 支持正在增长 (unreal-mcp 245 Stars)
   - Godot 开发支持稳定 (128 Stars)
   - 像素艺术工具开始出现

2. **Python 开发**: 
   - developer-kit 提供全面的 Python 支持
   - Pydantic AI 技能集专注于 AI 框架开发
   - FastAPI 开发技能支持现代 Web 开发

3. **自动化测试**: 
   - playwright-skill 是最热门的浏览器自动化工具 (1,863 Stars)
   - 多语言测试自动化 MCP 开始出现
   - AI 驱动的测试自动化解决方案兴起

4. **开发者工具**: 
   - superpowers 是最受欢迎的工程技能集 (4,1k+ Stars)
   - claude-tmux 提供创新的会话管理
   - claude-esp 提供调试辅助能力
   - ClaudeHub 连接 GitHub 工作流

---

## 🔗 参考链接

- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
- [playwright-skill](https://github.com/lackeyjb/playwright-skill)
- [developer-kit](https://github.com/giuseppe-trisciuoglio/developer-kit)
- [Unity-MCP](https://github.com/IvanMurzak/Unity-MCP)
- [mcp-unity](https://github.com/CoderGamester/mcp-unity)
- [unreal-mcp](https://github.com/codex精/unreal-mcp)
- [superpowers](https://github.com/obra/superpowers)
- [claude-tmux](https://github.com/nielsgroen/claude-tmux)
- [claude-esp](https://github.com/phiat/claude-esp)
