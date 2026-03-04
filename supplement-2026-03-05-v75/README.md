# Claude Code 热门插件补充调研 (v75)

> 2026年3月 游戏客户端/Python/自动化测试/开发者工具 - 最新热门插件完整调研

---

## 一、最新热门插件概览

### 1.1 本期重点关注领域

| 领域 | 插件数量 | 热门程度 |
|------|---------|---------|
| 游戏客户端开发 | 10+ | ⭐⭐⭐⭐ |
| Python 开发 | 15+ | ⭐⭐⭐⭐⭐ |
| 自动化测试 | 18+ | ⭐⭐⭐⭐⭐ |
| 开发者工具 | 25+ | ⭐⭐⭐⭐⭐ |

---

## 二、游戏客户端开发插件深度分析

### 2.1 Claude-Code-Game-Studios

> 将 Claude Code 转变为完整的游戏开发工作室

**核心特性**:
- 48 个专业 AI 代理
- 36 个工作流技能
- 完整的协调系统，模拟真实游戏工作室层级
- 支持 Unity、Unreal、Godot 等主流引擎

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

### 2.4 OH-Unity-GameDev-Skills

> Unity 游戏开发专用技能集

**包含技能**:
- 场景管理
- 组件操作
- 物理系统
- 动画状态机
- UI 系统
- 资源优化

**Stars**: 6 | **持续更新**

### 2.5 Unity AI Workflow

> AI 优先的 Unity 6.2+ 开发工作流

**包含组件**:
- Rules (规则定义)
- Agents (执行者)
- Skills (具体技能)
- Claude Code + Antigravity 集成

### 2.6 Unreal-MCP

> Unreal Engine 5 MCP 服务器

<<<<<<< HEAD
**功能支持**:
- 蓝图操作
- 材质管理
- 场景部署
- 性能分析
- 自动化测试

**Stars**: 128+ | **热门**

```bash
# 安装
npm install -g unreal-mcp
=======
**功能**:
- 蓝图可视化编程
- 材质和着色器管理
- 动画系统集成
- 多人游戏支持
- 发布配置

```bash
# 安装
pip install unreal-mcp
>>>>>>> origin/main

# 配置
{
  "mcpServers": {
    "unreal": {
<<<<<<< HEAD
      "command": "unreal-mcp",
      "args": ["--project", "MyGame.uproject"]
=======
      "command": "python",
      "args": ["-m", "unreal_mcp"]
>>>>>>> origin/main
    }
  }
}
```

<<<<<<< HEAD
### 2.7 游戏开发插件对比
=======
### 2.7 Godot-Development

> Godot 4.x 游戏引擎开发技能

**核心能力**:
- GDScript 编程
- Shader 开发
- 场景管理
- 资源打包
- 跨平台导出

### 2.8 游戏开发插件对比
>>>>>>> origin/main

| 插件 | Stars | 适用引擎 | 复杂度 |
|------|-------|---------|--------|
| Claude-Code-Game-Studios | 30 | 通用 | 高 |
| Claude-Code-Game-Master | 86 | 桌游/RPG | 中 |
| pixel-plugin | 56 | 像素游戏 | 低 |
| OH-Unity-GameDev-Skills | 6 | Unity | 中 |
| Unity AI Workflow | 4 | Unity 6.2+ | 中 |
<<<<<<< HEAD
| Unreal-MCP | 128+ | Unreal | 中 |
=======
| Unreal-MCP | 新兴 | Unreal 5 | 中 |
| Godot-Development | 15+ | Godot 4 | 中 |
>>>>>>> origin/main

---

## 三、Python 开发插件生态

### 3.1 FastAPI 开发技能

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

### 3.2 Pydantic AI 技能

| 特性 | 说明 |
|------|------|
| Stars | 138+ |
| 维护状态 | 官方维护 |
| 主要功能 | 类型验证、Agent 构建、LLM 集成 |

<<<<<<< HEAD
### 3.3 Python 测试集成
=======
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

### 3.4 Python 测试集成
>>>>>>> origin/main

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

<<<<<<< HEAD
### 3.4 Claude-Code-Playwright-MCP-Test
=======
### 3.5 Claude-Code-Playwright-MCP-Test
>>>>>>> origin/main

**Stars**: 164 | **YAML 驱动测试框架**

```yaml
# 测试配置示例
tests:
  - name: "登录流程"
    steps:
      - goto: "/login"
      - fill: "#username", "admin"
      - fill: "#password", "secret"
      - click: "button[type=submit]"
      - assert: ".dashboard"
