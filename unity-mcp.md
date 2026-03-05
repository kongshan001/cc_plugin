# Unity MCP Server

> AI 助手与 Unity Editor 之间的桥梁

## 项目信息

- **GitHub**: [CoplayDev/unity-mcp](https://github.com/CoplayDev/unity-mcp)
- **语言**: C#
- **最新更新**: 2026-03-03
- **类别**: 游戏客户端开发 / MCP 服务器
- **状态**: ✅ 已调研

---

## 简介

Unity MCP 充当桥梁，允许 AI 助手（如 Claude、Cursor）通过本地 MCP（Model Context Protocol）客户端直接与 Unity Editor 进行交互。赋予 LLM 管理资源、控制场景、编辑脚本和在 Unity 中自动执行任务的能力。

---

## 核心功能

### 🎮 资产管理
| 功能 | 说明 |
|------|------|
| 资源创建 | 动态创建 Unity 资源 |
| 资源删除 | 删除不再需要的资源 |
| 资源查询 | 查找和检索项目资源 |

### 🖼️ 场景控制
| 功能 | 说明 |
|------|------|
| 场景加载 | 动态加载 Unity 场景 |
| 场景保存 | 自动保存场景更改 |
| 场景切换 | 程序化场景切换 |

### 📝 脚本编辑
| 功能 | 说明 |
|------|------|
| 脚本读取 | 读取现有 C# 脚本 |
| 脚本修改 | 自动修改脚本内容 |
| 组件管理 | 动态添加/删除组件 |

### ⚙️ 任务自动化
| 功能 | 说明 |
|------|------|
| 构建自动化 | 自动构建项目 |
| 批量处理 | 批量资源处理 |
| 重复任务 | 自动执行重复性工作 |

---

## 安装配置

### 前置要求
- Unity 2020.3 或更高版本
- .NET SDK
- Node.js (用于 MCP 客户端)

### 安装步骤

```bash
# 1. 克隆仓库
git clone https://github.com/CoplayDev/unity-mcp.git

# 2. 在 Unity 中打开项目

# 3. 安装 Unity 包
# 通过 Package Manager 安装 unity-mcp package

# 4. 配置 MCP 服务器
# 在项目中配置 MCP 服务器设置
```

---

## 使用示例

### 资产管理
```
让 Claude 创建 10 个新的游戏对象Prefab
```

### 场景控制
```
让 Claude 加载 MainScene 并添加一个摄像机
```

### 脚本编辑
```
让 Claude 修改 PlayerController.cs 添加跳跃功能
```

---

## 应用场景

### 🎮 游戏开发
- 快速原型开发
- 资源批量导入
- 自动化构建流程

### 🛠️ 工具开发
- 编辑器扩展开发
- 自定义编辑器工具
- 自动化测试脚本

---

## 与其他方案对比

| 方案 | 优点 | 缺点 |
|------|------|------|
| Unity MCP | AI 集成、原生支持 | 相对较新 |
| Unity Editor Scripting | 完全控制 | 需要手动编写 |
| Unity CLI | 自动化构建 | 功能有限 |

---

## 优缺点分析

### ✅ 优点
- AI 驱动的自动化
- 自然语言交互
- 减少重复性工作
- 提高开发效率

### ⚠️ 缺点
- 早期项目，稳定性和生态仍在发展
- 需要配置 MCP 环境
- 功能覆盖仍在扩展

---

## 相关链接

- [GitHub 仓库](https://github.com/CoplayDev/unity-mcp)
- [Unity 官方文档](https://docs.unity3d.com/)
- [MCP 官方文档](https://modelcontextprotocol.io/)
