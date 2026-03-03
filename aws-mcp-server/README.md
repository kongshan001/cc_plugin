# AWS MCP Server - Claude Code AWS 集成

## 📋 文档信息

- **插件名称**: AWS MCP Server
- **GitHub**: [alexei-led/aws-mcp-server](https://github.com/alexei-led/aws-mcp-server)
- **Star**: ⭐ (活跃维护)
- **状态**: ✅ 已调研
- **调研日期**: 2026-03-04
- **分类**: MCP Server / 云服务集成 / AWS

---

## 1. 插件背景需求

### 问题痛点

- AWS 服务众多，配置复杂
- 本地开发需要手动管理 AWS 凭证
- 缺乏与 Claude Code 的深度集成
- 安全凭证管理困难

### 目标

AWS MCP Server 是一个**模型上下文协议 (MCP) 服务器**，为 Claude Code 提供 AWS 服务集成能力。通过 MCP 协议，可以直接在 Claude Code 中操作 AWS 资源，无需复杂的本地配置。

---

## 2. 设计方案

### 核心架构

```
┌─────────────────────────────────────────────────────────────────┐
│                    AWS MCP Server 架构                           │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│   ┌─────────────┐   ┌─────────────┐   ┌─────────────┐        │
│   │ Claude Code │◄──│   MCP       │◄──│    AWS      │        │
│   │   客户端    │   │   协议      │   │   服务      │        │
│   └─────────────┘   └──────┬──────┘   └─────────────┘        │
│                             │                                   │
│                             ▼                                   │
│                    ┌─────────────────┐                         │
│                    │  AWS MCP Server  │                         │
│                    │  本地/远程运行   │                         │
│                    └─────────────────┘                         │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### 支持的 AWS 服务

| 服务类别 | 支持的服务 |
|---------|----------|
| **计算** | EC2, Lambda, ECS, EKS |
| **存储** | S3, EFS, EBS |
| **数据库** | RDS, DynamoDB, ElastiCache |
| **网络** | VPC, ELB, CloudFront, Route53 |
| **无服务器** | API Gateway, Step Functions |
| **监控** | CloudWatch |
| **部署** | CodeDeploy, CodePipeline |

### MCP 工具

```markdown
### 可用工具
- aws_ec2_*: EC2 实例管理
- aws_s3_*: S3 存储操作
- aws_lambda_*: Lambda 函数管理
- aws_ecs_*: ECS 容器服务
- aws_rds_*: RDS 数据库
- aws_iam_*: IAM 权限管理
- aws_logs_*: CloudWatch 日志
```

---

## 3. 本地部署

### 前置要求

| 要求 | 说明 |
|-----|------|
| **Node.js** | 18+ |
| **AWS 凭证** | AWS_ACCESS_KEY_ID, AWS_SECRET_ACCESS_KEY |
| **AWS CLI** | 可选，建议安装 |

### 安装步骤

#### 方式 1: npm 全局安装

```bash
# 1. 安装
npm install -g @modelcontextprotocol/server-aws

# 2. 配置环境变量
export AWS_ACCESS_KEY_ID=your_key_id
export AWS_SECRET_ACCESS_KEY=your_secret_key
export AWS_REGION=us-east-1

# 3. 启动服务器
npx @modelcontextprotocol/server-aws
```

#### 方式 2: Docker 部署

```bash
# 1. 拉取镜像
docker pull alexeiled/aws-mcp-server

# 2. 运行容器
docker run -d \
  -e AWS_ACCESS_KEY_ID=your_key_id \
  -e AWS_SECRET_ACCESS_KEY=your_secret_key \
  -e AWS_REGION=us-east-1 \
  -p 3000:3000 \
  alexeiled/aws-mcp-server

# 3. 配置 MCP 客户端连接
# MCP_SERVER_URL=http://localhost:3000
```

#### 方式 3: 本地运行 + Claude Code 配置

```bash
# 1. 克隆仓库
git clone https://github.com/alexei-led/aws-mcp-server.git
cd aws-mcp-server

# 2. 安装依赖
npm install

# 3. 构建
npm run build

# 4. 配置 Claude Code
# 在 claude_settings.json 中添加:
{
  "mcpServers": {
    "aws": {
      "command": "node",
      "args": ["/path/to/aws-mcp-server/dist/index.js"],
      "env": {
        "AWS_ACCESS_KEY_ID": "your_key_id",
        "AWS_SECRET_ACCESS_KEY": "your_secret_key",
        "AWS_REGION": "us-east-1"
      }
    }
  }
}
```

---

## 4. 核心功能详解

### 4.1 EC2 实例管理

```markdown
### 可用操作
- 列出 EC2 实例
- 启动/停止实例
- 获取实例状态
- 查看实例信息

### 示例
"列出所有 EC2 实例"
"启动 my-server 实例"
"查看 t3.medium 实例状态"
```

### 4.2 S3 存储操作

```markdown
### 可用操作
- 列出 S3 桶
- 上传/下载文件
- 列出对象
- 创建桶

### 示例
"列出所有 S3 桶"
"上传 test.txt 到 my-bucket"
"列出 my-bucket 中的文件"
```

### 4.3 Lambda 函数管理

```markdown
### 可用操作
- 列出 Lambda 函数
- 调用函数
- 查看函数配置
- 更新函数代码

### 示例
"列出所有 Lambda 函数"
"调用 my-function 函数"
```

### 4.4 CloudWatch 日志

```markdown
### 可用操作
- 列出日志组
- 获取日志事件
- 搜索日志
- 创建日志流

### 示例
"查看 /aws/lambda/my-function 的日志"
"搜索错误日志"
```

---

## 5. 适用场景

### ✅ 适用场景

| 场景 | 说明 |
|------|------|
| **云资源管理** | 通过对话管理 AWS 资源 |
| **快速部署** | 快速部署应用到 AWS |
| **日志分析** | 查询和分析 CloudWatch 日志 |
| **故障排查** | 检查 EC2、Lambda 等服务状态 |
| **自动化运维** | 通过自然语言执行运维操作 |

### ⚠️ 注意事项

| 场景 | 说明 |
|------|------|
| 权限控制 | 确保 IAM 凭证权限最小化 |
| 成本控制 | 注意避免意外产生费用 |
| 安全凭证 | 不要提交凭证到 Git |

---

## 6. 优缺点分析

### ✅ 优点

| 优点 | 说明 |
|-----|------|
| **自然语言操作** | 用自然语言管理 AWS |
| **MCP 标准化** | 遵循 MCP 协议 |
| **多服务支持** | 支持多种 AWS 服务 |
| **本地/远程** | 支持多种部署方式 |

### ❌ 缺点

| 缺点 | 说明 |
|-----|------|
| **学习成本** | 需要了解 AWS 服务 |
| **凭证安全** | 凭证管理需要小心 |
| **功能限制** | 不覆盖所有 AWS API |

---

## 7. 安全最佳实践

### 凭证管理

```markdown
### 推荐方式
1. 使用 IAM 角色 (推荐)
2. 使用环境变量
3. 使用 AWS SSO
4. 定期轮换凭证

### 不要
- 硬编码凭证
- 提交到 Git
- 使用 root 账户
```

### IAM 权限

```markdown
### 最小权限原则
- 只授予必需的权限
- 使用 IAM 策略条件
- 定期审查权限
- 使用服务角色

### 推荐策略
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": [
        "ec2:Describe*",
        "s3:ListBucket",
        "lambda:GetFunction"
      ],
      "Resource": "*"
    }
  ]
}
```

---

## 8. 落地过程

### 调研日期
2026-03-04

### 快速开始

```bash
# 1. 安装 AWS MCP Server
npm install -g @modelcontextprotocol/server-aws

