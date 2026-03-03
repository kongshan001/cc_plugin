# Claude Code 插件调研补充 - 2026年3月

## 📋 文档信息

- **调研日期**: 2026-03-03
- **分类**: 补充调研 / 最新插件
- **状态**: 🆕 持续更新

---

## 一、最新热门插件 (2026年3月)

### 1.1 Claude Scientific Skills

| 项目 | 说明 |
|-----|------|
| **GitHub** | [K-Dense-AI/claude-scientific-skills](https://github.com/K-Dense-AI/claude-scientific-skills) |
| **Star** | ⭐ 活跃 |
| **许可** | MIT |
| **特点** | 科研/工程/分析/金融/写作技能集 |

### 核心功能

- **科研技能**: 文献综述、实验设计、数据分析
- **工程技能**: 软件工程、系统设计、代码审查
- **分析技能**: 数据分析、统计分析、机器学习
- **金融技能**: 财务分析、投资组合、风险评估
- **写作技能**: 技术文档、论文撰写、报告生成

### 适用场景

- 学术研究
- 工程开发
- 数据分析
- 金融建模
- 技术写作

---

### 1.2 parry - 提示注入扫描器

| 项目 | 说明 |
|-----|------|
| **GitHub** | [vaporif/parry](https://github.com/vaporif/parry) |
| **Star** | 🆕 新兴 |
| **类型** | 安全工具 / Hook |
| **特点** | 检测提示注入攻击 |

### 核心功能

- **注入检测**: 扫描工具输入/输出中的注入攻击
- **密钥检测**: 识别敏感信息泄露
- **数据外泄防护**: 防止数据外泄尝试
- **Hook 集成**: 作为 Claude Code Hook 运行

### 安全特性

```
输入验证 → 模式匹配 → 风险评估 → 拦截/警告
```

### 适用场景

- 安全敏感项目
- 防止提示注入攻击
- 保护敏感数据
- 代码审查安全检查

---

### 1.3 Dippy - AST 安全命令批准

| 项目 | 说明 |
|-----|------|
| **GitHub** | [ldayton/Dippy](https://github.com/ldayton/Dippy) |
| **Star** | 🆕 新兴 |
| **支持** | Claude Code / Gemini CLI / Cursor |
| **特点** | AST 自动批准安全命令 |

### 核心功能

- **AST 解析**: 使用抽象语法树分析命令
- **自动批准**: 对安全操作自动批准
- **交互确认**: 对危险操作提示确认
- **权限疲劳解决**: 无需禁用安全设置

### 技术原理

```typescript
// 命令分析流程
命令输入 → AST 解析 → 风险评估 → 决策(批准/确认)
```

### 适用场景

- 减少权限确认提示
- 平衡安全性与效率
- 团队统一安全策略

---

### 1.4 sudocode - 轻量级代理编排

| 项目 | 说明 |
|-----|------|
| **GitHub** | [sudocode-ai/sudocode](https://github.com/sudocode-ai/sudocode) |
| **Star** | 🆕 新兴 |
| **类型** | 编排工具 |
| **特点** | 集成 Jira 的轻量级代理编排 |

### 核心功能

- **代理编排**: 多代理协作工作流
- **Jira 集成**: 与项目管理工具无缝集成
- **规范框架**: 支持多种规范框架
- **轻量级**: 最小化依赖

### 与 Jira 集成

```
sudocode → Jira Issue → 任务分解 → 代理执行 → 状态更新
```

---

### 1.5 claude-tmux - tmux 会话管理

| 项目 | 说明 |
|-----|------|
| **GitHub** | [nielsgroen/claude-tmux](https://github.com/nielsgroen/claude-tmux) |
| **Star** | 🆕 新兴 |
| **类型** | 会话管理工具 |
| **平台** | Linux/macOS |

### 核心功能

- **tmux 集成**: 在 tmux 中管理 Claude Code
- **弹出菜单**: tmux popup 显示所有实例
- **快速切换**: 实例间快速切换
- **状态监控**: 实时监控会话状态
- **生命周期**: 完整的会话管理
- **PR 支持**: Git worktree 和 PR 支持

### 使用方式

```bash
# 启动 claude-tmux
claude-tmux

# 在 tmux 中使用
Prefix + ?  # 打开弹出菜单
```

---

### 1.6 claude-esp - 隐藏输出流式传输

| 项目 | 说明 |
|-----|------|
| **GitHub** | [phiat/claude-esp](https://github.com/phiat/claude-esp) |
| **Star** | 🆕 新兴 |
| **技术栈** | Go / TUI |
| **特点** | 流式传输 Claude Code 隐藏输出 |

### 核心功能

- **隐藏输出**: 监控 thinking、tool calls、subagents
- **多会话**: 同时监控多个会话
- **内容过滤**: 按内容类型过滤
- **后台任务**: 跟踪后台任务
- **调试友好**: 理解 Claude 内部工作原理

### 使用场景

- 调试代理行为
- 理解 Claude 决策过程
- 监控多个会话
- 学习 Claude 提示技术

---

## 二、安全相关插件

### 2.1 安全技能对比

| 插件 | 功能 | 适用场景 |
|-----|------|---------|
| **parry** | 提示注入扫描 | 输入安全检查 |
| **Dippy** | AST 命令批准 | 权限管理 |
| **trailofbits-skills** | CodeQL/Semgrep | 代码审计 |

### 2.2 安全插件选择建议

```
安全需求?
├─ 提示注入防护 → parry
├─ 命令权限管理 → Dippy
├─ 代码漏洞扫描 → trailofbits-skills
└─ 全面安全审计 → 组合使用
```

---

## 三、开发者效率插件

### 3.1 会话管理

| 插件 | 功能 | 特点 |
|-----|------|------|
| **claude-tmux** | tmux 集成 | 弹出菜单、快速切换 |
| **Claude Session Restore** | 跨会话恢复 | ZENG3LD/claude-session-restore |
| **recall** | 全文搜索 | zippoxer/recall 会话历史 |

### 3.2 工作流编排

| 插件 | 功能 | 特点 |
|-----|------|------|
| **sudocode** | 轻量编排 | Jira 集成 |
| **Claude Squad** | 多工作区 | smtg-ai/claude-squad |
| **Claude Swarm** | 多代理协同 | parruda/claude-swarm |

### 3.3 使用监控

| 插件 | 功能 | 平台 |
|-----|------|------|
| **CC Usage** | CLI 分析 | ryoppippi/ccusage |
| **ccflare** | Web 仪表板 | snipeship/ccflare |
| **Claudex** | 历史浏览器 | kunwar-shah/claudex |

---

## 四、新兴插件趋势

### 4.1 2026年3月趋势分析

| 方向 | 趋势 | 说明 |
|-----|------|------|
| **安全增强** | ⬆️ 上升 | parry、Dippy 等安全工具涌现 |
| **会话管理** | ⬆️ 上升 | tmux、session restore |
| **多代理协作** | ⬆️ 上升 | Swarm、Squad |
| **调试/监控** | ➡️ 稳定 | claude-esp、usage monitors |

### 4.2 值得关注的新插件

- **Claude Code Flow**: 代码优先编排层
- **Claude Swarm**: 多代理协同工作
- **Context Engineering Kit**: 上下文工程
- **Everything Claude Code**: 全方位资源库
- **Book Factory**: 自动化出版工作流

---

## 五、安装指南

### 5.1 安装新插件

```bash
# 克隆插件仓库
git clone https://github.com/用户名/插件名.git

# 复制到 Claude Code
cp -r 插件名 ~/.claude/

# 或使用技能安装
claude --install-skill gh-用户名-插件名
```

### 5.2 配置安全插件

```bash
# 配置 parry (提示注入扫描)
cd parry
./install.sh

# 配置 Dippy (命令批准)
cd Dippy
./setup.sh
```

---

## 六、推荐插件组合

### 6.1 基础开发套件

| 插件 | 用途 |
|-----|------|
| **fullstack-dev-skills** | 全栈开发 |
| **playwright-skill** | 自动化测试 |
| **cc-devops-skills** | DevOps |

### 6.2 安全增强套件

| 插件 | 用途 |
|-----|------|
| **parry** | 注入防护 |
| **Dippy** | 权限管理 |
| **trailofbits-skills** | 代码审计 |

### 6.3 效率提升套件

| 插件 | 用途 |
|-----|------|
| **claude-tmux** | 会话管理 |
| **Claude Code Tools** | 上下文保持 |
| **claude-esp** | 调试监控 |

---

## 📎 相关资源

- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
- [awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills)
- [Claude Code 官方文档](https://docs.anthropic.com/en/docs/claude-code)

---

*持续更新中，欢迎提交 PR 补充更多插件*
