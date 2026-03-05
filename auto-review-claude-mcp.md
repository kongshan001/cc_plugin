# Auto-Review-ClaudeMCP Unity PR 自动化审查

> 19 Stars | Python | 游戏项目 QA 自动化

## 1. 背景需求

Unity 游戏项目包含大量资源文件（二进制、图片、音频、.meta 文件），PR 审查时需要过滤这些文件，只关注实际代码变更。

## 2. 目标

提供 AI 驱动的 PR 审查工具，自动过滤不必要文件，加速游戏项目代码审查。

## 3. 设计方案

**核心功能**
- GitHub PR diff 获取
- 二进制/资源文件过滤
- Unity 特定文件处理
- AI 代码审查

**过滤的文件类型**
| 类型 | 示例 |
|------|------|
| Unity meta | .meta |
| 图片 | .png, .jpg, .psd |
| 音频 | .wav, .mp3, .ogg |
| Shader | .shader, .shadergraph |
| 二进制 | .dll, .bin |

## 4. 本地部署

```bash
# 安装
pip install auto-review-claude-mcp

# 配置 MCP 服务器
# 添加 GitHub token
```

## 5. 效果展示

- **GitHub Stars**: ⭐ 19
- **Fork**: 0
- **语言**: Python

## 6. 优缺点

| 优点 | 缺点 |
|------|------|
| 专为游戏项目优化 | 新项目，生态小 |
| 过滤不必要文件 | 主要针对 Unity |
| AI 驱动审查 | |
| 加速 PR 流程 | |

## 7. 平替插件

| 插件 | 特点 |
|------|------|
| pr-review-toolkit | 通用 PR 审查 |

## 8. 落地过程

1. 安装 Python 包
2. 配置 GitHub token
3. 配置 MCP 服务器
4. 自动审查 PR
