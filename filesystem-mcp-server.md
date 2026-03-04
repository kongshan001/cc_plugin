# Filesystem MCP 服务器

> 安全文件操作的 MCP 服务器

## 项目信息

- **官方维护**: Model Context Protocol
- **技能类别**: 开发者工具 / 文件系统
- **状态**: ✅ 官方参考实现

---

## 简介

Filesystem MCP 服务器是 Model Context Protocol 官方参考实现，提供安全的文件操作能力。

---

## 核心功能

| 功能 | 说明 |
|------|------|
| 目录浏览 | 浏览文件系统 |
| 文件读写 | 读取和写入文件 |
| 权限控制 | 可配置访问控制 |
| 安全限制 | 防止越权访问 |

---

## 技术架构

- **SDK**: TypeScript SDK
- **协议**: MCP (Model Context Protocol)
- **安全**: 可配置的访问控制列表

---

## 安装方式

```bash
# 官方参考实现，可从以下地址获取
# https://github.com/modelcontextprotocol/servers/tree/main/src/filesystem
```

---

## 配置选项

```json
{
  "filesystem": {
    "allowedDirectories": ["/path/to/allowed/dir"],
    "maxFileSize": 10485760,
    "readonly": false
  }
}
```

---

## 相关链接

- [MCP 官方服务器仓库](https://github.com/modelcontextprotocol/servers)
- [Fetch MCP 服务器](./fetch-mcp-server.md)
