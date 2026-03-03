# Shannon - AI 自动化渗透测试框架

## 📋 文档信息

- **插件名称**: Shannon
- **GitHub**: [KeygraphHQ/shannon](https://github.com/KeygraphHQ/shannon)
- **Star**: 26k ⭐
- **状态**: ✅ 已验证可用
- **调研日期**: 2026-03-03
- **分类**: 安全测试 / AI 渗透测试

---

## 1. 插件背景需求

### 问题痛点

随着 Claude Code、Cursor 等 AI 编程工具的普及，开发团队**代码产出速度大幅提升**，但安全测试仍然：
- **每年只做一次**渗透测试
- **364 天**处于安全真空期
- 上线后才发现漏洞，修复成本极高

### 目标

Shannon 作为**on-demand 白盒渗透测试器**，在每次构建后自动执行真实的漏洞利用验证，证明漏洞可被实际 exploitation，而不仅仅是报告潜在问题。

---

## 2. 设计方案

### 核心原理

```
┌─────────────────────────────────────────────────────────────────┐
│                      Shannon AI Pentester                       │
├─────────────────────────────────────────────────────────────────┤
│  ┌─────────────┐   ┌─────────────┐   ┌─────────────┐           │
│  │   Recon     │──▶│   Analysis  │──▶│  Exploitation│          │
│  │  侦察阶段    │   │   分析阶段   │   │    攻击验证   │          │
│  └─────────────┘   └─────────────┘   └─────────────┘           │
│        │                 │                  │                   │
│        ▼                 ▼                  ▼                   │
│  ┌─────────────┐   ┌─────────────┐   ┌─────────────┐           │
│  │ Nmap/Subfinder│  │ 代码语义分析 │   │ 浏览器自动化 │           │
│  │ WhatWeb     │   │ 数据流分析   │   │  注入验证    │           │
│  └─────────────┘   └─────────────┘   └─────────────┘           │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
                    ┌─────────────────┐
                    │  Pentest Report │
                    │  (含 PoC 代码)   │
                    └─────────────────┘
```

### 技术架构

- **核心引擎**: Anthropic Agent SDK (Claude 模型驱动)
- **运行环境**: Docker 容器化部署
- **工作流编排**: Temporal
- **攻击执行**: 集成浏览器自动化 + 命令行 exploit
- **支持认证**: 支持 2FA/TOTP、Google 登录等复杂认证流程

---

## 3. 本地部署

### 前置要求

| 要求 | 说明 |
|-----|------|
| **Docker** | 容器运行时 ([安装 Docker](https://docs.docker.com/get-docker/)) |
| **Anthropic API Key** | 推荐，或 Claude Code OAuth Token |
| **目标代码仓库** | 放入 `./repos/` 目录 |

### 安装步骤

```bash
# 1. 克隆仓库
git clone https://github.com/KeygraphHQ/shannon.git
cd shannon

# 2. 配置凭证 (二选一)

# 方式 A: 环境变量
export ANTHROPIC_API_KEY="your-api-key"
export CLAUDE_CODE_MAX_OUTPUT_TOKENS=64000

# 方式 B: .env 文件
cat > .env << 'EOF'
ANTHROPIC_API_KEY=your-api-key
CLAUDE_CODE_MAX_OUTPUT_TOKENS=64000
EOF

# 3. 放置目标仓库
git clone https://github.com/your-org/your-repo.git ./repos/your-repo

# 4. 启动渗透测试
./shannon start URL=https://your-app.com REPO=your-repo
```

### 监控进度

```bash
# 查看实时日志
./shannon logs

# 查询特定工作流状态
./shannon query ID=shannon-1234567890

# 打开 Temporal Web UI
open http://localhost:8233
```

### 停止服务

```bash
# 停止容器 (保留数据)
./shannon stop

# 完全清理 (删除所有数据)
./shannon stop CLEAN=true
```

### Windows 部署

```powershell
# 方式 1: Git Bash (需要 Docker Desktop)
git clone https://github.com/KeygraphHQ/shannon.git
cd shannon
./shannon start URL=https://your-app.com REPO=repo-name

# 方式 2: WSL2 (推荐)
wsl --install
# 然后在 WSL 中运行上述命令
```

---

## 4. 效果展示

### 核心功能

| 功能 | 说明 |
|-----|------|
| **全自动渗透测试** | 单一命令启动，全程无需干预 |
| **真实 Exploitation** | 执行实际的漏洞利用，而非仅扫描 |
| **Pentester 级报告** | 包含可复现的 PoC 代码 |
| **OWASP 漏洞覆盖** | Injection、XSS、SSRF、认证绕过等 |
| **支持 2FA/TOTP** | 自动处理双因素认证 |
| **并行处理** | 多漏洞类型同时检测 |

### 测试成果

- **OWASP Juice Shop**: 发现 **20+** 高危漏洞，包括完整认证绕过和数据库拖库
- **OWASP crAPI**: 发现 **15+** 关键漏洞，实现完整应用接管
- **Checkmarx c{api}tal**: 发现 **15** 个关键/高危漏洞

### 输出结构

```
audit-logs/{hostname}_{sessionId}/
├── session.json              # 指标和会话数据
├── agents/                   # 各 Agent 执行日志
├── prompts/                  # 提示词快照
└── deliverables/
    └── comprehensive_security_assessment_report.md  # 最终报告
```

---

## 5. 优缺点分析

### ✅ 优点

| 优点 | 说明 |
|-----|------|
| **高准确率** | XBOW 基准测试 96.15% 成功率 |
| **零误报** | 报告包含实际 PoC，可直接验证 |
| **自动化程度高** | 单一命令完成全流程 |
| **支持复杂认证** | 2FA/TOTP、Google 登录不在话下 |
| **开源可用** | Lite 版本 AGPL-3.0 免费使用 |

### ❌ 缺点

| 缺点 | 说明 |
|-----|------|
| **白盒测试** | 需要源代码，不适合黑盒测试场景 |
| **Docker 依赖** | 本地需运行 Docker |
| **资源消耗** | 并行处理需要较多 API 配额 |
| **非传统插件** | 是独立 CLI 工具，非 Claude Code 插件 |

---

## 6. 平替插件对比

| 工具 | 特点 | 适用场景 |
|-----|------|---------|
| **Shannon** | AI 自动化渗透测试 | 深度安全审计 |
| **OWASP ZAP** | 传统扫描器 | 常规安全扫描 |
| **Burp Suite** | 手动渗透测试 | 专业安全人员 |
| **claude-mem** | 长期记忆 | 记住安全发现 |

---

## 7. 落地过程

### 调研日期
2026-03-03

### 调研结果

#### 🔍 技术定位

Shannon **不是传统意义上的 Claude Code 插件**，而是一个：
- 独立运行的 Docker CLI 工具
- 使用 Claude (Anthropic) 作为 AI 引擎
- 内置基于 Anthropic Agent SDK 的多 Agent 架构
- 支持 Claude Code OAuth Token 认证

#### 📝 关键发现

1. **版本区别**
   - **Shannon Lite**: AGPL-3.0 开源版
   - **Shannon Pro**: 商业版，包含高级数据流分析引擎

2. **测试范围**
   - 仅支持**白盒测试** (需要源代码)
   - 适合：CI/CD 集成、自动化安全门禁
   - 不适合：外部黑盒渗透测试

3. **配置选项**
   - 支持自定义认证流程
   - 支持 TOTP 2FA
   - 支持工作区恢复 (断点续测)

#### ✅ 适用场景

- 每次 git push 后自动安全扫描
- 定期自动化渗透测试
- 开发阶段安全门禁 (CI/CD)
- 合规性安全测试

#### ⚠️ 注意事项

- 仅测试自有应用，**不要**用于未经授权的渗透测试
- 需要提供源代码访问权限
- API 消耗较大 (建议配置 `CLAUDE_CODE_MAX_OUTPUT_TOKENS=64000`)

---

## 8. 常见问题

### Q: Shannon 是 Claude Code 插件吗？
A: 不是。它是一个独立的 Docker CLI 工具，使用 Claude 作为 AI 引擎。类似 Claude Code 的"上下游工具"。

### Q: 支持黑盒测试吗？
A: 不支持。Shannon 是**白盒测试**工具，需要源代码访问权限。

### Q: 可以用于生产环境吗？
A: 可以，但建议先在测试环境验证。它会执行实际的漏洞利用，有一定风险。

### Q: 如何集成到 CI/CD？
A: Shannon Pro 版本支持 CI/CD 集成。Lite 版本可通过 Docker 命令集成。

---

## 📎 相关链接

- [GitHub](https://github.com/KeygraphHQ/shannon)
- [官网](https://keygraph.io)
- [Discord](https://discord.gg/KAqzSHHpRt)
- [OWASP Juice Shop 报告示例](./sample-reports/shannon-report-juice-shop.md)
- [XBOW 基准测试结果](./xben-benchmark-results/README.md)

---

*让 AI 成为你的 Red Team* 🛡️
