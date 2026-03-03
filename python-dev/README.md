# Claude Code Python 开发技能补充调研

## 📋 文档信息

- **调研日期**: 2026-03-03
- **分类**: Python 开发 / 云服务 / AI 框架
- **状态**: ✅ 补充调研

---

## 1. Python Web 框架技能

### 1.1 Django/Flask/FastAPI

| 项目 | 说明 |
|-----|------|
| **来源** | awesome-claude-code 技能库 |
| **特点** | Python Web 开发完整支持 |

### 核心功能

- **项目初始化**: Django/Flask/FastAPI 项目创建
- **ORM 操作**: 数据库模型定义和查询
- **API 开发**: RESTful API 设计
- **认证系统**: 用户认证和授权
- **测试支持**: 单元测试和集成测试

### 适用场景

- Web 应用开发
- API 服务开发
- 微服务架构

---

## 2. AWS 云服务集成

### 2.1 AWS MCP Server

| 项目 | 说明 |
|-----|------|
| **GitHub** | [alexei-led/aws-mcp-server](https://github.com/alexei-led/aws-mcp-server) |
| **Star** | ⭐ 活跃 |
| **语言** | Python |
| **特点** | AWS CLI 集成，多环境支持 |

### 核心功能

- **多环境配置**: 多种 Python 环境选项
- **代码规范**: 详细的代码风格指南
- **错误处理**: 全面的错误处理建议
- **安全考虑**: AWS CLI 安全最佳实践

### 支持的服务

| 服务类别 | 支持内容 |
|---------|---------|
| **计算** | EC2, Lambda, ECS, EKS |
| **存储** | S3, EBS, EFS |
| **数据库** | RDS, DynamoDB, ElastiCache |
| **网络** | VPC, CloudFront, Route53 |
| **安全** | IAM, Secrets Manager |

---

## 3. Pydantic AI 深度集成

### 3.1 pydantic-ai-skills

| 项目 | 说明 |
|-----|------|
| **GitHub** | [DougTrajano/pydantic-ai-skills](https://github.com/DougTrajano/pydantic-ai-skills) |
| **Star** | ⭐ 136 |
| **语言** | Python |
| **特点** | Agent Skills 支持 Pydantic AI |

### 核心功能

- **类型安全**: Pydantic 模型强制类型检查
- **渐进式提示**: 按需披露信息
- **AI 集成**: 与主流 LLM 无缝集成
- **验证系统**: 内置强大的数据验证

### 适用场景

- AI 应用开发
- 类型安全 API 构建
- LLM 应用集成
- 数据验证管道

---

## 4. PostgreSQL 数据库技能

### 4.1 read-only-postgres

| 项目 | 说明 |
|-----|------|
| **GitHub** | [jawwadfirdousi/agent-skills](https://github.com/jawwadfirdousi/agent-skills) |
| **功能** | PostgreSQL 只读查询技能 |
| **特点** | 安全优先的数据库查询 |

### 核心功能

- **只读查询**: 仅支持 SELECT/SHOW/EXPLAIN/WITH
- **多连接支持**: 配置多个数据库连接
- **安全验证**: 严格的验证机制
- **超时控制**: 防止长时间查询
- **行数限制**: 防止大规模数据泄露

### 支持的查询类型

```sql
-- SELECT 查询
SELECT * FROM users WHERE id = 1;

-- SHOW 命令
SHOW max_connections;

-- EXPLAIN 分析
EXPLAIN ANALYZE SELECT * FROM orders;

-- WITH 公共表表达式
WITH recent_orders AS (
    SELECT * FROM orders WHERE created_at > NOW() - INTERVAL '7 days'
)
SELECT * FROM recent_orders;
```

### 4.2 postgres

| 项目 | 说明 |
|-----|------|
| **GitHub** | [sanjay3290/ai-skills](https://github.com/sanjay3290/ai-skills) |
| **功能** | PostgreSQL 完整集成 |
| **特点** | 多连接支持 + 防御性安全 |

---

## 5. 语音转文字集成

### 5.1 stt-mcp-server-linux

| 项目 | 说明 |
|-----|------|
| **GitHub** | [marcindulak/stt-mcp-server-linux](https://github.com/marcindulak/stt-mcp-server-linux) |
| **语言** | Python |
| **特点** | 本地语音转文字，无需外部 API |

### 核心功能

- **本地运行**: 完全本地化的语音识别
- **Docker 部署**: 容器化部署
- **Tmux 集成**: 与 Claude Code 无缝集成
- **隐私保护**: 语音数据不离开本地

### 技术架构

```
麦克风 → 语音录制 → STT MCP Server → 文本 → Claude Code
```

---

## 6. Python 测试开发

### 6.1 test-driven-development

| 项目 | 说明 |
|-----|------|
| **来源** | superpowers 技能集 |
| **功能** | TDD 开发流程 |
| **特点** | 红色-绿色-重构 |

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

### 6.2 测试修复技能

| 技能 | 功能 |
|-----|------|
| **test-fixing** | 测试修复 |
| **test-writing** | 测试编写 |
| **test-running** | 测试运行 |
| **bug-finding** | Bug 查找 |

---

## 7. 开发者工具包

### 7.1 Developer Kit

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
- **自动化**: 开发工作流自动化

### 7.2 Claude Code Tools

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

### 7.3 Claudekit

| 项目 | 说明 |
|-----|------|
| **GitHub** | [carlrannaberg/claudekit](https://github.com/carlrannaberg/claudekit) |
| **功能** | CLI 工具包 |
| **子代理数量** | 20+ |

### 子代理列表

| 代理名称 | 功能 |
|---------|------|
| oracle | GPT-5 集成 |
| code-reviewer | 6 方面深度分析 |
| typescript-expert | TypeScript 专家 |
| ai-sdk-expert | Vercel AI SDK |

---

## 8. Python 开发技能汇总

| 技能名称 | 功能 | 适用场景 |
|---------|------|---------|
| **read-only-postgres** | PostgreSQL 只读查询 | 数据库调试/分析 |
| **postgres** | PostgreSQL 完整集成 | 生产数据库操作 |
| **pydantic-ai-skills** | Pydantic AI 集成 | AI 应用开发 |
| **aws-mcp-server** | AWS 云服务集成 | 云端开发部署 |
| **stt-mcp-server-linux** | 语音转文字 | 语音交互 |
| **developer-kit** | 开发者工具包 | 项目快速启动 |
| **claude-code-tools** | 会话连续性 | 复杂项目开发 |
| **test-driven-development** | TDD 开发流程 | 规范开发 |

---

## 9. 部署指南

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

### 安装 AWS MCP Server

```bash
# 克隆仓库
git clone https://github.com/alexei-led/aws-mcp-server.git

# 安装依赖
pip install -r requirements.txt

# 配置 AWS 凭证
aws configure
```

### 安装语音转文字服务

```bash
# 克隆仓库
git clone https://github.com/marcindulak/stt-mcp-server-linux.git

# 使用 Docker 运行
cd stt-mcp-server-linux
docker-compose up -d
```

---

## 10. 优缺点分析

### ✅ 优点

| 优点 | 说明 |
|-----|------|
| **数据库安全** | 只读查询防止意外修改 |
| **类型安全** | Pydantic 集成保证类型正确 |
| **多平台支持** | 覆盖 Python/AWS/数据库 |
| **工具链完整** | 从开发到测试全覆盖 |
| **云服务集成** | AWS 完整支持 |
| **语音支持** | 本地语音转文字 |

### ❌ 缺点

| 缺点 | 说明 |
|-----|------|
| **数据库限制** | 主要支持 PostgreSQL |
| **环境依赖** | 部分需要额外配置 |
| **学习成本** | 需要了解各技能用法 |
| **版本兼容** | Python 版本兼容性 |

---

## 11. 相关技能推荐

### 测试开发

- **test-driven-development** (superpowers) - TDD 开发流程
- **test-fixing** - 测试修复技能
- **test-writing** - 测试编写

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
- [AWS MCP Server](https://github.com/alexei-led/aws-mcp-server)
- [stt-mcp-server-linux](https://github.com/marcindulak/stt-mcp-server-linux)
- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
- [awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills)

---

*持续更新中...*
