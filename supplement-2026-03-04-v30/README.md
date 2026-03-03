# Claude Code 热门插件补充调研 (第三十期)

> 调研时间: 2026-03-04 | 数据来源: GitHub Trending, awesome-claude-code

---

## 一、游戏客户端开发技能 (更新)

### 1.1 Claude Code Game Studios ⭐⭐ 强烈推荐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [Donchitos/Claude-Code-Game-Studios](https://github.com/Donchitos/Claude-Code-Game-Studios) |
| **Star** | ⭐ 30+ (持续增长) |
| **更新** | 活跃维护 |
| **特点** | 48个AI代理 + 36个工作流技能 + 完整协调系统 |

#### 核心能力

```markdown
# 工作室层级架构
├── Tier 1: 决策层 (Opus)
│   ├── creative-director: 创意总监
│   ├── technical-director: 技术总监
│   └── producer: 制作人
│
├── Tier 2: 部门Lead (Sonnet)
│   ├── game-designer: 游戏设计师
│   ├── lead-programmer: 首席程序员
│   ├── art-director: 美术总监
│   └── qa-lead: QA负责人
│
└── Tier 3: 专家层 (Sonnet/Haiku)
    ├── gameplay-programmer: 游戏逻辑程序
    ├── ui-programmer: UI程序
    └── tools-programmer: 工具程序
```

### 1.2 Unity 开发技能矩阵

| 技能 | GitHub | Star | 核心领域 |
|-----|--------|------|---------|
| **cc-plugin-unity-gamedev** | tjboudreaux/cc-plugin-unity-gamedev | ⭐1 | 21个专业技能 |
| **OH-Unity-GameDev-Skills** | OstrichHermit/OH-Unity-GameDev-Skills | ⭐6 | DoTween, MediaPipe |
| **unity-ai-workflow** | David-GD13/unity-ai-workflow | ⭐4 | Unity 6.2+ AI工作流 |
| **solana-game-skill** | solanabr/solana-game-skill | ⭐5 | Solana区块链游戏 |

### 1.3 机器人/游戏开发技能

| 技能 | GitHub | Star | 特点 |
|-----|--------|------|------|
| **robotics-agent-skills** | arpitg1304/robotics-agent-skills | ⭐115 | ROS1/ROS2 + 生产级机器人软件 |

#### 核心能力

```markdown
### 机器人开发技能
- ROS1/ROS2 集成
- 设计模式 (SOLID)
- 测试框架
- 嵌入式系统

### 适用场景
- 游戏物理引擎开发
- 机器人模拟
- 实时系统
```

---

## 二、Python 开发技能 (更新)

### 2.1 Python 开发框架

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **orchestkit** | yonatangross/orchestkit | ⭐98 | 61技能 + 36代理 + FastAPI/React/LangGraph |
| **claude-arsenal** | majiayu000/claude-arsenal | ⭐9 | 39+技能 + 9专业代理 |

#### orchestkit 核心特性

```markdown
### 技术栈覆盖
├── FastAPI
│   ├── RESTful API 设计
│   ├── 数据库集成 (SQLAlchemy)
│   └── 认证/授权
│
├── React 19
│   ├── 组件开发
│   ├── 状态管理
│   └── 性能优化
│
├── LangGraph
│   ├── Agent 工作流
│   ├── 状态机
│   └── 多代理编排
│
└── Testing & Security
    ├── 单元测试
    ├── 安全审计
    └── CI/CD
```

### 2.2 数据库集成

| 技能 | GitHub | 功能 | 安全性 |
|-----|--------|------|--------|
| **read-only-postgres** | jawwadfirdousi/agent-skills | PostgreSQL只读查询 | ⭐⭐⭐⭐⭐ |
| **supabase-pentest-skills** | yoanbernabeu/supabase-pentest-skills | ⭐31 | Supabase 安全审计 |

#### Supabase 安全审计技能

```markdown
### 安全检测能力
- 密钥提取检测
- RLS (Row Level Security) 测试
- 存储审计
- IDOR 检测
- 综合报告生成

### 适用场景
- Supabase 应用安全审计
- 权限配置验证
- 数据泄露检测
```

### 2.3 Python 测试技能

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **tap-test-skill** | aviz85/tap-test-skill | ⭐8 | 真实 API 集成测试 |
| **rego-skill** | Void3110/rego-skill | ⭐10 | OPA Rego 策略测试 |

#### tap-test-skill 特点

```markdown
### 核心特性
- 真实 HTTP 请求 (无 Mock)
- 真实数据库集成
- 端到端测试
- 集成测试优先

### 适用场景
- API 集成测试
- 微服务测试
- E2E 测试套件
```

---

## 三、自动化测试技能 (更新)

