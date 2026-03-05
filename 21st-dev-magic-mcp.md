# 21st.dev Magic MCP - AI UI 组件生成

> AI 驱动的 UI 组件生成工具

## 1. 背景需求

前端开发需要快速生成高质量的 UI 组件，传统方式效率低下。

## 2. 目标

通过自然语言描述快速生成现代化的 UI 组件。

## 3. 核心功能

- 🎨 自然语言生成 UI
- 🖥️ 多 IDE 支持
  - Cursor
  - Windsurf
  - VSCode + Cline
  - Claude Code
- ⚡ 实时预览
- 📦 组件库集成
- 🔧 TypeScript 支持
- 🎭 SVGL 品牌资源集成

## 4. 本地部署

### 快速安装

```bash
# 安装 CLI
npx @21st-dev/cli@latest install <client> --api-key <key>

# 支持的客户端: cursor, windsurf, cline, claude
```

### 手动配置

```json
{
  "mcpServers": {
    "@21st-dev/magic": {
      "command": "npx",
      "args": ["-y", "@21st-dev/magic@latest"],
      "env": {
        "API_KEY": "${input:apiKey}"
      }
    }
  }
}
```

### 配置位置

- Cursor: `~/.cursor/mcp.json`
- Windsurf: `~/.codeium/windsurf/mcp_config.json`
- Cline: `~/.cline/mcp_config.json`
- Claude: `~/.claude/mcp_config.json`

## 5. 使用方法

1. 获取 API Key: https://21st.dev/magic/console
2. 安装并配置 MCP
3. 在 AI 助手中使用 `/ui` 命令
4. 描述你需要的组件

示例:
```
/ui create a modern navigation bar with responsive design
```

## 6. 效果展示

- 即时生成 UI 组件
- 灵感来自 21st.dev 设计库
- 完全可定制

## 7. 优缺点

✅ 快速生成 UI
✅ 多 IDE 支持
✅ 高质量组件

⚠️ 需要 API Key
⚠️ 付费功能

## 8. 替代方案

| 工具 | 特点 |
|------|------|
| v0 | AI UI 生成 |
| bolt.new | 全栈开发 |
| Lovable | AI 开发平台 |

## 9. 相关链接

- [21st.dev](https://21st.dev)
- [Magic 官网](https://21st.dev/magic)
- [GitHub](https://github.com/21st-dev)