```

<<<<<<< HEAD
### 3.5 AI-Testing-MCP
=======
### 3.6 AI-Testing-MCP
>>>>>>> origin/main

> AI 驱动的测试自动化 MCP 服务器

**Stars**: 6 | **TestSprite 替代方案**

**工作流程**:
1. 代码分析 → 理解应用结构
2. 测试生成 → AI 生成测试用例
3. 测试执行 → 自动运行测试
4. 失败分析 → 智能定位问题
5. 修复建议 → 提供修复方案

<<<<<<< HEAD
### 3.6 Python 插件完整列表
=======
### 3.7 Python 插件完整列表
>>>>>>> origin/main

| 插件名称 | Stars | 用途 |
|---------|-------|------|
| pydantic-ai-skills | 138+ | Pydantic AI 开发 |
| fastapi-development | 中 | FastAPI 开发 |
<<<<<<< HEAD
=======
| django-mcp | 新兴 | Django 开发 |
>>>>>>> origin/main
| playwright-skill | 1860 | 浏览器自动化测试 |
| claude-code-playwright-mcp-test | 164 | YAML 测试框架 |
| ai-testing-mcp | 6 | AI 测试生成 |
| learn-claude-code | 高 | 代理学习(Python) |
<<<<<<< HEAD
| mastering-langgraph-agent-skill | 高 | LangGraph AI 工作流 |
=======
>>>>>>> origin/main

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

<<<<<<< HEAD
### 4.4 测试插件对比
=======
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

### 4.7 测试插件对比
>>>>>>> origin/main

| 插件 | Stars | 测试类型 | 特点 |
|------|-------|---------|------|
| playwright-skill | 1860 | E2E | 模型驱动 |
| claude-code-playwright-mcp-test | 164 | E2E | YAML 驱动 |
| ai-testing-mcp | 6 | AI 生成 | 智能修复 |
| claude-code-frontend-dev | 12 | 视觉测试 | 多模态 |
| lazy-bird | 212 | 通用 | 15+ 框架预设 |
<<<<<<< HEAD
=======
| TestSprite MCP | 500+ | 企业级 | 无代码 |
| Percy-MCP | 新兴 | 视觉回归 | 自动化 |
| Cypress-MCP | 新兴 | E2E | 成熟稳定 |
>>>>>>> origin/main

---

## 五、开发者工具插件深度分析

### 5.1 Lazy-Bird

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

### 5.2 Claude-Skills-Marketplace

**Stars**: 431 | **软件工程工作流**

**功能模块**:
- Git 自动化: 智能提交、PR 管理、分支策略
- 测试集成: 单元测试、集成测试、覆盖率
- 代码质量: Linting、格式化、类型检查
<<<<<<< HEAD

### 5.3 ClaudeCode-Rule2Hook

**Stars**: 407 | **自然语言转 Hooks**

**使用示例**:
```
"当提交信息包含 'bug' 时,运行测试"
→ 自动生成 PreCommit Hook

"每次修改 *.py 文件时,检查类型"
→ 自动生成 PreToolUse Hook
```

### 5.4 Developer-Kit

> 多语言开发工具包

**Stars**: 新兴 | **模块化设计**

**包含模块**:
- Java/Spring Boot/LangChain4J
- TypeScript/NestJS/React
- Python
- PHP/WordPress
- AWS CloudFormation
- AI patterns

### 5.5 Nelson

> 海军指挥结构代理协调

**Stars**: 新兴 | **创新架构**

**功能**:
- 皇家海军指挥结构
- 作战计划和命令
- 行动站和舰长日志
- 复杂任务管理

### 5.6 开发者工具对比

| 插件 | Stars | 复杂度 | 适用场景 |
|------|-------|--------|---------|
| lazy-bird | 212 | 中 | 通用自动化 |
| claude-skills-marketplace | 431 | 低 | Git/测试/审查 |
| claude-code-rule2hook | 407 | 中 | 规则自动化 |
| developer-kit | 新兴 | 中 | 多语言 |
| nelson | 新兴 | 高 | 复杂任务 |

---

## 六、MCP 服务器最新动态

### 6.1 官方 MCP 服务器

| 服务器 | 用途 | 评分 |
|--------|------|------|
| playwright | 浏览器自动化 | 高 |
| filesystem | 文件系统操作 | 高 |
| git | Git 操作 | 高 |
| memory | 记忆系统 | 高 |
| aws | AWS 云服务 | 高 |
| sequential-thinking | 思考链 | 高 |

### 6.2 第三方 MCP 服务器

| 服务器 | Stars | 用途 |
|--------|-------|------|
| context7 | 50+框架 | 上下文管理 |
| snyk | 安全扫描 | 漏洞检测 |
| unreal | 128+ | 游戏引擎 |

### 6.3 最新 MCP 服务器

- **Playwright Bot Bypass**: 绕过机器人检测
- **Jira Skill**: 智能 Jira 集成
- **HAM Memory**: 记忆系统，节省 50% token

---

## 七、游戏客户端自动化测试

### 7.1 现有方案对比

| 方案 | 引擎支持 | 特点 |
|------|---------|------|
| Playwright MCP | 通用 Web | 浏览器自动化 |
| GameDriver | Unity/Unreal | 专用游戏测试 |
| Airtest | 跨平台 | 图像识别 |
| Airtest MCP | 通用 | 移动游戏测试 |

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
pip install pytest pytest-asyncio
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
=======
- 部署流程: CI/CD、Docker、K8s

### 5.3 Superpowers

> 核心工程技能集

**Stars**: 4100+ | **顶级工程技能**

**核心能力**:
- 代码审查
- 调试技能
- 重构技能
- 测试技能
- 安全审计
- 性能优化

### 5.4 AgentSys

> 工作流自动化系统

**功能**:
- 任务编排
- PR 管理
- 代码清理
- 性能调查
- 多代理审查

### 5.5 DevTools-MCP

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

# 配置
{
  "mcpServers": {
    "github": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-github"]
>>>>>>> origin/main
    }
  }
}
```