### 3.1 Playwright 测试

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **playwright-cli-agents** | yusuftayman/playwright-cli-agents | ⭐11 | Playwright E2E 测试生成 |
| **playwright-skill** | lackeyjb/playwright-skill | ⭐1.8k | 浏览器自动化 |

#### playwright-cli-agents 特性

```markdown
### 核心能力
├── 自动测试生成
│   ├── Page Object Model 模式
│   ├── 测试用例生成
│   └── 测试维护
│
├── 调试支持
│   ├── 失败截图
│   ├── 视频录制
│   └── 调试日志
│
└── CI/CD 集成
    ├── GitHub Actions
    ├── 并行执行
    └── 报告生成
```

### 3.2 测试评估框架

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **cc-plugin-eval** | sjnims/cc-plugin-eval | ⭐13 | 4阶段评估框架 |
| **vibe-testing** | knot0-com/vibe-testing | ⭐14 | LLM 推理压力测试 |

#### cc-plugin-eval 评估流程

```markdown
### 4阶段评估
1. 技能触发验证
2. 代理激活检测
3. 命令执行验证
4. LLM 判断整合

### 评估指标
- 技能触发率
- 响应准确性
- 执行效率
```

### 3.3 QA 测试目录

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **qaskills** | PramodDutta/qaskills | ⭐71 | QA 测试技能目录 |

#### 覆盖领域

```markdown
### 测试类型
- 单元测试
- 集成测试
- E2E 测试
- 性能测试
- 安全测试

### 工具支持
- Selenium
- Playwright
- Cypress
- Appium
```

---

## 四、开发者工具技能 (更新)

### 4.1 开发框架

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **Product-Manager-Skills** | deanpeters/Product-Manager-Skills | ⭐802 | 产品管理框架 |
| **claudest** | gupsammy/Claudest | ⭐34 | 插件市场 |

#### Product-Manager-Skills 核心

```markdown
### 产品管理能力
├── 需求分析
├── 路线规划
├── 用户研究
└── 数据分析

### 适用场景
- 产品需求文档
- 功能规划
- 用户故事编写
```

### 4.2 安全工具

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **supabase-pentest-skills** | yoanbernabeu/supabase-pentest-skills | ⭐31 | Supabase 安全审计 |
| **trailofbits-skills** | trailofbits/skills | - | CodeQL/Semgrep 集成 |

#### 安全测试覆盖

```markdown
### 检测类型
- 密钥泄露
- 权限配置错误
- SQL 注入
- XSS 攻击
- IDOR 漏洞

### 报告输出
- 详细问题描述
- 修复建议
- 风险等级
```

### 4.3 DevOps 工具

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **agent-skills** | terramate-io/agent-skills | ⭐26 | Terraform/Terramate |
| **safeclaw** | ykdojo/safeclaw | ⭐115 | 多会话容器管理 |

#### safeclaw 特性

```markdown
### 核心功能
├── 容器化隔离
│   ├── 独立会话
│   ├── 资源隔离
│   └── 安全边界
│
├── 仪表板管理
│   ├── 会话监控
│   ├── 资源使用
│   └── 日志查看
│
└── 快速部署
    ├── 一键启动
    ├── 默认配置
    └── 弹性扩展
```

### 4.4 Claude Code 最佳实践

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **jeffreysprompts.com** | Dicklesworthstone/jeffreysprompts.com | ⭐86 | 精选提示词集合 |
| **pm-ai-playbook** | fimoklei/pm-ai-playbook | ⭐8 | 产品经理 AI 手册 |

#### jeffreysprompts.com 特点

```markdown
### 提示词分类
├── 代码生成
├── 代码审查
├── 调试排错
├── 重构优化
└── 文档编写

### 安装方式
- 直接复制
- 安装为 Skills
- 定制化调整
```

### 4.5 Power Platform 开发

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| **power-platform-skills** | DanielKerridge/claude-code-power-platform-skills | ⭐8 | Power Apps/ Dataverse |

#### 覆盖领域

```markdown
### 开发能力
- Power Apps 开发
- Dataverse 配置
- 插件开发
- PCF 控件
- 部署管理

### 测试支持
- 单元测试
- 集成测试
- UAT 测试
```

---

## 五、技能选择决策树

### 5.1 游戏开发方向

```
游戏客户端开发?
├─ Unity → Claude-Code-Game-Studios
├─ Godot → unity-ai-workflow
├─ 区块链游戏 → solana-game-skill
├─ 机器人/物理 → robotics-agent-skills
└─ 通用 → Antigravity Skills
```

### 5.2 Python 开发方向

