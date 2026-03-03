# Playwright MCP Server - Claude Code 浏览器自动化

## 📋 文档信息

- **插件名称**: Playwright MCP Server
- **GitHub**: [modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers/tree/main/src/playwright)
- **Star**: ⭐ (官方维护)
- **状态**: ✅ 已调研
- **调研日期**: 2026-03-04
- **分类**: MCP Server / 浏览器自动化 / 测试工具

---

## 1. 插件背景需求

### 问题痛点

- 浏览器自动化测试配置复杂
- 缺乏与 AI 编程助手的深度集成
- 手动编写测试脚本耗时
- 跨浏览器测试困难

### 目标

Playwright MCP Server 是一个**模型上下文协议 (MCP) 服务器**，为 Claude Code 提供浏览器自动化能力。通过 MCP 协议，可以直接在 Claude Code 中进行浏览器操作、自动化测试和网页抓取。

---

## 2. 设计方案

### 核心架构

```
┌─────────────────────────────────────────────────────────────────┐
│                  Playwright MCP Server 架构                      │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│   ┌─────────────┐   ┌─────────────┐   ┌─────────────┐        │
│   │ Claude Code │◄──│   MCP       │◄──│  Playwright │        │
│   │   客户端    │   │   协议      │   │   浏览器    │        │
│   └─────────────┘   └──────┬──────┘   └─────────────┘        │
│                             │                                   │
│                             ▼                                   │
│                    ┌─────────────────┐                         │
│                    │  Playwright    │                         │
│                    │  MCP Server     │                         │
│                    └─────────────────┘                         │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### 核心能力

| 能力 | 说明 |
|------|------|
| **浏览器控制** | 启动、关闭浏览器 |
| **页面操作** | 导航、点击、输入 |
| **元素定位** | CSS、XPath、ARIA |
| **截图** | 页面截图、元素截图 |
| **PDF** | 生成 PDF |
| **网络拦截** | 模拟请求/响应 |

---

## 3. 本地部署

### 前置要求

| 要求 | 说明 |
|-----|------|
| **Node.js** | 18+ |
| **Playwright** | 已安装 (自动安装 Chromium) |
| **浏览器** | Chromium/Firefox/WebKit |

### 安装步骤

#### 方式 1: npm 安装

```bash
# 1. 安装 MCP 服务器
npm install -g @modelcontextprotocol/server-playwright

# 2. 安装浏览器
npx playwright install chromium

# 3. 验证安装
npx @modelcontextprotocol/server-playwright --help
```

#### 方式 2: Docker 部署

```bash
# 1. 拉取镜像
docker pull mcp/playwright

# 2. 运行容器
docker run -d \
  -p 3000:3000 \
  mcp/playwright

# 3. 配置 Claude Code
# MCP_SERVER_URL=http://localhost:3000
```

#### 方式 3: 本地运行 + Claude Code 配置

```bash
# 1. 克隆仓库
git clone https://github.com/modelcontextprotocol/servers.git
cd servers

# 2. 安装依赖
npm install

# 3. 构建
npm run build --workspace=@modelcontextprotocol/server-playwright

# 4. 配置 Claude Code
# 在 claude_settings.json 中添加:
{
  "mcpServers": {
    "playwright": {
      "command": "node",
      "args": ["/path/to/servers/dist/playwright/index.js"]
    }
  }
}
```

---

## 4. 核心功能详解

### 4.1 浏览器操作

```markdown
### 可用操作
- 启动浏览器 (chromium/firefox/webkit)
- 关闭浏览器
- 新建页面
- 关闭页面

### 示例
"打开一个新的 Chromium 浏览器"
"关闭当前浏览器"
```

### 4.2 页面导航

```markdown
### 可用操作
- 导航到 URL
- 返回上一页
- 前进到下一页
- 刷新页面
- 获取当前 URL
- 获取页面标题

### 示例
"导航到 https://example.com"
"刷新当前页面"
```

### 4.3 元素交互

```markdown
### 可用操作
- 点击元素
- 输入文本
- 下拉选择
- 复选框/单选框
- 拖拽元素
- 悬停

