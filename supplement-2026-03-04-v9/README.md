# Claude Code 插件调研报告 - 补充调研第九期

> 持续跟踪 Claude Code 生态热门插件，聚焦游戏开发、Python 开发、自动化测试、开发者工具方向

---

## 📋 本期调研概要

| 维度 | 统计 |
|-----|------|
| **调研时间** | 2026-03-04 |
| **覆盖方向** | 游戏开发、Python开发、自动化测试、开发者工具 |
| **新增技能** | 50+ |
| **数据来源** | Antigravity Skills, awesome-claude-code |

---

## 一、MCP 服务器与开发者工具 (新增重点)

### 1.1 MCP Builder 系列

| 技能ID | 名称 | 核心能力 | 评分 |
|----------|------|---------|------|
| **mcp-builder** | MCP 服务器构建 | 创建高质量 MCP 服务器 | ⭐⭐⭐⭐ |
| **mcp-builder-ms** | MCP 服务器构建 (微软版) | 微软生态 MCP 服务器 | ⭐⭐⭐⭐ |

#### MCP (Model Context Protocol) 概述

MCP 是一种开放协议，用于将 AI 模型与外部服务和工具连接。通过 MCP 服务器，Claude Code 可以：

- 访问文件系统
- 执行 shell 命令
- 集成第三方 API
- 操作数据库
- 控制浏览器

#### MCP Builder 核心能力

```markdown
## MCP 服务器设计原则

1. **工具定义**: 清晰的工具 schema
   - name: 工具名称
   - description: 功能描述
   - inputSchema: 参数规范

2. **错误处理**: 健壮的异常处理
   - 优雅降级
   - 清晰错误消息
   - 重试机制

3. **安全性**: 
   - 输入验证
   - 权限控制
   - 审计日志
```

### 1.2 Agent Memory MCP

| 项目 | 说明 |
|-----|------|
| **技能ID** | agent-memory-mcp |
| **功能** | 混合记忆系统，为 AI 代理提供持久化、可搜索的知识管理 |
| **用途** | 架构、模式、决策的知识管理 |

#### 核心能力

- **持久化存储**: 长期记忆保存
- **语义搜索**: 基于向量的知识检索
- **上下文管理**: 自动上下文注入
- **多模态支持**: 文本、代码、文档

### 1.3 AWS 开发者工具系列

| 技能ID | 名称 | 核心能力 |
|--------|------|----------|
| **aws-skills** | AWS 开发 | 基础设施自动化、云架构模式 |
| **aws-serverless** | AWS 无服务器 | Lambda、API Gateway、DynamoDB |
| **aws-cost-optimizer** | AWS 成本优化 | 成本分析、优化建议 |
| **aws-cost-cleanup** | AWS 成本清理 | 自动清理未使用资源 |

#### AWS Serverless 开发模式

```yaml
# SAM 模板示例
AWSTemplateFormatVersion: '2010-09-09'
Transform: AWS::Serverless-2016-10-31

Resources:
  GameFrameSyncFunction:
    Type: AWS::Serverless::Function
    Properties:
      Handler: index.handler
      Runtime: python3.12
      Events:
        Api:
          Type: Api
          Properties:
            Path: /game/{room_id}
            Method: ANY
```

#### AWS 成本优化最佳实践

| 策略 | 说明 | 节省比例 |
|------|------|---------|
| **Reserved Instances** | 预付费实例 | 30-60% |
| **Spot Instances** | 竞价实例 | 60-90% |
| **Lambda 优化** | 内存/超时调优 | 20-40% |
| **S3 智能分层** | 自动存储分层 | 40-60% |

### 1.4 Azure AI 系列

| 技能ID | 名称 | 核心能力 |
|--------|------|----------|
| **azure-ai-projects-py** | Azure AI Projects | AI Foundry 项目管理 |
| **azure-ai-openai-dotnet** | Azure OpenAI | OpenAI API 集成 |
| **azure-ai-document-intelligence** | 文档智能 | OCR、表单识别 |
| **azure-ai-ml-py** | Azure ML | 机器学习工作流 |

---

## 二、自动化测试深入分析

### 2.1 Playwright 测试矩阵

| 技能ID | 名称 | 核心能力 | 评分 |
|----------|------|---------|------|
| **e2e-testing** | E2E 测试工作流 | Playwright 完整流程 | ⭐⭐⭐⭐⭐ |
| **e2e-testing-patterns** | E2E 测试模式 | 可靠测试套件构建 | ⭐⭐⭐⭐⭐ |
| **browser-automation** | 浏览器自动化 | 等待策略、选择器 | ⭐⭐⭐⭐⭐ |
| **azure-microsoft-playwright-testing-ts** | Azure Playwright | 云端大规模测试 | ⭐⭐⭐⭐ |

