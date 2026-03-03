# Claude Code 插件调研报告 - 2026年3月 (补充-第六期)

> 持续跟踪 Claude Code 生态热门插件，聚焦游戏开发、Python 开发、自动化测试、开发者工具方向

---

## 📋 调研概要

| 维度 | 统计 |
|-----|------|
| **调研时间** | 2026-03-04 |
| **覆盖方向** | 游戏开发、Python开发、自动化测试、开发者工具 |
| **技能总数** | 150+ 精选 |
| **数据来源** | awesome-claude-code, GitHub trending, Antigravity Skills |

---

## 一、游戏客户端开发技能 (补充)

### 1.1 Claude Code Game Studios ⭐ 主流

| 项目 | 说明 |
|-----|------|
| **GitHub** | [Donchitos/Claude-Code-Game-Studios](https://github.com/Donchitos/Claude-Code-Game-Studios) |
| **Star** | ⭐ 26 |
| **更新** | 3天前 |
| **特点** | 48个AI代理 + 36个工作流技能 + 完整协调系统 |

#### 核心能力

- **48个专业AI代理**: 覆盖游戏开发全流程
- **36个工作流技能**: 完整游戏开发管线
- **工作室协调系统**: 模拟真实游戏工作室工作流
- **多引擎支持**: Unity, Unreal, Godot, WebGL

### 1.2 Antigravity 游戏开发技能

#### 核心 Skills 矩阵

| Skill ID | 名称 | 核心能力 | 适用引擎 | 评分 |
|----------|------|---------|---------|------|
| unity-developer | Unity 6 LTS 专家 | URP/HDRP、跨平台部署 | Unity | ⭐⭐⭐⭐⭐ |
| unity-ecs-patterns | DOTS/ECS 架构 | Jobs System、Burst | Unity | ⭐⭐⭐⭐⭐ |
| unreal-engine-cpp-pro | UE5 C++ 开发 | UObject、网络同步 | Unreal | ⭐⭐⭐⭐⭐ |
| godot-gdscript-patterns | Godot 4 专家 | GDScript 2.0、信号系统 | Godot | ⭐⭐⭐⭐ |
| bevy-ecs-expert | Bevy ECS | Rust 游戏引擎 | Bevy | ⭐⭐⭐⭐⭐ |
| game-development | 游戏开发编排器 | 自动路由到子 Skills | 通用 | ⭐⭐⭐⭐ |

### 1.3 网络同步专题

| 技术点 | 说明 |
|--------|------|
| 帧同步 | 相同输入 → 相同输出，确定性 |
| 状态同步 | 服务器权威，状态差异同步 |
| 延迟补偿 | Jitter: 0-200ms, 丢包: 5%-20% |
| 客户端预测 | 本地先行，回滚机制 |

---

## 二、Python 开发技能 (补充)

### 2.1 Python Skills 完整列表

| Skill ID | 名称 | 核心能力 | 评分 |
|----------|------|---------|------|
| python-pro | Python 3.12+ 专家 | 现代特性、生产级实践 | ⭐⭐⭐⭐⭐ |
| python-fastapi-development | FastAPI 开发 | SQLAlchemy、Pydantic | ⭐⭐⭐⭐⭐ |
| async-python-patterns | 异步编程 | asyncio、高并发 | ⭐⭐⭐⭐ |
| python-patterns | 设计模式 | 类型提示、最佳实践 | ⭐⭐⭐⭐ |
| python-performance-optimization | 性能优化 | cProfile、py-spy | ⭐⭐⭐⭐ |
| python-testing-patterns | 测试模式 | pytest、fixtures、TDD | ⭐⭐⭐⭐⭐ |
| python-packaging | PyPI 发布 | 包管理、版本控制 | ⭐⭐⭐⭐ |
| python-development-python-scaffold | 项目脚手架 | uv 工具链 | ⭐⭐⭐⭐ |

### 2.2 Modern Python 工具链

| 工具 | 用途 | 性能 |
|------|------|------|
| **uv** | 包管理器 | 10-100x pip |
| **ruff** | 格式化/lint | 替代 black/isort/flake8 |
| **mypy/pyright** | 类型检查 | 严格模式 |
| **pyproject.toml** | 项目配置 | 现代标准 |

### 2.3 FastAPI 高级特性

- FastAPI 0.100+ 新特性
- Pydantic V2 数据验证
- 自动 OpenAPI/Swagger
- WebSocket 实时通信
- BackgroundTasks 后台任务
- SQLAlchemy 2.0+ 异步
- Repository 模式

### 2.4 AWS 云服务集成

#### AWS MCP Server

| 项目 | 说明 |
|-----|------|
| **GitHub** | [alexei-led/aws-mcp-server](https://github.com/alexei-led/aws-mcp-server) |
| **语言** | Python |
| **特点** | AWS CLI 集成，多环境支持 |

#### 支持的服务

| 服务类别 | 支持内容 |
|---------|---------|
| **计算** | EC2, Lambda, ECS, EKS |
| **存储** | S3, EBS, EFS |
| **数据库** | RDS, DynamoDB, ElastiCache |
| **网络** | VPC, CloudFront, Route53 |
| **安全** | IAM, Secrets Manager |

---

## 三、游戏客户端自动化测试 (补充)

### 3.1 浏览器自动化测试 - Playwright

#### Playwright Skill (核心)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [lackeyjb/playwright-skill](https://github.com/lackeyjb/playwright-skill) |
| **Star** | ⭐ 1.8k |
| **功能** | Playwright 浏览器自动化 |
| **特点** | 模型调用的 Playwright 自动化 |

#### 核心功能

- **Web 应用测试**: 自动化测试 Web 应用功能
- **UI 验证**: 验证前端功能和行为
- **截图捕获**: 自动截图记录测试状态
- **调试支持**: 辅助调试 UI 行为
- **Bot 检测绕过**: Patchright 支持反检测

### 3.2 Playwright Bot Bypass

| 项目 | 说明 |
|-----|------|
| **GitHub** | [greekr4/playwright-bot-bypass](https://github.com/greekr4/playwright-bot-bypass) |
| **特点** | Bot 检测绕过 (Google CAPTCHA 等) |

### 3.3 游戏客户端测试方案

| 测试类型 | 工具 | 适用场景 |
|---------|------|---------|
| 单元测试 | Unity Test Framework, pytest | 游戏逻辑验证 |
| 集成测试 | Playwright, Selenium | 客户端与服务端交互 |
| UI测试 | Playwright, Appium | 游戏UI交互 |
| 性能测试 | Unity Profiler, RenderDoc | 帧率、内存测试 |
| 回归测试 | CI/CD + Playwright | 版本发布验证 |

### 3.4 TDD 开发流程

| 阶段 | 动作 | 必须执行 |
|------|------|---------|
| RED | 写失败的测试 | ✅ |
| VERIFY | 验证失败原因 | ✅ |
| GREEN | 最小代码通过 | ✅ |
| VERIFY | 验证测试通过 | ✅ |
| REFACTOR | 重构改进 | 可选 |

**TDD 铁律**: NO PRODUCTION CODE WITHOUT A FAILING TEST FIRST

---

## 四、其他开发者工具 (补充)

### 4.1 Agent 编排工具

| 项目 | GitHub | 功能 |
|------|--------|------|
| **Claude Squad** | smtg-ai/claude-squad | 终端应用管理多个 Claude Code、Codex |
| **Claude Swarm** | parruda/claude-swarm | 连接 Claude Code 到代理群体 |
| **sudocode** | sudocode-ai/sudocode | 轻量级 agent 编排开发工具 |
| **Auto-Claude** | AndyMik90/Auto-Claude | 自主多代理框架，SDLC 全流程 |

### 4.2 IDE 集成

| 工具 | GitHub | 平台 |
|-----|--------|------|
| **claude-code.nvim** | greggh/claude-code.nvim | Neovim |
| **claude-code.el** | stevemolitor/claude-code.el | Emacs |
| **Claude Code Chat** | andrepimenta/claude-code-chat | VS Code |
| **Claudix** | Haleclipse/Claudix | VS Code |
| **claude-code-ide.el** | manzaltu/claude-code-ide.el | Emacs 增强 |

### 4.3 Hook 系统

| 技能 | GitHub | 语言 |
|-----|--------|------|
| **claude-hooks** | johnlindquist/claude-hooks | TypeScript |
| **cchooks** | GowayLee/cchooks | Python |
| **claude-code-hooks-sdk** | beyondcode/claude-hooks-sdk | PHP |

### 4.4 使用监控

| 项目 | GitHub | 功能 |
|------|--------|------|
| **CC Usage** | ryoppippi/ccusage | CLI 管理和分析使用情况 |
| **ccflare** | snipeship/ccflare | Web 仪表盘 |
| **better-ccflare** | tombii/better-ccflare | ccflare 增强分支 |
| **Claudex** | kunwar-shah/claudex | Web 浏览器探索历史 |

### 4.5 记忆与上下文

| 项目 | GitHub | 功能 |
|------|--------|------|
| **HAM** | kromahlusenii-ops/ham | AI 记忆系统，减少 50% token |
| **Claude Mem** | thedotmack/claude-mem | 自动捕获编码会话 |
| **ContextKit** | FlineDev/ContextKit | 4阶段规划方法论 |

### 4.6 安全工具

| 项目 | GitHub | 特点 |
|------|--------|------|
| **trailofbits-skills** | trailofbits/skills | CodeQL/Semgrep 集成 |
| **parry** | vaporif/parry | 提示注入扫描器 |
| **Dippy** | ldayton/Dippy | AST 自动批准安全命令 |

### 4.7 替代客户端

| 项目 | GitHub | 特点 |
|------|--------|------|
| **claude-esp** | phiat/claude-esp | Go TUI 隐藏输出流式传输 |
| **claude-tmux** | nielsgroen/claude-tmux | tmux 会话管理 |
| **Omnara** | omnara-ai/omnara | 跨终端同步 |
| **crystal** | stravu/crystal | 桌面应用编排 |

### 4.8 Slash Commands 分类

#### 版本控制 & Git

| 命令 | 来源 | 功能 |
|-----|------|------|
| /commit | evmts/tevm-monorepo | 传统提交格式 |
| /create-pr | toyamarinyon/giselle | 完整 PR 工作流 |
| /fix-github-issue | jeremymailen/kotlinter-gradle | GitHub Issue 修复 |

#### 代码分析 & 测试

| 命令 | 来源 | 功能 |
|-----|------|------|
| /check | rygwdn/slack-tools | 代码质量和安全检查 |
| /tdd | zscott/pane | TDD 开发流程 |
| /repro-issue | rzykov/metabase | 可复现测试用例 |

#### 项目管理

| 命令 | 来源 | 功能 |
|-----|------|------|
| /create-plan | hesreallyhim/inkverse-fork | 产品需求文档 |
| /prd-generator | dredozubov/prd-generator | PRD 生成器 |
| /todo | chrisleyva/todo-slash-command | 待办事项管理 |

---

## 五、推荐技能组合

### 5.1 游戏开发组合

```
推荐: /game-development (编排器，自动路由)
     /unity-developer + /unity-ecs-patterns
     /godot-gdscript-patterns + /2d-games
     /unreal-engine-cpp-pro + /glsl-shaders
     /bevy-ecs-expert (Rust 游戏引擎)
```

### 5.2 Python 开发组合

```
推荐: /python-pro + /python-fastapi-development + /python-testing-patterns
     /fastapi-pro + /async-python-patterns + /python-performance-optimization
     /temporal-python-pro + /python-testing-patterns (分布式工作流)
```

### 5.3 自动化测试组合

```
推荐: /e2e-testing-patterns + /playwright-skill + /testing-qa
     /python-testing-patterns + /test-driven-development
     /ai-test-automation (AI 驱动测试)
```

### 5.4 DevOps 组合

```
推荐: /workflow-automation + /deployment-engineer + /debugging-strategies
     /dependency-upgrade + /dependency-management
     /defensive-bash + /bats-testing
```

---

## 六、趋势分析

### 技术趋势

| 方向 | 趋势 | 说明 |
|-----|------|------|
| **Agent工作流** | ⬆️ 上升 | agentsys, Claude Code Flow, Claude Squad |
| **安全审计** | ⬆️ 上升 | trailofbits-skills, parry, Dippy |
| **游戏开发** | ⬆️ 上升 | Claude Code Game Studios, Unity 6 LTS, DOTS |
| **测试自动化** | ⬆️ 上升 | Playwright 主导，TDD 命令丰富 |
| **Hook 生态** | ⬆️ 上升 | 多语言 SDK (Python, PHP, TypeScript) |
| **替代客户端** | ⬆️ 上升 | Claude-tmux, Omnara, crystal |

### 技术栈分布

- **TypeScript**: 35+ 技能
- **Python**: 25+ 技能
- **Go**: 5+ 技能 (cc-tools, ccexp, claude-esp)
- **PHP**: 2+ 技能 (claude-hooks-sdk)

---

## 七、实战案例

### 案例 1: 使用 Skills 开发帧同步游戏后端

```bash
# 1. 项目初始化
>> /python-pro 创建一个新的 Python 项目，使用 uv 管理依赖

# 2. FastAPI 开发
>> /fastapi-pro 设计帧同步游戏的 REST API

# 3. 异步处理
>> /async-python-patterns 实现游戏房间管理，高并发

# 4. 测试
>> /python-testing-patterns 编写房间管理测试
>> /test-driven-development 使用 TDD 开发新功能

# 5. 部署
>> /deployment-engineer 设置 Docker 部署
>> /workflow-automation 配置 CI/CD
```

### 案例 2: 使用 Skills 测试游戏客户端

```bash
# 1. 单元测试
>> /python-testing-patterns 编写同步逻辑测试

# 2. E2E 测试
>> /playwright-skill 测试游戏 Web 管理后台
>> /e2e-testing-patterns 测试用户注册流程

# 3. 质量保证
>> /testing-qa 建立完整 QA 流程
>> /ai-test-automation 设置 AI 驱动测试
```

---

## 八、总结

本期调研亮点：

1. **游戏开发**: Claude Code Game Studios (48 代理) + Unity 6 LTS DOTS + Godot 4
2. **Python 工具链**: uv (10-100x pip) + ruff + mypy
3. **测试自动化**: Playwright 1.8k stars + TDD 命令体系
4. **代理编排**: Claude Squad/Swarm + Auto-Claude
5. **安全增强**: parry 提示注入扫描 + Dippy AST 安全批准
6. **IDE 集成**: Neovim/Emacs/VSCode 全覆盖

---

## 📚 参考链接

- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
- [awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills)
- [Claude Code Handbook](https://nikiforovall.blog/claude-code-rules/)
- [Claude Code Ultimate Guide](https://github.com/FlorianBruniaux/claude-code-ultimate-guide)
- [Claude Code Game Studios](https://github.com/Donchitos/Claude-Code-Game-Studios)
- [Unity AI Workflow](https://github.com/David-GD13/unity-ai-workflow)
- [Playwright Skill](https://github.com/lackeyjb/playwright-skill)
- [Trail of Bits Skills](https://github.com/trailofbits/skills)
- [Claude Code Tools](https://github.com/pchalasani/claude-code-tools)
- [AWS MCP Server](https://github.com/alexei-led/aws-mcp-server)

---

*持续更新中，欢迎提交 PR 补充更多技能*