```
Python 开发?
├─ Web 框架 → orchestkit
├─ 数据库 → supabase-pentest-skills
├─ 测试 → tap-test-skill / qaskills
├─ 安全 → supabase-pentest-skills
└─ 全栈 → claude-arsenal
```

### 5.3 测试方向

```
自动化测试?
├─ Playwright → playwright-cli-agents
├─ 评估 → cc-plugin-eval
├─ 压力测试 → vibe-testing
├─ QA 流程 → qaskills
└─ 集成测试 → tap-test-skill
```

### 5.4 开发者效率方向

```
效率工具?
├─ 多会话 → safeclaw
├─ 产品管理 → Product-Manager-Skills
├─ 提示词 → jeffreysprompts.com
├─ DevOps → agent-skills
└─ 专业开发 → orchestkit
```

---

## 六、热门技能排行榜 (2026年3月)

### 6.1 总榜 Top 10

| 排名 | 技能 | Star | 类别 |
|------|------|------|------|
| 1 | antigravity-awesome-skills | ⭐18600 | 技能集合 |
| 2 | Product-Manager-Skills | ⭐802 | 产品管理 |
| 3 | robotics-agent-skills | ⭐115 | 机器人开发 |
| 4 | safeclaw | ⭐115 | 会话管理 |
| 5 | orchestkit | ⭐98 | 开发框架 |
| 6 | jeffreysprompts.com | ⭐86 | 提示词 |
| 7 | qaskills | ⭐71 | 测试 |
| 8 | Claudest | ⭐34 | 插件市场 |
| 9 | supabase-pentest-skills | ⭐31 | 安全 |
| 10 | agent-skills | ⭐26 | DevOps |

### 6.2 游戏开发方向 Top 5

| 排名 | 技能 | Star | 特点 |
|------|------|------|------|
| 1 | Claude-Code-Game-Studios | ⭐30+ | 48代理全栈 |
| 2 | robotics-agent-skills | ⭐115 | ROS/机器人 |
| 3 | unity-ai-workflow | ⭐4 | Unity 6.2+ |
| 4 | OH-Unity-GameDev-Skills | ⭐6 | DoTween/MediaPipe |
| 5 | solana-game-skill | ⭐5 | 区块链游戏 |

### 6.3 Python 开发方向 Top 5

| 排名 | 技能 | Star | 特点 |
|------|------|------|------|
| 1 | orchestkit | ⭐98 | 61技能全栈 |
| 2 | claude-arsenal | ⭐9 | 39+技能 |
| 3 | tap-test-skill | ⭐8 | 真实API测试 |
| 4 | rego-skill | ⭐10 | OPA策略测试 |
| 5 | supabase-pentest-skills | ⭐31 | 安全审计 |

### 6.4 测试方向 Top 5

| 排名 | 技能 | Star | 特点 |
|------|------|------|------|
| 1 | playwright-skill | ⭐1.8k | 浏览器自动化 |
| 2 | qaskills | ⭐71 | QA目录 |
| 3 | playwright-cli-agents | ⭐11 | E2E生成 |
| 4 | cc-plugin-eval | ⭐13 | 评估框架 |
| 5 | vibe-testing | ⭐14 | LLM推理 |

---

## 七、安装指南

### 7.1 快速安装

```bash
# 安装单个技能
claude install <skill-url>

# 示例: 安装 orchestkit
claude install https://github.com/yonatangross/orchestkit

# 安装到项目
cd your-project
claude install https://github.com/username/repo
```

### 7.2 技能组合推荐

```bash
# 游戏开发组合
Claude-Code-Game-Studios + robotics-agent-skills + unity-ai-workflow

# Python 开发组合
orchestkit + supabase-pentest-skills + tap-test-skill

# 测试自动化组合
playwright-cli-agents + qaskills + cc-plugin-eval

# 企业开发组合
safeclaw + Product-Manager-Skills + jeffreysprompts.com
```

---

## 八、总结与建议

### 8.1 趋势分析

1. **多代理协作**: Claude-Code-Game-Studios 引领多代理工作室模式
2. **专业化**: 垂直领域技能增多 (机器人、安全、测试)
3. **安全重视**: Supabase 安全审计技能需求增长
4. **测试智能化**: LLM 推理测试 (vibe-testing) 成为新方向

### 8.2 推荐策略

| 场景 | 首推技能 | 备选 |
|-----|---------|------|
| **游戏开发** | Claude-Code-Game-Studios | robotics-agent-skills |
| **Python 后端** | orchestkit | claude-arsenal |
| **测试自动化** | playwright-cli-agents | qaskills |
| **安全审计** | supabase-pentest-skills | trailofbits-skills |
| **开发者效率** | safeclaw | jeffreysprompts.com |

---

> 持续更新中，欢迎提交 Issue 补充更多优质技能！