#### Playwright 最佳实践

```typescript
// 1. 智能等待
await page.waitForSelector('[data-testid="game-room"]', { 
  state: 'visible',
  timeout: 30000,
  timeoutFn: () => checkGameLoaded()
});

// 2. 测试隔离
test.describe('Game Room', () => {
  let roomId: string;
  
  test.beforeEach(async () => {
    roomId = await createTestRoom();
  });
  
  test.afterEach(async () => {
    await cleanupRoom(roomId);
  });
});

// 3. API Mock
await page.route('**/api/game/*', route => {
  if (route.request().url().includes('/game/state')) {
    route.fulfill({
      json: mockGameState
    });
  } else {
    route.continue();
  }
});
```

### 2.2 API 测试与安全

| 技能ID | 名称 | 核心能力 |
|--------|------|----------|
| **api-security-testing** | API 安全测试 | 认证、授权、限流 |
| **api-testing-observability-api-mock** | API Mock | 模拟真实 API 行为 |
| **burp-suite-testing** | Burp Suite | Web 渗透测试 |

#### API 安全测试清单

```markdown
## 认证测试
- [ ] JWT 无签名验证
- [ ] 弱密码策略
- [ ] 会话管理
- [ ] OAuth 2.0 漏洞

## 授权测试
- [ ] 水平越权
- [ ] 垂直越权
- [ ] IDOR
- [ ] 批量分配

## 输入验证
- [ ] SQL 注入
- [ ] XSS
- [ ] 命令注入
- [ ] 路径遍历
```

### 2.3 游戏客户端测试专题

#### Unity Test Framework 进阶

| 测试类型 | 运行环境 | 适用场景 |
|----------|----------|----------|
| **Edit Mode** | 编辑器 | 纯逻辑单元测试 |
| **Play Mode** | 运行时 | 集成测试、UI 测试 |

```csharp
// 帧同步确定性测试
[Test]
public void FrameSync_Deterministic_Verification()
{
    // 准备：创建相同初始状态
    var state1 = CreateInitialGameState();
    var state2 = CreateInitialGameState();
    
    // 给定：相同输入序列
    var inputs = GenerateInputSequence(100);
    
    // 执行：执行帧逻辑
    ExecuteFrameSequence(state1, inputs);
    ExecuteFrameSequence(state2, inputs);
    
    // 验证：状态完全一致
    Assert.AreEqual(state1.PlayerPosition, state2.PlayerPosition);
    Assert.AreEqual(state1.Health, state2.Health);
    Assert.AreEqual(state1.Score, state2.Score);
}

// 网络延迟模拟测试
[UnityTest]
public IEnumerator NetworkLatency_Simulation()
{
    var networkSim = new NetworkSimulation();
    
    // 模拟 200ms 延迟
    networkSim.SetLatency(200);
    networkSim.SetJitter(50);
    networkSim.SetPacketLoss(0.05f);
    
    var player = new GameObject("Player");
    var networkComponent = player.AddComponent<NetworkComponent>();
    
    networkComponent.Connect("ws://game-server");
    yield return new WaitForSeconds(1);
    
    // 验证重连机制
    networkSim.Disconnect();
    yield return new WaitForSeconds(0.5f);
    networkSim.Reconnect();
    
    Assert.IsTrue(networkComponent.IsConnected);
}
```

### 2.4 测试工具矩阵

| 工具 | 语言 | 适用场景 | 特点 |
|------|------|----------|------|
| **Playwright** | TypeScript | E2E、Web 测试 | 跨浏览器、自动等待 |
| **Cypress** | JavaScript | E2E 测试 | 简单易用、实时重载 |
| **Pytest** | Python | API/单元测试 | 丰富插件、参数化 |
| **Jest** | JavaScript | 单元/集成测试 | 快照测试、Mock |
| **Unity Test Framework** | C# | 游戏客户端测试 | Edit Mode/Play Mode |

---

## 三、Python 开发进阶

### 3.1 FastAPI 生态

| 技能ID | 名称 | 核心能力 |
|--------|------|----------|
| **fastapi-pro** | FastAPI 专家 | 高性能异步 API |
| **fastapi-templates** | FastAPI 模板 | 生产级项目脚手架 |
| **fastapi-router-py** | FastAPI 路由 | CRUD 操作最佳实践 |

#### FastAPI 生产级架构

