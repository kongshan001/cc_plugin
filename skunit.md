# SkUnit - AI 单元测试框架

> ⭐ 171 Stars · Python · 测试工具

## 1. 背景需求

AI 组件（MCP 服务器、代理、聊天客户端）的测试需要专门的测试框架。

## 2. 目标

提供针对 AI 单元的测试工具，支持 IChatClient、MCP 服务器和代理的测试。

## 3. 核心功能

- 🧪 AI 组件测试
- 🔌 MCP 服务器测试
- 🤖 代理行为验证
- 📊 测试报告

## 4. 本地部署

```bash
# 安装
pip install skunit

# 使用
from skunit import TestClient

client = TestClient()
result = client.test_agent("test_scenario")
```

## 5. 效果展示

- GitHub Stars：⭐ 171

## 6. 优缺点

✅ 专门的 AI 测试框架
✅ 支持 MCP 服务器测试
✅ 代理验证

⚠️ 社区较小

## 7. 替代方案

| 插件 | 特点 |
|------|------|
| Playwright-Skill | E2E 测试 |
| MCP Inspector | MCP 服务器测试 |
| MCP-Universe | 代理基准测试 |
