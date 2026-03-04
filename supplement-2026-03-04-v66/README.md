# Claude Code 热门插件补充调研 (v66)

> 2026年3月 游戏/Python/测试/开发者工具 - 深度调研续篇

---

## 一、游戏客户端开发插件深度分析

### 1.1 Unreal-MCP 深入分析

> 通过自然语言控制 Unreal Engine 5.5+ 的 MCP 服务器

#### 技术架构

```
┌─────────────────────────────────────────────────────────────┐
│                    Claude Code / Cursor                     │
├─────────────────────────────────────────────────────────────┤
│                      MCP Protocol                            │
├─────────────────────────────────────────────────────────────┤
│                   unreal-mcp Server                          │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────────────┐  │
│  │ Actor Mgmt  │  │ Blueprint   │  │ Editor Control      │  │
│  │ - Create    │  │ - Create    │  │ - Viewport         │  │
│  │ - Delete    │  │ - Compile   │  │ - Camera           │  │
│  │ - Transform │  │ - Nodes     │  │ - Focus            │  │
│  └─────────────┘  └─────────────┘  └─────────────────────┘  │
├─────────────────────────────────────────────────────────────┤
│                  Unreal Engine 5.5+                         │
│                  C++ Plugin + Python API                    │
└─────────────────────────────────────────────────────────────┘
```

#### 核心能力详解

| 功能模块 | 支持操作 | 状态 |
|---------|---------|------|
| Actor 生命周期 | Create, Delete, Find, List | ✅ 稳定 |
| Transform | Position, Rotation, Scale | ✅ 稳定 |
| Blueprint | Create, Compile, Add Components | ⚠️ 实验 |
| 材质/纹理 | 创建、赋值 | ⚠️ 实验 |
| 序列器 | 镜头控制、播放 | 🚧 规划 |

#### 实际使用示例

```python
# 通过自然语言创建游戏对象
"创建一个命名为 PlayerSpawn 的立方体，放置在 (0, 0, 100) 位置"
"添加一个点光源到场景，设置为蓝色"
"创建一个继承自 Character 的 Blueprint，添加 CapsuleComponent"
```

#### 部署注意事项

1. **UE 版本要求**：5.5+ (早期版本不兼容)
2. **Python 环境**：3.12+ 推荐
3. **编译需求**：需要 Visual Studio + UE 源码
4. **网络要求**：本地运行，无需外网

---

### 1.2 Claude-Code-Game-Studios 完整工作流

> 48 个 AI 代理 + 36 个工作流技能的全栈游戏开发工作室

#### 代理架构

```
┌─────────────────────────────────────────────────────────────┐
│                    Studio Director                            │
│                  (主协调代理)                                   │
├───────────────┬───────────────┬───────────────┬──────────────┤
│   Design     │   Code        │   Art         │   Audio      │
│   Team       │   Team        │   Team        │   Team       │
│  ┌─────────┐ │  ┌─────────┐  │  ┌─────────┐   │  ┌─────────┐  │
│  │Game     │ │  │Unity    │  │  │3D      │   │  │Music   │  │
│  │Designer │ │  │Engineer │  │  │Artist  │   │  │Composer│  │
│  └─────────┘ │  └─────────┘  │  └─────────┘   │  └─────────┘  │
│  ┌─────────┐ │  ┌─────────┐  │  ┌─────────┐   │  ┌─────────┐  │
│  │Level    │ │  │Shader  │  │  │VFX    │   │  │Sound   │  │
│  │Designer │ │  │Dev     │  │  │Artist  │   │  │Designer│  │
│  └─────────┘ │  └─────────┘  │  └─────────┘   │  └─────────┘  │
├───────────────┴───────────────┴───────────────┴──────────────┤
│                    QA & DevOps Team                           │
│  ┌─────────┐  ┌─────────┐  ┌─────────┐  ┌─────────────────┐   │
│  │QA       │  │Build    │  │Release  │  │Performance      │   │
│  │Engineer│  │Engineer │  │Manager  │  │Analyst          │   │
│  └─────────┘  └─────────┘  └─────────┘  └─────────────────┘   │
└─────────────────────────────────────────────────────────────┘
```