<<<<<<< HEAD
---

## 九、插件选择指南

### 9.1 场景推荐

| 场景 | 推荐插件 | 优先级 |
|------|---------|--------|
| 游戏客户端开发 | Claude-Code-Game-Studios | ⭐⭐⭐⭐⭐ |
| Unity 开发 | OH-Unity-GameDev-Skills | ⭐⭐⭐⭐ |
| 像素艺术 | pixel-plugin | ⭐⭐⭐ |
| Unreal 开发 | Unreal-MCP | ⭐⭐⭐⭐ |
| Python API | fastapi-mcp | ⭐⭐⭐⭐⭐ |
| E2E 测试 | playwright-skill | ⭐⭐⭐⭐⭐ |
| 视觉测试 | claude-code-frontend-dev | ⭐⭐⭐ |
| 通用自动化 | lazy-bird | ⭐⭐⭐⭐ |
| Git 自动化 | claude-skills-marketplace | ⭐⭐⭐⭐ |
| Jira 集成 | jira-skill | ⭐⭐⭐⭐ |

### 9.2 学习路径

```
入门阶段:
├── 安装 Claude Code
├── 试用 playwright-skill
└── 配置 lazy-bird

进阶阶段:
├── 集成 Claude-Code-Game-Studios
├── 配置 MCP 服务器
└── 使用 claude-skills-marketplace

专家阶段:
├── 自定义工作流
├── 开发专属技能
└── 团队协作优化
```

---

## 十、总结

### 10.1 本期要点

1. **游戏客户端开发**: Claude-Code-Game-Studios 成为最全面的游戏开发套件，Unreal-MCP 成为新热点
2. **Python 开发**: Pydantic AI 和 FastAPI MCP 生态成熟，LangGraph 技能值得关注
3. **自动化测试**: Playwright 主导，1860 Stars 说明一切，视觉测试成为新方向
4. **开发者工具**: lazy-bird 和 marketplace 提供通用能力，Nelson 提供创新架构

### 10.2 发展趋势

- **多模态测试**: AI 视觉理解成为新热点
- **游戏专用化**: 越来越多的游戏引擎专用插件
- **自动化程度提升**: 从被动响应到主动执行
- **安全集成**: Parry 等安全工具日益重要

### 10.3 新兴插件推荐

| 插件 | 方向 | 潜力 |
|------|------|------|
| nelson | 代理协调 | 高 |
| developer-kit | 多语言 | 高 |
| jira-skill | 项目管理 | 中 |
| ham | 记忆系统 | 高 |

---

## 参考资源

