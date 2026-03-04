# Context7 MCP Server

> 实时代码文档服务 - 50+ 框架支持

## 项目信息

- **GitHub**: [upstash/context7](https://github.com/upstash/context7)
- **GitHub Stars**: ⭐ 活跃
- **类型**: MCP 服务器 (官方维护)
- **状态**: ✅ 已调研

---

## 简介

Context7 MCP Server 是 Upstash 提供的实时代码文档服务，为 Claude Code 等 AI 编码助手提供最新的框架和库文档。

---

## 核心功能

| 功能 | 说明 |
|------|------|
| 实时文档 | 无需 API Key，即时获取最新文档 |
| 多框架支持 | 支持 50+ 主流框架和库 |
| 本地缓存 | 高效的文档缓存机制 |
| 语义搜索 | 智能文档检索 |

---

## 支持的框架

### Web 框架

| 框架 | 状态 |
|------|------|
| React | ✅ |
| Vue | ✅ |
| Angular | ✅ |
| Next.js | ✅ |
| Svelte | ✅ |
| FastAPI | ✅ |
| Django | ✅ |
| Express | ✅ |

### 数据库

| 框架 | 状态 |
|------|------|
| PostgreSQL | ✅ |
| MongoDB | ✅ |
| Redis | ✅ |
| Prisma | ✅ |

### 其他工具

| 框架 | 状态 |
|------|------|
| TypeScript | ✅ |
| Python | ✅ |
| Go | ✅ |
| Rust | ✅ |

---

## 安装方式

```bash
# 使用 npm 安装
npm install -g @context7/mcp-server

# 使用 npx 直接运行
npx -y @context7/mcp-server
```

---

## Claude Desktop 配置

```json
{
  "mcpServers": {
    "context7": {
      "command": "npx",
      "args": ["-y", "@context7/mcp-server"]
    }
  }
}
```

---

## 使用示例

### 查询 React 文档

```
查询 React useEffect 的正确用法
```

### 查询 Python 库

```
解释 asyncio 的基本用法
```

---

## 优缺点

### ✅ 优点

- 无需 API Key
- 实时更新的文档
- 多框架支持
- 本地缓存高效
- 免费使用

### ❌ 缺点

- 需要网络连接
- 首次加载较慢

---

## 对比竞品

| 服务 | API Key | 框架数 | 实时性 |
|------|---------|-------|--------|
| Context7 | ❌ 不需要 | 50+ | ✅ 实时 |
| Context9 | ✅ 需要 | 较少 | ✅ 实时 |
| Claude Docs | 内置 | 有限 | ⚠️ 滞后 |

---

## 相关资源

- [Context7 官网](https://context7.ai)
- [Upstash 文档](https://upstash.com)
- [MCP 官方文档](https://modelcontextprotocol.io)
