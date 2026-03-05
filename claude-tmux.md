# Claude-Tmux Claude Code 会话管理工具

> 在 tmux 中管理 Claude Code 会话 | 多会话切换、状态监控、Git Worktree 支持

## 1. 背景需求

Claude Code 开发者经常面临：
- 同时处理多个项目/任务
- 需要在不同的 Claude Code 会话间切换
- 缺乏可视化的会话状态监控
- Git worktree 和 PR 管理不便

## 2. 目标

提供在 tmux 环境中管理 Claude Code 会话的解决方案，实现：
- 多会话统一管理
- 快速切换
- 状态监控
- Git worktree 和 PR 无缝集成

## 3. 设计方案

### 3.1 核心架构

- **tmux popup 界面**: 所有 Claude Code 实例的可视化弹出窗口
- **会话生命周期管理**: 创建、切换、监控、终止
- **Git 集成**: worktree 支持、PR 管理

### 3.2 功能模块

```
┌─────────────────────────────────────┐
│ Claude Code Sessions               │
├─────────────────────────────────────┤
│ 1. project-a [main] ● Running      │
│ 2. project-b [feature/x] ● Idle    │
│ 3. backend-api  ○ Stopped          │
│                                     │
│ [New] [Switch] [Kill] [Refresh]    │
└─────────────────────────────────────┘
```

- **状态指示**: ● 运行中 ○ 已停止
- **分支显示**: 当前 Git 分支
- **实时更新**: 会话状态自动刷新

## 4. 本地部署

```bash
# 方法 1: 克隆到插件目录
git clone https://github.com/nielsgroen/claude-tmux ~/.claude/plugins/claude-tmux

# 方法 2: 手动安装
# 1. 确保 tmux 已安装
which tmux

# 2. 添加快捷键绑定 (~/.tmux.conf)
# 运行插件提供的配置脚本

# 3. 启动 tmux 并加载插件
tmux source-file ~/.tmux.conf

# 4. 唤起 Claude Code 会话管理器
# 默认快捷键: Ctrl+b c
```

## 5. 效果展示

- **GitHub Stars**: ⭐ 持续增长中
- **用户评价**: "极大提升多项目开发效率"
- **兼容性**: macOS, Linux, WSL

## 6. 优缺点

| 优点 | 缺点 |
|------|------|
| 多会话统一管理 | 需要 tmux 基础 |
| 快速切换 | 配置有一定门槛 |
| Git 集成完善 | |
| 轻量级 | |

## 7. 平替插件

| 插件 | 特点 |
|------|------|
| Claude-ESP | 隐藏输出流调试 |
| Claude-Squad | 多代理终端管理 |
| Happy-Coder | 手机/桌面并行控制 |

## 8. 落地过程

1. 安装 tmux (如未安装)
2. 安装 tmux 插件管理器 (TPM)
3. 克隆 claude-tmux
4. 配置 tmux.conf 绑定
5. 启动并使用

---
参考: https://github.com/nielsgroen/claude-tmux
