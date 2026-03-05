# Claude Code 插件实践指南

> 记录每个插件的落地实践过程

## 📚 插件列表

| 插件名称 | 描述 | 状态 |
|-----------|------|------|
| [claude-code-game-studios](./claude-code-game-studios.md) | 48 AI 代理游戏工作室，⭐ 26-30 | ✅ |
| [cc-plugin-unity-gamedev](./cc-plugin-unity-gamedev.md) | 21 个专业 Unity 技能 | ✅ |
| [pydantic-ai-skills](./pydantic-ai-skills.md) | Pydantic AI 开发技能，⭐ 136 | ✅ |
| [playwright-mcp](./playwright-mcp.md) | Playwright MCP 服务器，评分 3.581 | ✅ |
| [aws-mcp-server](./aws-mcp-server.md) | AWS 云服务 MCP，⭐ 1350+ | ✅ |
| [agentsys](./agentsys.md) | 工作流自动化系统 | ✅ |
| [superpowers](./superpowers.md) | 核心工程技能集，⭐ 4.1k+ | ✅ |
| [claude-mem](./claude-mem.md) | 智能记忆系统 | ✅ |
| [agentsys](./agentsys/README.md) | 模块化编排系统 | ✅ |
| [superpowers](./superpowers/README.md) | 核心工程技能集 | ✅ |
| [trailofbits-skills](./trailofbits-skills/README.md) | 安全审计技能 | ✅ |
| [fastapi-development](./fastapi-development.md) | FastAPI 开发技能 | ✅ |
| [git-mcp-server](./git-mcp-server.md) | Git MCP 服务器 (官方) | ✅ |
| [memory-mcp-server](./memory-mcp-server.md) | Memory MCP 服务器 (官方) | ✅ |
| [filesystem-mcp-server](./filesystem-mcp-server.md) | Filesystem MCP 服务器 (官方) | ✅ |
| [adb-skill](./adb-skill.md) | ADB 设备操作技能 | ✅ |
| [godot-development](./godot-development.md) | Godot 游戏开发技能 | ✅ |
| [sequential-thinking-mcp](./sequential-thinking-mcp.md) | 顺序思考 MCP (官方) | ✅ |
| [supplement-2026-03-04-v39](./supplement-2026-03-04-v39/) | 补充调研 v39 | ✅ |
| [supplement-2026-03-04-v40](./supplement-2026-03-04-v40/) | 补充调研 v40 - 游戏/Python/测试/开发工具 | ✅ |
| [supplement-2026-03-04-v42](./supplement-2026-03-04-v42/) | 补充调研 v42 - 游戏/Python/测试/开发工具 | ✅ |
| [supplement-2026-03-04-v43](./supplement-2026-03-04-v43/) | 补充调研 v43 - 深度调研游戏/Python/测试/开发工具 | ✅ |
| [supplement-2026-03-04-v44](./supplement-2026-03-04-v44/) | 补充调研 v44 - 游戏/Python/测试/开发工具热门插件 | ✅ |
| [supplement-2026-03-04-v45](./supplement-2026-03-04-v45/) | 补充调研 v45 - 新增热门插件科学研究/安全/开发者工具 | ✅ |
| [supplement-2026-03-04-v46](./supplement-2026-03-04-v46/) | 补充调研 v46 - 游戏/Python/测试/开发者工具热门插件 | ✅ |
| [supplement-2026-03-04-v47](./supplement-2026-03-04-v47/) | 补充调研 v47 - 游戏/Python/测试/开发者工具热门插件深度调研 | ✅ |
| [supplement-2026-03-04-v48](./supplement-2026-03-04-v48/) | 补充调研 v48 - 新增热门插件 Sudocode/Parry/Dippy/开发者工具 | ✅ |
| [supplement-2026-03-04-v49](./supplement-2026-03-04-v49/) | 补充调研 v49 - Unreal-MCP/FastAPI-MCP/MCPJam/Snyk 安全扫描 | 🆕 |
| [supplement-2026-03-04-v50](./supplement-2026-03-04-v50/) | 补充调研 v50 - 游戏/Python/测试/开发者工具完整调研 | ✅ |
| [supplement-2026-03-04-v51](./supplement-2026-03-04-v51/) | 补充调研 v51 - 游戏/Python/测试/开发者工具热门插件完整调研 | ✅ |
| [supplement-2026-03-04-v52](./supplement-2026-03-04-v52/) | 补充调研 v52 - 游戏/Python/测试/开发者工具热门插件完整调研 | ✅ |
| [supplement-2026-03-04-v53](./supplement-2026-03-04-v53/) | 补充调研 v53 - 游戏/Python/测试/开发者工具热门插件完整调研 | ✅ |
| [supplement-2026-03-04-v54](./supplement-2026-03-04-v54/) | 补充调研 v54 - 游戏/Python/测试/开发者工具深度调研 | ✅ |
| [supplement-2026-03-04-v55](./supplement-2026-03-04-v55/) | 补充调研 v55 - 游戏/Python/测试/开发者工具热门插件完整调研 | ✅ |
| [supplement-2026-03-04-v56](./supplement-2026-03-04-v56/) | 补充调研 v56 - 游戏/Python/测试/开发者工具热门插件补充调研 | ✅ |
| [supplement-2026-03-04-v57](./supplement-2026-03-04-v57/) | 补充调研 v57 - 游戏/Python/测试/开发者工具热门插件补充调研 | ✅ |
| [supplement-2026-03-04-v58](./supplement-2026-03-04-v58/) | 补充调研 v58 - 游戏/Python/测试/开发者工具深度调研 | ✅ |
| [supplement-2026-03-04-v59](./supplement-2026-03-04-v59/) | 补充调研 v59 - 游戏/Python/测试/开发者工具热门插件完整调研 | ✅ |
| [supplement-2026-03-04-v60](./supplement-2026-03-04-v60/) | 补充调研 v60 - 游戏/Python/测试/开发者工具热门插件深度调研 | ✅ |
| [supplement-2026-03-04-v61](./supplement-2026-03-04-v61/) | 补充调研 v61 - 游戏/Python/测试/开发者工具热门插件完整调研 | ✅ |
| [supplement-2026-03-04-v62](./supplement-2026-03-04-v62/) | 补充调研 v62 - 新增热门插件深度分析 (8616+仓库索引/DevOps/项目管理) | 🆕最新 |
| [supplement-2026-03-04-v63](./supplement-2026-03-04-v63/) | 补充调研 v63 - 游戏/Python/测试/开发者工具完整调研 | ✅ |
| [supplement-2026-03-04-v64](./supplement-2026-03-04-v64/) | 补充调研 v64 - 游戏/Python/测试/开发者工具热门插件完整调研 | ✅ |
| [context7-mcp-server](./context7-mcp-server.md) | Context7 MCP 服务器，50+ 框架支持 | ✅ |
| [claudeforge](./claudeforge.md) | CLAUDE.md 生成和维护工具 | ✅ |
| [skyll](./skyll.md) | AI 技能自主发现学习工具 | ✅ |
| [sudocode](./sudocode.md) | 轻量级代理编排工具，Git 原生规范管理 | 🆕 |
| [parry](./parry.md) | 提示注入扫描器，多层安全防护 | 🆕 |
| [dippy](./dippy.md) | Bash 命令过滤器，减少权限疲劳 | 🆕 |
| [supplement-2026-03-04-v65](./supplement-2026-03-04-v65/) | 补充调研 v65 - 游戏/Python/测试/开发者工具热门插件完整调研 | ✅ |
| [supplement-2026-03-04-v67](./supplement-2026-03-04-v67/) | 补充调研 v67 - 游戏/Python/测试/开发者工具热门插件最新调研 (Sudocode/Parry/Dippy) | 🆕最新 |
| [supplement-2026-03-04-v66](./supplement-2026-03-04-v66/) | 补充调研 v66 - 游戏/Python/测试/开发者工具深度调研续篇 | ✅ |
| [supplement-2026-03-05-v68](./supplement-2026-03-05-v68/) | 补充调研 v68 - 游戏客户端/Python/自动化测试/开发者工具完整调研 | 🆕最新 |
| [supplement-2026-03-05-v69](./supplement-2026-03-05-v69/) | 补充调研 v69 - 游戏客户端/Python/自动化测试/开发者工具最新调研 | 🆕最新 |
| [supplement-2026-03-05-v70](./supplement-2026-03-05-v70/) | 补充调研 v70 - 游戏客户端/Python/自动化测试/开发者工具完整调研 | 🆕最新 |
| [supplement-2026-03-05-v71](./supplement-2026-03-05-v71/) | 补充调研 v71 - 游戏客户端/Python/自动化测试/开发者工具热门插件深度调研 | 🆕最新 |
| [supplement-2026-03-05-v72](./supplement-2026-03-05-v72/) | 补充调研 v72 - 游戏客户端/Python/自动化测试/开发者工具最新调研 | 🆕最新 |
| [supplement-2026-03-05-v73](./supplement-2026-03-05-v73/) | 补充调研 v73 - 游戏客户端/Python/自动化测试/开发者工具热门插件完整调研 | 🆕最新 |
| [supplement-2026-03-05-v74](./supplement-2026-03-05-v74/) | 补充调研 v74 - 游戏客户端/Python/自动化测试/开发者工具最新热门插件完整调研 | 🆕最新 |
| [supplement-2026-03-05-v75](./supplement-2026-03-05-v75/) | 补充调研 v75 - 游戏客户端/Python/自动化测试/开发者工具热门插件深度调研 | 🆕最新 |
| [supplement-2026-03-05-v76](./supplement-2026-03-05-v76/) | 补充调研 v76 - 游戏客户端/Python/自动化测试/开发者工具热门插件完整调研 | 🆕最新 |
| [supplement-2026-03-05-v77](./supplement-2026-03-05-v77/) | 补充调研 v77 - 游戏客户端/Python/自动化测试/开发者工具最新热门插件完整调研 | 🆕最新 |
| [supplement-2026-03-05-v78](./supplement-2026-03-05-v78/) | 补充调研 v78 - 游戏客户端/Python/自动化测试/开发者工具热门插件完整调研 | 🆕最新 |
| [supplement-2026-03-05-v79](./supplement-2026-03-05-v79/) | 补充调研 v79 - 游戏客户端/Python/自动化测试/开发者工具最新热门插件完整调研 | 🆕最新 |
| [git-context-controller](./git-context-controller.md) | Git 风格上下文管理框架 | 🆕 |
| [supplement-2026-03-05-v81](./supplement-2026-03-05-v81/) | 补充调研 v81 - 游戏客户端/Python/自动化测试/开发者工具最新热门插件完整调研 | 🆕最新 |
| [supplement-2026-03-05-v80](./supplement-2026-03-05-v80/) | 补充调研 v80 - 官方插件深度分析 (PR Review/Security/Frontend/Feature Dev) | 🆕最新 |
| [pr-review-toolkit](./pr-review-toolkit.md) | 官方 PR 审查工具包，6 专业代理 | 🆕 |
| [security-guidance](./security-guidance.md) | 官方安全提醒钩子，9 种安全模式 | 🆕 |
| [frontend-design-plugin](./frontend-design-plugin.md) | 官方前端设计插件 | 🆕 |
| [feature-dev-plugin](./feature-dev-plugin.md) | 官方功能开发工作流，7 阶段 | 🆕 |
| [claude-scientific-skills](./claude-scientific-skills.md) | 科学研究技能集，研究/分析/金融/写作 | 🆕 |
| [unity-mcp](./unity-mcp.md) | Unity MCP 服务器，游戏引擎自动化 | 🆕 |
| [cc-devops-skills](./cc-devops-skills.md) | DevOps 工程师技能集，IaC 自动化 | 🆕 |
| [supplement-2026-03-05-v82](./supplement-2026-03-05-v82/) | 补充调研 v82 - 游戏客户端/Python/自动化测试/开发者工具最新热门插件完整调研 | 🆕最新 |
| [antigravity-awesome-skills](./antigravity-awesome-skills.md) | 超大规模代理技能集合，978+ 技能跨 10+ AI 助手 | 🆕最新 |
| [claude-code-pm](./claude-code-pm.md) | 全面项目管理框架 | 🆕最新 |
| [claude-hub](./claude-hub.md) | GitHub Webhook 集成 | 🆕最新 |
| [pypict-claude-skill](./pypict-claude-skill.md) | PICT 成对测试用例生成 | 🆕最新 |
| [supplement-2026-03-05-v83](./supplement-2026-03-05-v83/) | 补充调研 v83 - 游戏客户端/Python/自动化测试/开发者工具热门插件补充调研 | 🆕最新 |
| [mcp-unity](./mcp-unity.md) | 主流 Unity MCP 集成方案，⭐ 1,382 | 🆕 |
| [developer-kit](./developer-kit.md) | 全栈开发工具包，133 Stars | 🆕 |
| [mcp-ssh-manager](./mcp-ssh-manager.md) | SSH 远程管理工具，37 工具 | 🆕 |
| [auto-review-claude-mcp](./auto-review-claude-mcp.md) | Unity PR 自动化审查 | 🆕 |
| [agents-claude-code](./agents-claude-code.md) | 100 超专业 AI 代理 | 🆕 |
| [supplement-2026-03-05-v84](./supplement-2026-03-05-v84/) | 补充调研 v84 - 游戏客户端/Python/自动化测试/开发者工具完整调研 | 🆕最新 |
| [supplement-2026-03-05-v85](./supplement-2026-03-05-v85/) | 补充调研 v85 - 游戏客户端/Python/自动化测试/开发者工具热门插件完整调研 | 🆕最新 |
| [supplement-2026-03-05-v86](./supplement-2026-03-05-v86/) | 补充调研 v86 - 游戏客户端/Python/自动化测试/开发者工具热门插件深度调研 | 🆕最新 |
| [supplement-2026-03-05-v87](./supplement-2026-03-05-v87/) | 补充调研 v87 - Claude Code 热门插件最新调研 | 🆕最新 |
| [supplement-2026-03-05-v88](./supplement-2026-03-05-v88/) | 补充调研 v88 - 游戏客户端/Python/自动化测试/开发者工具最新热门插件完整调研 | 🆕最新 |
| [supplement-2026-03-05-v89](./supplement-2026-03-05-v89/) | 补充调研 v89 - Claude Code 热门插件最新调研 | 🆕最新 |
| [supplement-2026-03-05-v90](./supplement-2026-03-05-v90/) | 补充调研 v90 - 游戏客户端/Python/自动化测试/开发者工具完整调研 | 🆕最新 |
| [supplement-2026-03-05-v91](./supplement-2026-03-05-v91/) | 补充调研 v91 - 游戏客户端/Python/自动化测试/开发者工具热门插件最新调研 | 🆕最新 |
| [claude-tmux](./claude-tmux.md) | Claude Code tmux 会话管理工具 | 🆕 |
| [claude-esp](./claude-esp.md) | Claude Code 隐藏输出流调试工具 | 🆕 |
| [local-testing-agent](./local-testing-agent.md) | 多语言测试自动化 MCP | 🆕 |
| [unibrowse](./unibrowse.md) | 高级浏览器自动化插件 | 🆕 |