### 示例
"点击登录按钮"
"在搜索框输入 '游戏'"
"选择下拉框中的选项"
```

### 4.4 元素定位策略

```markdown
### 定位方式
- CSS 选择器
- XPath
- ARIA 角色
- 文本内容
- ID/Class
- 自定义属性

### 最佳实践
1. 使用 data-testid (推荐)
2. 使用 ARIA 角色
3. 避免脆弱的 XPath
4. 使用文本内容
```

### 4.5 截图功能

```markdown
### 可用操作
- 页面截图
- 元素截图
- 截取特定区域

### 示例
"截图保存到 /tmp/screenshot.png"
"截取登录表单区域"
```

### 4.6 网络拦截

```markdown
### 可用操作
- 拦截请求
- 模拟响应
- 修改请求头
- 模拟网络条件

### 示例
"拦截所有 API 请求并返回模拟数据"
"模拟 3G 网络环境"
```

---

## 5. 适用场景

### ✅ 适用场景

| 场景 | 说明 |
|------|------|
| **自动化测试** | E2E 测试脚本生成 |
| **网页抓取** | 数据采集 |
| **表单自动化** | 批量填写表单 |
| **截图** | 生成网页截图 |
| **PDF 生成** | 将网页转为 PDF |
| **浏览器测试** | 兼容性测试 |

### ⚠️ 注意事项

| 场景 | 说明 |
|------|------|
| 反爬虫 | 遵守网站 robots.txt |
| 登录状态 | 处理认证需要额外配置 |
| 资源消耗 | 多浏览器实例占用资源 |

---

## 6. 优缺点分析

### ✅ 优点

| 优点 | 说明 |
|-----|------|
| **官方维护** | Anthropic 官方 MCP 服务器 |
| **功能完整** | 覆盖大多数浏览器操作 |
| **跨浏览器** | 支持 Chromium/Firefox/WebKit |
| **MCP 标准化** | 统一的协议接口 |

### ❌ 缺点

| 缺点 | 说明 |
|-----|------|
| **资源消耗** | 浏览器实例占用内存 |
| **速度** | 比纯 API 操作慢 |
| **不稳定** | 页面结构变化可能导致失败 |

---

## 7. 与 Claude Code 集成

### 配置示例

```json
{
  "mcpServers": {
    "playwright": {
      "command": "npx",
      "args": ["@modelcontextprotocol/server-playwright"],
      "env": {
        "PLAYWRIGHT_BROWSERS_PATH": "/usr/local/share/playwright"
      }
    }
  }
}
```

### 使用示例

```
# 自然语言指令
"打开浏览器访问 example.com"
"点击页面上的登录按钮"
"截图保存到桌面"
"填写表单: 用户名=test, 密码=123456"
```

---

## 8. 落地过程

### 调研日期
2026-03-04

### 快速开始

```bash
# 1. 安装 Playwright MCP Server
npm install -g @modelcontextprotocol/server-playwright

# 2. 安装浏览器
npx playwright install chromium

# 3. 启动服务器
npx @modelcontextprotocol/server-playwright

# 4. 在 Claude Code 中使用
# "打开浏览器访问 https://example.com"
```

### 验证结果

| 验证项 | 结果 |
|-------|------|
| 仓库可访问 | ✅ |
| npm 包可用 | ✅ |
| 功能完整性 | ✅ |
| 文档完整性 | ✅ |

---

## 9. 游戏客户端测试应用

### Web 管理后台测试

```markdown
### 适用场景
1. 登录页面自动化测试
2. 用户管理界面测试
3. 游戏配置管理测试
4. 数据统计页面测试

### 示例命令
"测试游戏后台登录流程"
"验证用户管理页面的 CRUD 操作"
"截图游戏配置页面"
```

### 集成测试

```markdown
### 测试场景
1. API 响应验证
2. WebSocket 连接测试
3. 实时数据展示
4. 文件上传功能

### 命令示例
"测试用户登录 API"
"验证 WebSocket 连接"
```

---

## 📎 相关链接

- [GitHub](https://github.com/modelcontextprotocol/servers)
- [Playwright 文档](https://playwright.dev/docs/intro)
- [MCP 协议](https://modelcontextprotocol.io/)
- [Playwright MCP 示例](https://github.com/modelcontextprotocol/servers/tree/main/src/playwright)

---

*让浏览器自动化变得简单* 🕸️
