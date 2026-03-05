# Anthropic Python SDK - Claude API Python 客户端

> 官方 Python SDK for Claude API

## 1. 背景需求

Python 开发者需要官方 SDK 来访问 Claude API，实现 AI 功能集成。

## 2. 目标

提供 Python 应用中访问 Claude API 的官方解决方案。

## 3. 核心功能

- 🐍 纯 Python 实现
- 📦 官方维护
- 🔄 异步支持
- 💬 消息创建和管理
- 🌊 流式响应
- 📝 完整类型提示

## 4. 本地部署

### 安装

```bash
pip install anthropic
```

### 基本使用

```python
import os
from anthropic import Anthropic

client = Anthropic(
    api_key=os.environ.get("ANTHROPIC_API_KEY")
)

message = client.messages.create(
    max_tokens=1024,
    messages=[
        {
            "role": "user",
            "content": "Hello, Claude",
        }
    ],
    model="claude-opus-4-6",
)

print(message.content)
```

### 异步使用

```python
import asyncio
from anthropic import AsyncAnthropic

async def main():
    client = AsyncAnthropic()
    
    message = await client.messages.create(
        max_tokens=1024,
        messages=[
            {
                "role": "user", 
                "content": "Hello, Claude"
            }
        ],
        model="claude-opus-4-6",
    )
    
    print(message.content)

asyncio.run(main())
```

## 5. 支持的模型

- claude-opus-4-6
- claude-sonnet-4-6
- claude-haiku-3-5
- 等等

## 6. 效果展示

- 官方维护和更新
- 完善的文档
- 活跃的社区

## 7. 优缺点

✅ 官方支持
✅ 类型安全
✅ 持续更新
✅ 文档完善

⚠️ 需要 API Key
⚠️ 付费使用

## 8. 替代方案

| SDK | 特点 |
|-----|------|
| anthropic-sdk-python | 官方 Python SDK |
| LangChain | LLM 集成框架 |
| LiteLLM | 统一 LLM API |

## 9. 要求

- Python 3.9+
- Anthropic API Key

## 10. 相关链接

- [PyPI](https://pypi.org/project/anthropic/)
- [官方文档](https://docs.anthropic.com/en/api/claude-api)
- [GitHub](https://github.com/anthropics/anthropic-sdk-python)
