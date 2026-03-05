# Chrome DevTools MCP - 浏览器开发者工具

> 为 AI 编码代理提供 Chrome 开发者工具能力

## 1. 背景需求

AI 编码代理需要浏览器自动化能力来进行 Web 开发、测试和调试。

## 2. 目标

将 Chrome 开发者工具的能力带给 Claude Code 和其他 MCP 主机。

## 3. 核心功能

- 🌐 浏览器自动化
- 🔍 DOM 检查和操作
- 📊 网络请求监控
- 🖥️ 控制台分析
- 📸 页面截图
- ⏱️ 性能分析
- 🍪 Cookie 和存储管理

## 4. 本地部署

### 安装

```bash
# 通过 npm 安装
npm install -g @chromedevtools/mcp-server

# 或使用 npx
npx -y @chromedevtools/mcp-server
```

### MCP 配置

```json
{
  "mcpServers": {
    "chrome-devtools": {
      "command": "npx",
      "args": ["-y", "@chromedevtools/mcp-server"]
    }
  }
}
```

## 5. 可用工具

- `chromium_navigate` - 导航到 URL
- `chromium_screenshot` - 截图
- `chromium_dom` - 获取 DOM
- `chromium_console` - 获取控制台日志
- `chromium_network` - 网络请求
- `chromium_cookies` - Cookie 操作

## 6. 效果展示

- 完整的浏览器控制能力
- 适合 Web 开发自动化
- 支持测试自动化

## 7. 优缺点

✅ 功能完整
✅ 官方维护
✅ 持续更新

⚠️ 需要 Chrome/Chromium
⚠️ 依赖本地浏览器

## 8. 替代方案

| 工具 | 特点 |
|------|------|
| Playwright | 更强大的测试框架 |
| Puppeteer | Google 官方 |
| Selenium | 老牌自动化工具 |

## 9. 相关链接

- [Chrome DevTools](https://developer.chrome.com/docs/devtools)
- [GitHub](https://github.com/ChromeDevTools/chrome-devtools-mcp)
- [npm](https://www.npmjs.com/package/@chromedevtools/mcp-server)
