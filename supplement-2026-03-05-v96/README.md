# Claude Code 插件补充调研 v96

> 游戏客户端 / Python 开发 / 自动化测试 / 开发者工具 | 最新热门插件完整调研

## 调研概述

本次调研继续深入分析 Claude Code 热门插件，聚焦以下方向：
1. 游戏客户端开发
2. Python 开发
3. 游戏客户端自动化测试
4. 其他开发者工具

通过分析 awesome-claude-code、GitHub Topics 和最新插件发布，总结实用插件和工具。

---

## 一、游戏客户端开发相关插件

### 1.1 Unreal MCP - Unreal Engine 集成

- **GitHub**: [https://github.com/CoplayDev/unreal-mcp](https://github.com/CoplayDev/unreal-mcp)
- **功能**: AI 助手与 Unreal Editor 的桥梁
- **特点**:
  - 资产管理自动化
  - 场景控制
  - 蓝图脚本编辑
  - 构建任务自动化
- **适用**: Unreal Engine 5 游戏开发

### 1.2 Godot Development - Godot 游戏引擎

- **GitHub**: [https://github.com/foxware/godot-development](https://github.com/foxware/godot-development)
- **功能**: Godot 4.x 游戏开发技能集
- **特点**:
  - GDScript 开发
  - 场景管理
  - 节点操作
  - 信号系统

### 1.3 Claude Code Game Studios - 48 个 AI 游戏工作室

- **GitHub**: [https://github.com/1024pix/claude-code-game-studios](https://github.com/1024pix/claude-code-game-studios)
- **Stars**: ⭐ 26-30
- **功能**: 专业游戏开发 AI 代理集合
- **包含**:
  - Unity 开发代理
  - Unreal 开发代理
  - WebGL 开发代理
  - 跨平台游戏开发

### 1.4 Unity MCP - 主流 Unity 集成

- **GitHub**: [https://github.com/CoplayDev/unity-mcp](https://github.com/CoplayDev/unity-mcp)
- **Stars**: ⭐ 1,382
- **功能**: Unity Editor 与 AI 助手集成
- **核心能力**:
  | 能力 | 描述 |
  |------|------|
  | 资产管理 | 创建/删除/查询 Unity 资源 |
  | 场景控制 | 加载/保存/切换场景 |
  | 脚本编辑 | 读取/修改 C# 脚本 |
  | 构建自动化 | 自动构建项目 |

### 1.5 Auto-Review-Claude-MCP - Unity PR 审查

- **功能**: Unity 项目自动化代码审查
- **特点**:
  - PR 自动审查
  - Unity 特定规则
  - 性能建议

---

## 二、Python 开发相关插件

### 2.1 FastMCP - 最流行 Python MCP 框架

- **GitHub**: [https://github.com/jlowin/fastmcp](https://github.com/jlowin/fastmcp)
- **Stars**: ⭐ 23,383
- **特点**:
  - 简洁装饰器 API
  - 完整异步支持
  - 100+ 示例项目
  - 类型安全
- **安装**: `pip install fastmcp`

### 2.2 Developer-Kit - 全栈开发工具包

- **GitHub**: [https://github.com/giuseppe-trisciuoglio/developer-kit](https://github.com/giuseppe-trisciuoglio/developer-kit)
- **Stars**: ⭐ 133
- **功能**: 多语言开发工具包
- **支持领域**:
  | 领域 | 技术栈 |
  |------|--------|
  | Java | Spring Boot、LangChain4J |
  | TypeScript | NestJS、React |
  | Python | Python 完整开发 |
  | PHP | WordPress |
  | AWS | CloudFormation |
  | AI | LLM 应用开发 |

### 2.3 Context7 MCP Server - Python 文档

- **GitHub**: [https://github.com/ModelContextProtocol/context7-mcp-server](https://github.com/ModelContextProtocol/context7-mcp-server)
- **功能**: 50+ 框架文档索引
- **Python 支持**:
  - 最新 PyPI 库文档
  - 文档自动更新
  - 代码示例检索

### 2.4 FastAPI Development - FastAPI 开发技能

- **功能**: FastAPI 开发专项技能
- **特点**:
  - 路由定义
  - 依赖注入
  - 中间件开发
  - 数据库集成

### 2.5 Pydantic-AI Skills - Pydantic AI 开发

- **GitHub**: [https://github.com/pydantic/pydantic-ai-skill](https://github.com/pydantic/pydantic-ai-skill)
- **Stars**: ⭐ 136
- **功能**: Pydantic AI Agent 开发技能
- **特点**:
  - Agent 开发模式
  - 类型安全
  - 工具集成

### 2.6 PyPICT Claude Skill - 测试用例生成

- **GitHub**: [https://github.com/microsoft/pypict-claude-skill](https://github.com/microsoft/pypict-claude-skill)
- **功能**: PICT 成对测试用例生成
- **场景**:
  - 参数组合测试
  - 正交分析
  - 测试覆盖率优化

---

## 三、自动化测试相关插件

### 3.1 MCP Inspector - MCP 协议测试工具

- **GitHub**: [https://github.com/modelcontextprotocol/inspector](https://github.com/modelcontextprotocol/inspector)
- **Stars**: ⭐ 8,900
- **功能**: 官方 MCP 可视化测试工具
- **特点**:
  - 所有 MCP 协议测试
  - 可视化调试界面
  - 实时请求/响应监控
- **安装**:
```bash
npm install -g @modelcontextprotocol/inspector
mcp-inspector
```

### 3.2 Playwright MCP - 浏览器自动化

- **GitHub**: [https://github.com/anthropics/playwright-mcp](https://github.com/anthropics/playwright-mcp)
- **Stars**: ⭐ 3,581
- **功能**: 官方浏览器自动化工具
- **特点**:
  - 跨浏览器测试 (Chromium/Firefox/WebKit)
  - 视觉回归测试
  - API 集成测试
  - 移动端模拟
- **场景**:
  - Web 应用 E2E 测试
  - 视觉回归测试
  - 爬虫和数据抓取

### 3.3 Vibetest-Use - AI 驱动 QA

- **GitHub**: [https://github.com/Use/Vibetest](https://github.com/Use/Vibetest)
- **Stars**: ⭐ 771
- **功能**: AI 自动化测试代理
- **特点**:
  - Browser-Use 集成
  - 智能测试生成
  - 视觉回归测试
  - 自然语言测试用例

### 3.4 SkUnit - 单元测试框架

- **GitHub**: [https://github.com/skunit/skunit](https://github.com/skunit/skunit)
- **功能**: Claude Code 单元测试技能
- **特点**:
  - 测试用例生成
  - Mock 框架
  - 断言库
  - CI/CD 集成

### 3.5 Playwright Skill - 测试自动化

- **功能**: Playwright 专项测试技能
- **特点**:
  - Page Object 模式
  - 测试数据管理
  - 并行测试执行
  - 报告生成

### 3.6 TDD Guard - 测试驱动开发

- **GitHub**: [https://github.com/nizos/tdd-guard](https://github.com/nizos/tdd-guard)
- **功能**: TDD 原则强制执行
- **特点**:
  - 实时文件监控
  - TDD 违规拦截
  - 渐进式测试

---

## 四、其他开发者工具

### 4.1 Claude-Tmux - 会话管理

- **GitHub**: [https://github.com/nielsgroen/claude-tmux](https://github.com/nielsgroen/claude-tmux)
- **功能**: tmux 中的 Claude Code 管理
- **特点**:
  - tmux 弹出式界面
  - 多会话快速切换
  - 状态实时监控
  - Git worktree 支持
  - PR 集成
- **安装**:
```bash
git clone https://github.com/nielsgroen/claude-tmux ~/.claude/plugins/
```

### 4.2 Claude-ESP - 调试工具

- **GitHub**: [https://github.com/phiat/claude-esp](https://github.com/phiat/claude-esp)
- **功能**: Claude Code 隐藏输出流调试
- **特点**:
  - 实时流式输出监控
  - 多会话同时观看
  - 内容类型过滤
  - 后台任务跟踪
- **技术栈**: Go + TUI

### 4.3 Rulesync - 配置同步

- **GitHub**: [https://github.com/dyoshikawa/rulesync](https://github.com/dyoshikawa/rulesync)
- **功能**: AI 代理配置转换工具
- **特点**:
  - Claude Code ↔ 其他代理双向转换
  - 规则文件同步
  - MCP 服务器配置
  - 忽略文件管理

### 4.4 Claude-Hub - GitHub 集成

- **GitHub**: [https://github.com/claude-did-this/claude-hub](https://github.com/claude-did-this/claude-hub)
- **功能**: GitHub Webhook 服务
- **特点**:
  - PR 自动分析
  - Issue 智能回复
  - 代码库理解增强

### 4.5 Superpowers - 核心工程技能

- **GitHub**: [https://github.com/obra/superpowers](https://github.com/obra/superpowers)
- **Stars**: ⭐ 4,100+
- **功能**: 核心软件工程技能集
- **覆盖**:
  | 阶段 | 技能 |
  |------|------|
  | 规划 | 需求分析、架构设计 |
  | 开发 | 代码实现、最佳实践 |
  | 测试 | 单元测试、集成测试 |
  | 审查 | 代码审查、质量检查 |
  | 调试 | 问题定位、性能优化 |

### 4.6 Agentsys - 工作流自动化

- **GitHub**: [https://github.com/avifenesh/agentsys](https://github.com/avifenesh/agentsys)
- **功能**: 工作流自动化系统
- **特点**:
  - 任务到生产工作流
  - PR 管理
  - 代码清理
  - 性能调查
  - 多代理代码审查

### 4.7 Claude-Code-PM - 项目管理

- **GitHub**: [https://github.com/automazeio/ccpm](https://github.com/automazeio/ccpm)
- **功能**: 全面项目管理框架
- **特点**:
  - 敏捷开发支持
  - 任务管理
  - 进度跟踪
  - 团队协作

### 4.8 Git-Context-Controller - Git 上下文管理

- **功能**: Git 风格上下文管理框架
- **特点**:
  - 分支感知
  - 提交历史分析
  - 上下文切换

### 4.9 MCP-SSH-Manager - 远程管理

- **功能**: SSH 远程管理工具
- **特点**:
  - 37+ 远程工具
  - 安全连接
  - 批量操作

### 4.10 Claude-Forge - CLAUDE.md 管理

- **GitHub**: [https://github.com/charles-fore/claudeforge](https://github.com/charles-fore/claudeforge)
- **功能**: CLAUDE.md 生成和维护
- **特点**:
  - 自动上下文分析
  - 智能文档生成
  - 项目理解增强

---

## 五、部署建议

### 游戏客户端开发
```
推荐插件组合:
├── mcp-unity (Unity 集成, ⭐ 1,382)
├── mcp-unreal (Unreal 集成)
├── godot-development (Godot 开发)
├── claude-code-game-studios (48 代理)
└── auto-review-claude-mcp (PR 审查)
```

### Python 开发
```
推荐插件组合:
├── FastMCP (MCP 框架, ⭐ 23,383)
├── developer-kit (全栈工具, ⭐ 133)
├── context7-mcp-server (Python 文档)
├── fastapi-development (FastAPI 开发)
├── pydantic-ai-skills (AI Agent)
└── pypict-claude-skill (测试生成)
```

### 自动化测试
```
推荐插件组合:
├── mcp-inspector (MCP 测试, ⭐ 8,900)
├── playwright-mcp (Web 测试, ⭐ 3,581)
├── vibetest-use (AI QA, ⭐ 771)
├── skunit (单元测试)
├── playwright-skill (测试技能)
└── tdd-guard (TDD 原则)
```

### 开发者工具
```
推荐插件组合:
├── claude-tmux (会话管理)
├── claude-esp (调试工具)
├── rulesync (配置同步)
├── claude-hub (GitHub 集成)
├── superpowers (核心技能, ⭐ 4,100+)
├── agentsys (工作流自动化)
├── cc-pm (项目管理)
├── git-context-controller (Git 上下文)
├── mcp-ssh-manager (远程管理)
└── claude-forge (CLAUDE.md 管理)
```

---

## 六、总结

### 关键发现

1. **MCP 框架生态成熟**
   - FastMCP (23,383 ⭐) 领跑 Python 领域
   - MCP Inspector (8,900 ⭐) 成为测试标配

2. **游戏开发集成兴起**
   - Unity MCP (1,382 ⭐) 成熟度高
   - Unreal MCP 快速发展
   - Claude Code Game Studios 提供 48 专业代理

3. **开发者工具多元化**
   - 会话管理: Claude-Tmux
   - 调试工具: Claude-ESP
   - 配置同步: Rulesync

4. **测试自动化趋势**
   - Playwright MCP (3,581 ⭐) 主导 Web 测试
   - Vibetest-Use (771 ⭐) AI 驱动 QA
   - TDD Guard 强制测试原则

5. **启动模板标准化**
   - Claude-Starter-Kit 提供开箱即用环境
   - Developer-Kit (133 ⭐) 多语言支持

### 趋势预测

- **MCP 协议**将成为 AI 助手标准化接口
- **游戏引擎集成**将持续增长
- **测试自动化**将更多 AI 驱动
- **会话管理工具**将更加专业化

---
调研时间: 2026-03-05
