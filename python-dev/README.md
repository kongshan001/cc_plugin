# Claude Code Python 开发插件调研

## 📋 文档信息

- **调研日期**: 2026-03-03
- **分类**: Python 开发 / 数据库
- **状态**: ✅ 已调研

---

## 1. read-only-postgres - PostgreSQL 只读查询技能

### 插件概述

| 项目 | 说明 |
|-----|------|
| **GitHub** | [jawwadfirdousi/agent-skills](https://github.com/jawwadfirdousi/agent-skills) |
| **功能** | PostgreSQL 只读查询技能 |
| **特点** | 安全优先的数据库查询 |

### 核心功能

- **只读查询**: 仅支持 SELECT/SHOW/EXPLAIN/WITH 查询
- **多连接支持**: 配置多个数据库连接，带描述说明
- **安全验证**: 严格的验证机制、超时控制、行数限制
- **防御性设计**: 多层安全保护

### 技术特点

```python
# 支持的查询类型
- SELECT 查询
- SHOW 命令
- EXPLAIN 分析
- WITH 公共表表达式
```

### 适用场景

- 数据分析
- 数据库调试
- 快速数据探索

---

## 2. postgres - PostgreSQL 完整集成技能

### 插件概述

| 项目 | 说明 |
|-----|------|
| **GitHub** | [sanjay3290/ai-skills](https://github.com/sanjay3290/ai-skills) |
| **功能** | PostgreSQL 完整集成 |
| **特点** | 多连接支持 + 防御性安全 |

### 核心功能

- 安全只读 SQL 查询
- 多数据库连接管理
- 防御性安全设计
- 完善的错误处理

---

## 3. Python 开发相关技能汇总

| 技能名称 | 功能 | 适用场景 |
|---------|------|---------|
| **read-only-postgres** | PostgreSQL 只读查询 | 数据库调试/分析 |
| **postgres** | PostgreSQL 完整集成 | 生产数据库操作 |
| **pypict-claude-skill** | PICT 测试用例生成 | 组合测试 |
| **test-driven-development** | TDD 开发流程 | 规范开发 |

---

## 4. 部署指南

### 安装步骤

```bash
# 克隆技能仓库
git clone https://github.com/jawwadfirdousi/agent-skills.git

# 复制到 Claude Code 技能目录
cp -r agent-skills/read-only-postgres ~/.claude/skills/

# 或使用技能安装命令
claude --install-skill gh-jawwadfirdousi-read-only-postgres
```

### 配置数据库连接

```bash
# 配置环境变量或配置文件
export POSTGRES_HOST=localhost
export POSTGRES_USER=your_user
export POSTGRES_PASSWORD=your_password
export POSTGRES_DATABASE=your_db
```

---

## 5. 优缺点分析

### ✅ 优点

| 优点 | 说明 |
|-----|------|
| **安全优先** | 只读查询防止意外数据修改 |
| **多连接** | 支持配置多个数据库 |
| **轻量级** | 简单易用，无需复杂配置 |
| **防御性** | 超时和行数限制保护 |

### ❌ 缺点

| 缺点 | 说明 |
|-----|------|
| **仅 PostgreSQL** | 不支持其他数据库 |
| **功能有限** | 主要是查询，不支持 DDL/DML |
| **需自行部署** | 需要配置数据库连接 |

---

## 6. 相关技能推荐

### 测试开发

- **test-driven-development** (superpowers) - TDD 开发流程
- **test-fixing** - 测试修复技能
- **pypict-claude-skill** - PICT 组合测试

### 代码质量

- **software-architecture** - 软件架构设计
- **subagent-driven-development** - 子代理开发模式
- **prompt-engineering** - 提示工程

---

## 📎 相关链接

- [read-only-postgres GitHub](https://github.com/jawwadfirdousi/agent-skills)
- [postgres 技能](https://github.com/sanjay3290/ai-skills)
- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
- [awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills)

---

*持续更新中...*
