# MCP-For-Security - 安全测试 MCP 工具集合

> ⭐ 559 Stars · Python · 安全工具

## 1. 背景需求

安全研究人员和渗透测试人员需要将常用安全工具集成到 AI 工作流中。

## 2. 目标

提供流行安全工具的 MCP 服务器集合，集成到 AI 代理工作流。

## 3. 核心功能

- 🔍 SQLMap 集成
- 🌐 FFUF 集成
- 📡 NMAP 集成
- ⚡ Masscan 集成
- 🤖 AI 驱动扫描

## 4. 本地部署

```bash
# 安装
pip install mcp-for-security

# 配置
# 添加到 claude_desktop_config.json
{
  "mcpServers": {
    "security": {
      "command": "mcp-for-security",
      "args": ["--tools", "nmap,sqlmap"]
    }
  }
}
```

## 5. 效果展示

- GitHub Stars：⭐ 559

## 6. 优缺点

✅ 集成主流安全工具
✅ 自动化渗透测试
✅ AI 增强分析

⚠️ 仅供安全研究使用

## 7. 替代方案

| 插件 | 特点 |
|------|------|
| LitterBox | 恶意软件分析 |
| SecOps-MCP | 综合安全工具箱 |