```python
# 项目结构
project/
├── app/
│   ├── __init__.py
│   ├── main.py              # 应用入口
│   ├── api/
│   │   ├── v1/
│   │   │   ├── endpoints/
│   │   │   │   ├── game.py
│   │   │   │   └── room.py
│   │   │   └── router.py
│   │   └── dependencies.py
│   ├── core/
│   │   ├── config.py
│   │   ├── security.py
│   │   └── database.py
│   ├── models/
│   │   ├── domain/
│   │   └── schemas/
│   ├── services/
│   │   ├── game_service.py
│   │   └── room_service.py
│   └── utils/
├── tests/
├── pyproject.toml
└── uv.lock

# main.py 示例
from fastapi import FastAPI
from fastapi.middleware.cors import CORSMiddleware
from contextlib import asynccontextmanager

@asynccontextmanager
async def lifespan(app: FastAPI):
    # 启动时
    await database.connect()
    await cache.connect()
    yield
    # 关闭时
    await cache.disconnect()
    await database.disconnect()

app = FastAPI(
    title="Game Frame Sync API",
    version="1.0.0",
    lifespan=lifespan
)

app.add_middleware(
    CORSMiddleware,
    allow_origins=["*"],
    allow_credentials=True,
)
```

### 3.2 异步 Python 模式

| 技能ID | 名称 | 核心能力 |
|--------|------|----------|
| **async-python-patterns** | 异步编程 | asyncio、高并发模式 |
| **python-performance-optimization** | 性能优化 | Profiling、最佳实践 |

#### 异步模式详解

```python
# 1. 信号量限流
async def api_call_with_limit(url: str, semaphore: asyncio.Semaphore):
    async with semaphore:
        async with aiohttp.ClientSession() as session:
            async with session.get(url) as response:
                return await response.json()

# 使用
semaphore = asyncio.Semaphore(10)  # 最多 10 个并发
tasks = [api_call_with_limit(url, semaphore) for url in urls]
results = await asyncio.gather(*tasks)

# 2. 错误重试与超时
async def retry_with_timeout(func, max_retries=3, timeout=30):
    for attempt in range(max_retries):
        try:
            return await asyncio.wait_for(func(), timeout=timeout)
        except asyncio.TimeoutError:
            if attempt == max_retries - 1:
                raise
            await asyncio.sleep(2 ** attempt)
        except Exception as e:
            if attempt == max_retries - 1:
                raise
            await asyncio.sleep(2 ** attempt)

# 3. 异步生成器流式处理
async def game_event_stream():
    """游戏事件流处理器"""
    queue = asyncio.Queue(maxsize=1000)
    
    async def producer():
        async for event in game_event_source():
            await queue.put(event)
    
    async def consumer():
        while True:
            event = await queue.get()
            await process_game_event(event)
    
    await asyncio.gather(producer(), consumer())
```

### 3.3 工作流编排

| 技能ID | 名称 | 核心能力 |
|--------|------|----------|
| **dbos-python** | DBOS 工作流 | 持久化工作流、容错 |
| **temporal-python-pro** | Temporal 工作流 | 分布式事务、Saga 模式 |
| **temporal-python-testing** | Temporal 测试 | 时间跳过、Mock |

#### Temporal 工作流示例

```python
from temporalio import workflow
from datetime import timedelta

@workflow.defn
class GameMatchWorkflow:
    @workflow.run
    async def run(self, match_id: str) -> MatchResult:
        # 1. 创建比赛
        match = await workflow.execute_activity(
            create_match,
            match_id,
            start_to_close_timeout=timedelta(seconds=30)
        )
        
        # 2. 等待玩家加入 (带超时)
        try:
            await workflow.wait_for_condition(
                lambda: len(match.players) >= match.min_players,
                timeout=timedelta(minutes=5)
            )
        except asyncio.TimeoutError:
            # 超时取消
            await workflow.execute_activity(
                cancel_match,
                match_id,
                start_to_close_timeout=timedelta(seconds=10)
            )
            return MatchResult(status="cancelled")
        
        # 3. 开始游戏 (Saga 模式)
        try:
            await workflow.execute_activity(
                start_game,
                match_id,
                start_to_close_timeout=timedelta(seconds=30)
            )
            
            # 4. 等待游戏结束
            result = await workflow.wait_for_condition(
                lambda: match.is_finished,
                timeout=timedelta(hours=2)
            )
            
            return MatchResult(status="completed", result=result)
            
        except Exception as e:
            # Saga 补偿
            await workflow.execute_activity(
                refund_players,
                match_id,
                start_to_close_timeout=timedelta(seconds=30)
            )
            raise
```

---

## 四、游戏开发技能汇总

### 4.1 引擎特定技能