---

## 📝 新增插件文档

## 📝 文档规范

每个插件文档包含 8 部分：

## 📝 文档规范

每个插件文档包含 8 部分：

1. **背景需求** - 为什么需要这个插件
2. **目标** - 插件要解决什么问题
3. **设计方案** - 插件的技术架构
4. **本地部署** - 安装和使用指南
5. **效果展示** - 评分和实际效果
6. **优缺点分析** - 优势与不足
7. **平替对比** - 类似插件对比
8. **落地过程** - 实践验证的完整记录

---

## 📂 补充调研文档

- [补充调研-第五期](./supplement-2026-03-04-v3/README.md) (2026-03-04)
- [补充调研-第六期](./supplement-2026-03-04-v4/README.md) (2026-03-04)
- [补充调研-第七期](./supplement-2026-03-04-v5/README.md) (2026-03-04)
- [补充调研-第八期](./supplement-2026-03-04-v6/README.md) (2026-03-04)
- [补充调研-第九期](./supplement-2026-03-04-v7/README.md) (2026-03-04)
- [补充调研-第十期](./supplement-2026-03-04-v8/README.md) (2026-03-04)
- [补充调研-第十一期](./supplement-2026-03-04-v9/README.md) (2026-03-04)
- [补充调研-第十二期](./supplement-2026-03-04-v10/README.md) (2026-03-04)
- [补充调研-第十三期](./supplement-2026-03-04-v11/README.md) (2026-03-04)
- [补充调研-第十四期](./supplement-2026-03-04-v12/README.md) (2026-03-04)
- [补充调研-第十五期](./supplement-2026-03-04-v14/README.md) (2026-03-04 热门插件补充)
- [补充调研-第十六期](./supplement-2026-03-04-v15/README.md) (2026-03-04 GitHub热门趋势分析)
- [补充调研-第十七期](./supplement-2026-03-04-v17/README.md) (2026-03-04 完整调研更新)
- [补充调研-第十八期](./supplement-2026-03-04-v18/README.md) (2026-03-04 Unity-MCP + Game Studios 深度调研)
- [补充调研-第十九期](./supplement-2026-03-04-v19/README.md) (2026-03-04 Python开发/游戏客户端测试/MCP服务器调研)
- [补充调研-第二十期](./supplement-2026-03-04-v20/README.md) (2026-03-04 热门插件补充调研)
- [补充调研-第二十一期](./supplement-2026-03-04-v21/README.md) (2026-03-04 游戏/Python/测试/开发者工具调研)
- [补充调研-第二十二期](./supplement-2026-03-04-v22/README.md) (2026-03-04 游戏/Python/测试/开发者工具调研)
- [补充调研-第二十三期](./supplement-2026-03-04-v23/README.md) (2026-03-04 游戏/Python/测试/开发者工具调研)
- [补充调研-第二十四期](./supplement-2026-03-04-v24/README.md) (2026-03-04 游戏/Python/测试/开发者工具调研)
- [补充调研-第二十五期](./supplement-2026-03-04-v25/README.md) (2026-03-04 游戏/Python/测试/开发者工具调研)
- [补充调研-第二十六期](./supplement-2026-03-04-v26/README.md) (2026-03-04 游戏/Python/测试/开发者工具调研)
- [补充调研-第二十七期](./supplement-2026-03-04-v27/README.md) (2026-03-04 游戏/Python/测试/开发者工具调研)
- [补充调研-第二十八期](./supplement-2026-03-04-v28/README.md) (2026-03-04 游戏/Python/测试/开发者工具调研)
- [补充调研-第二十九期](./supplement-2026-03-04-v29/README.md) (2026-03-04 游戏/Python/测试/开发者工具调研)
- [补充调研-第三十期](./supplement-2026-03-04-v30/README.md) (2026-03-04 游戏/Python/测试/开发者工具调研)
- [补充调研-第三十一期](./supplement-2026-03-04-v31/README.md) (2026-03-04 游戏/Python/测试/开发者工具调研)
- [补充调研-第三十二期](./supplement-2026-03-04-v32/README.md) (2026-03-04 游戏/Python/测试/开发者工具补充调研)
- [补充调研-第三十三期](./supplement-2026-03-04-v33/README.md) (2026-03-04 Claude Code 热门插件调研)
- [补充调研-第三十四期](./supplement-2026-03-04-v34/README.md) (2026-03-04 Claude Code 热门插件调研)
- [补充调研-第三十五期](./supplement-2026-03-04-v35/README.md) (2026-03-04 游戏客户端/Python/自动化测试/开发者工具调研) ✨最新
- [补充调研-第三十六期](./supplement-2026-03-04-v36/README.md) (2026-03-04 热门插件补充调研) ✨最新
- [补充调研-第三十七期](./supplement-2026-03-04-v66/README.md) (2026-03-04 游戏/Python/测试/开发者工具深度调研续篇) 🆕最新

---

## 🔧 如何贡献

1. 在根目录创建插件 Markdown 文件
2. 按照上述规范编写内容
3. 在 README.md 表格中添加链接
4. 提交 PR
