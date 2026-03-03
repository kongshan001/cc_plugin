# Trail of Bits Security Skills - AI 安全代码审计技能集

## 📋 文档信息

- **插件名称**: Trail of Bits Security Skills
- **GitHub**: [trailofbits/skills](https://github.com/trailofbits/skills)
- **Star**: 高 ⭐ (Trail of Bits 官方)
- **状态**: ✅ 已调研
- **调研日期**: 2026-03-03
- **分类**: 安全测试 / 代码审计 / AI 辅助安全

---

## 1. 插件背景需求

### 问题痛点

AI 编程助手（如 Claude Code）虽能快速生成代码，但存在安全盲点：
- **缺乏专业安全知识** - AI 不熟悉最新漏洞模式
- **无法深度审计** - 不会使用 CodeQL、Semgrep 等专业工具
- **误报率高** - 缺乏针对特定语言的漏洞理解
- **供应链风险** - 依赖项安全评估困难

### 目标

Trail of Bits Security Skills 作为**专业安全公司的 AI 技能集**，让 Claude Code 具备：
- 企业级代码审计能力
- 自动化漏洞检测
- 安全最佳实践验证
- 供应链风险评估

---

## 2. 设计方案

### 核心架构

```
┌─────────────────────────────────────────────────────────────────┐
│              Trail of Bits Security Skills 架构                  │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│   ┌─────────────────────────────────────────────────────────┐  │
│   │                    安全技能层                             │  │
│   ├──────────────┬──────────────┬──────────────┬───────────┤  │
│   │   智能合约    │   代码审计    │   漏洞检测    │   供应链  │  │
│   │   Security   │    Audit     │  Detection   │  Supply  │  │
│   └──────────────┴──────────────┴──────────────┴───────────┘  │
│                                                                 │
│   ┌─────────────────────────────────────────────────────────┐  │
│   │                   工具集成层                             │  │
│   ├──────────────┬──────────────┬──────────────┬───────────┤  │
│   │    CodeQL    │   Semgrep    │     YARA     │  SARIF    │  │
│   └──────────────┴──────────────┴──────────────┴───────────┘  │
│                                                                 │
│   ┌─────────────────────────────────────────────────────────┐  │
│   │                 Claude Code 集成层                       │  │
│   │            (通过 Agent Skills 机制加载)                  │  │
│   └─────────────────────────────────────────────────────────┘  │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### 技能分类

| 类别 | 技能数量 | 代表技能 |
|-----|---------|---------|
| **智能合约安全** | 2 | building-secure-contracts, entry-point-analyzer |
| **代码审计** | 5 | audit-context-building, differential-review |
| **漏洞检测** | 6 | static-analysis, semgrep-rule-creator, sharp-edges |
| **供应链安全** | 1 | supply-chain-risk-auditor |
| **密码学安全** | 2 | constant-time-analysis, zeroize-audit |
| **测试** | 2 | property-based-testing, testing-handbook-skills |
| **通用开发** | 8 | modern-python, devcontainer-setup |
| **其他** | 4 | yara-authoring, burpsuite-project-parser |

### 技能列表

#### 🛡️ 智能合约安全

| 技能 | 功能 |
|-----|------|
| **building-secure-contracts** | 智能合约安全工具包，支持 6 条区块链的漏洞扫描 |
| **entry-point-analyzer** | 识别智能合约中可改变状态的入口点 |

#### 🔍 代码审计

| 技能 | 功能 |
|-----|------|
| **agentic-actions-auditor** | 审计 GitHub Actions 工作流中的 AI Agent 安全漏洞 |
| **audit-context-building** | 通过超细粒度代码分析构建深度架构上下文 |
| **differential-review** | 安全导向的代码变更审查，含 git 历史分析 |
| **static-analysis** | 静态分析工具包，支持 CodeQL、Semgrep、SARIF |
| **variant-analysis** | 跨代码库的模式化漏洞搜索 |

#### 🚨 漏洞检测

| 技能 | 功能 |
|-----|------|
| **insecure-defaults** | 检测不安全默认配置、硬编码凭据、防守失败模式 |
| **semgrep-rule-creator** | 创建和优化自定义漏洞检测的 Semgrep 规则 |
| **semgrep-rule-variant-creator** | 将现有 Semgrep 规则移植到新目标语言 |
| **sharp-edges** | 识别易错的 API、危险配置和"脚枪"设计 |
| **supply-chain-risk-auditor** | 审计项目依赖的供应链威胁态势 |
| **testing-handbook-skills** | 测试手册技能：模糊器、静态分析、清理器、覆盖率 |

#### 🔐 密码学安全

| 技能 | 功能 |
|-----|------|
| **constant-time-analysis** | 检测加密代码中的编译器诱导时序侧信道 |
| **zeroize-audit** | 检测 C/C++ 和 Rust 中缺失的敏感数据清零 |

#### 🧪 测试

| 技能 | 功能 |
|-----|------|
| **property-based-testing** | 多语言和智能合约的属性测试指导 |
| **spec-to-code-compliance** | 规范到代码的合规性检查器 |

---

## 3. 本地部署

### 前置要求

| 要求 | 说明 |
|-----|------|
| **Claude Code** | 已安装并配置 |
| **网络** | 访问 GitHub 下载技能 |
| **工具** | 部分技能需要 CodeQL、Semgrep 等 |

### 安装步骤

#### 方式 1: 插件市场（推荐）

```bash
# 添加插件市场
/plugin marketplace add trailofbits/skills

# 查看可用插件
/plugin menu
```

#### 方式 2: 手动克隆

```bash
# 克隆技能仓库
git clone https://github.com/trailofbits/skills.git

# 移动到 Claude Code 技能目录
# 方式 A: 链接方式
ln -s /path/to/skills ~/.claude/plugins/trailofbits-skills

# 方式 B: 复制方式
cp -r skills ~/.claude/plugins/trailofbits-skills
```

### 验证安装

```bash
# 查看已安装技能
ls ~/.claude/plugins/

# 或在 Claude Code 中查看技能列表
```

---

## 4. 效果展示

### 核心功能

| 功能 | 说明 |
|-----|------|
| **CodeQL 集成** | 自动生成和优化 CodeQL 查询 |
| **Semgrep 规则** | 创建自定义漏洞检测规则 |
| **智能合约审计** | 6 条区块链的自动化安全扫描 |
| **供应链审计** | 依赖项威胁评估 |
| **差分审查** | git 历史感知的代码变更安全审查 |
| **变体分析** | 跨代码库的漏洞模式搜索 |

### 使用示例

#### 示例 1: 静态分析

```
用户: "帮我分析这个 Python 项目的安全问题"

Claude Code 自动:
1. 加载 static-analysis 技能
2. 运行 Semgrep 扫描
3. 解析 SARIF 报告
4. 生成漏洞修复建议
```

#### 示例 2: 智能合约审计

```
用户: "审计这个 Solidity 合约"

Claude Code 自动:
1. 加载 building-secure-contracts 技能
2. 识别区块链类型
3. 运行漏洞扫描器
4. 生成审计报告
```

#### 示例 3: Semgrep 规则创建

```
用户: "创建一个检测 SQL 注入的规则"

Claude Code 自动:
1. 加载 semgrep-rule-creator 技能
2. 分析目标语言
3. 生成 Semgrep 规则
4. 提供测试用例
```

### 实际发现

Trail of Bits Skills 已被用于发现真实漏洞：

| 技能 | 发现 |
|-----|------|
| constant-time-analysis | [ML-DSA 签名时序侧信道](https://github.com/RustCrypto/signatures/pull/1144) |

---

## 5. 优缺点分析

### ✅ 优点

| 优点 | 说明 |
|-----|------|
| **专业背书** | Trail of Bits 官方出品，全球顶级安全公司 |
| **工具完整** | 集成 CodeQL、Semgrep、YARA 等主流工具 |
| **覆盖广泛** | 智能合约、传统代码、供应链多领域覆盖 |
| **实际验证** | 已发现真实安全漏洞 |
| **开源可用** | CC-BY-SA-4.0 许可证 |
| **活跃维护** | 持续更新新技能 |

### ❌ 缺点

| 缺点 | 说明 |
|-----|------|
| **工具依赖** | 部分技能需要安装额外工具 (CodeQL, Semgrep) |
| **学习曲线** | 需要理解安全工具才能有效使用 |
| **权限要求** | 部分操作需要代码库写入权限 |
| **误报可能** | 自动扫描结果需人工复核 |

---

## 6. 平替插件对比

| 工具 | 特点 | 适用场景 |
|-----|------|---------|
| **Trail of Bits Skills** | 专业安全公司技能集 | 企业级安全审计 |
| **Shannon** | AI 自动化渗透测试 | 深度渗透测试 |
| **OWASP ZAP** | 传统 Web 扫描器 | 常规安全扫描 |
| **Burp Suite** | 手动渗透测试 | 专业安全人员 |

---

## 7. 落地过程

### 调研日期
2026-03-03

### 调研结果

#### 🔍 技术定位

Trail of Bits Skills 是 **Claude Code 的专业安全技能集**，特点：
- 来自全球顶级安全公司 Trail of Bits
- 专注于代码审计和漏洞检测
- 集成企业级安全工具 (CodeQL, Semgrep)
- 支持智能合约安全审计

#### 📝 关键发现

1. **技能组织**
   - 按功能分类：智能合约、代码审计、漏洞检测等
   - 每个技能独立，可按需选用

2. **安装方式**
   - 支持插件市场方式安装
   - 支持手动克隆到本地

3. **工具集成**
   - CodeQL: 静态分析
   - Semgrep: 模式匹配漏洞检测
   - YARA: 恶意软件检测规则
   - SARIF: 标准化分析结果格式

4. **与 Shannon 对比**
   | 特性 | Trail of Bits Skills | Shannon |
   |-----|---------------------|---------|
   | 类型 | Agent Skills | 独立渗透测试工具 |
   | 方式 | 白盒代码审计 | 黑盒渗透测试 |
   | 工具 | CodeQL/Semgrep | 浏览器自动化 |
   | 范围 | 代码级漏洞 | 运行时漏洞 |

#### ✅ 适用场景

- **代码安全审计** - 自动化发现代码中的安全漏洞
- **智能合约审计** - 6 条区块链的自动化安全扫描
- **供应链安全** - 评估依赖项威胁
- **CI/CD 集成** - 安全门禁
- **漏洞研究** - 变体分析和复现

#### ⚠️ 注意事项

- 部分技能需要安装额外工具
- 扫描结果需要人工复核
- 某些操作可能产生误报

---

## 8. 常见问题

### Q: Trail of Bits Skills 是 Claude Code 插件吗？
A: 是的。它是 Claude Code 的 Agent Skills，可通过插件市场安装。

### Q: 和 Shannon 有什么区别？
A: Shannon 是独立渗透测试工具，侧重运行时漏洞利用；Trail of Bits Skills 是代码审计技能集，侧重代码级漏洞检测。

### Q: 需要安装额外工具吗？
A: 部分技能需要 CodeQL、Semgrep 等工具。建议按需安装。

### Q: 支持中文吗？
A: 技能描述为英文，但可配合 Claude Code 的中文能力使用。

---

## 📎 相关链接

- [GitHub](https://github.com/trailofbits/skills)
- [Trail of Bits 官网](https://www.trailofbits.com/)
- [Testing Handbook](https://appsec.guide)
- [CLAUDE.md 编写指南](https://github.com/trailofbits/skills/blob/main/CLAUDE.md)

---

*让 AI 成为你的安全审计专家* 🛡️
