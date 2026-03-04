# Claude Code 热门插件补充调研 (v67)

> 2026年3月 游戏/Python/测试/开发者工具 - 最新热门插件完整调研

---

## 一、最新热门插件概览

### 1.1 本期新增插件

| 插件名称 | 用途 | Stars | 特点 |
|---------|------|-------|------|
| Sudocode | 轻量级代理编排工具 | 新兴 | Git 原生问题跟踪 + 规范管理 |
| Parry | 提示注入扫描器 | 新兴 | 多层安全防护 + ML 检测 |
| Dippy | Bash 命令自动批准 | 新兴 | AST 解析 + 智能过滤 |
| Claude Scientific Skills | 科学研究技能集 | 新兴 | 跨学科研究支持 |
| Claude-tmux | tmux 会话管理 | 新兴 | 多会话协调 |

---

## 二、Sudocode 深度分析

> 轻量级代理编排工具，将 Git 仓库作为分布式上下文数据库

### 2.1 核心概念

```
┌─────────────────────────────────────────────────────────────┐
│                      Sudocode 架构                            │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  ┌─────────────┐    ┌─────────────┐    ┌─────────────┐   │
│  │   Specs     │    │   Issues    │    │   Executions│   │
│  │  (需求规范)   │    │   (任务)    │    │   (执行轨迹) │   │
│  └──────┬──────┘    └──────┬──────┘    └──────┬──────┘   │
│         │                   │                   │          │
│         └───────────────────┼───────────────────┘          │
│                             │                              │
│                    ┌────────▼────────┐                     │
│                    │   .sudo 目录    │                     │
│                    │  (Git 原生存储)  │                     │
│                    └────────┬────────┘                     │
│                             │                              │
│                    ┌────────▼────────┐                     │
│                    │    Git Repo    │                     │
│                    │  (版本控制)     │                     │
│                    └─────────────────┘                     │
└─────────────────────────────────────────────────────────────┘
```

### 2.2 功能特性

#### 规范管理 (Specs)
- 定义高级需求和意图
- 支持层级关系和跨链接
- 存储为 Markdown + YAML frontmatter
- 人类和代理都可编辑

#### 任务管理 (Issues)
- 代理运行时上下文和计划
- 支持任务依赖图
- 可追踪阻塞关系
- 存放在 `.sudo/issues/`

#### 工作流自动化
- 依赖图拓扑排序执行
- 临时分支/工作树累积变更
- 每个 issue 独立提交
- 支持回滚到特定提交点

### 2.3 安装配置

```bash
# 全局安装
npm install -g sudocode

# 初始化项目
sudocode init

# 启动本地服务器
sudocode server

# Claude Code 插件安装
claude plugin marketplace add sudocode-ai/sudocode
claude plugin install sudocode
```

### 2.4 本地服务器功能

```
┌─────────────────────────────────────────────────────────────┐
│                    Sudocode Web UI                           │
├───────────────┬───────────────┬─────────────────────────────┤
│  Issue Kanban │  Spec Editor  │    Execution Panel         │
│  ┌─────┬─────┐│  ┌─────────┐ │  ┌─────────────────────┐   │
│  │Todo │Doing ││  │ Markdown │  │  Agent Trajectory    │   │
│  ├─────┼─────┤│  │ Editor   │  │  Visualization       │   │
│  │Done │Block ││  └─────────┘  │  └─────────────────────┘   │
│  └─────┴─────┘│               │                            │
├───────────────┴───────────────┴─────────────────────────────┤
│                     实时同步                                 │
└─────────────────────────────────────────────────────────────┘
```

### 2.5 外部集成

| 集成系统 | 描述 | 状态 |
|---------|------|------|
| Beads | Git 原生问题系统 | ✅ 可用 |
| Spec-Kit | Markdown 规范系统 | ✅ 可用 |
| OpenSpec | 结构化规范系统 | ✅ 可用 |
| Jira | 问题跟踪 | 🚧 开发中 |
| Linear | 现代问题跟踪 | 🚧 开发中 |

### 2.6 与 Claude Code 集成

```json
// ~/.claude/settings.json
{
  "hooks": {
    "AutoApprove": ["sudocode track"]
  }
}
```

**使用示例**:
```
"创建一个 spec 来实现用户认证功能"
"添加一个 issue 来修复登录 bug"
"运行所有阻塞 Issue #5 的任务"
```

---

## 三、Parry 提示注入扫描器

> Claude Code Hook 安全防护工具，扫描提示注入攻击