#### 工作流技能分类

| 类别 | 技能数量 | 示例 |
|------|---------|------|
| 项目管理 | 6 | 版本规划、任务分配、进度跟踪 |
| 代码审查 | 8 | 性能检查、安全审计、架构评审 |
| 测试自动化 | 7 | 单元测试、集成测试、回归测试 |
| 部署发布 | 5 | 构建打包、版本发布、热更新 |
| 性能优化 | 4 | 帧率分析、内存优化、网络优化 |
| 文档生成 | 6 | API文档、用户手册、变更日志 |

---

### 1.3 游戏客户端自动化测试框架

#### Playwright MCP 游戏测试方案

```bash
# 安装 Playwright MCP
npx -y @modelcontextprotocol/server-playwright

# 配置 Claude Desktop
# ~/.config/claude-desktop/mcp.json
{
  "mcpServers": {
    "playwright": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-playwright"]
    }
  }
}
```

#### 游戏测试用例示例

```yaml
# game-login-test.yaml
name: 游戏登录流程测试
steps:
  - action: navigate
    target: http://localhost:3000
  - action: click
    target: "#login-btn"
  - action: type
    target: "#username"
    value: "test_player"
  - action: type
    target: "#password"  
    value: "test123"
  - action: click
    target: "#submit"
  - assert: "#game-lobby" is visible
  - screenshot: "login-success.png"
```

#### 专用游戏测试工具

| 工具 | 用途 | 特点 |
|-----|------|------|
| GameDriver | 游戏自动化测试 | 支持 Unity/Unreal/Godot |
| Airtest | 跨平台游戏测试 | 图像识别 + 脚本 |
| PyAutoGUI | 通用自动化 | 简单易用 |
| WinAppDriver | Windows 游戏测试 | Appium 生态 |

---

### 1.4 Unity 开发技能集

#### 主要 Unity 技能包对比

| 技能包 | Stars | 技能数量 | 特点 |
|--------|-------|---------|------|
| cc-plugin-unity-gamedev | 1 | 21 | 基础但全面 |
| OH-Unity-GameDev-Skills | 6+ | 15+ | 持续维护 |
| Claude-Code-Game-Studios | 28 | 48+ | 全栈工作室 |

#### Unity 技能应用场景

```markdown
## 常用 Unity 开发技能

### 1. 场景管理
- /create-scene: 创建新场景
- /setup-scene: 配置场景元素
- /optimize-scene: 场景优化

### 2. 组件开发
- /create-script: 创建 MonoBehaviour
- /add-component: 添加组件
- /setup-physics: 配置物理系统

### 3. 资源管理
- /import-asset: 导入资源
- /organize-project: 整理项目
- /build-check: 构建检查

### 4. 调试测试
- /debug-scene: 场景调试
- /run-test: 运行测试
- /profile: 性能分析
```

---

### 1.5 Godot 开发技能

#### Godot 4.x 集成

```gdscript
# Godot 4.x 示例：通过 MCP 创建场景
extends Node

func _ready():
    # 创建角色
    var player = CharacterBody3D.new()
    player.name = "Player"
    add_child(player)
    
    # 添加碰撞体
    var collider = CollisionShape3D.new()
    var shape = CapsuleShape3D.new()
    collider.shape = shape
    player.add_child(collider)
```

#### MCP Godot 服务器

