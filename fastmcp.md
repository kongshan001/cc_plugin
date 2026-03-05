# FastMCP - Pythonic MCP 服务器框架

> ⭐ 23,383 Stars · Python · MCP

## 1. 背景需求

MCP (Model Context Protocol) 需要简洁的 Python 框架来快速构建服务器和客户端。

## 2. 目标

提供快速、Pythonic 的方式构建 MCP 服务器和客户端。

## 3. 核心功能

- 🚀 快速构建 MCP 服务器
- 🐍 纯 Python 实现
- ⚡ 异步支持
- 🔗 Prefect 工作流集成

## 4. 本地部署

```bash
pip install fastmcp

# 快速开始
from fastmcp import FastMCP

mcp = FastMCP("my-server")

@mcp.tool()
def hello(name: str) -> str:
    return f"Hello, {name}!"

# 运行
mcp.run()
```

## 5. 效果展示

- GitHub Stars：⭐ 23,383
- Forks: 1,795
- 趋势: 持续增长

## 6. 优缺点

✅ 性能优秀
✅ 文档完善
✅ 社区活跃

⚠️ 需要 Python 3.9+
⚠️ 学习曲线

## 7. 落地过程

1. 安装: `pip install fastmcp`
2. 创建服务器
3. 定义工具
4. 运行服务
5. 集成到 Claude Code
