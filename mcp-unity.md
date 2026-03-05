# mcp-unity 主流 Unity MCP 集成方案

> 1,382 Stars | 游戏引擎自动化 | C#

## 1. 背景需求

Unity 是最流行的游戏引擎之一，开发者需要将 AI 助手集成到 Unity 开发流程中，提高开发效率。

## 2. 目标

提供 Claude Code 与 Unity Editor 的无缝集成，通过 MCP 协议实现 AI 驱动的游戏开发自动化。

## 3. 设计方案

**核心架构**
- Model Context Protocol (MCP) 服务器
- Unity Editor 插件
- 跨 AI 助手支持（Cursor、Claude Code、Codex、Windsurf）

**功能模块**
- 场景操作模块
- 资源管理模块
- 脚本编辑模块
- 构建自动化模块
- 游戏对象控制模块

## 4. 本地部署

```bash
# 通过 npm 安装
npm install mcp-unity

# 或克隆仓库
git clone https://github.com/CoderGamester/mcp-unity.git

# 在 Claude Code 配置中添加
{
  "mcpServers": {
    "unity": {
      "command": "npx",
      "args": ["-y", "mcp-unity"]
    }
  }
}
```

## 5. 效果展示

- **GitHub Stars**: ⭐ 1,382
- **Fork**: 170
- **活跃度**: 高（2026-03-04 更新）

## 6. 优缺点

| 优点 | 缺点 |
|------|------|
| 活跃度高，1.3k+ stars | 需要 Unity Editor 运行 |
| 跨多 AI 助手支持 | 部分功能需要特定 Unity 包 |
| 完整 Unity 集成 | |
| 持续更新 | |

## 7. 平替插件

| 插件 | 特点 |
|------|------|
| UnityAgentClient | 通用 Agent 协议 |
| gamekit-cli | 轻量 CLI |
| claude-unity-bridge | 文件协议 |

## 8. 落地过程

1. 安装 npm 包或克隆仓库
2. 在 Unity 中安装对应包
3. 配置 MCP 服务器
4. 开始 AI 辅助开发
