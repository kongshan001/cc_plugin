# Claude Code 热门插件补充调研 (v78)

> 2026年3月 游戏客户端/Python/自动化测试/开发者工具 - 最新热门插件完整调研

---

## 一、最新热门插件概览

### 1.1 本期重点关注领域

| 领域 | 插件数量 | 热门程度 |
|------|---------|---------|
| 游戏客户端开发 | 15+ | ⭐⭐⭐⭐ |
| Python 开发 | 20+ | ⭐⭐⭐⭐⭐ |
| 自动化测试 | 25+ | ⭐⭐⭐⭐⭐ |
| 开发者工具 | 35+ | ⭐⭐⭐⭐⭐ |

### 1.2 本期重点插件

| 插件名称 | 方向 | Stars | 特点 |
|---------|------|-------|------|
| Claude Code Agents | E2E开发工作流 | 新兴 | 多审计员并行/微检查点协议 |
| Claude Scientific Skills | 科学研究 | v2.26.0 | 研究/科学/工程 |
| Superpowers | 核心工程 | 4100+ | SDLC全面覆盖 |
| AgentSys | 工作流自动化 | v5.3.7 | 生产级验证 |
| Claude Code Settings | 云平台集成 | v2.1.0 | Azure/GitHub/MongoDB |

---

## 二、游戏客户端开发插件深度分析

### 2.1 Claude-Code-Game-Studios

> 将 Claude Code 转变为完整的游戏开发工作室

**核心特性**:
- 48 个专业 AI 代理
- 36 个工作流技能
- 完整的协调系统，模拟真实游戏工作室层级
- 支持 Unity、Unreal、Godot 等主流引擎

**Stars**: 26-30 | **状态**: ✅ 活跃

**安装配置**:
```bash
# 克隆仓库
git clone https://github.com/Sstobo/Claude-Code-Game-Studios.git ~/.claude/plugins/game-studios

# 使用示例
"创建一个射击游戏原型"
"添加一个敌人 AI 行为树"
"实现多人游戏大厅"
```

### 2.2 Claude-Code-Game-Master

> 使用 RAG 和 RPG 规则集玩持久冒险游戏

**功能特点**:
- RAG (检索增强生成) 支持
- RPG 规则集集成
- 持久世界/书籍冒险
- API 驱动的游戏世界

**Stars**: 86 | **发展迅速**

```bash
# 安装
git clone https://github.com/Sstobo/Claude-Code-Game-Master.git

# 使用
"开始一个新的冒险"
"探索地下城"
"与 NPC 交互"
```

### 2.3 pixel-plugin

> Claude Code 像素艺术插件

**功能支持**:
- Aseprite 集成 ✅
- 动画创建 ✅
- 复古调色板 (50+)
- 抖动效果 ✅
- 游戏引擎导出 (Unity/Godot/Pixel)

**Stars**: 56 | **实用工具**

```bash
# 安装
npm install -g pixel-plugin

# 使用示例
"创建一个 32x32 的角色精灵"
"添加行走动画"
"导出为 Unity 格式"
```

### 2.4 Unreal-MCP

> Unreal Engine 5 MCP 服务器

**功能支持**:
- 蓝图可视化编程
- 材质和着色器管理
- 动画系统集成
- 多人游戏支持
- 发布配置

**Stars**: 128+ | **热门**

```bash
# 安装
pip install unreal-mcp

# 配置
{
  "mcpServers": {
    "unreal": {
      "command": "python",
      "args": ["-m", "unreal_mcp"]
    }
  }
}
```

### 2.5 Unity AI Workflow

> AI 优先的 Unity 6.2+ 开发工作流

**包含组件**:
- Rules (规则定义)
- Agents (执行者)
- Skills (具体技能)
- Claude Code + Antigravity 集成

### 2.6 Godot-Development

> Godot 4.x 游戏引擎开发技能

**核心能力**:
- GDScript 编程
- Shader 开发
- 场景管理
- 资源打包
- 跨平台导出

**Stars**: 15+ | **持续更新**

### 2.7 OH-Unity-GameDev-Skills

> Unity 游戏开发专用技能集

