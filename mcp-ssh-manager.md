# mcp-ssh-manager SSH 远程管理工具

> 63 Stars | JavaScript | DevOps 自动化

## 1. 背景需求

DevOps 工程师需要管理多台远程服务器，传统 SSH 操作效率低下，需要自动化工具。

## 2. 目标

提供 37 个 Claude Code 和 OpenAI Codex 远程 SSH 管理工具，实现 DevOps 自动化。

## 3. 设计方案

**核心功能**
- SSH 连接管理
- 远程命令执行
- 数据库操作
- 健康监控
- 备份管理
- 部署自动化

**工具列表（37 个）**
| 类别 | 工具数 |
|------|--------|
| SSH 连接 | 8 |
| 文件操作 | 6 |
| 数据库 | 8 |
| 监控 | 5 |
| 备份 | 5 |
| 部署 | 5 |

## 4. 本地部署

```bash
# 通过 npm 安装
npm install mcp-ssh-manager

# 配置 SSH 连接
# 在 MCP 配置中添加服务器信息
```

## 5. 效果展示

- **GitHub Stars**: ⭐ 63
- **Fork**: 16
- **语言**: JavaScript

## 6. 优缺点

| 优点 | 缺点 |
|------|------|
| 37 个工具 | 需要 SSH 权限 |
| DevOps 全面支持 | 安全考虑 |
| 数据库集成 | |
| 持续更新 | |

## 7. 平替插件

| 插件 | 特点 |
|------|------|
| claude-k8s-plugin | K8s 运算符开发 |
| kube-audit-kit | K8s 安全审计 |

## 8. 落地过程

1. 安装 npm 包
2. 配置 SSH 服务器信息
3. 在 Claude Code 中配置 MCP
4. 开始远程管理
