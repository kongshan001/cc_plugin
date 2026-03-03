# superpowers - Agentic Skills 框架

## 📋 文档信息

- **插件名称**: superpowers
- **GitHub**: [obra/superpowers](https://github.com/obra/superpowers)
- **Star**: 68k ⭐
- **状态**: ✅ 已调研
- **调研日期**: 2026-03-03

---

## 1. 插件背景需求

### 问题痛点

当前的 AI 编程助手存在以下问题：
- **急于写代码**: 不理解需求就上手，导致返工
- **缺乏设计**: 没有规划，直接开干
- **测试缺失**: 写完代码再补测试，效率低
- **单线程工作**: 无法并行处理多个任务

### 目标

构建一套完整的**软件工程工作流**，让 AI 编程助手：
1. 先理解需求，再动手
2. 有设计文档才行动
3. 严格 TDD
4. 能并行处理任务

---

## 2. 设计方案

### 核心工作流

```
┌─────────────────────────────────────────────────────────────┐
│                     Superpowers 工作流                       │
└─────────────────────────────────────────────────────────────┘

     ┌──────────┐
     │ 启动会话  │
     └────┬─────┘
          ▼
     ┌──────────┐     ┌──────────┐
     │ brainstorming │───▶ 需求澄清 & 设计 │
     │ (需求分析)  │     └────┬─────┘
     └──────────┘          ▼
                    ┌──────────────┐
                    │ writing-plans │───▶ 任务拆分
                    │ (任务规划)    │     └────┬─────┘
                    └──────────────┘          ▼
                                     ┌──────────────┐
                                     │ subagent-driven│───▶ 并行执行
                                     │ -development  │
                                     └───────┬──────┘
                                             ▼
                                     ┌──────────────┐
                                     │ finishing-a  │───▶ 合并/清理
                                     │ -development │
                                     └──────────────┘
```

### 内置 Skills

| Skill | 功能 | 触发时机 |
|-------|------|---------|
| **brainstorming** | 需求澄清、Socratic 推演 | 写代码前 |
| **writing-plans** | 任务拆分 (2-5分钟粒度) | 设计完成后 |
| **subagent-driven-development** | 并行子任务执行 + 两阶段审查 | 执行计划时 |
| **test-driven-development** | RED-GREEN-REFACTOR | 编写代码时 |
| **requesting-code-review** | 代码审查 | 任务间隔 |
| **using-git-worktrees** | 隔离工作分支 | 设计批准后 |
| **finishing-a-development-branch** | 收尾、合并选项 | 任务完成 |

---

## 3. 本地部署

### Claude Code

```bash
# 1. 注册插件市场
/plugin marketplace add obra/superpowers-marketplace

# 2. 安装插件
/plugin install superpowers@superpowers-marketplace

# 3. 重启 Claude Code

# 4. 更新插件
/plugin update superpowers
```

### Cursor

```bash
# 从市场安装
/plugin-add superpowers
```

### Codex / OpenCode

```bash
# 告诉 Codex
Fetch and follow instructions from https://raw.githubusercontent.com/obra/superpowers/refs/heads/main/.codex/INSTALL.md

# 告诉 OpenCode
Fetch and follow instructions from https://raw.githubusercontent.com/obra/superpowers/refs/heads/main/.opencode/INSTALL.md
```

### Windows

> 同样的命令，在 PowerShell 或 CMD 中运行

---

## 4. 效果展示

### 触发示例

启动新会话后，说：
- "帮我规划这个功能"
- "让我们调试这个问题"

Agent 会**自动**触发对应技能，无需手动选择。

### 预期行为

1. **brainstorming**: 不直接写代码，而是问你"真正想做什么"
2. **writing-plans**: 生成 2-5 分钟粒度的任务清单
3. **subagent-driven**: 自动调度子任务，并行执行
4. **TDD**: 先写失败的测试，再写代码让它通过

---

## 5. 优缺点分析

### ✅ 优点

| 优点 | 说明 |
|-----|------|
| **完整工作流** | 覆盖需求→设计→开发→测试→审查→合并 |
| **强制执行** | Skills 自动触发，不是建议 |
| **子任务并行** | 可自主工作数小时不偏离计划 |
| **两阶段审查** | 先检查规范符合，再检查代码质量 |
| **MIT 许可** | 开源免费 |

### ❌ 缺点

| 缺点 | 说明 |
|-----|------|
| **学习曲线** | 需要理解 Skills 触发机制 |
| **初期慢** | 设计阶段耗时，但减少返工 |
| **不适合小任务** | 简单任务反而是负担 |
| **依赖特定平台** | 需要 Claude Code/Cursor/Codex |

---

## 6. 平替插件对比

| 插件 | 特点 | 适用场景 |
|-----|------|---------|
| **superpowers** | 完整工程工作流 + 并行开发 | 大型项目 |
| **claude-mem** | 长期记忆 | 跨会话上下文 |
| **OpenClaw** | 完整 AI 助手框架 | 需要更多能力 |

---

## 7. 落地过程

### 调研日期
2026-03-03

### 调研结果

1. **安装可行性**: ✅ Claude Code / Cursor / Codex / OpenCode 均支持
2. **文档完整性**: ✅ 官方文档详细
3. **社区活跃度**: ⭐ 68k stars，活跃维护

### 待验证

- [x] 实际安装效果 ✅
- [x] 与 Claude Code 原生能力兼容性 ✅
- [ ] 子任务并行执行效果
- [ ] Windows 兼容性

---

## 7. 落地过程

### 调研日期
2026-03-03

### 验证步骤

1. **检查插件状态**
   ```bash
   claude plugin list
   ```
   结果: superpowers@superpowers-marketplace 已安装并启用

2. **实际测试**
   ```bash
   echo "帮我设计一个用户登录功能" | claude -p
   ```

3. **验证结果**
   ✅ **成功触发 brainstorming skill**
   - AI 没有直接写代码
   - 而是询问需求细节（登录用途、后端情况、数据存储等）
   - 这正是 superpowers 的核心价值：先理解需求，再动手

### 验证结论

| 验证项 | 结果 |
|-------|------|
| 安装成功 | ✅ |
| 自动触发 Skills | ✅ |
| 不影响原生能力 | ✅ |
| 中文支持 | ✅ |

---

## 8. 常见问题

### Q: 会影响 Claude Code 原生能力吗？
A: 不会，Skills 在特定时机自动触发。

### Q: 可以禁用某些 Skill 吗？
A: 可以通过配置文件自定义。

### Q: 支持中文项目吗？
A: 支持，Skills 基于对话触发，与语言无关。

---

## 📎 相关链接

- [GitHub](https://github.com/obra/superpowers)
- [Marketplace](https://github.com/obra/superpowers-marketplace)
- [官方博客](https://blog.fsck.com/2025/10/09/superpowers/)