**包含技能**:
- 场景管理
- 组件操作
- 物理系统
- 动画状态机
- UI 系统
- 资源优化

**Stars**: 6 | **持续更新**

### 2.8 游戏开发插件对比

| 插件 | Stars | 适用引擎 | 复杂度 |
|------|-------|---------|--------|
| Claude-Code-Game-Studios | 26-30 | 通用 | 高 |
| Claude-Code-Game-Master | 86 | 桌游/RPG | 中 |
| pixel-plugin | 56 | 像素游戏 | 低 |
| Unreal-MCP | 128+ | Unreal 5 | 中 |
| Unity AI Workflow | 4 | Unity 6.2+ | 中 |
| Godot-Development | 15+ | Godot 4 | 中 |
| OH-Unity-GameDev-Skills | 6 | Unity | 中 |

---

## 三、Python 开发插件生态

### 3.1 Pydantic AI Skills

> Pydantic AI 开发技能集

**核心功能**:
- 类型验证
- Agent 构建
- LLM 集成
- 数据验证

**Stars**: 138+ | **官方维护**

```bash
# 安装
pip install pydantic-ai

# 使用
from pydantic_ai import Agent

agent = Agent(
    'claude-sonnet-4-20250514',
    result_type=MyModel
)
```

### 3.2 FastAPI 开发技能

> FastAPI 异步 Web 框架开发技能

**核心功能**:
- 异步 API 开发
- 类型提示
- 自动文档 (OpenAPI/Swagger)
- 依赖注入

```bash
# 快速启动
uv venv && uv pip install -r requirements.txt
uv run python -m pytest tests/

# MCP 服务器配置
{
  "mcpServers": {
    "fastapi": {
      "command": "uv",
      "args": ["run", "fastapi-mcp", "--app", "main:app"]
    }
  }
}
```

### 3.3 Django-MCP

> Django 框架 MCP 服务器

**功能**:
- ORM 操作
- 管理命令执行
- 迁移管理
- 模型检查

```bash
# 安装
pip install django-mcp

# 配置 settings.py
INSTALLED_APPS = [
    'django_mcp',
    # ...
]
```

### 3.4 LangGraph 技能

> LangGraph AI 工作流开发

**功能**:
- 状态图工作流
- 多代理编排
- 循环和条件
- 持久化状态

**Stars**: 高 | **AI 工作流**

```python
# 基本使用
from langgraph.graph import StateGraph

workflow = StateGraph(AgentState)
workflow.add_node("agent", agent_node)
workflow.add_edge("__start__", "agent")
```

### 3.5 Python 测试集成

#### Playwright Skill (核心)

**Stars**: 1860 | **最热门测试插件**

**功能**:
- 模型驱动的浏览器自动化
- Claude 自主编写和执行测试
- 支持视觉测试
- CI/CD 集成

```bash
# 安装
npm install -g playwright-skill

# 使用
"创建一个登录测试"
"验证首页加载"
"截图对比测试"
```

### 3.6 Claude Code Agents - E2E 开发工作流

> 全面的 E2E 开发工作流，支持多审计员并行

**核心功能**:
- 多审计员并行运行
- 微检查点协议自动修复
- 基于浏览器的 QA
- 防止 AI 失控的严格协议

**Stars**: 新兴 | **E2E 开发**

```bash
# 安装
git clone https://github.com/undeadlist/claude-code-agents.git ~/.claude/plugins/claude-code-agents

# 使用
"使用 E2E 工作流开发用户认证模块"
"运行完整测试套件"
"并行审计代码质量"
```

### 3.7 Python 完整插件列表

| 插件名称 | Stars | 用途 |
|---------|-------|------|
| pydantic-ai-skills | 138+ | Pydantic AI 开发 |
| fastapi-development | 中 | FastAPI 开发 |
| django-mcp | 新兴 | Django 开发 |
| playwright-skill | 1860 | 浏览器自动化测试 |
| claude-code-playwright-mcp-test | 164 | YAML 测试框架 |
| ai-testing-mcp | 6 | AI 测试生成 |
| mastering-langgraph-agent-skill | 高 | LangGraph AI 工作流 |
| read-only-postgres | 新兴 | PostgreSQL 查询 |

