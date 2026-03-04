# Claude Code 热门插件补充调研 (v78)

> 2026年3月 游戏客户端/Python/自动化测试/开发者工具 - ComposioHQ/awesome-claude-skills 最新插件完整调研

---

## 一、最新插件生态概览

### 1.1 本期重点关注

| 领域 | 插件数量 | 数据来源 |
|------|---------|---------|
| 游戏客户端开发 | 5+ | Claude-Code-Game-Studios |
| Python 开发 | 15+ | pydantic-ai, fastapi-mcp |
| 自动化测试 | 20+ | Playwright, ComposioHQ |
| 开发者工具 | 50+ | awesome-claude-skills |

---

## 二、ComposioHQ 官方技能库深度分析

### 2.1 文档处理技能

| 技能名称 | 功能 | 适用场景 |
|---------|------|---------|
| docx | Word 文档创建、编辑、格式化 | 报告、合同 |
| pdf | PDF 文本提取、表格、元数据 | 数据提取 |
| pptx | PPT 生成、模板、布局 | 演示文稿 |
| xlsx | 电子表格操作、公式、图表 | 数据分析 |
| claude-epub-skill | Markdown 转 EPUB 电子书 | 出版、文档转换 |

### 2.2 开发与代码工具技能

**核心技能列表**:

- **aws-skills** - AWS CDK 开发、成本优化 MCP
- **Changelog Generator** - 自动生成用户友好的变更日志
- **Claude Code Terminal Title** - 终端窗口动态标题
- **D3.js Visualization** - D3 图表和数据可视化
- **FFUF Web Fuzzing** - Web 安全模糊测试
- **iOS Simulator** - iOS 模拟器交互测试
- **jules** - 委托任务给 Google Jules AI
- **LangSmith Fetch** - LangChain/LangGraph 调试
- **MCP Builder** - MCP 服务器创建指南
- **Playwright Browser Automation** - 浏览器自动化测试
- **pypict-claude-skill** - PICT  pairwise 测试
- **Skill Creator** - 创建有效 Claude 技能

### 2.3 测试相关技能

#### Playwright Browser Automation

**功能**:
- 模型驱动的浏览器自动化
- Web 应用测试和验证
- 截图对比
- 前端调试

**Stars**: 高 | **官方推荐**

```bash
# 安装
git clone https://github.com/lackeyjb/playwright-skill.git ~/.claude/plugins/playwright

# 使用
"测试登录页面"
"验证购物车功能"
"截图对比 UI 变化"
```

#### pypict-claude-skill

**功能**:
- PICT (Pairwise Independent Combinatorial Testing)
- 优化测试用例生成
- pairwise 覆盖率

```yaml
# 使用示例
参数:
  - 浏览器: [Chrome, Firefox, Safari]
  - 操作系统: [Windows, macOS, Linux]
  - 屏幕: [1920x1080, 1366x768]
```

### 2.4 项目管理技能

| 技能 | 支持平台 | 功能 |
|------|---------|------|
| Asana Automation | Asana | 任务、项目、工作区 |
| Basecamp Automation | Basecamp | 待办、消息、团队 |
| ClickUp Automation | ClickUp | 任务、列表、目标 |
| Jira Automation | Jira | 问题、JQL、 sprints |
| Linear Automation | Linear | 问题、周期、团队 |
| Monday.com Automation | Monday | 看板、项、组 |
| Notion Automation | Notion | 页面、数据库、块 |
| Trello Automation | Trello | 看板、卡片、列表 |

### 2.5 DevOps 自动化技能

| 技能 | 功能 |
|------|------|
| GitHub Automation | Issue、PR、代码搜索 |
| GitLab Automation | Issue、MR、流水线 |
| CircleCI Automation | 流水线、工作流 |
| Vercel Automation | 部署、项目、域名 |
| Sentry Automation | 问题、事件、告警 |
| Datadog Automation | 监控、仪表盘、事件 |
| PagerDuty Automation | 事件、服务、值班 |

---

## 三、Python 开发技能深度分析

### 3.1 Pydantic AI 技能生态

```bash
# 安装
pip install pydantic-ai

# 配置 MCP
{
  "mcpServers": {
    "pydantic-ai": {
      "command": "uvx",
      "args": ["pydantic-ai-mcp"]
    }
  }
}
```

**核心功能**:
- 类型验证
- Agent 构建
- LLM 集成
- 输出验证

### 3.2 FastAPI 开发技能

**MCP 服务器配置**:

```bash
# 快速启动
uv venv && uv pip install -r requirements.txt

# 运行
uv run python -m pytest tests/
uv run uvicorn main:app --reload
```

### 3.3 PostgreSQL 技能

```bash
# 安装
git clone https://github.com/sanjay3290/ai-skills.git

# 使用
"查询所有活跃用户"
"分析销售数据趋势"
"导出报表"
```

**安全特性**:
- 只读查询
- 超时保护
- 行数限制
- 多连接支持

---

## 四、自动化测试新趋势

### 4.1 AI 驱动测试

