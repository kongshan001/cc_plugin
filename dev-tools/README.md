# Claude Code 开发者工具技能补充调研

## 📋 文档信息

- **调研日期**: 2026-03-03
- **分类**: 开发者工具 / 效率提升 / 生产力 / DevOps / 云服务
- **状态**: ✅ 补充调研

---

## 1. 工作流自动化系统

### 1.1 AgentSys (推荐)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [avifenesh/agentsys](https://github.com/avifenesh/agentsys) |
| **Star** | ⭐ 活跃 (v5.3.7) |
| **特点** | 生产级工作流系统 |

### 核心功能

- **插件系统**: 灵活的插件机制
- **代理集成**: 多代理协作
- **任务自动化**: 端到端自动化
- **PR 管理**: 自动化的 PR 处理
- **代码清理**: 自动代码优化
- **性能调查**: 性能问题诊断

### 技术特点

- **确定检测**: 使用正则和 AST
- **LLM 判断**: 智能决策
- **生产验证**: 经过生产环境测试
- **全面测试**: 数千行代码 + 数千测试

### 适用场景

- 大型项目管理
- 团队协作流程
- 自动化代码审查
- CI/CD 集成

### 1.2 Superpowers

| 项目 | 说明 |
|-----|------|
| **GitHub** | [obra/superpowers](https://github.com/obra/superpowers) |
| **Star** | ⭐ 热门 (v4.1.1) |
| **状态** | ✅ 已验证可用 |

### 核心功能

- **SDLC 全覆盖**: 从规划到发布
- **代码审查**: 专业化审查技能
- **测试驱动**: TDD 开发流程
- **调试技能**: 问题追踪定位

### 包含技能列表

| 技能名称 | 功能 |
|---------|------|
| brainstorming | 结构化头脑风暴 |
| test-driven-development | TDD 开发流程 |
| finishing-a-development-branch | 分支完成工作流 |
| root-cause-tracing | 根因追踪 |
| using-git-worktrees | Git Worktree 使用 |

### 1.3 Claude Code Agents

| 项目 | 说明 |
|-----|------|
| **GitHub** | [undeadlist/claude-code-agents](https://github.com/undeadlist/claude-code-agents) |
| **特点** | 全面的端到端开发 |

### 核心功能

- **多个审计代理**: 并行运行代码审计
- **自动化修复**: 微检查点协议
- **浏览器 QA**: 基于浏览器的质量保证
- **防失控协议**: 严格的安全机制

### 1.4 Claude Code Flow

| 项目 | 说明 |
|-----|------|
| **GitHub** | [ruvnet/claude-code-flow](https://github.com/ruvnet/claude-code-flow) |
| **特点** | 代码优先编排层 |

### 核心功能

- **递归代理循环**: 自动迭代开发
- **代码编写/编辑/测试**: 完整开发流程
- **性能优化**: 自动优化代码
- **跨语言支持**: 多编程语言

### 1.5 Claude Swarm

| 项目 | 说明 |
|-----|------|
| **GitHub** | [parruda/claude-swarm](https://github.com/parruda/claude-swarm) |
| **特点** | 多代理协同工作 |

### 核心功能

- **多代理并行**: 同时运行多个代理
- **任务分解**: 自动拆分复杂任务
- **结果聚合**: 合并多代理结果

### 1.6 Claude Squad

| 项目 | 说明 |
|-----|------|
| **GitHub** | [smtg-ai/claude-squad](https://github.com/smtg-ai/claude-squad) |
| **特点** | 多工作区管理 |

### 核心功能

- **工作区管理**: 同时管理多个项目
- **代理池**: 智能任务分配
- **状态同步**: 跨工作区状态共享

---

## 2. DevOps 工具

### 2.1 cc-devops-skills (推荐)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [akin-ozer/cc-devops-skills](https://github.com/akin-ozer/cc-devops-skills) |
| **目标用户** | DevOps 工程师 |
| **特点** | 超详细 IaC 代码生成 |

### 核心功能

- **多平台支持**: AWS/Azure/GCP 等
- **验证工具**: 内置代码验证
- **生成器**: 自动化代码生成
- **Shell 脚本**: 运维脚本集成

### 支持平台

| 云平台 | 状态 |
|-------|------|
| AWS | ✅ 完整支持 |
| Azure | ✅ 完整支持 |
| GCP | ✅ 完整支持 |
| Kubernetes | ✅ 完整支持 |
| Docker | ✅ 完整支持 |
| Terraform | ✅ 完整支持 |

### 2.2 Claude Code Templates

| 项目 | 说明 |
|-----|------|
| **GitHub** | [davila7/claude-code-templates](https://github.com/davila7/claude-code-templates) |
| **特点** | 超全面的资源集合 |

### 核心功能

- **使用仪表盘**: 追踪 Claude Code 使用情况
- **分析功能**: 使用数据分析
- **命令集**: 丰富的 Slash 命令
- **Hooks**: 多种自动化钩子
- **子代理**: 专业化的子代理配置

---

## 3. 云服务集成

### 3.1 Claude Codex Settings

| 项目 | 说明 |
|-----|------|
| **GitHub** | [fcakyon/claude-codex-settings](https://github.com/fcakyon/claude-codex-settings) |
| **版本** | v2.1.0 |
| **特点** | 组织良好的插件集 |

### 核心功能

- **云平台集成**: GitHub, Azure, MongoDB
- **服务集成**: Tavily, Playwright
- **清晰结构**: 不过度复杂
- **多提供商兼容**: 支持多个 AI 提供商

### 3.2 AWS MCP Server

| 项目 | 说明 |
|-----|------|
| **GitHub** | [alexei-led/aws-mcp-server](https://github.com/alexei-led/aws-mcp-server) |
| **版本** | v1.7.0 |
| **特点** | AWS CLI 集成 |

### 支持服务

- EC2, Lambda, ECS, EKS
- S3, RDS, DynamoDB
- VPC, CloudFront
- IAM, Secrets Manager

---

## 4. 全栈开发

### 4.1 Fullstack Dev Skills

| 项目 | 说明 |
|-----|------|
| **GitHub** | [jeffallan/claude-skills](https://github.com/jeffallan/claude-skills) |
| **技能数量** | 65+ 专业化技能 |
| **版本** | v0.4.9 |

### 核心功能

- **9 个项目工作流命令**: 覆盖完整开发流程
- **Jira/Confluence 集成**: 项目管理无缝衔接
- **上下文工程**: `/common-ground` 命令揭示 Claude 假设
- **框架覆盖**: 多种前端/后端框架

### 技能分类

| 类别 | 技能数量 |
|-----|---------|
| 前端框架 | 15+ |
| 后端服务 | 12+ |
| 数据库 | 8+ |
| DevOps | 10+ |
| 测试 | 8+ |
| 其他 | 12+ |

---

## 5. 专业开发环境

### 5.1 Claude Code Pro

| 项目 | 说明 |
|-----|------|
| **GitHub** | [maxritter/claude-codepro](https://github.com/maxritter/claude-codepro) |
| **版本** | v7.1.3 |
| **特点** | 专业级开发环境 |

### 核心功能

- **规范驱动**: Spec-driven workflow
- **TDD 强制**: 测试驱动开发
- **跨会话记忆**: 持久化上下文
- **语义搜索**: 代码语义检索
- **质量钩子**: 代码质量检查
- **模块化规则**: 可组合规则

### 5.2 Claude Scientific Skills

| 项目 | 说明 |
|-----|------|
| **GitHub** | [K-Dense-AI/claude-scientific-skills](https://github.com/K-Dense-AI/claude-scientific-skills) |
| **版本** | v2.25.0 |
| **特点** | 科研/工程/分析技能集 |

### 适用领域

- 研究
- 科学计算
- 工程分析
- 金融
- 写作

---

## 6. 项目管理与协作

### 6.1 Claude Code PM

| 项目 | 说明 |
|-----|------|
| **GitHub** | [automazeio/ccpm](https://github.com/automazeio/ccpm) |
| **功能** | 项目管理 |

### 核心功能

- 任务管理
- 进度跟踪
- 团队协作
- 报告生成

### 6.2 Simone

| 项目 | 说明 |
|-----|------|
| **GitHub** | [Helmi/claude-simone](https://github.com/Helmi/claude-simone) |
| **版本** | simone-mcp/v0.4.0 |

### 核心功能

- 项目规划
- 任务分配
- 进度追踪
- 文档管理

---

## 7. 安全与审计

### 7.1 Trail of Bits Security Skills

| 项目 | 说明 |
|-----|------|
| **GitHub** | [trailofbits/skills](https://github.com/trailofbits/skills) |
| **许可证** | CC-BY-SA-4.0 |
| **特点** | 专业安全审计 |

### 核心功能

- **静态分析**: CodeQL 集成
- **代码扫描**: Sem- **变体grep 集成
分析**: 漏洞变体追踪
- **修复验证**: 修复确认
- **差异审查**: 代码变更审查

### 技能列表

| 技能 | 功能 |
|-----|------|
| code-audit | 代码审计 |
| vulnerability-detection | 漏洞检测 |
| fix-verification | 修复验证 |
| semgrep-scan | Semgrep 扫描 |
| codeql-analysis | CodeQL 分析 |

---

## 8. MCP 服务器

### 8.1 Codex Skill

| 项目 | 说明 |
|-----|------|
| **GitHub** | [klaudworks/skill-codex](https://github.com/skills-directory/skill-codex) |
| **功能** | Codex CLI 集成 |

### 核心功能

- 从 Claude Code 调用 Codex
- 自动参数推断
- 会话连续性

### 8.2 STT MCP Server

| 项目 | 说明 |
|-----|------|
| **GitHub** | [marcindulak/stt-mcp-server-linux](https://github.com/marcindulak/stt-mcp-server-linux) |
| **功能** | 语音转文字 |

### 8.3 Claude Code MCP Enhanced

| 项目 | 说明 |
|-----|------|
| **GitHub** | [grahama1970/claude-code-mcp-enhanced](https://github.com/grahama1970/claude-code-mcp-enhanced) |
| **功能** | MCP 增强 |

---

## 9. 上下文工程

### 9.1 Context Engineering Kit

| 项目 | 说明 |
|-----|------|
| **GitHub** | [NeoLabHQ/context-engineering-kit](https://github.com/NeoLabHQ/context-engineering-kit) |
| **版本** | v2.1.1 |
| **许可证** | GPL-3.0 |

### 核心功能

- 高级上下文工程技术
- 最少 token 消耗
- 提高 agent 结果质量

### 9.2 Everything Claude Code

| 项目 | 说明 |
|-----|------|
| **GitHub** | [affaan-m/everything-claude-code](https://github.com/affaan-m/everything-claude-code) |
| **版本** | v1.7.0 |

### 核心功能

- 核心工程域资源全覆盖
- 每个资源独立价值
- 可选工作流模式

---

## 10. 开发者工具技能汇总

### 按用途分类

| 用途 | 推荐技能 |
|-----|---------|
| **全栈开发** | Fullstack Dev Skills (65+ 技能) |
| **DevOps** | cc-devops-skills |
| **测试** | test-driven-development |
| **代码审查** | AgentSys, Claude Code Agents |
| **效率提升** | Claude Code Templates |
| **安全审计** | Trail of Bits Security Skills |
| **专业开发** | Claude CodePro |
| **云服务** | Claude Codex Settings |

### 按复杂度分类

| 级别 | 技能 |
|-----|------|
| **入门级** | Claude Code Templates |
| **进阶级** | Superpowers |
| **专业级** | cc-devops-skills |
| **企业级** | AgentSys |

---

## 11. 部署指南

### 快速安装

```bash
# 克隆资源库
git clone https://github.com/davila7/claude-code-templates.git
git clone https://github.com/jeffallan/claude-skills.git

# 安装到 Claude Code
cp -r claude-code-templates/* ~/.claude/
cp -r claude-skills/skills ~/.claude/
```

### 选择性安装

```bash
# 只安装特定技能
cp -r superpowers/skills/test-driven-development ~/.claude/skills/
cp -r superpowers/skills/brainstorming ~/.claude/skills/
```

### 使用技能安装命令

```bash
# 安装 Superpowers
claude --install-skill gh-obra-superpowers

# 安装 Claude Code Templates
claude --install-skill gh-davila7-claude-code-templates
```

---

## 12. 优缺点分析

### ✅ 优点

| 优点 | 说明 |
|-----|------|
| **功能全面** | 覆盖开发全流程 |
| **开箱即用** | 安装配置简单 |
| **社区活跃** | 持续更新维护 |
| **文档完善** | 学习资源丰富 |
| **可扩展** | 灵活定制 |
| **多云支持** | AWS/Azure/GCP |

### ❌ 缺点

| 缺点 | 说明 |
|-----|------|
| **配置复杂** | 部分技能需要配置 |
| **学习成本** | 需要时间熟悉 |
| **资源占用** | 技能数量多占用空间 |
| **版本兼容** | 需跟进更新 |

---

## 13. 发展趋势

### 13.1 当前趋势

| 方向 | 说明 |
|-----|------|
| **Agent 工作流** | 越来越多人使用 agent 系统 |
| **安全审计** | 安全技能需求增加 |
| **多云集成** | 云服务集成更完善 |
| **上下文工程** | 优化提示和上下文 |

### 13.2 值得关注

- Claude Scientific Skills - 科研领域
- Context Engineering Kit - 上下文优化
- Everything Claude Code - 全方位资源

---

## 📎 相关资源

- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
- [awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills)
- [Claude Code Handbook](https://nikiforovall.blog/claude-code-rules/)
- [Claude Code Ultimate Guide](https://github.com/FlorianBruniaux/claude-code-ultimate-guide)

---

*选择合适的开发者工具技能可以显著提升开发效率，建议根据项目需求选择性安装。*