- [Claude-Code-Game-Studios](https://github.com/Sstobo/Claude-Code-Game-Studios)
- [Claude-Code-Game-Master](https://github.com/Sstobo/Claude-Code-Game-Master)
- [pixel-plugin](https://github.com/nickbild/pixel-plugin)
- [playwright-skill](https://github.com/anthropics/playwright-skill)
- [lazy-bird](https://github.com/lazy-bird/lazy-bird)
- [claude-skills-marketplace](https://github.com/anthropics/claude-skills-marketplace)
- [Awesome Claude Code](https://github.com/hesreallyhim/awesome-claude-code)
- [developer-kit](https://github.com/giuseppe-trisciuoglio/developer-kit)
- [nelson](https://github.com/harrymunro/nelson)

---

*文档版本: v75 - 2026-03-05*
=======
### 5.6 AWS-MCP-Server

> AWS 云服务 MCP 服务器

**Stars**: 1350+ | **云服务集成**

**支持服务**:
- EC2, S3, Lambda
- RDS, DynamoDB
- CloudWatch
- IAM

### 5.7 Context7-MCP-Server

> 代码库上下文管理

**Stars**: 新兴 | **50+ 框架支持**

**功能**:
- 智能代码检索
- 上下文记忆
- 框架特定知识

### 5.8 开发者工具对比

| 插件 | Stars | 用途 | 特点 |
|------|-------|------|------|
| Lazy-Bird | 212 | 通用自动化 | 15+框架 |
| Claude-Skills-Marketplace | 431 | 工程工作流 | 完整 |
| Superpowers | 4100+ | 核心工程 | 顶级 |
| AgentSys | 新兴 | 工作流 | 编排 |
| DevTools-MCP | 新兴 | 开发者工具 | 集合 |
| AWS-MCP-Server | 1350+ | 云服务 | 官方支持 |
| Context7-MCP | 新兴 | 上下文 | 50+框架 |

---

## 六、本期新增热门插件

### 6.1 Claude-Scientific-Skills

> 科学研究技能集

**功能**:
- 研究工具
- 科学计算
- 数据分析
- 论文写作

**Stars**: 新兴 | **科研利器**

### 6.2 Sudocode

> 轻量级代理编排工具

**功能**:
- Git 原生规范管理
- 规范驱动开发
- 轻量级编排
- 项目管理集成

**Stars**: 新兴 | **创新工具**

### 6.3 Parry

> 提示注入扫描器

**功能**:
- 注入攻击检测
- 敏感信息扫描
- 数据泄露防护

**Stars**: 新兴 | **安全工具**

### 6.4 Dippy

> Bash 命令过滤器

**功能**:
- AST 解析
- 自动批准安全命令
- 权限管理
- 多平台支持

**Stars**: 新兴 | **效率工具**

### 6.5 Claude-Tmux

> Tmux 会话管理

**功能**:
- 多会话管理
- 状态监控
- 快速切换
- PR 支持

---

## 七、落地实践建议

### 7.1 游戏开发方向推荐

| 推荐插件 | 适用场景 | 优先级 |
|---------|---------|--------|
| Claude-Code-Game-Studios | 完整游戏工作室 | ⭐⭐⭐⭐⭐ |
| Godot-Development | Godot 4 开发 | ⭐⭐⭐⭐ |
| Unreal-MCP | UE5 开发 | ⭐⭐⭐ |
| pixel-plugin | 像素游戏 | ⭐⭐⭐ |

### 7.2 Python 开发推荐

| 推荐插件 | 适用场景 | 优先级 |
|---------|---------|--------|
| pydantic-ai-skills | AI 开发 | ⭐⭐⭐⭐⭐ |
| FastAPI-Development | API 开发 | ⭐⭐⭐⭐⭐ |
| Django-MCP | Django 开发 | ⭐⭐⭐⭐ |
| Playwright-Skill | 测试 | ⭐⭐⭐⭐⭐ |

### 7.3 自动化测试推荐

| 推荐插件 | 适用场景 | 优先级 |
|---------|---------|--------|
| Playwright-Skill | E2E 测试 | ⭐⭐⭐⭐⭐ |
| TestSprite-MCP | 企业测试 | ⭐⭐⭐⭐ |
| Percy-MCP | 视觉测试 | ⭐⭐⭐ |
| Claude-Code-Frontend-Dev | 前端测试 | ⭐⭐⭐ |

### 7.4 开发者工具推荐

| 推荐插件 | 适用场景 | 优先级 |
|---------|---------|--------|
| Superpowers | 核心工程 | ⭐⭐⭐⭐⭐ |
| Lazy-Bird | 通用自动化 | ⭐⭐⭐⭐ |
| AWS-MCP-Server | 云服务 | ⭐⭐⭐⭐ |
| Context7-MCP | 代码上下文 | ⭐⭐⭐ |

---

## 八、总结与展望

### 8.1 本期调研结论

1. **游戏客户端开发**: Claude-Code-Game-Studios 成为最全面的游戏开发解决方案，支持主流引擎
2. **Python 开发**: Pydantic AI 和 FastAPI 开发技能最受欢迎，生态系统完善
3. **自动化测试**: Playwright 系列占据主导地位，AI 驱动的测试工具正在崛起
4. **开发者工具**: Superpowers 和 Lazy-Bird 成为工程效率的利器

### 8.2 发展趋势

- AI 驱动的测试自动化正在快速发展
- 游戏开发插件正在向专业化、引擎特定化发展
- MCP 服务器成为标准化的工具集成方式
- 上下文管理和记忆能力越来越重要

### 8.3 下期预告

- 更多 AI Agent 编排工具调研
- 云原生开发工具深度分析
- 安全和审计工具专项调研
- 移动开发工具生态探索

---

**调研时间**: 2026年3月5日
**数据来源**: awesome-claude-code, GitHub
**版本**: v75
>>>>>>> origin/main
