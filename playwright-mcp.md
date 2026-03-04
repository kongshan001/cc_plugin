# playwright-mcp Playwright MCP 服务器

> Playwright 浏览器自动化 MCP 服务器版本

## 1. 背景需求

需要通过 MCP 协议调用 Playwright 进行浏览器自动化。

## 2. 目标

提供 Playwright MCP 服务器版本，支持模型驱动自动化。

## 3. 设计方案

- MCP 协议集成
- 模型调用式自动化
- 浏览器控制
- E2E 测试

## 4. 本地部署

```bash
npx -y @modelcontextprotocol/server-playwright
```

## 5. 效果展示

- ClawHub 评分：3.581

## 6. 优缺点

✅ MCP 集成 ✅ 模型驱动  
⚠️ 配置复杂

## 7. 平替

| 技能 | 特点 |
|------|------|
| playwright | 基础版本 |

## 8. 落地过程

1. 安装 MCP 服务器
2. 配置 playwright
3. 编写测试