---

## 四、自动化测试插件深度分析

### 4.1 测试插件生态概览

**测试类型支持**:
- 单元测试 (pytest, unittest)
- 集成测试 (APIs MCP)
- E2E测试 (Playwright MCP)
- 视觉测试 (AI Vision Testing)
- 性能测试 (k6 MCP)

### 4.2 Playwright MCP 服务器

```bash
# 官方安装
npx -y @modelcontextprotocol/server-playwright

# 配置
{
  "mcpServers": {
    "playwright": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-playwright"]
    }
  }
}
```

### 4.3 Claude-Code-Frontend-Dev

> 首个多模态 AI 视觉测试插件

**Stars**: 12 | **创新功能**

**特点**:
- 10x 更快的前端开发
- Claude 4.5 Sonnet 视觉理解
- UI 修复建议
- 视觉差异报告

### 4.4 TestSprite MCP

> 开源 AI 测试自动化平台

**功能**:
- 无代码测试创建
- 智能元素定位
- 跨浏览器测试
- CI/CD 集成

**Stars**: 500+ | **企业级**

### 4.5 Percy-MCP

> 视觉回归测试平台

**功能**:
- 自动化截图对比
- 视觉 diff 检测
- 审批工作流
- 团队协作

### 4.6 Cypress-MCP

> Cypress E2E 测试集成

```javascript
// cypress-mcp.config.js
module.exports = {
  mcpServers: {
    cypress: {
      command: 'npx',
      args: ['cypress', 'mcp-server']
    }
  }
}
```

### 4.7 测试 Slash Commands

| 命令 | 功能 | 适用场景 |
|------|------|---------|
| /tdd | 测试驱动开发 | 红绿重构流程 |
| /tdd-implement | TDD 实现 | 功能开发 |
| /repro-issue | 复现问题 | Bug 调试 |
| /testing_plan_integration | 测试计划集成 | 项目管理 |
| /check | 代码质量检查 | CI/CD |
| /clean | 代码清理 | 代码维护 |

### 4.8 测试插件对比

| 插件 | Stars | 测试类型 | 特点 |
|------|-------|---------|------|
| playwright-skill | 1860 | E2E | 模型驱动 |
| claude-code-playwright-mcp-test | 164 | E2E | YAML 驱动 |
| ai-testing-mcp | 6 | AI 生成 | 智能修复 |
| claude-code-frontend-dev | 12 | 视觉测试 | 多模态 |
| TestSprite MCP | 500+ | 企业级 | 无代码 |
| Percy-MCP | 新兴 | 视觉回归 | 自动化 |
| Cypress-MCP | 新兴 | E2E | 成熟稳定 |

---

## 五、开发者工具插件深度分析

### 5.1 Superpowers

> 核心工程技能集

**Stars**: 4100+ | **顶级工程技能**

**核心能力**:
- 代码审查
- 调试技能
- 重构技能
- 测试技能
- 安全审计
- 性能优化

**安装**:
```bash
git clone https://github.com/obra/superpowers ~/.claude/plugins/superpowers
```

### 5.2 Lazy-Bird

> 通用开发自动化工具

**Stars**: 212 | **15+ 框架预设**

**框架支持**:
- 前端: React, Vue, Next.js, React Native
- 后端: NestJS, FastAPI, Django
- 移动: Flutter

**核心能力**:
- 特性开发
- 测试运行
- PR 创建
- 代码审查
- 问题跟踪
- 安全扫描

**效率提升**: 20-100 小时/月

### 5.3 Claude-Skills-Marketplace

**Stars**: 431 | **软件工程工作流**

**功能模块**:
- Git 自动化: 智能提交、PR 管理、分支策略
- 测试集成: 单元测试、集成测试、覆盖率
- 代码质量: Linting、格式化、类型检查
- 部署流程: CI/CD、Docker、K8s

### 5.4 AgentSys

> 工作流自动化系统

**功能**:
- 任务编排
- PR 管理
- 代码清理
- 性能调查
- 多代理审查

**Stars**: v5.3.7 | **生产级**