# 2. 配置 AWS 凭证
export AWS_ACCESS_KEY_ID=AKIAIOSFODNN7EXAMPLE
export AWS_SECRET_ACCESS_KEY=wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY
export AWS_REGION=us-east-1

# 3. 启动服务器
npx @modelcontextprotocol/server-aws

# 4. 在 Claude Code 中使用
# "列出所有 EC2 实例"
```

### 验证结果

| 验证项 | 结果 |
|-------|------|
| 仓库可访问 | ✅ |
| npm 包可用 | ✅ |
| 文档完整性 | ✅ |
| AWS 服务覆盖 | ✅ |

---

## 9. 与 game-frame-sync 结合

### 云端部署场景

```markdown
### 部署场景
1. 后端服务部署到 EC2/Lambda
2. 静态资源部署到 S3 + CloudFront
3. 数据库使用 RDS
4. 日志分析使用 CloudWatch

### 示例命令
"部署 game-frame-sync 后端到 EC2"
"将静态资源上传到 S3"
"查看后端服务的日志"
```

---

## 📎 相关链接

- [GitHub](https://github.com/alexei-led/aws-mcp-server)
- [AWS 文档](https://aws.amazon.com/documentation/)
- [MCP 协议](https://modelcontextprotocol.io/)
- [IAM 最佳实践](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html)

---

*用自然语言管理 AWS 资源* ☁️