- **项目**: [pkamata2/godot-development](https://github.com/pkamata2/godot-development)
- **功能**: GDScript 代码生成、场景管理、节点操作

---

## 二、Python 开发插件生态

### 2.1 FastAPI-MCP 深入实践

#### 架构设计

```
┌─────────────────────────────────────────────────────────────┐
│                      FastAPI App                             │
│  ┌─────────────────────────────────────────────────────┐   │
│  │                  Endpoints                           │   │
│  │  GET /items    POST /users    PUT /orders           │   │
│  └─────────────────────────────────────────────────────┘   │
│  ┌─────────────────────────────────────────────────────┐   │
│  │              FastApiMCP Adapter                      │   │
│  │  - OpenAPI → MCP Tool Schema                         │   │
│  │  - Request/Response → MCP Format                     │   │
│  │  - Auth → MCP Authentication                         │   │
│  └─────────────────────────────────────────────────────┘   │
│  ┌─────────────────────────────────────────────────────┐   │
│  │                    ASGI Server                       │   │
│  │              (Uvicorn/Hypercorn)                    │   │
│  └─────────────────────────────────────────────────────┘   │
└─────────────────────────────────────────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────────────┐
│                    MCP Protocol                              │
│              (JSON-RPC over HTTP/SSE)                       │
└─────────────────────────────────────────────────────────────┘
```

#### 认证集成示例

```python
from fastapi import FastAPI, Depends
from fastapi_mcp import FastApiMCP
from typing import Annotated

app = FastAPI()

# 现有认证依赖
async def get_current_user():
    # 你的认证逻辑
    return {"user_id": 1, "role": "admin"}

# MCP 端点受保护
mcp = FastApiMCP(
    app,
    auth_dependency=get_current_user,  # 继承 FastAPI 认证
    expose=["read_items", "write_items"],  # 暴露指定端点
)

mcp.mount()

# 访问: https://your-app.com/mcp
```

#### 与 Claude Code 集成

```json
{
  "mcpServers": {
    "my-api": {
      "command": "uv",
      "args": [
        "run",
        "fastapi-mcp",
        "--app",
        "main:app",
        "--auth"
      ]
    }
  }
}
```

---

### 2.2 Python 测试框架集成

#### Pytest + Claude Code

```bash
# 安装
pip install pytest pytest-mcp

# 配置 conftest.py
# pytest 配置让 Claude Code 理解测试结构
```

#### 测试驱动开发流程

```
┌─────────────────────────────────────────────────────────────┐
│                      TDD 循环                                │
│                                                             │
│   ┌──────────┐     ┌──────────┐     ┌──────────┐         │
│   │  RED     │────▶│  GREEN   │────▶│  REFACTOR│         │
│   │  写失败测试│     │  写通过代码│     │  重构优化  │         │
│   └──────────┘     └──────────┘     └──────────┘         │
│        ▲                                      │           │
│        └──────────────────────────────────────┘           │
│                    迭代改进                                   │
└─────────────────────────────────────────────────────────────┘
```

#### Claude Code TDD 技能

```markdown
## /tdd 命令技能

使用步骤：
1. 分析需求，编写失败测试
2. 实现最小化代码让测试通过
3. 重构改进代码质量
4. 提交并运行完整测试套件

示例:
/tdd implement user authentication
/tdd create api endpoint for items
```

---

### 2.3 Python 数据科学插件

#### Jupyter MCP 集成

```bash
# 安装
pip install jupyter-mcp

# 配置
{
  "mcpServers": {
    "jupyter": {
      "command": "jupyter-mcp",
      "args": []
    }
  }
}
```

#### 数据分析工作流

```
1. 数据获取 → MCP 工具获取数据
2. 数据清洗 → Claude Code 编写清洗代码
3. 数据分析 → 执行 Jupyter 单元
4. 可视化 → 生成图表
5. 报告 → Markdown 格式输出
```

---

### 2.4 Python AI/ML 开发工具

#### 主要插件对比

| 插件 | 用途 | Stars | 特点 |
|------|------|-------|------|
| pydantic-ai-skills | Pydantic AI 开发 | 138 | 官方维护 |
| langgraph-agent-skill | LangGraph 工作流 | - | 有状态代理 |
| claude-forge | Token 优化 | 活跃 | 多语言支持 |

#### LangGraph 集成示例

```python
from langgraph.graph import StateGraph
from typing import TypedDict

class AgentState(TypedDict):
    messages: list
    context: dict

def create_agent():
    graph = StateGraph(AgentState)
    
    # 添加节点
    graph.add_node("think", think_node)
    graph.add_node("act", act_node)
    
    # 添加边
    graph.add_edge("__start__", "think")
    graph.add_conditional_edges(
        "think",
        should_continue,
        {"continue": "act", "end": "__end__"}
    )
    
    return graph.compile()
```

---

## 三、自动化测试与调试工具

### 3.1 MCPJam Inspector 完整指南

#### 功能架构

```
┌─────────────────────────────────────────────────────────────┐
│                    MCPJam Inspector                          │
├─────────────┬─────────────┬─────────────┬─────────────────┤
│ Apps Builder│   OAuth     │    LLM      │   MCP Tools     │
│             │  Debugger   │ Playground  │    Testing      │
├─────────────┴─────────────┴─────────────┴─────────────────┤
│                     可视化调试面板                            │
├─────────────────────────────────────────────────────────────┤
│  ┌────────────┐  ┌────────────┐  ┌────────────┐          │
│  │  Tools     │  │ Resources  │  │ Prompts    │          │
│  │  调用日志   │  │  响应内容   │  │  执行结果   │          │
│  └────────────┘  └────────────┘  └────────────┘          │
└─────────────────────────────────────────────────────────────┘
```

#### 安装方式

```bash
# CLI 方式（推荐）
npx @mcpjam/inspector@latest

# 桌面应用
# Mac: DMG 下载
# Windows: EXE 安装包
# Linux: AppImage

# Docker 方式
docker run -p 6274:6274 mcpjam/mcp-inspector
```

#### OAuth 调试流程

```
1. 启动 Inspector
2. 选择 OAuth Debugger
3. 输入配置:
   - Authorization URL
   - Token URL
   - Client ID
   - Scopes
4. 点击 "Start Flow"
5. 逐步查看:
   - 请求参数
   - 响应内容
   - Token 交换
   - 错误诊断
```

---

### 3.2 Playwright MCP 高级应用

#### 浏览器自动化最佳实践

```python
# 高级配置
from playwright.async_api import async_playwright

async def setup():
    async with async_playwright() as p:
        # 启动 Chromium
        browser = await p.chromium.launch(
            headless=False,  # 可视化模式
            args=[
                '--disable-blink-features=AutomationControlled',
                '--disable-dev-shm-usage'
            ]
        )
        
        context = await browser.new_context(
            viewport={'width': 1280, 'height': 720},
            user_agent='Mozilla/5.0...'
        )
        
        return context
```

#### 游戏客户端测试配置

```javascript
// playwright.config.js
module.exports = {
  testDir: './tests',
  timeout: 30000,
  use: {
    baseURL: 'http://localhost:8080',
    trace: 'on-first-retry',
    screenshot: 'only-on-failure',
    video: 'retain-on-failure'
  },
  projects: [
    {
      name: 'chromium',
      use: { browserName: 'chromium' }
    },
    {
      name: 'firefox', 
      use: { browserName: 'firefox' }
    }
  ]
};
```

---

### 3.3 自动化测试技能集

#### Claude Code 测试命令

```markdown
## /test 命令集

### 单元测试
/test create-unit <function_name>
/test run-unit <module>

### 集成测试
/test create-integration <endpoint>
/test run-integration

### E2E 测试
/test create-e2e <user_flow>
/test run-e2e

### 性能测试
/test create-load <endpoint>
/test run-load

### 安全测试
/test scan-vulnerabilities
/test check-dependencies
```

#### TDD Guard 实时监控

```bash
# 安装
git clone https://github.com/nizos/tdd-guard ~/.claude/plugins/

# 配置文件
# ~/.claude/tdd-guard/config.yaml
watch_paths:
  - src/
  - tests/

enforcement:
  - test_before_implementation
  - no_tests_no_code
  - green_before_commit
```

---

## 四、开发者工具深度评测

### 4.1 Snyk Agent Scan 安全扫描

#### 检测的安全风险

**MCP 服务器风险**:

| 风险代码 | 描述 | 严重程度 |
|---------|------|---------|
| E001 | Prompt Injection | 🔴 高 |
| E002 | Tool Shadowing | 🟠 中高 |
| E003 | Tool Poisoning | 🔴 高 |
| TF001 | Toxic Flows | 🟠 中高 |
| W005 | Rug Pull | 🟡 中 |

**Skills 风险**:

| 风险代码 | 描述 | 严重程度 |
|---------|------|---------|
| E004 | Prompt Injection | 🔴 高 |
| E006 | Malware Payloads | 🔴 高 |
| W007 | Credential Handling | 🟠 中高 |
| W008 | Hardcoded Secrets | 🟠 中高 |
| W011 | Untrusted Content | 🟡 中 |

#### 扫描示例

```bash
# 扫描所有 skills
uvx snyk-agent-scan@latest --skills

# 扫描 MCP 配置
uvx snyk-agent-scan@latest ~/.claude/mcp.json

# 扫描特定 skill
uvx snyk-agent-scan@latest --skills ~/my-skills/SKILL.md

# 输出 JSON 格式
uvx snyk-agent-scan@latest --skills --json
```

---

### 4.2 Context7 MCP Server 文档服务

#### 支持的框架 (50+)

```
Web Frameworks:
├── React, Vue, Angular, Svelte
├── Next.js, Nuxt, SvelteKit
├── Express, FastAPI, Flask, Django
└── Spring, Rails, Laravel

Data Science:
├── PyTorch, TensorFlow, JAX
├── Pandas, NumPy, Polars
├── LangChain, LlamaIndex
└── Jupyter

Mobile:
├── React Native, Flutter
├── SwiftUI, Jetpack Compose
└── Ionic, Capacitor

More:
├── Stripe, Twilio, SendGrid
├── AWS, GCP, Azure
└── Docker, Kubernetes
```

#### 使用示例

```bash
# 安装
npm install -g @context7/mcp-server

# 配置
{
  "mcpServers": {
    "context7": {
      "command": "npx",
      "args": ["-y", "@context7/mcp-server"]
    }
  }
}

# 使用
"查看 React useState 的最新用法"
"如何用 FastAPI 创建 WebSocket?"
"LangChain Agent 的最佳实践?"
```

---

### 4.3 Token 优化工具对比

#### 主流工具对比

| 工具 | 功能 | Token 减少 | 适用场景 |
|------|------|-----------|---------|
| token-optimizer | 幽灵 Token 发现 | 10-20% | 会话分析 |
| ham | 记忆系统 | 50% | 长期项目 |
| claude-forge | Token 优化配置 | 15-30% | 多语言开发 |
| claude-code-tools | 上下文恢复 | 20-40% | 会话连续 |

#### HAM 记忆系统

```bash
# 安装
git clone https://github.com/kromahlusenii-ops/ham ~/.claude/plugins/

# 使用
ham init my-project    # 初始化项目记忆
ham add "用户认证逻辑在 auth/"  # 添加记忆
ham context            # 生成上下文
ham clear              # 清理记忆
```

---

### 4.4 多代理协调系统

#### Nelson 海军指挥架构

```
┌─────────────────────────────────────────────────────────────┐
│                        Admiral                               │
│                   (总协调指挥)                                 │
├─────────────────────────────────────────────────────────────┤
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────────┐     │
│  │  Captain    │  │  Captain    │  │    Captain      │     │
│  │  (代理 1)   │  │  (代理 2)   │  │    (代理 3)      │     │
│  │  - Frontend │  │  - Backend  │  │    - DevOps     │     │
│  └─────────────┘  └─────────────┘  └─────────────────┘     │
├─────────────────────────────────────────────────────────────┤
│                      Ship's Log                              │
│                  (共享上下文/记忆)                             │
└─────────────────────────────────────────────────────────────┘
```

#### Claude Squad 多会话管理

```bash
# 安装
git clone https://github.com/smtg-ai/claude-squad ~/.claude/plugins/

# 启动
claude-squad start

# 添加任务
claude-squad add "修复登录 bug"
claude-squad add "优化数据库查询"

# 状态查看
claude-squad status
```

---

## 五、部署配置模板

### 5.1 游戏开发环境配置

```bash
# ~/.config/claude-desktop/mcp.json
{
  "mcpServers": {
    "unreal-mcp": {
      "command": "uv",
      "args": ["--directory", "/path/to/unreal-mcp/Python", "run", "unreal_mcp_server.py"]
    },
    "playwright": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-playwright"]
    },
    "context7": {
      "command": "npx",
      "args": ["-y", "@context7/mcp-server"]
    }
  }
}
```

### 5.2 Python 开发环境配置

```bash
# Python 项目 MCP 配置
{
  "mcpServers": {
    "fastapi-dev": {
      "command": "uv",
      "args": ["run", "fastapi-mcp", "--app", "main:app"]
    },
    "jupyter": {
      "command": "jupyter-mcp",
      "args": []
    },
    "snyk": {
      "command": "uvx",
      "args": ["snyk-agent-scan@latest", "--json"]
    }
  }
}
```

### 5.3 测试调试环境配置

```bash
# 测试专用配置
{
  "mcpServers": {
    "inspector": {
      "command": "npx",
      "args": ["@mcpjam/inspector@latest"]
    },
    "playwright": {
      "command": "npx", 
      "args": ["-y", "@modelcontextprotocol/server-playwright"]
    },
    "browserbase": {
      "command": "npx",
      "args": ["-y", "@browserbase/mcp-server"]
    }
  }
}
```

---

## 六、总结与推荐

### 6.1 插件选择指南

| 场景 | 推荐插件 | 备选 |
|------|---------|------|
| Unreal 游戏开发 | unreal-mcp | Claude-Code-Game-Studios |
| Unity 游戏开发 | Claude-Code-Game-Studios | cc-plugin-unity-gamedev |
| Python Web 开发 | fastapi-mcp | pydantic-ai-skills |
| Python AI 开发 | pydantic-ai-skills | langgraph-agent-skill |
| MCP 开发调试 | mcpjam-inspector | playwright-mcp |
| 安全扫描 | snyk-agent-scan | - |
| 文档查询 | context7-mcp-server | - |
| Token 优化 | token-optimizer | ham |

### 6.2 学习路径推荐

```
新手入门:
1. 安装 Claude Code
2. 配置 context7-mcp-server
3. 尝试 playwright-mcp
4. 克隆 claude-starter-kit

进阶:
1. 学习 MCP 协议
2. 部署 fastapi-mcp
3. 使用 snyk-agent-scan
4. 配置 token-optimizer

专家:
1. 开发自定义 MCP 服务器
2. 创建 Claude Skills
3. 配置多代理系统
4. 集成 DevOps 流程
```

---

## 参考资源

- [Awesome MCP Servers](https://github.com/punkpeye/awesome-mcp-servers)
- [Awesome Agent Skills](https://github.com/VoltAgent/awesome-agent-skills)
- [MCP 官方文档](https://modelcontextprotocol.io)
- [Claude Code 官方文档](https://docs.anthropic.com/en/docs/claude-code/overview)
- [Unreal MCP GitHub](https://github.com/chongdashu/unreal-mcp)
- [FastAPI-MCP PyPI](https://pypi.org/project/fastapi-mcp/)

---

*文档版本: v66 - 2026-03-04*