```bash
# 安装
git clone https://github.com/avifenesh/agentsys.git ~/.claude/plugins/agentsys

# 特性
- agnix: Agent 配置 linting
- 确定性检测 (regex, AST)
- LLM 判断
- 数千测试用例
```

### 5.5 Claude Code Settings

> 云平台和开发服务集成

**Stars**: v2.1.0 | **多平台支持**

**支持平台**:
- GitHub
- Azure
- MongoDB
- Tavily
- Playwright

**特点**: 清晰、不强加观点、兼容多提供商

### 5.6 Claude Code Settings 详细配置

```json
{
  "mcpServers": {
    "github": {
      "command": "uvx",
      "args": ["mcp-server-github"]
    },
    "azure": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-azure"]
    },
    "mongodb": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-mongodb"]
    }
  }
}
```

### 5.7 DevTools-MCP

> 开发者工具 MCP 服务器集合

**包含工具**:
- GitHub API
- Docker
- Kubernetes
- AWS
- Azure

```bash
# 安装
npm install -g devtools-mcp
```

### 5.8 AWS-MCP-Server

> AWS 云服务 MCP 服务器

**Stars**: 1350+ | **云服务集成**

**支持服务**:
- EC2, S3, Lambda
- RDS, DynamoDB
- CloudWatch
- IAM

### 5.9 Context7-MCP-Server

> 代码库上下文管理

**Stars**: 新兴 | **50+ 框架支持**

**功能**:
- 智能代码检索
- 上下文记忆
- 框架特定知识

### 5.10 ClaudeCode-Rule2Hook

**Stars**: 407 | **自然语言转 Hooks**

**使用示例**:
```
"当提交信息包含 'bug' 时,运行测试"
→ 自动生成 PreCommit Hook

"每次修改 *.py 文件时,检查类型"
→ 自动生成 PreToolUse Hook
```

### 5.11 开发者工具对比

| 插件 | Stars | 用途 | 特点 |
|------|-------|------|------|
| Superpowers | 4100+ | 核心工程 | 顶级 |
| Lazy-Bird | 212 | 通用自动化 | 15+框架 |
| Claude-Skills-Marketplace | 431 | 工程工作流 | 完整 |
| AgentSys | v5.3.7 | 工作流 | 编排 |
| Claude Code Settings | v2.1.0 | 云平台 | 多集成 |
| DevTools-MCP | 新兴 | 开发者工具 | 集合 |
| AWS-MCP-Server | 1350+ | 云服务 | 官方支持 |
| Context7-MCP | 新兴 | 上下文 | 50+框架 |

---

## 六、新兴工具深度分析

### 6.1 Claude-Scientific-Skills

> 科学研究技能集

**功能**:
- 研究工具
- 科学计算
- 数据分析
- 论文写作

**Stars**: v2.26.0 | **科研利器**

**适用领域**:
- 机器学习研究
- 数据科学
- 金融分析
- 学术写作

### 6.2 Sudocode

> 轻量级代理编排工具

**功能**:
- Git 原生规范管理
- 规范驱动开发
- 轻量级编排
- 项目管理集成

**Stars**: 新兴 | **创新工具**

```bash
# 安装
npm install -g sudocode

# 使用
sudocode init
sudocode plan
sudocode execute
```

### 6.3 Parry

> 提示注入扫描器

**功能**:
- 注入攻击检测
- 敏感信息扫描
- 数据泄露防护
- 多层安全防护

**Stars**: 新兴 | **安全工具**

```bash
# 安装
npm install -g parry

# 使用
parry scan --input file.txt
parry monitor --hook pre-commit
```

### 6.4 Dippy

> Bash 命令过滤器

**功能**:
- AST 解析
- 自动批准安全命令
- 权限管理
- 多平台支持 (Claude Code, Gemini CLI, Cursor)

**Stars**: 新兴 | **效率工具**

**核心价值**: 解决权限疲劳问题，不禁用安全措施

### 6.5 Claude-Tmux

> Tmux 会话管理

**功能**:
- 多会话管理
- 状态监控
- 快速切换
- Git worktree 支持
- PR 支持

**Stars**: 新兴 | **会话管理**

### 6.6 Claude-ESP

> 调试和监控工具