| 技能 | 特点 | 适用场景 |
|------|------|---------|
| AI-Testing-MCP | 智能测试生成 | 单元测试 |
| Playwright Skill | 浏览器自动化 | E2E 测试 |
| LangSmith Fetch | 调试追踪 | LangChain |
| pypict-claude-skill | pairwise 测试 | 参数测试 |

### 4.2 ComposioHQ 测试技能

**Webapp Testing**:
```bash
# 测试本地 Web 应用
"测试用户注册流程"
"验证支付功能"
"检查响应式布局"
```

**工作流程**:
1. 启动本地服务器
2. 执行 Playwright 测试
3. 截图验证
4. 生成测试报告

### 4.3 安全测试技能

| 技能 | 功能 |
|------|------|
| FFUF Web Fuzzing | Web 模糊测试 |
| threat-hunting-with-sigma-rules | Sigma 规则威胁追踪 |
| computer-forensics | 数字取证分析 |

---

## 五、开发者工具技能全面覆盖

### 5.1 代码质量

| 技能 | 功能 |
|------|------|
| software-architecture | 架构模式、SOLID 原则 |
| test-driven-development | TDD 开发流程 |
| finishing-a-development-branch | 分支完成工作流 |
| root-cause-tracing | 根因分析 |

### 5.2 效率提升技能

| 技能 | 功能 |
|------|------|
| subagent-driven-development | 子代理开发模式 |
| skill-seekers | 文档转技能 |
| prompt-engineering | 提示工程 |
| Skill Creator | 技能创建指南 |

### 5.3 通信与协作

| 技能 | 平台 |
|------|------|
| Slack Automation | Slack |
| Discord Automation | Discord |
| Telegram Automation | Telegram |
| Microsoft Teams Automation | Teams |
| Gmail Automation | Gmail |
| WhatsApp Automation | WhatsApp |

---

## 六、游戏开发技能

### 6.1 现有游戏开发技能

| 技能 | 引擎 | 功能 |
|------|------|------|
| Claude-Code-Game-Studios | 通用 | 48 AI 代理工作室 |
| OH-Unity-GameDev-Skills | Unity | 专业开发技能 |
| pixel-plugin | 像素游戏 | Aseprite 集成 |
| Claude-Code-Game-Master | RPG | 桌游/RPG |

### 6.2 游戏测试技能

**Playwright 游戏测试**:
```bash
# Web 游戏测试
"测试游戏大厅加载"
"验证多人匹配"
"检查支付流程"
```

---

## 七、部署配置模板

### 7.1 Python 项目配置

```json
{
  "mcpServers": {
    "pydantic-ai": {
      "command": "uvx",
      "args": ["pydantic-ai-mcp"]
    },
    "fastapi": {
      "command": "uv",
      "args": ["run", "fastapi-mcp", "--app", "main:app"]
    }
  }
}
```

### 7.2 测试环境配置

```bash
# Python 测试环境
uv venv
source .venv/bin/activate
pip install pytest pytest-asyncio playwright
playwright install chromium
```

### 7.3 Composio 配置

```bash
# 安装 Composio
claude --plugin-dir ./connect-apps-plugin
/connect-apps:setup
# 输入 API key
```

---

## 八、插件选择指南

### 8.1 场景推荐

| 场景 | 推荐技能 | 优先级 |
|------|---------|--------|
| Web 测试 | Playwright Browser Automation | ⭐⭐⭐⭐⭐ |
| Python API | FastAPI + Pydantic AI | ⭐⭐⭐⭐⭐ |
| 项目管理 | Linear/Jira Automation | ⭐⭐⭐⭐ |
| DevOps | Vercel/GitHub Automation | ⭐⭐⭐⭐ |
| 游戏开发 | Claude-Code-Game-Studios | ⭐⭐⭐⭐ |
| 安全测试 | FFUF + Sigma Rules | ⭐⭐⭐ |

### 8.2 学习路径

```
入门阶段:
├── 安装 Claude Code
├── 配置 Playwright Skill
└── 试用 Slack/GitHub Automation

进阶阶段:
├── 集成 Pydantic AI
├── 配置 MCP 服务器
└── 使用 TDD 技能

专家阶段:
├── 自定义工作流
├── 开发专属技能
└── 团队协作优化
```

---

## 九、总结

### 9.1 本期要点

1. **ComposioHQ 技能库**: 50+ 官方维护技能，覆盖全场景
2. **Python 开发**: Pydantic AI + FastAPI 生态成熟
3. **自动化测试**: Playwright 主导，AI 驱动测试兴起
4. **开发者工具**: 从代码到 DevOps 全覆盖

### 9.2 发展趋势

- **技能商店化**: ComposioHQ 提供 78+ SaaS 集成
- **AI 增强测试**: 智能测试生成和修复
- **自动化普及**: 从开发到运维全流程自动化
- **安全集成**: 安全测试技能日益重要

---

## 参考资源

- [ComposioHQ/awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills)
- [playwright-skill](https://github.com/lackeyjb/playwright-skill)
- [pydantic-ai](https://github.com/anthropics/pydantic-ai)
- [Claude-Code-Game-Studios](https://github.com/Sstobo/Claude-Code-Game-Studios)
- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)

---

*文档版本: v78 - 2026-03-05*
