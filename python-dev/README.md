# Claude Code Python 开发插件调研

## 📋 文档信息

- **调研日期**: 2026-03-03
- **分类**: Python 开发 / 数据库 / AI 集成
- **状态**: ✅ 已调研

---

## 1. 数据库相关技能

### 1.1 read-only-postgres

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

### 1.2 postgres

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

## 2. Pydantic AI 集成

### 2.1 Pydantic AI Skills

| 项目 | 说明 |
|-----|------|
| **GitHub** | [DougTrajano/pydantic-ai-skills](https://github.com/DougTrajano/pydantic-ai-skills) |
| **Star** | ⭐ 136 |
| **语言** | Python |
| **特点** | Agent Skills 支持 Pydantic AI，渐进式提示 |

### 核心功能

- **文件系统支持**: 文件操作技能
- **Web 搜索**: 网络搜索能力
- **渐进式提示**: 按需披露信息
- **类型安全**: Pydantic 模型集成

### 适用场景

- AI 应用开发
- 类型安全 API 构建
- LLM 应用集成

---

## 3. Python 测试开发

### 3.1 test-driven-development

| 项目 | 说明 |
|-----|------|
| **来源** | superpowers 技能集 |
| **功能** | TDD 开发流程 |
| **特点** | 测试先行，红色-绿色-重构 |

### 核心流程

```
1. 编写失败测试 (红色)
2. 实现功能通过测试 (绿色)
3. 重构代码 (重构)
```

### 适用场景

- 规范开发
- 回归测试保证
- 代码质量提升

---

### 3.2 pypict-claude-skill

| 项目 | 说明 |
|-----|------|
| **功能** | PICT 测试用例生成 |
| **用途** | 组合测试 |
| **场景** | 参数组合测试 |

### 核心功能

- Pairwise 测试生成
- 参数组合优化
- 测试用例精简

---

## 4. 开发者工具包

### 4.1 Developer Kit

| 项目 | 说明 |
|-----|------|
| **GitHub** | [giuseppe-trisciuoglio/developer-kit](https://github.com/giuseppe-trisciuoglio/developer-kit) |
| **Star** | ⭐ 128 |
| **语言** | Python |
| **特点** | Claude Code 模块化插件系统 |

### 包含内容

- **Skills**: 可复用技能
- **Agents**: 自动化代理
- **Commands**: 快捷命令
- **自动化**: 开发工作流自动化 |

### 适用场景

- 项目快速启动
- 团队协作标准化
- 开发流程自动化

---

### 4.2 Claude Code Tools

| 项目 | 说明 |
|-----|------|
| **GitHub** | [pchalasani/claude-code-tools](https://github.com/pchalasani/claude-code-tools) |
| **功能** | 会话连续性工具集 |
| **特点** | 跨会话上下文恢复 |

### 核心功能

- **会话保持**: 避免上下文压缩
- **跨代理切换**: Claude Code ↔ Codex CLI
- **全文搜索**: Rust/Tantivy 全文索引
- **TMux 集成**: 终端会话管理

### 技术特点

```
- Rust + Tantivy 全文搜索
- TUI 界面
- 快速检索
- 零配置
```

---

### 4.3 Claudekit

| 项目 | 说明 |
|-----|------|
| **GitHub** | [carlrannaberg/claudekit](https://github.com/carlrannaberg/claudekit) |
| **功能** | CLI 工具包 |

### 核心功能

- **自动保存**: Checkpointing
- **代码质量**: Quality hooks
- **规范生成**: Specification generation
- **20+ 子代理**: 专业代理配置

### 子代理列表

| 代理名称 | 功能 |
|---------|------|
| oracle | GPT-5 集成 |
| code-reviewer | 6 方面深度分析 |
| typescript-expert | TypeScript 专家 |
| ai-sdk-expert | Vercel AI SDK |

---

## 5. iOS 开发 (Python 工具链)

### 5.1 iOS Simulator Skill

| 项目 | 说明 |
|-----|------|
| **GitHub** | [conorluddy/ios-simulator-skill](https://github.com/conorluddy/ios-simulator-skill) |
| **Star** | ⭐ 557 |
| **语言** | Python |
| **功能** | iOS 模拟器集成 |

### 核心功能

- 构建 iOS 应用
- 运行模拟器
- 应用交互
- 零配置使用

### 适用场景

- iOS 应用开发
- 移动端测试
- Swift 项目开发

---

## 6. Python 开发技能汇总

| 技能名称 | 功能 | 适用场景 |
|---------|------|---------|
| **read-only-postgres** | PostgreSQL 只读查询 | 数据库调试/分析 |
| **postgres** | PostgreSQL 完整集成 | 生产数据库操作 |
| **pydantic-ai-skills** | Pydantic AI 集成 | AI 应用开发 |
| **developer-kit** | 开发者工具包 | 项目快速启动 |
| **claude-code-tools** | 会话连续性 | 复杂项目开发 |
| **test-driven-development** | TDD 开发流程 | 规范开发 |
| **ios-simulator-skill** | iOS 模拟器 | iOS 开发 |

---

## 7. 部署指南

### 安装 PostgreSQL 技能

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
# 配置环境变量
export POSTGRES_HOST=localhost
export POSTGRES_USER=your_user
export POSTGRES_PASSWORD=your_password
export POSTGRES_DATABASE=your_db
```

### 安装 Pydantic AI 技能

```bash
# 克隆仓库
git clone https://github.com/DougTrajano/pydantic-ai-skills.git

# 安装依赖
pip install -r requirements.txt

# 复制技能
cp -r pydantic-ai-skills ~/.claude/skills/
```

### 安装 iOS Simulator 技能

```bash
# 安装技能
claude --install-skill gh-conorluddy-ios-simulator-skill

# 或手动安装
git clone https://github.com/conorluddy/ios-simulator-skill.git
cp -r ios-simulator-skill ~/.claude/skills/
```

---

## 8. 优缺点分析

### ✅ 优点

| 优点 | 说明 |
|-----|------|
| **数据库安全** | 只读查询防止意外修改 |
| **类型安全** | Pydantic 集成保证类型正确 |
| **多平台支持** | 覆盖 Python/iOS/数据库 |
| **工具链完整** | 从开发到测试全覆盖 |
| **社区活跃** | 部分技能 Star 较高 |

### ❌ 缺点

| 缺点 | 说明 |
|-----|------|
| **数据库限制** | 主要支持 PostgreSQL |
| **环境依赖** | 部分需要额外配置 |
| **学习成本** | 需要了解各技能用法 |
| **版本兼容** | Python 版本兼容性 |

---

## 9. 相关技能推荐

### 测试开发

- **test-driven-development** (superpowers) - TDD 开发流程
- **test-fixing** - 测试修复技能
- **pypict-claude-skill** - PICT 组合测试

### 代码质量

- **software-architecture** - 软件架构设计
- **subagent-driven-development** - 子代理开发模式
- **prompt-engineering** - 提示工程

### AI 集成

- **pydantic-ai-skills** - Pydantic AI
- **ai-sdk-expert** (claudekit) - Vercel AI SDK

---

## 📎 相关链接

- [read-only-postgres GitHub](https://github.com/jawwadfirdousi/agent-skills)
- [postgres 技能](https://github.com/sanjay3290/ai-skills)
- [Pydantic AI Skills](https://github.com/DougTrajano/pydantic-ai-skills)
- [iOS Simulator Skill](https://github.com/conorluddy/ios-simulator-skill)
- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
- [awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills)

---

*持续更新中...*
