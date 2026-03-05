# Claude-ESP Claude Code 隐藏输出流调试工具

> 实时流式查看 Claude Code 隐藏输出 | 多会话监控 | 内容过滤

## 1. 背景需求

Claude Code 开发者在调试和理解 AI 行为时面临挑战：
- 无法直接看到 AI 的"思考"过程
- 子代理执行细节不可见
- 工具调用信息难以追踪
- 需要在不影响主会话的情况下监控后台任务

## 2. 目标

提供 Claude Code 隐藏输出流的实时调试工具，实现：
- 实时流式输出查看
- 多会话同时监控
- 内容类型过滤
- 后台任务跟踪

## 3. 设计方案

### 3.1 技术架构

- **Go + TUI**: 高性能终端界面
- **流式处理**: 实时捕获 Claude Code 输出
- **多会话支持**: 同时监控多个会话

### 3.2 功能模块

```
┌──────────────────────────────────────────────────┐
│ Claude ESP - Session Monitor                     │
├──────────────────────────────────────────────────┤
│ [Thinking] ████████████░░░░░░░░ 65%             │
│ [Tool: Read] ████████░░░░░░░░░░░ 40%           │
│ [Subagent] ▶ Planning...                         │
│                                                  │
│ Filter: [All] [Thinking] [Tools] [Errors]       │
└──────────────────────────────────────────────────┘
```

- **输出类型**:
  - Thinking: AI 思考过程
  - Tool Calls: 工具调用详情
  - Subagents: 子代理活动
  - Errors: 错误信息
- **过滤功能**: 按类型筛选显示

## 4. 本地部署

```bash
# 方法 1: 直接安装 (推荐)
go install github.com/phiat/claude-esp@latest

# 方法 2: 从源码编译
git clone https://github.com/phiat/claude-esp.git
cd claude-esp
go build -o claude-esp .

# 配置 Claude Code 输出重定向
# 在 Claude Code 配置中添加:
{
  "esp": {
    "enabled": true,
    "port": 8080
  }
}

# 启动监控
claude-esp
```

## 5. 效果展示

- **GitHub Stars**: ⭐ 增长中
- **调试效率**: 大幅提升 AI 行为理解
- **适用场景**: 复杂任务调试、代理行为分析

## 6. 优缺点

| 优点 | 缺点 |
|------|------|
| 实时流式输出 | 需要额外终端窗口 |
| 多会话监控 | Go 运行时依赖 |
| 内容过滤 | 配置有一定门槛 |
| 后台任务跟踪 | |

## 7. 平替插件

| 插件 | 特点 |
|------|------|
| Claude-Tmux | 会话管理 |
| cclogviewer | JSONL 日志查看 |
| Claude-ESP | 实时流式 |

## 8. 落地过程

1. 安装 Go 运行时 (1.21+)
2. 安装 claude-esp
3. 配置 Claude Code 输出端点
4. 启动监控界面
5. 根据需要过滤和调试

---
参考: https://github.com/phiat/claude-esp
