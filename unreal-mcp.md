# Unreal-MCP Unreal Engine 5 MCP 服务器

> ⭐ 1,504 Stars · C++ · 游戏引擎

## 1. 背景需求

游戏开发者需要通过自然语言控制 Unreal Engine，实现 AI 辅助开发。

## 2. 目标

让 AI 助手 (Claude, Cursor, Windsurf) 通过自然语言控制 Unreal Engine。

## 3. 核心功能

- 🎮 UE5 引擎控制
- 📐 蓝图代码生成
- 🏗️ 关卡编辑
- 📦 资产管理
- 🔧 自动化构建

## 4. 本地部署

```bash
# 安装
pip install unreal-mcp

# 配置 claude_desktop_config.json
{
  "mcpServers": {
    "unreal": {
      "command": "unreal-mcp",
      "args": ["--project", "YourProject.uproject"]
    }
  }
}
```

## 5. 效果展示

- GitHub Stars：⭐ 1,504
- Forks: 225

## 6. 优缺点

✅ 完整的 UE5 集成
✅ 蓝图生成
✅ 关卡自动化

⚠️ 需要 UE5 环境
⚠️ 配置复杂

## 7. 替代方案

| 插件 | 特点 |
|------|------|
| unity-mcp | Unity 游戏引擎 |
| godot-development | Godot 引擎 |