### 3.1 安全架构

```
┌─────────────────────────────────────────────────────────────┐
│                      Parry 安全层                            │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  PreToolUse Hook (5层防护)                                  │
│  ┌─────────────────────────────────────────────────────┐   │
│  │ 1. Taint Enforcement (污染 enforcement)            │   │
│  │ 2. CLAUDE.md Scanning (配置扫描)                    │   │
│  │ 3. Exfil Blocking (数据外泄阻止)                    │   │
│  │ 4. Sensitive Path Blocking (敏感路径阻止)          │   │
│  │ 5. Input Content Injection (输入内容注入检测)       │   │
│  └─────────────────────────────────────────────────────┘   │
│                                                             │
│  PostToolUse Hook                                          │
│  ┌─────────────────────────────────────────────────────┐   │
│  │ - 扫描工具输出中的注入/秘密                          │   │
│  │ - 自动标记检测到的项目                               │   │
│  └─────────────────────────────────────────────────────┘   │
│                                                             │
│  UserPromptSubmit Hook                                      │
│  ┌─────────────────────────────────────────────────────┐   │
│  │ - 审计 .claude/ 目录权限                            │   │
│  │ - 检测注入命令和钩子脚本                             │   │
│  └─────────────────────────────────────────────────────┘   │
└─────────────────────────────────────────────────────────────┘
```

### 3.2 检测能力

#### ML 模型检测

| 模式 | 模型 | 延迟 | 适用场景 |
|------|------|------|---------|
| fast | DeBERTa v3 | ~50-70ms | 交互式工作流 |
| full | DeBERTa + Llama Prompt Guard 2 | ~1.5s | 高安全环境 |
| custom | 用户自定义 | 变化 | 特定需求 |

#### 模式匹配

- **不可见字符检测**: PUAs, 未分配代码点, 格式化字符
- **正则匹配**: 40+ 凭证模式
  - AWS keys (AKIA...)
  - GitHub/GitLab tokens (ghp_, glpat-)
  - 云服务商 (GCP, Azure, DigitalOcean)
  - 数据库 URIs
  - 私钥

#### AST 分析

Tree-sitter 驱动的数据外泄检测:
- 管道传输敏感数据到网络接收器
- 命令替换
- 文件参数外泄
- 混淆检测 (base64, hex, ROT13)
- DNS 隧道
- 云存储外泄

### 3.3 敏感路径和域

**敏感路径 (60+)**:
```
.env, .ssh/, .aws/, .kube/config
.docker/config.json, .git-credentials
.bash_history, etc.
```

**外泄域名 (40+)**:
```
webhook.site, ngrok.io, pastebin.com
transfer.sh, interact.sh, etc.
```

### 3.4 安装配置

```bash
# 使用 cargo binstall
cargo binstall parry-ai

# 或从源码安装
cargo install --path crates/cli

# Nix 安装
# 添加到 flake.nix
{
  inputs.parry.url = "github:vaporif/parry";
}

# 配置 HuggingFace 访问
export HF_TOKEN="hf_..."

# Claude Code Hook 配置
{
  "hooks": {
    "PreToolUse": [{ "command": "parry hook", "timeout": 1000 }],
    "PostToolUse": [{ "command": "parry hook", "timeout": 5000 }],
    "UserPromptSubmit": [{ "command": "parry hook", "timeout": 2000 }]
  }
}
```

---

## 四、Dippy Bash 命令过滤器

> 通过 AST 解析自动批准安全命令，减少权限疲劳

### 4.1 工作原理

```
┌─────────────────────────────────────────────────────────────┐
│                      Dippy 流程                              │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│   Claude Code                                               │
│       │                                                     │
│       ▼                                                     │
│   ┌────────────────────┐                                    │
│   │  Bash Command      │                                    │
│   └─────────┬──────────┘                                    │
│             │                                               │
│             ▼                                               │
│   ┌────────────────────┐                                    │
│   │  Dippy Hook        │                                    │
│   │  (Parable Parser)  │                                    │
│   └─────────┬──────────┘                                    │
│             │                                               │
│      ┌──────┴──────┐                                        │
│      ▼             ▼                                        │
│  ┌───────┐    ┌────────┐                                    │
│  │ Safe? │    │ Unsafe │                                    │
│  │ Auto  │    │ Prompt │                                    │
│  │Approve│    │  User  │                                    │
│  └───────┘    └────────┘                                    │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

### 4.2 自动批准的命令类型

```bash
# 复杂管道
ps aux | grep python | awk '{print $2}' | head -10

