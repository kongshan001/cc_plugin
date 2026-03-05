# antigravity-awesome-skills 超大规模代理技能集合

> 978+ 通用代理技能，跨多个 AI 编码助手

## 1. 背景需求

AI 编码助手（如 Claude Code、Cursor、Gemini）虽然智能，但缺乏特定领域的工具和知识。它们不了解公司的特定部署协议或特定技术的语法。技能（Skills）是小型 Markdown 文件，可以教会 AI 精确完成特定任务。

## 2. 目标

提供一个超大规模的通用代理技能库，兼容多个主流 AI 编码助手，让用户能够快速获得各种专业能力。

## 3. 设计方案

### 3.1 核心架构

- **技能格式**: 统一 SKILL.md 格式
- **安装方式**: npx 一键安装
- **跨平台兼容**: 支持 10+ AI 编码助手

### 3.2 技能分类

| 类别 | 焦点 | 示例技能 |
|------|------|----------|
| Architecture | 系统设计、ADRs、C4 | architecture, c4-context, senior-architect |
| Business | 增长、定价、CRO、SEO | copywriting, pricing-strategy, seo-audit |
| Data & AI | LLM 应用、RAG、agents | rag-engineer, prompt-engineer, langgraph |
| Development | 语言精通、框架模式 | typescript-expert, python-patterns, react-patterns |
| General | 规划、文档、产品运营 | brainstorming, doc-coauthoring, writing-plans |
| Infrastructure | DevOps、云、CI/CD | docker-expert, aws-serverless, vercel-deployment |
| Security | AppSec、pentesting、漏洞分析 | api-security-best-practices, sql-injection-testing |
| Testing | TDD、测试设计、修复 | test-driven-development, testing-patterns, test-fixing |
| Workflow | 自动化、编排、jobs | workflow-automation, inngest, trigger-dev |

### 3.3 兼容平台

- 🟣 Claude Code (Anthropic CLI)
- 🔵 Gemini CLI (Google DeepMind)
- 🟢 Codex CLI (OpenAI)
- 🟠 Kiro CLI/IDE (AWS)
- 🟠 Antigravity IDE (Google DeepMind)
- 🩵 GitHub Copilot (VSCode Extension)
- 🟠 Cursor (AI-native IDE)
- ⚪ OpenCode (Open-source CLI)
- 🌸 AdaL CLI (Self-evolving Coding Agent)

## 4. 本地部署

### 4.1 安装命令

```bash
# 默认安装 (Antigravity)
npx antigravity-awesome-skills

# Claude Code
npx antigravity-awesome-skills --claude

# Gemini CLI
npx antigravity-awesome-skills --gemini

# Codex CLI
npx antigravity-awesome-skills --codex

# Cursor
npx antigravity-awesome-skills --cursor

# 自定义路径
npx antigravity-awesome-skills --path ./my-skills
```

### 4.2 手动安装

```bash
# Claude Code
git clone https://github.com/sickn33/antigravity-awesome-skills.git .claude/skills

# Gemini CLI
git clone https://github.com/sickn33/antigravity-awesome-skills.git .gemini/skills

# Codex CLI
git clone https://github.com/sickn33/antigravity-awesome-skills.git .codex/skills
```

### 4.3 使用方式

```bash
# 在对话中使用
"Use @brainstorming to plan a SaaS MVP."
"Run @lint-and-validate on this file."

# 使用技能包 (Bundles)
# Web 开发: Web Wizard
# 安全: Security Engineer
# 通用: Essentials
```

## 5. 效果展示

- **⭐ GitHub Stars**: 978+ (持续增长)
- **技能数量**: 978+ 个
- **更新时间**: 2026-03-05 (持续更新)
- **兼容助手**: 10+ 个

## 6. 优缺点分析

### 6.1 优点

✅ **超大规模**: 978+ 技能，覆盖几乎所有开发场景  
✅ **跨平台兼容**: 支持 10+ AI 编码助手  
✅ **官方源支持**: 包含 Anthropic、OpenAI、Google、Microsoft 官方技能  
✅ **持续更新**: 活跃开发，新技能不断添加  
✅ **Bundle 打包**: 提供预打包的技能集，方便选择  
✅ **Web App**: 提供交互式 Web 界面浏览和使用技能  

### 6.2 缺点

⚠️ **学习曲线**: 技能太多，需要时间了解  
⚠️ **选择困难**: 需要从大量技能中挑选合适的  
⚠️ **Windows 兼容**: 需要启用开发者模式处理符号链接  

## 7. 平替对比

| 插件 | 特点 | 适用场景 |
|------|------|----------|
| Antigravity Awesome Skills | 978+ 技能，最大全包 | 需要全面覆盖 |
| Superpowers | 4.1k+ stars，核心工程技能 | 通用开发 |
| Everything Claude Code | 精选资源，高质量 | 学习参考 |
| Claude Code Templates | 精美 UI，仪表板 | 可视化展示 |

## 8. 落地过程

1. **安装**: 运行 npx 命令安装到指定路径
2. **选择 Bundle**: 根据角色选择合适的技能包
3. **开始使用**: 在 AI 对话中引用技能
4. **持续更新**: 定期运行更新获取新技能

---

*文档版本: v1.0*
*更新日期: 2026-03-05*
