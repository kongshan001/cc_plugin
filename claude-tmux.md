# claude-tmux Claude Code 会话管理工具

> Claude Code 在 tmux 中的会话管理 | 新增

## 1. 背景需求

Claude Code 用户在进行长时间开发时，需要管理多个会话实例，监控运行状态，并在不同项目间快速切换。tmux 是强大的终端复用工具，但缺乏对 Claude Code 会话的专门支持。

## 2. 目标

在 tmux 中实现 Claude Code 实例的可视化管理和快速切换，提供状态监控、生命周期管理和 Git/PR 支持。

## 3. 设计方案

**核心架构**
- tmux popup 界面
- 多实例状态监控
- 会话生命周期管理
- Git worktree 集成
- PR 支持

**功能模块**
- 会话列表展示
- 状态监控面板
- 快速切换机制
- 生命周期控制
- Git 集成

## 4. 本地部署

```bash
# 克隆仓库
git clone https://github.com/nielsgroen/claude-tmux.git

# 添加到 PATH 或复制到 tmux 配置目录
# 配置 tmux 快捷键激活
```

## 5. 效果展示

- **GitHub Stars**: ⭐ 新增
- **功能**: tmux popup 管理界面
- **支持**: 状态监控、实例切换

## 6. 优缺点

| 优点 | 缺点 |
|------|------|
| 多会话管理 | 需要 tmux 环境 |
| 状态监控 | 配置有一定门槛 |
| Git 集成 | |
| PR 支持 | |

## 7. 平替插件

| 插件 | 特点 |
|------|------|
| claude-esp | TUI 隐藏输出流 |
| popkit-claude | 模块化插件套件 |

## 8. 落地过程

1. 安装 tmux（如未安装）
2. 克隆 claude-tmux 仓库
3. 配置 tmux 快捷键
4. 启动 Claude Code 并在 tmux 中管理