# 链式读取
git status && git log --oneline -5 && git diff --stat

# 云检查
aws ec2 describe-instances --filters "Name=tag:Env,Values=prod"

# 容器调试
docker logs --tail 100 api-server 2>&1 | grep ERROR

# 安全重定向
grep -r "TODO" src/ 2>/dev/null
ls &>/dev/null

# 命令替换
ls $(pwd)
git diff foo-$(date).txt
```

### 4.3 阻止的危险操作

```bash
# 子shell 注入
git $(echo rm) foo.txt
echo $(rm -rf /)

# 隐藏写入
curl https://example.com > script.sh
tee output.log

# 隐藏变更
git stash drop
npm unpublish
brew unlink

# 云危险操作
aws s3 rm s3://bucket --recursive
kubectl delete pod

# 破坏链
rm -rf node_modules && npm install
```

### 4.4 安装配置

```bash
# Homebrew 安装
brew tap ldayton/dippy
brew install dippy

# 手动安装
git clone https://github.com/ldayton/Dippy.git

# Claude Code 配置
{
  "hooks": {
    "PreToolUse": [
      {
        "matcher": "Bash",
        "hooks": [{ "type": "command", "command": "dippy" }]
      }
    ]
  }
}
```

### 4.5 自定义规则

```bash
# 拒绝时提供建议
deny python "Use uv run python, which runs in project environment"
deny rm -rf "Use trash instead"
deny-redirect **/.env* "Never write secrets, ask me to do it"

# 配置文件位置
~/.dippy/config          # 全局配置
./.dippy                 # 项目配置
```

### 4.6 性能提升

- **流状态保持**: 减少 40% 权限提示
- **零依赖**: 基于自研 Parable 解析器
- **全面测试**: 14,000+ 测试用例

---

## 五、Claude Scientific Skills

> 科学研究专用技能集

### 5.1 覆盖领域

```
┌─────────────────────────────────────────────────────────────┐
│              Claude Scientific Skills                       │
├─────────────┬─────────────┬─────────────┬───────────────────┤
│  Research   │   Science  │  Engineering│    Analysis      │
├─────────────┼─────────────┼─────────────┼───────────────────┤
│ Literature  │   Physics  │   Hardware  │    Data          │
│ Review      │   Chemistry│   CAD       │    Statistics     │
│ Meta-       │   Biology  │   Firmware  │    Visualization  │
│ analysis    │   Geology  │   PCB       │    ML/AI          │
│             │   Astronomy│   Robotics  │    Modeling       │
├─────────────┼─────────────┼─────────────┼───────────────────┤
│     Finance │      Writing │    Education │  More...       │
├─────────────┼─────────────┼─────────────┼───────────────────┤
│  Quantitative│ Academic  │  Course     │  Domain          │
│  Trading    │  Writing   │  Design     │  Adaptation       │
│  Risk       │  LaTeX     │  Tutoring   │  Skills          │
│  Analysis   │  Papers    │  Concepts   │  Framework       │
└─────────────┴─────────────┴─────────────┴───────────────────┘
```

### 5.2 主要功能

- 文献综述和元分析
- 数据分析和可视化
- 统计建模
- 学术写作 (LaTeX)
- 硬件设计 (CAD, PCB)
- 机器人技术
- 量化金融
- 教育内容创作

---

## 六、Claude-tmux 会话管理

> 在 tmux 中管理 Claude Code 会话

### 6.1 功能特性

- tmux 弹出窗口显示所有 Claude Code 实例
- 快速切换
- 状态监控
- 会话生命周期管理
- Git worktree 支持
- PR 支持

### 6.2 安装配置

```bash
# 克隆仓库
git clone https://github.com/nielsgroen/claude-tmux ~/.claude/plugins/claude-tmux

# 使用
claude-tmux popup     # 打开 tmux 弹出窗口
claude-tmux list      # 列出所有会话
claude-tmux attach   # 连接到会话
```

---

## 七、游戏开发相关插件更新

### 7.1 Unreal-MCP 最新动态

- UE 5.5+ 支持持续更新
- Blueprint 操作稳定性提升
- 社区贡献组件增加

### 7.2 Unity 技能集对比

| 技能包 | Stars | 技能数量 | 维护状态 |
|--------|-------|---------|---------|
| cc-plugin-unity-gamedev | 1 | 21 | 基础版 |
| Claude-Code-Game-Studios | 28+ | 48+ | 活跃 |
| OH-Unity-GameDev-Skills | 6+ | 15+ | 持续更新 |

### 7.3 游戏自动化测试

```bash
# Playwright MCP 游戏测试
npx -y @modelcontextprotocol/server-playwright