**功能**:
- 隐藏输出流传输
- 多会话同时观看
- 内容类型过滤
- 后台任务跟踪

**Stars**: 新兴 | **调试工具**

**适用场景**:
- 调试 Agent 行为
- 理解 Claude 内部逻辑
- 监控后台任务

### 6.7 cc-tools

> 高性能 Go 实现

**功能**:
- Hooks 和工具
- 智能 linting
- 测试
- 状态线生成

**特点**: 最小开销

---

## 七、游戏客户端自动化测试

### 7.1 现有方案对比

| 方案 | 引擎支持 | 特点 |
|------|---------|------|
| Playwright MCP | 通用 Web | 浏览器自动化 |
| Unreal-MCP | Unreal 5 | 蓝图/材质/动画 |
| Unity AI Workflow | Unity 6.2+ | AI 优先开发 |
| Airtest | 跨平台 | 图像识别 |
| GameDriver | Unity/Unreal | 专用游戏测试 |

### 7.2 Playwright 游戏测试

```bash
# 安装
npx -y @modelcontextprotocol/server-playwright

# 游戏 Web 测试
"测试游戏大厅加载"
"验证多人匹配功能"
"检查支付流程"
```

### 7.3 游戏特定测试方案

| 方案 | 适用场景 | 成熟度 |
|------|---------|--------|
| Unreal-MCP | Unreal 5 项目 | 高 |
| Unity AI Workflow | Unity 6.2+ | 中 |
| Airtest MCP | 移动游戏 | 高 |
| GameDriver | 商业游戏测试 | 高 |
| Playwright | Web/轻量游戏 | 高 |

### 7.4 E2E 测试工作流

使用 Claude Code Agents 实现完整的 E2E 测试工作流：

```bash
# 1. 初始化 E2E 测试环境
"设置 Playwright 测试环境"

# 2. 编写测试规范
"创建登录流程测试规范"

# 3. 生成测试代码
"根据规范生成 Playwright 测试"

# 4. 运行测试
"执行完整测试套件"

# 5. 并行审计
"运行多审计员并行审查"
```

---

## 八、部署配置模板

### 8.1 游戏开发配置

```json
{
  "mcpServers": {
    "playwright": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-playwright"]
    },
    "filesystem": {
      "command": "uvx",
      "args": ["mcp-server-filesystem", "--allowed-directory", "/project"]
    },
    "unreal": {
      "command": "python",
      "args": ["-m", "unreal_mcp"]
    }
  }
}
```

### 8.2 Python 测试配置

```bash
# Python 项目配置
uv venv
source .venv/bin/activate

# 安装依赖
pip install pytest pytest-asyncio playwright
npx -y @modelcontextprotocol/server-playwright
```

### 8.3 多语言开发配置

```json
{
  "mcpServers": {
    "context7": {
      "command": "npx",
      "args": ["-y", "@context7/mcp-server"]
    },
    "github": {
      "command": "uvx",
      "args": ["mcp-server-github"]
    },
    "aws": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-aws-kb-retrieval-server"]
    }
  }
}
```

### 8.4 E2E 开发工作流配置

```json
{
  "mcpServers": {
    "playwright": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-playwright"]
    },
    "github": {
      "command": "uvx",
      "args": ["mcp-server-github"]
    }
  },
  "skills": {
    "e2e-workflow": "claude-code-agents"
  }
}
```

---

## 九、插件选择指南

### 9.1 场景推荐

| 场景 | 推荐插件 | 优先级 |
|------|---------|--------|
| 游戏客户端开发 | Claude-Code-Game-Studios | ⭐⭐⭐⭐⭐ |
| Unity 开发 | OH-Unity-GameDev-Skills | ⭐⭐⭐ |
| 像素艺术 | pixel-plugin | ⭐⭐⭐ |
| Unreal 开发 | Unreal-MCP | ⭐⭐⭐⭐ |
| Python API | FastAPI-MCP | ⭐⭐⭐⭐⭐ |
| Python AI 开发 | Pydantic-AI-Skills | ⭐⭐⭐⭐⭐ |
| E2E 测试 | Playwright-Skill + Claude Code Agents | ⭐⭐⭐⭐⭐ |
| 视觉测试 | Claude-Code-Frontend-Dev | ⭐⭐⭐ |
| 通用自动化 | Lazy-Bird | ⭐⭐⭐⭐ |
| Git 自动化 | Claude-Skills-Marketplace | ⭐⭐⭐⭐ |
| 核心工程 | Superpowers | ⭐⭐⭐⭐⭐ |
| 安全审计 | Trail-of-Bits-Skills | ⭐⭐⭐⭐ |
| 云服务 | AWS-MCP-Server | ⭐⭐⭐⭐ |
| 生产工作流 | AgentSys | ⭐⭐⭐⭐ |