| 技能ID | 引擎 | 核心能力 | 评分 |
|----------|------|---------|------|
| **unity-developer** | Unity 6 LTS | URP/HDRP、跨平台 | ⭐⭐⭐⭐⭐ |
| **unity-ecs-patterns** | Unity DOTS | ECS、Jobs、Burst | ⭐⭐⭐⭐⭐ |
| **unreal-engine-cpp-pro** | Unreal 5 | C++、网络同步 | ⭐⭐⭐⭐⭐ |
| **godot-gdscript-patterns** | Godot 4 | GDScript 2.0 | ⭐⭐⭐⭐ |
| **godot-4-migration** | Godot 4 | 迁移指南 | ⭐⭐⭐⭐ |

### 4.2 游戏类型开发

| 技能ID | 游戏类型 | 核心能力 |
|--------|----------|----------|
| **2d-games** | 2D 游戏 | 精灵、瓦片地图、物理 |
| **3d-games** | 3D 游戏 | 渲染、着色器、相机 |
| **mobile-games** | 移动游戏 | 触控、性能优化 |
| **pc-games** | PC/主机游戏 | 平台特性、优化 |
| **web-games** | Web 游戏 | WebGPU、PWA |

### 4.3 游戏开发支持

| 技能ID | 名称 | 核心能力 |
|--------|------|----------|
| **game-design** | 游戏设计 | GDD、平衡、玩家心理 |
| **game-art** | 游戏美术 | 视觉风格、资源管线 |
| **game-audio** | 游戏音频 | 音效设计、适应性音频 |
| **game-development** | 游戏开发编排 | 自动路由到相关技能 |

---

## 五、推荐 Skills 组合

### 5.1 游戏后端开发组合

```
推荐: /python-pro + /fastapi-pro + /async-python-patterns
     /temporal-python-pro + /temporal-python-testing (游戏状态管理)
     /aws-serverless + /aws-cost-optimizer (成本优化)
     /e2e-testing + /api-security-testing (API 测试)
```

### 5.2 游戏客户端开发组合

```
推荐: /unity-developer + /unity-ecs-patterns (性能优化)
     /godot-gdscript-patterns + /2d-games (2D 游戏)
     /unreal-engine-cpp-pro + /game-audio (UE5 开发)
```

### 5.3 自动化测试组合

```
推荐: /e2e-testing + /e2e-testing-patterns (E2E 测试)
     /browser-automation + /api-security-testing (安全测试)
     /playwright-skill + /azure-microsoft-playwright-testing-ts (云端测试)
```

### 5.4 DevOps 组合

```
推荐: /aws-skills + /aws-serverless + /aws-cost-optimizer
     /mcp-builder + /mcp-builder-ms (MCP 服务器开发)
     /cicd-automation-workflow-automate + /changelog-automation
```

---

## 六、实战案例

### 案例: 游戏房间服务开发

```bash
# 1. 项目初始化
>> /python-pro 初始化项目，使用 uv 管理依赖

# 2. FastAPI 开发
>> /fastapi-pro 创建游戏房间管理 API
>> /fastapi-templates 使用模板快速启动

# 3. 异步处理
>> /async-python-patterns 实现高并发房间管理

# 4. 工作流编排 (可选)
>> /temporal-python-pro 实现游戏状态持久化

# 5. 测试
>> /python-testing-patterns 编写房间管理测试
>> /e2e-testing 使用 Playwright 测试 Web API

# 6. 部署
>> /aws-serverless 部署到 AWS Lambda
>> /aws-cost-optimizer 优化成本
```

### 案例: Unity ECS 游戏开发

```bash
# 1. 项目设置
>> /unity-developer 初始化 Unity 6 项目

# 2. ECS 架构
>> /unity-ecs-patterns 设计 ECS 架构

# 3. 性能优化
>> 使用 Jobs 和 Burst 编译优化

# 4. 测试
>> /playwright-skill (Web 管理后台测试)
```

---

## 七、安装指南

### 默认安装 (Antigravity)

```bash
npx antigravity-awesome-skills
```

### Claude Code

```bash
npx antigravity-awesome-skills --claude
```

### Gemini CLI

```bash
npx antigravity-awesome-skills --gemini
```

### Codex CLI

```bash
npx antigravity-awesome-skills --codex
```

---

## 八、使用方式

### Claude Code

```bash
>> /skill-name 帮助我...
```

### Gemini CLI/Codex CLI

```bash
Use @skill-name to help me...
```

---

## 九、相关资源

- [Antigravity Awesome Skills](https://github.com/sickn33/antigravity-awesome-skills)
- [MCP 官方文档](https://modelcontextprotocol.io/)
- [AWS Serverless](https://aws.amazon.com/serverless/)
- [Temporal Python SDK](https://docs.temporal.io/)
- [Playwright](https://playwright.dev/)
- [cc_plugin 仓库](https://github.com/kongshan001/cc_plugin)

---

**文档更新时间**: 2026-03-04
**Claude Code 插件调研 - 第九期**
