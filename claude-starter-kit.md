# Claude-Starter-Kit 全栈开发模板

> Claude Code 全栈开发启动模板 | 预配置 MCP 服务器、技能和代理

## 1. 背景需求

现代软件开发需要完善的工作流支持。开发者经常面临：
- 项目启动时配置繁琐
- 团队成员开发环境不一致
- 缺乏系统化的开发流程
- 任务管理和代码审查效率低

## 2. 目标

提供开箱即用的 Claude Code 开发环境，通过预配置的 MCP 服务器、技能、代理和命令，实现：
- 快速项目启动
- 团队协作标准化
- 开发流程自动化
- 代码质量保障

## 3. 设计方案

### 3.1 MCP 服务器 (4个)

| 服务器 | 用途 | 特点 |
|--------|------|------|
| Context7 | 最新库文档 | 实时更新的代码文档 |
| Serena | 语义代码分析 | LSP 符号导航、引用跟踪 |
| Task Master | 任务管理 | PRD 解析、复杂度分析 |
| Pal | 多模型集成 | 聊天、调试、代码审查 |

### 3.2 开发技能 (6个)

- **analysis-process**: 实施前 - 将想法转化为 PRD、设计文档和实施计划
- **implementation-process**: 实施 - 分批步骤实施，架构审查检查点
- **testing-process**: 测试后 - 测试覆盖指南、表驱动测试、集成测试
- **documentation-process**: 文档后 - 更新 ARCHITECTURE.md、TESTING.md
- **development-guidelines**: 实施中 - 最佳实践强制执行
- **solid-code-review**: 代码审查 - SOLID 原则、安全检查

### 3.3 任务编排代理 (3个)

- **task-orchestrator**: 分析任务依赖，识别并行化机会，部署执行器
- **task-executor**: 实现特定任务，将任务规范转化为工作代码
- **task-checker**: QA 验证，检查实施是否符合要求

### 3.4 Slash 命令 (50+)

- Task Master: 47 个命令覆盖完整任务生命周期
- CoVe: 2 个命令用于验证提示
- Bash 验证: 路径保护钩子
- 状态行: 最小化显示

## 4. 本地部署

```bash
# 1. 从模板创建新项目
# 访问: https://github.com/new?template_name=claude-starter-kit&template_owner=serpro69

# 2. 克隆项目
git clone https://github.com/yourusername/your-project.git
cd your-project

# 3. 配置 MCP 服务器 (~/.claude.json)
{
  "context7": {
    "type": "http",
    "url": "https://mcp.context7.com/mcp",
    "headers": { "CONTEXT7_API_KEY": "YOUR_API_KEY" }
  },
  "serena": {
    "type": "stdio",
    "command": "uvx",
    "args": ["--from", "git+https://github.com/oraios/serena", "serena", "start-mcp-server"]
  },
  "task-master-ai": {
    "type": "stdio",
    "command": "npx",
    "args": ["-y", "--package=task-master-ai", "task-master-ai"]
  }
}

# 4. 运行初始化
chmod +x bootstrap.sh && ./bootstrap.sh
```

## 5. 效果展示

- **功能完整度**: ⭐⭐⭐⭐⭐
- **易用性**: ⭐⭐⭐⭐⭐
- **团队协作**: ⭐⭐⭐⭐⭐

## 6. 优缺点

| 优点 | 缺点 |
|------|------|
| 开箱即用 | 需要 API 密钥配置 |
| 完整的开发工作流 | 学习曲线较陡 |
| 团队协作友好 | 某些功能需要特定工具 |
| 持续更新 | |

## 7. 平替插件

| 插件 | 特点 |
|------|------|
| Claude-CodePro | 专业开发环境，TDD 强制 |
| ContextKit | 4 阶段规划方法论 |
| SuperClaude | 认知人格配置 |

## 8. 落地过程

1. 从模板创建项目
2. 配置 MCP 服务器和 API 密钥
3. 运行 bootstrap.sh 初始化
4. 根据需要自定义配置
5. 使用 Task Master 管理任务

---
参考: https://github.com/serpro69/claude-starter-kit
