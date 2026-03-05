# claude-esp Claude Code 隐藏输出流工具

> Claude Code 调试辅助工具 | Go

## 1. 背景需求

Claude Code 在执行复杂任务时会产生大量隐藏输出，包括 thinking 过程、工具调用、子代理状态等。开发者需要一种方式来监控这些输出，进行调试和理解 Claude 的行为。

## 2. 目标

提供 Claude Code 隐藏输出的流式传输和可视化，让开发者能够调试、理解 AI 的行为模式。

## 3. 设计方案

**核心架构**
- Go 语言 TUI 应用
- 独立的终端输出流
- 多会话同时监控
- 内容类型过滤

**功能模块**
- thinking 过程显示
- 工具调用追踪
- 子代理状态监控
- 后台任务跟踪
- 调试日志

## 4. 本地部署

```bash
# 通过 Go 安装
go install github.com/phiat/claude-esp@latest

# 或克隆仓库
git clone https://github.com/phiat/claude-esp.git
cd claude-esp
go build

# 运行
./claude-esp
```

## 5. 效果展示

- **GitHub Stars**: ⭐ 新增
- **语言**: Go
- **功能**: 隐藏输出流监控

## 6. 优缺点

| 优点 | 缺点 |
|------|------|
| 多会话同时监控 | 需要 Go 环境 |
| 内容类型过滤 | 学习曲线 |
| 后台任务跟踪 | |
| 调试辅助 | |

## 7. 平替插件

| 插件 | 特点 |
|------|------|
| claude-tmux | tmux 会话管理 |
| popkit-claude | 模块化插件套件 |

## 8. 落地过程

1. 安装 Go 1.21+
2. 克隆并构建 claude-esp
3. 启动 Claude Code
4. 在 claude-esp 中查看输出流