### 9.2 学习路径

```
入门阶段:
├── 安装 Claude Code
├── 试用 Playwright-Skill
└── 配置 Claude Code Settings

进阶阶段:
├── 集成 Claude-Code-Game-Studios
├── 配置 MCP 服务器
├── 使用 Claude Code Agents E2E 工作流
└── 尝试 Superpowers

专家阶段:
├── 自定义工作流
├── 开发专属技能
├── 安全集成 (Parry)
└── 团队协作优化
```

---

## 十、总结

### 10.1 本期要点

1. **游戏客户端开发**: Claude-Code-Game-Studios 成为最全面的游戏开发套件，Unreal-MCP 成为新热点，Godot 开发技能持续更新

2. **Python 开发**: Pydantic AI 和 FastAPI MCP 生态成熟，LangGraph 技能值得关注，PostgreSQL 查询技能提供数据库支持

3. **自动化测试**: Playwright 主导 (1860 Stars)，Claude Code Agents 提供完整 E2E 工作流，视觉测试成为新方向

4. **开发者工具**: Superpowers (4100+ Stars) 成为顶级工程技能，AgentSys 提供生产级工作流自动化

5. **新兴工具**: 
   - Claude Code Settings 提供多云平台集成
   - Sudocode 提供轻量级编排
   - Parry 强化安全防护
   - Dippy 解决权限疲劳

### 10.2 发展趋势

- **E2E 自动化**: Claude Code Agents 引领全面自动化
- **多云集成**: Claude Code Settings 统一多平台
- **生产级验证**: AgentSys 通过数千测试用例
- **安全集成**: Parry 等安全工具日益重要
- **游戏专用化**: 越来越多的游戏引擎专用插件

### 10.3 下期预告

- 更多 AI Agent 编排工具调研
- 云原生开发工具深度分析
- 安全和审计工具专项调研
- 移动开发工具生态探索

---

## 参考资源

- [Claude-Code-Game-Studios](https://github.com/Sstobo/Claude-Code-Game-Studios)
- [Claude-Code-Game-Master](https://github.com/Sstobo/Claude-Code-Game-Master)
- [pixel-plugin](https://github.com/nickbild/pixel-plugin)
- [Unreal-MCP](https://github.com/HackerTheme-LLC/Unreal-MCP)
- [Playwright-Skill](https://github.com/anthropics/playwright-skill)
- [Superpowers](https://github.com/obra/superpowers)
- [Lazy-Bird](https://github.com/lazy-bird/lazy-bird)
- [Claude-Skills-Marketplace](https://github.com/anthropics/claude-skills-marketplace)
- [AWS-MCP-Server](https://github.com/modelcontextprotocol/servers)
- [Claude Code Agents](https://github.com/undeadlist/claude-code-agents)
- [AgentSys](https://github.com/avifenesh/agentsys)
- [Claude Code Settings](https://github.com/fcakyon/claude-codex-settings)
- [Awesome Claude Code](https://github.com/hesreallyhim/awesome-claude-code)
- [Pydantic-AI](https://github.com/pydantic/pydantic-ai)
- [Parry](https://github.com/vaporif/parry)
- [Dippy](https://github.com/ldayton/Dippy)
- [Sudocode](https://github.com/sudocode-ai/sudocode)
- [Claude Scientific Skills](https://github.com/K-Dense-AI/claude-scientific-skills)

---

*文档版本: v78 - 2026-03-05*
*数据来源: awesome-claude-code, GitHub, Claude Code 官方文档*
