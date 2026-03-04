# Claude Code 自动化测试插件调研

> 2026年3月 Claude Code 热门自动化测试相关插件调研

## 1. Playwright Skill Playwright 自动化技能

> 浏览器自动化 Claude Code 技能，模型驱动

## 1.1 背景需求

需要通过 Claude Code 进行浏览器自动化和 E2E 测试。

## 1.2 目标

让 Claude 能够自主编写和执行自定义自动化。

## 1.3 设计方案

- 模型调用式自动化
- 浏览器控制
- E2E 测试
- 网页交互
- 截图/录屏

## 1.4 本地部署

```bash
# MCP 服务器方式
npx -y @modelcontextprotocol/server-playwright

# 技能方式
git clone https://github.com/lackeyjb/playwright-skill ~/.claude/plugins/
```

## 1.5 效果展示

- GitHub Stars：⭐ 1.9k
- 最流行的 Claude Code 自动化技能

## 1.6 优缺点

✅ 成熟稳定 ✅ 生态丰富 ✅ 模型驱动  
⚠️ 配置复杂 ⚠️ 需要 Playwright 基础

---

## 2. Claude Code Playwright MCP Test 测试框架

> 专为 Claude Code 设计的 YAML-based Playwright MCP 自动化测试框架

## 2.1 背景需求

需要声明式的测试框架。

## 2.2 目标

用 YAML 配置定义测试流程。

## 2.3 设计方案

- YAML 配置驱动
- MCP 协议集成
- 声明式测试定义
- CI/CD 友好

## 2.4 本地部署

```bash
git clone https://github.com/terryso/claude-code-playwright-mcp-test ~/.claude/plugins/
```

## 2.5 效果展示

- GitHub Stars：⭐ 164

## 2.6 优缺点

✅ YAML配置 ✅ 声明式 ✅ 易于维护  
⚠️ 学习新语法

---

## 3. Claude Code Frontend Dev 前端视觉测试

> 首个多模态 AI 驱动的 Claude Code 视觉测试插件

## 3.1 背景需求

前端开发需要视觉测试能力。

## 3.2 目标

让 AI 能"看见"UI 进行测试。

## 3.3 设计方案

- 多模态 AI
- 视觉识别
- 10倍开发速度
- 闭源方案

## 3.4 本地部署

```bash
git clone https://github.com/hemangjoshi37a/claude-code-frontend-dev ~/.claude/plugins/
```

## 3.5 效果展示

- GitHub Stars：⭐ 12

## 3.6 优缺点

✅ 视觉测试 ✅ 创新技术  
⚠️ 闭源 ⚠️ 新技术风险

---

## 4. AI Testing MCP AI测试MCP服务器

> AI 驱动的测试自动化 MCP 服务器

## 4.1 背景需求

需要智能化的测试生成和执行。

## 4.2 目标

用 AI 替代传统测试编写。

## 4.3 设计方案

- TestSprite 替代方案
- AI 测试生成
- 智能测试用例
- MCP 协议

## 4.4 本地部署

```bash
git clone https://github.com/Twisted66/ai-testing-mcp ~/.claude/plugins/
```

## 4.5 效果展示

- GitHub Stars：⭐ 6

---

## 5. Claude Code Templates 测试模板

> 包含测试工作流的完整资源集合

## 5.1 背景需求

需要开箱即用的测试模板。

## 5.2 目标

提供完整测试工作流。

## 5.3 设计方案

- 代码质量检查
- 测试命令
- 分析工具
- 使用仪表板
- 分析功能

## 5.4 本地部署

```bash
git clone https://github.com/davila7/claude-code-templates ~/.claude/plugins/
```

## 5.5 效果展示

- 功能丰富的 UI
- 使用分析

---

## 6. Claude Code Marketplace 测试市场

> Git 自动化、测试和代码审查的软件工程技能

## 6.1 背景需求

需要完整的测试工作流。

## 6.2 目标

覆盖完整 SDLC。

## 6.3 设计方案

- Git 自动化
- 测试生成
- 代码审查
- 多框架支持

## 6.4 本地部署

```bash
git clone https://github.com/mhattingpete/claude-skills-marketplace ~/.claude/plugins/
```

## 6.5 效果展示

- GitHub Stars：⭐ 428

---

## 7. Claude Code Rules2Hook 规则自动化

> 将自然语言项目规则转换为 Claude Code 自动化钩子

## 7.1 背景需求

需要用自然语言定义自动化规则。

## 7.2 目标

用英语写规则，Claude 自动执行。

## 7.3 设计方案

- 自然语言规则
- 自动转换
- Hook 集成
- 灵活配置

## 7.4 本地部署

```bash
pip install claudecode-rule2hook
# 或
git clone https://github.com/zxdxjtu/claudecode-rule2hook ~/.claude/plugins/
```

## 7.5 效果展示

- GitHub Stars：⭐ 407

---

## 8. Claude Code Agents 端到端开发

> 完整的 E2E 开发工作流

## 8.1 背景需求

需要完整的开发到测试流程。

## 8.2 目标

从需求到部署的完整自动化。

## 8.3 设计方案

- 多审计员并行
- 微检查点协议
- 浏览器 QA
- 严格协议防止失控

## 8.4 本地部署

```bash
git clone https://github.com/undeadlist/claude-code-agents ~/.claude/plugins/
```

---

## 9. Claude Code E2E Testing E2E 测试系统

> 完整的端到端测试解决方案

## 9.1 背景需求

需要覆盖全链路的测试。

## 9.2 目标

从 UI 到数据库的完整测试。

## 9.3 设计方案

- UI 测试
- API 测试
- 集成测试
- 报告生成

## 9.4 本地部署

```bash
# 已在 cc_plugin 中
# 参考 playwright-mcp.md
```

---

## 总结：自动化测试插件生态

| 插件 | 方向 | Stars | 特点 |
|------|------|-------|------|
| playwright-skill | 浏览器 | 1.9k | 最流行 |
| claude-code-playwright-mcp-test | 框架 | 164 | YAML驱动 |
| claude-code-frontend-dev | 视觉 | 12 | 多模态AI |
| ai-testing-mcp | AI测试 | 6 | 智能生成 |
| claude-skills-marketplace | 市场 | 428 | 完整工作流 |
| claudecode-rule2hook | 规则 | 407 | 自然语言 |

**推荐**：
- 通用浏览器自动化 → playwright-skill
- 声明式测试 → claude-code-playwright-mcp-test
- 视觉测试 → claude-code-frontend-dev
- 规则自动化 → claudecode-rule2hook
- 完整工作流 → claude-skills-marketplace
