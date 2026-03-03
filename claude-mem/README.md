# claude-mem - Claude 长期记忆插件

## 📋 文档信息

- **插件名称**: claude-mem
- **GitHub**: [thedotmack/claude-mem](https://github.com/thedotmack/claude-mem)
- **Star**: 32k ⭐
- **状态**: ✅ 已验证可用
- **验证日期**: 2026-03-03

---

## 1. 插件背景需求

### 问题痛点

Claude Code 每次会话都是**全新开始**的，之前会话中：
- 解决的问题
- 发现的坑
- 重要的决策
- 项目特有的约定

都不会被记住。每次都要重新解释，效率低下。

### 目标

让 Claude Code 具备**长期记忆能力**，自动记住会话中的关键信息，在后续会话中自动注入相关上下文。

---

## 2. 设计方案

### 核心原理

```
┌─────────────┐    捕获工具调用    ┌─────────────┐
│  Claude     │ ───────────────▶ │  claude-mem │
│  Code       │                  │  Worker     │
└─────────────┘                  └──────┬──────┘
      ▲                                 │
      │ 注入上下文                       │ AI 压缩
      │                                 ▼
      │                          ┌─────────────┐
      └──────────────────────────│  本地向量库  │
           未来会话自动             │  (SQLite)   │
           加载相关记忆             └─────────────┘
```

### 技术架构

- **存储**: SQLite 本地向量数据库
- **索引**: 自动语义摘要 + 工具调用记录
- **检索**: 基于相似度的上下文召回
- **压缩**: 使用 Claude AI 压缩记忆内容

---

## 3. 本地部署

### macOS / Linux

```bash
# 方式一：通过 Claude Code 插件市场安装
/plugin marketplace add thedotmack/claude-mem
/plugin install claude-mem

# 重启 Claude Code
# 之后每次会话会自动加载历史记忆
```

### Windows

```powershell
# 同样的命令，在 PowerShell 或 CMD 中运行
/plugin marketplace add thedotmack/claude-mem
/plugin install claude-mem

# 重启 Claude Code
```

### 验证安装

```bash
# 查看插件状态
/plugin list

# 应该能看到 claude-mem
```

---

## 4. 效果展示

### 首次使用

首次安装后，会话开始时显示：
```
📚 Loading context from previous sessions...
```

### 后续会话

Claude 会自动记住：
- 之前修复过的 Bug
- 项目架构决策
- 重要的文件位置
- 特定的代码约定

---

## 5. 优缺点分析

### ✅ 优点

| 优点 | 说明 |
|-----|------|
| **零配置** | 安装即用，无需额外设置 |
| **本地存储** | 隐私安全，数据不离开本地 |
| **自动摘要** | AI 自动压缩记忆内容 |
| **跨平台** | macOS/Windows/Linux 通用 |

### ❌ 缺点

| 缺点 | 说明 |
|-----|------|
| **首次冷启动** | 需要积累一段时间才有效 |
| **存储上限** | SQLite 有大小限制，大项目需清理 |
| **无选择性记忆** | 无法指定"只记住这个" |

---

## 6. 平替插件对比

| 插件 | 特点 | 适用场景 |
|-----|------|---------|
| **claude-mem** | 自动捕获 + AI 摘要 | 通用场景 |
| **memory** | 手动添加记忆 | 需要精确控制 |
| **openclaw** | 完整 AI 助手框架 | 需要更多功能 |

---

## 7. 落地过程

### 验证日期
2026-03-03

### 验证步骤

1. **安装插件**
   ```bash
   claude plugin marketplace add thedotmack/claude-mem
   claude plugin install claude-mem
   ```

2. **检查安装状态**
   ```bash
   claude plugin list
   # 结果: claude-mem@thedotmack ✔ enabled
   ```

3. **启动 Worker 服务** ⚠️ **关键步骤**
   ```bash
   # 需要先安装 Bun 运行时
   curl -fsSL https://bun.sh/install | bash
   
   # 启动 Worker
   cd ~/.claude/plugins/marketplaces/thedotmack/plugin
   node scripts/worker-cli.js start
   ```

4. **验证 Worker 状态**
   ```bash
   # 检查日志
   cat ~/.claude-mem/logs/claude-mem-*.log
   ```

### 验证结果

| 验证项 | 结果 | 说明 |
|-------|------|------|
| 插件安装 | ✅ 成功 | v10.5.2 |
| 配置生成 | ✅ 成功 | ~/.claude-mem/settings.json |
| Bun 安装 | ✅ 成功 | v1.1.168 |
| Worker 启动 | ✅ 成功 | PID: 203169, Port: 37777 |
| API 健康检查 | ✅ 成功 | {"status":"ok"} |

### 发现的问题

1. **依赖 Bun 运行时**
   - Worker 服务需要 Bun 才能运行
   - 文档中未明确说明此依赖
   - 安装命令: `curl -fsSL https://bun.sh/install | bash`

2. **Worker 默认不启动**
   - 插件安装后 Worker 不会自动启动
   - 需要手动启动: `bun scripts/worker-service.cjs`
   - 或者配置自动启动

3. **日志位置**
   - Worker 日志: `~/.claude-mem/logs/worker-YYYY-MM-DD.log`
   - MCP 日志: `~/.claude-mem/logs/claude-mem-YYYY-MM-DD.log`

### 待验证

- [x] Worker 启动
- [ ] 实际记忆效果（需要与 Claude Code 集成测试）
- [ ] Windows 兼容性
- [ ] 记忆清理机制

---

## 8. 常见问题

### Q: 安装后没有生效？
A: 需要**完全退出并重启** Claude Code，不是断开重连。

### Q: 记忆可以手动删除吗？
A: 可以，删除 `~/.claude-mem/` 目录即可。

### Q: Worker 启动失败？
A: 确保已安装 Bun 运行时: `curl -fsSL https://bun.sh/install | bash`

### Q: 支持自定义记忆范围吗？
A: 暂不支持自动捕获，需要手动记忆可用 `memory` 插件。

### Q: 日志在哪里？
A: `~/.claude-mem/logs/claude-mem-YYYY-MM-DD.log`

---

## 📎 相关链接

- [GitHub](https://github.com/thedotmack/claude-mem)
- [NPM](https://www.npmjs.com/package/claude-mem)
- [awesome-claude-code](https://github.com/thedotmack/awesome-claude-code)
- [Bun 官网](https://bun.sh)