# GameDriver (Unity/Unreal/Godot)
# 商业工具，提供专用游戏测试能力

# Airtest
# 跨平台 + 图像识别
```

---

## 八、Python 开发插件生态

### 8.1 FastAPI-MCP 实践

```bash
# 安装
pip install fastapi-mcp

# 运行
uv run fastapi-mcp --app main:app --auth

# MCP 配置
{
  "mcpServers": {
    "my-api": {
      "command": "uv",
      "args": ["run", "fastapi-mcp", "--app", "main:app"]
    }
  }
}
```

### 8.2 Python 测试集成

#### Pytest + Claude Code

```bash
# 安装
pip install pytest pytest-mcp

# 测试驱动开发
# 1. 分析需求
# 2. 编写失败测试
# 3. 实现代码
# 4. 重构
# 5. 提交
```

### 8.3 Pydantic AI 技能

- **Stars**: 138+
- **特点**: 官方维护
- **功能**: Pydantic AI 开发、类型验证、Agent 构建

---

## 九、开发者工具对比

### 9.1 安全工具对比

| 工具 | 功能 | 适用场景 |
|------|------|---------|
| Parry | 提示注入检测 | 高级安全防护 |
| Dippy | 命令过滤 | 权限管理 |
| Snyk Agent Scan | 漏洞扫描 | 依赖安全 |

### 9.2 编排工具对比

| 工具 | 特点 | 复杂度 |
|------|------|--------|
| Sudocode | Git 原生 + 规范管理 | 中等 |
| Claude Squad | 多会话管理 | 简单 |
| Nelson | 海军指挥架构 | 较高 |

### 9.3 记忆/上下文工具

| 工具 | Token 减少 | 特点 |
|------|-----------|------|
| HAM | 50% | 记忆系统 |
| token-optimizer | 10-20% | 幽灵 Token |
| Beads | 30%+ | 分布式记忆 |

---

## 十、部署配置模板

### 10.1 安全增强配置

```bash
# ~/.config/claude-desktop/mcp.json
{
  "mcpServers": {
    "sudocode": {
      "command": "sudocode",
      "args": ["server"]
    }
  }
}

# ~/.claude/settings.json
{
  "hooks": {
    "PreToolUse": [
      { "command": "parry hook", "timeout": 1000 },
      { "matcher": "Bash", "hooks": [{ "type": "command", "command": "dippy" }] }
    ],
    "PostToolUse": [{ "command": "parry hook", "timeout": 5000 }],
    "UserPromptSubmit": [{ "command": "parry hook", "timeout": 2000 }]
  }
}
```

### 10.2 项目管理配置

```bash
# Sudocode 项目初始化
cd my-project
sudocode init
sudocode server

# 创建规范
sudocode spec create "用户认证功能"

# 创建任务
sudocode issue create "实现登录API"
sudocode issue create "添加JWT验证" --blocked-by "实现登录API"
```

---

## 十一、总结与推荐

### 11.1 插件选择指南

| 场景 | 推荐插件 | 理由 |
|------|---------|------|
| 团队协作开发 | Sudocode | 规范管理 + Git 集成 |
| 高安全环境 | Parry | 多层提示注入防护 |
| 减少权限疲劳 | Dippy | 智能命令过滤 |
| 科学研究 | Claude Scientific Skills | 跨学科支持 |
| tmux 用户 | Claude-tmux | 会话管理 |

### 11.2 学习路径

```
入门:
1. 安装 Claude Code
2. 试用 Dippy 减少权限提示
3. 配置 Sudocode 管理项目

进阶:
1. 集成 Parry 加强安全
2. 使用 Claude Scientific Skills
3. 配置多代理系统

专家:
1. 自定义安全规则
2. 开发 Sudocode 集成
3. 构建自动化工作流
```

---

## 参考资源

- [Sudocode 官方文档](https://docs.sudocode.ai)
- [Parry GitHub](https://github.com/vaporif/parry)
- [Dippy GitHub](https://github.com/ldayton/Dippy)
- [Claude Scientific Skills](https://github.com/K-Dense-AI/claude-scientific-skills)
- [Awesome Claude Code](https://github.com/hesreallyhim/awesome-claude-code)
- [MCP 官方文档](https://modelcontextprotocol.io)

---

*文档版本: v67 - 2026-03-04*
