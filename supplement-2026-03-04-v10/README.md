# Claude Code 插件调研报告 - 补充调研第十二期

> 持续跟踪 Claude Code 生态热门插件，聚焦游戏开发、Python 开发、自动化测试、开发者工具方向

---

## 📋 本期调研概要

| 维度 | 统计 |
|-----|------|
| **调研时间** | 2026-03-04 |
| **覆盖方向** | 游戏开发、Python开发、自动化测试、开发者工具 |
| **新增技能** | 60+ |
| **数据来源** | Antigravity Skills (970+), awesome-claude-code |

---

## 一、游戏客户端开发技能 (更新)

### 1.1 Unity 全栈开发 (更新)

| 技能ID | 名称 | 核心能力 | 评分 |
|----------|------|---------|------|
| **unity-developer** | Unity 6 LTS 专家 | URP/HDRP、跨平台部署、渲染优化 | ⭐⭐⭐⭐⭐ |
| **unity-ecs-patterns** | Unity DOTS/ECS | ECS、Jobs、Burst 编译、性能优化 | ⭐⭐⭐⭐⭐ |

#### Unity 6 LTS 核心特性

```csharp
// Unity 6 新特性示例
public class GameLoopExample : MonoBehaviour
{
    // 使用 Unity 6 的更新系统
    void OnUpdate(float deltaTime)
    {
        // 确定性帧同步
        FrameSync.Update(deltaTime);
    }
    
    // 新的增量式 GC
    void Start()
    {
        GarbageCollector.GCMode = GarbageCollector.Mode.Enabled;
    }
}

// ECS 示例
public partial struct MovementSystem : ISystem
{
    [BurstCompile]
    public void OnUpdate(ref SystemState state)
    {
        float deltaTime = SystemAPI.Time.DeltaTime;
        
        foreach (var (transform, velocity) in 
                 SystemAPI.Query<RefRW<LocalTransform>, RefRO<Velocity>>())
        {
            transform.ValueRW.Position += velocity.ValueRO.Value * deltaTime;
        }
    }
}
```

### 1.2 Godot 游戏开发

| 技能ID | 名称 | 核心能力 | 评分 |
|----------|------|---------|------|
| **godot-gdscript-patterns** | Godot GDScript 2.0 | 节点系统、信号、动画 | ⭐⭐⭐⭐ |
| **godot-4-migration** | Godot 4 迁移 | 从 Godot 3 迁移指南 | ⭐⭐⭐⭐ |

#### Godot 4 核心模式

```gdscript
# Godot 4 GDScript 2.0 示例
extends Node

signal player_died

@export var speed: float = 300.0
@onready var animation_player: AnimationPlayer = $AnimationPlayer

func _physics_process(delta: float) -> void:
    var direction := Input.get_axis("move_left", "move_right")
    velocity.x = direction * speed
    move_and_slide()

# 信号连接
func _ready() -> void:
    player_died.connect(_on_player_died)

# 新特性: @export_group
@export_group("Player Stats")
@export var max_health: int = 100
@export var damage: int = 10
```

### 1.3 Unreal Engine C++ 开发

| 技能ID | 名称 | 核心能力 | 评分 |
|----------|------|---------|------|
| **unreal-engine-cpp-pro** | Unreal 5 C++ 专家 | 网络同步、角色控制器、UMG | ⭐⭐⭐⭐⭐ |

#### Unreal 5 核心架构

```cpp
// Unreal 5 角色控制器示例
#include "GameFramework/Character.h"
#include "Net/UnrealNetwork.h"

class AMyCharacter : public ACharacter
{
    GENERATED_BODY()

public:
    AMyCharacter();

protected:
    virtual void BeginPlay() override;
    virtual void Tick(float DeltaTime) override;
    virtual void GetLifetimeReplicatedProps(TArray<FLifetimeProperty>& OutLifetimeProps) const override;

public:
    // 移动组件
    UPROPERTY(VisibleAnywhere, BlueprintReadOnly)
    class UMyMovementComponent* MyMovementComp;

    // 网络同步属性
    UPROPERTY(Replicated)
    float CurrentHealth;

    // RPC 函数
    UFUNCTION(Server, Reliable)
    void ServerPerformAction(FVector ActionLocation);
    
    UFUNCTION(NetMulticast, Reliable)
    void MulticastOnActionPerformed(FVector Location);
};
```

### 1.4 游戏开发综合技能

| 技能ID | 名称 | 核心能力 |
|--------|------|----------|
| **game-development** | 游戏开发编排 | 自动路由到相关引擎技能 |

---

## 二、Python 开发技能 (更新)

### 2.1 Python Pro 深度更新

| 技能ID | 名称 | 核心能力 | 评分 |
|----------|------|---------|------|
| **python-pro** | Python 3.12+ 专家 | 现代特性、async、性能优化 | ⭐⭐⭐⭐⭐ |
| **python-patterns** | Python 设计模式 | GoF 模式实现 | ⭐⭐⭐⭐ |
| **python-testing-patterns** | Python 测试模式 | pytest、Mock、Fixtures | ⭐⭐⭐⭐⭐ |

#### Python 3.12+ 新特性

```python
# Python 3.12 特性示例
from typing import TypeVar, Generic
from dataclasses import dataclass
import asyncio

# 1. 改进的错误消息
# def foo(x: int) -> int:
#     return x + "hello"  # 精确的错误位置

# 2. 性能提升 (freelist, 更快的启动)
# 3. type parameter 语法 (PEP 695)
type MyList[T] = list[T]  # 新的类型别名语法

# 4. match statement (3.10+)
def handle_game_event(event: dict) -> str:
    match event:
        case {"type": "player_join", "name": str(name)}:
            return f"Player {name} joined"
        case {"type": "player_move", "position": [x, y]}:
            return f"Moved to ({x}, {y})"
        case _:
            return "Unknown event"

# 5. 异步模式
async def game_event_processor(events: list[dict]):
    """游戏事件流处理器"""
    async with asyncio.TaskGroup() as tg:
        for event in events:
            tg.create_task(process_event(event))

# 6. 性能优化
# 使用 __slots__ 减少内存
class GameObject:
    __slots__ = ['x', 'y', 'velocity']
    
    def __init__(self, x: float, y: float):
        self.x = x
        self.y = y
        self.velocity = (0, 0)
```

### 2.2 异步 Python 进阶

| 技能ID | 名称 | 核心能力 | 评分 |
|----------|------|---------|------|
| **async-python-patterns** | 异步编程模式 | asyncio、高并发、流处理 | ⭐⭐⭐⭐⭐ |

#### 异步模式详解

```python
# 1. 异步上下文管理器
class AsyncGameConnection:
    async def __aenter__(self):
        self.ws = await websockets.connect(self.uri)
        return self
    
    async def __aexit__(self, exc_type, exc_val, exc_tb):
        await self.ws.close()

# 使用
async with AsyncGameConnection("ws://game-server") as conn:
    await conn.send({"type": "join", "room": "room1"})

# 2. 异步生成器
async def game_event_stream(room_id: str):
    """游戏事件流"""
    while True:
        event = await get_next_event(room_id)
        yield event

# 使用
async for event in game_event_stream("room1"):
    await process_event(event)

# 3. 信号量限流
async def limited_api_call(semaphore: asyncio.Semaphore, url: str):
    async with semaphore:
        return await fetch(url)

# 4. 错误重试
async def retry_async(coro, max_retries=3, base_delay=1.0):
    for attempt in range(max_retries):
        try:
            return await coro
        except Exception as e:
            if attempt == max_retries - 1:
                raise
            await asyncio.sleep(base_delay * (2 ** attempt))
```

### 2.3 FastAPI 与 Web 开发

| 技能ID | 名称 | 核心能力 | 评分 |
|----------|------|---------|------|
| **python-fastapi-development** | FastAPI 开发 | 异步 API、依赖注入 | ⭐⭐⭐⭐⭐ |
| **python-development-python-scaffold** | 项目脚手架 | 项目初始化、最佳实践 | ⭐⭐⭐⭐ |

#### FastAPI 生产级示例

```python
from fastapi import FastAPI, Depends, HTTPException
from fastapi.middleware.cors import CORSMiddleware
from contextlib import asynccontextmanager
from pydantic import BaseModel, Field
from typing import Optional

# 1. 游戏房间模型
class GameRoom(BaseModel):
    id: str
    name: str
    max_players: int = Field(ge=2, le=100)
    status: str = "waiting"
    created_by: str

# 2. 应用生命周期
@asynccontextmanager
async def lifespan(app: FastAPI):
    # 启动
    await redis.connect()
    await db.connect()
    yield
    # 关闭
    await redis.disconnect()
    await db.disconnect()

app = FastAPI(title="Game API", lifespan=lifespan)

# 3. CORS 中间件
app.add_middleware(
    CORSMiddleware,
    allow_origins=["https://game.example.com"],
    allow_credentials=True,
)

# 4. 依赖注入
async def get_current_player(token: str = Depends(oauth2_scheme)):
    player = await validate_token(token)
    if not player:
        raise HTTPException(status_code=401)
    return player

# 5. WebSocket 路由
@app.websocket("/ws/room/{room_id}")
async def websocket_room(ws: WebSocket, room_id: str):
    await ws.accept()
    try:
        while True:
            data = await ws.receive_json()
            await handle_game_event(room_id, data)
    except WebSocketDisconnect:
        await cleanup_room(room_id)
```

### 2.4 工作流编排

| 技能ID | 名称 | 核心能力 | 评分 |
|----------|------|---------|------|
| **dbos-python** | DBOS 工作流 | 持久化、容错、工作流 | ⭐⭐⭐⭐ |
| **temporal-python-pro** | Temporal 工作流 | 分布式事务、Saga | ⭐⭐⭐⭐⭐ |
| **temporal-python-testing** | Temporal 测试 | 时间跳过、Mock | ⭐⭐⭐⭐ |

#### Temporal 工作流示例

```python
from temporalio import workflow
from temporalio.common import RetryPolicy

@workflow.defn
class GameMatchWorkflow:
    @workflow.run
    async def run(self, match_id: str) -> dict:
        # 重试策略
        retry_policy = RetryPolicy(
            initial_interval_seconds=1,
            maximum_interval_seconds=60,
            maximum_attempts=3,
            non_retryable_error_types=["ValidationError"]
        )
        
        # 1. 创建比赛
        match = await workflow.execute_activity(
            CreateMatch,
            match_id,
            start_to_close_timeout=30,
            retry_policy=retry_policy
        )
        
        # 2. 等待玩家加入
        try:
            await workflow.wait_for_condition(
                lambda: len(match.players) >= match.min_players,
                timeout=300  # 5分钟超时
            )
        except asyncio.TimeoutError:
            await workflow.execute_activity(
                CancelMatch,
                match_id,
                start_to_close_timeout=10
            )
            return {"status": "cancelled", "reason": "timeout"}
        
        # 3. 开始游戏
        await workflow.execute_activity(
            StartGame,
            match_id,
            start_to_close_timeout=30
        )
        
        # 4. 等待结束
        await workflow.wait_for_condition(
            lambda: match.is_finished,
            timeout=7200  # 2小时
        )
        
        return {"status": "completed", "result": match.result}
```

---

## 三、自动化测试深入分析 (更新)

### 3.1 E2E 测试工作流

| 技能ID | 名称 | 核心能力 | 评分 |
|----------|------|---------|------|
| **e2e-testing** | E2E 测试工作流 | Playwright 完整流程 | ⭐⭐⭐⭐⭐ |
| **e2e-testing-patterns** | E2E 测试模式 | 可靠测试套件 | ⭐⭐⭐⭐⭐ |
| **browser-automation** | 浏览器自动化 | 等待策略、选择器 | ⭐⭐⭐⭐⭐ |

#### Playwright 高级模式

```typescript
// 1. 游戏房间测试
test.describe('Game Room', () => {
  let roomId: string;
  
  test.beforeEach(async ({ page }) => {
    // 模拟登录
    await page.addInitScript(() => {
      localStorage.setItem('player', JSON.stringify({
        id: 'test-player',
        name: 'TestPlayer'
      }));
    });
    
    // 创建测试房间
    roomId = await createTestRoom();
    await page.goto(`/game/${roomId}`);
  });
  
  // 2. 游戏状态测试
  test('should sync game state correctly', async ({ page }) => {
    // 等待 WebSocket 连接
    const wsConnected = await page.waitForFunction(() => {
      return (window as any).gameSocket?.readyState === WebSocket.OPEN;
    });
    
    // 发送移动指令
    await page.keyboard.press('ArrowRight');
    
    // 验证位置更新
    await expect(page.locator('#player-position')).toHaveText('(100, 50)');
  });
  
  // 3. 性能测试
  test('should maintain 60fps during gameplay', async ({ page }) => {
    const metrics = await page.evaluate(() => {
      return new Promise(resolve => {
        let frames = 0;
        let lastTime = performance.now();
        
        function countFrame() {
          frames++;
          const currentTime = performance.now();
          if (currentTime - lastTime >= 1000) {
            resolve({ fps: frames, frames });
            return;
          }
          requestAnimationFrame(countFrame);
        }
        
        requestAnimationFrame(countFrame);
      });
    });
    
    expect(metrics.fps).toBeGreaterThanOrEqual(55);
  });
});

// 4. API Mock
test.mock('/api/game/state', {
  players: [{ id: '1', name: 'Bot', position: { x: 0, y: 0 } }],
  status: 'playing'
});
```

### 3.2 游戏客户端自动化测试

| 技能ID | 名称 | 核心能力 |
|--------|------|----------|
| **unity-developer** | Unity 测试 | Edit Mode/Play Mode 测试 |
| **game-development** | 游戏测试编排 | 单元/集成/E2E |

#### Unity Test Framework

```csharp
// 帧同步确定性测试
public class FrameSyncTests
{
    [UnityTest]
    public IEnumerator TestDeterministicSimulation()
    {
        // 创建相同初始状态
        var state1 = CreateTestState();
        var state2 = CreateTestState();
        
        // 相同输入序列
        var inputs = GenerateInputSequence(100);
        
        // 执行
        ExecuteFrames(state1, inputs);
        ExecuteFrames(state2, inputs);
        
        // 验证
        Assert.AreEqual(state1.GetHashCode(), state2.GetHashCode());
        
        yield return null;
    }
    
    [UnityTest]
    public IEnumerator TestNetworkPrediction()
    {
        var player = CreateTestPlayer();
        var originalPos = player.transform.position;
        
        // 模拟客户端预测
        player.PredictMove(Vector3.forward);
        
        // 等待服务器校正
        yield return new WaitForSeconds(0.5f);
        
        // 验证平滑校正
        Assert.AreNotEqual(originalPos, player.transform.position);
    }
}

// 网络延迟模拟
public class NetworkSimulationTests
{
    [Test]
    public void TestLatencyCompensation()
    {
        var sim = new NetworkSimulator();
        sim.SetLatency(200);  // 200ms
        sim.SetJitter(50);
        
        var packet = new GamePacket 
        { 
            SequenceNumber = 1, 
            Timestamp = Time.time 
        };
        
        var received = sim.SimulateDelivery(packet);
        
        Assert.IsNotNull(received);
        Assert.GreaterOrEqual(received.Timestamp - packet.Timestamp, 0.2f, 0.05f);
    }
}
```

### 3.3 API 安全测试

| 技能ID | 名称 | 核心能力 | 评分 |
|----------|------|---------|------|
| **api-security-testing** | API 安全测试 | 认证、授权、注入 | ⭐⭐⭐⭐⭐ |
| **api-testing-observability-api-mock** | API Mock | Mock、可观测性 | ⭐⭐⭐⭐ |
| **burp-suite-testing** | Burp Suite 渗透测试 | Web 漏洞扫描 | ⭐⭐⭐⭐ |

#### API 安全测试清单

```markdown
## 认证测试
- [ ] JWT 无签名验证 → 尝试 'alg': 'none'
- [ ] 弱密码策略 →暴力破解
- [ ] 会话固定 → 测试 session 复用
- [ ] OAuth 漏洞 → CSRF、redirect_uri

## 授权测试
- [ ] 水平越权 → 修改用户 ID
- [ ] 垂直越权 → 提升权限
- [ ] IDOR → 直接对象引用
- [ ] 批量分配 → 尝试额外字段

## 输入验证
- [ ] SQL 注入 → ' OR '1'='1
- [ ] XSS → <script>alert(1)</script>
- [ ] 命令注入 → ; ls -la
- [ ] 路径遍历 → ../../../etc/passwd
```

### 3.4 测试工具矩阵

| 工具 | 语言 | 适用场景 | 特点 |
|------|------|----------|------|
| **Playwright** | TypeScript | E2E、Web | 跨浏览器、自动等待 |
| **Cypress** | JavaScript | E2E | 简单易用、实时重载 |
| **Pytest** | Python | API/单元 | 丰富插件、参数化 |
| **Jest** | JavaScript | 单元/集成 | 快照测试、Mock |
| **Unity Test Framework** | C# | 游戏客户端 | Edit/Play Mode |

---

## 四、其他开发者工具 (新增)

### 4.1 MCP 服务器开发

| 技能ID | 名称 | 核心能力 | 评分 |
|----------|------|---------|------|
| **mcp-builder** | MCP 构建器 | 创建 MCP 服务器 | ⭐⭐⭐⭐⭐ |
| **mcp-builder-ms** | MCP 微软版 | 微软生态 MCP | ⭐⭐⭐⭐ |

#### MCP 服务器架构

```typescript
// MCP 服务器示例
import { Server } from '@modelcontextprotocol/sdk/server/index.js';
import { StdioServerTransport } from '@modelcontextprotocol/sdk/server/stdio.js';

const server = new Server({
  name: 'game-server',
  version: '1.0.0'
}, {
  capabilities: {
    tools: {},
    resources: {}
  }
});

// 定义工具
server.setRequestHandler('tools/list', async () => {
  return {
    tools: [
      {
        name: 'create_game_room',
        description: 'Create a new game room',
        inputSchema: {
          type: 'object',
          properties: {
            name: { type: 'string' },
            maxPlayers: { type: 'number', minimum: 2, maximum: 100 }
          },
          required: ['name']
        }
      },
      {
        name: 'join_game_room',
        description: 'Join an existing game room',
        inputSchema: {
          type: 'object',
          properties: {
            roomId: { type: 'string' },
            playerName: { type: 'string' }
          },
          required: ['roomId', 'playerName']
        }
      }
    ]
  };
});

// 处理工具调用
server.setRequestHandler('tools/call', async (request) => {
  const { name, arguments: args } = request.params;
  
  switch (name) {
    case 'create_game_room':
      return { content: [{ type: 'text', text: await createRoom(args) }] };
    case 'join_game_room':
      return { content: [{ type: 'text', text: await joinRoom(args) }] };
  }
});

// 启动
const transport = new StdioServerTransport();
await server.connect(transport);
```

### 4.2 云服务集成

| 技能ID | 名称 | 核心能力 |
|--------|------|----------|
| **aws-skills** | AWS 开发 | EC2、S3、Lambda |
| **aws-serverless** | AWS 无服务器 | Serverless 模式 |
| **aws-cost-optimizer** | AWS 成本优化 | 成本分析 |
| **azure-ai-projects-py** | Azure AI | AI Foundry |

### 4.3 工作流自动化

| 技能ID | 名称 | 核心能力 |
|--------|------|----------|
| **cicd-automation-workflow-automate** | CI/CD 自动化 | GitHub Actions |
| **changelog-automation** | Changelog 自动生成 | 版本记录 |
| **github-workflow-automation** | GitHub 工作流 | Issue/PR 自动化 |

---

## 五、推荐 Skills 组合

### 5.1 游戏后端开发

```
推荐: /python-pro + /python-fastapi-development
     /async-python-patterns + /temporal-python-pro
     /aws-serverless + /aws-cost-optimizer
```

### 5.2 游戏客户端开发

```
推荐: /unity-developer + /unity-ecs-patterns (性能)
     /godot-gdscript-patterns + /godot-4-migration
     /unreal-engine-cpp-pro + /game-development
```

### 5.3 自动化测试

```
推荐: /e2e-testing + /e2e-testing-patterns
     /browser-automation + /api-security-testing
     /python-testing-patterns
```

### 5.4 MCP 开发

```
推荐: /mcp-builder + /mcp-builder-ms
     /aws-skills + /azure-ai-projects-py
```

---

## 六、安装指南

### Antigravity 安装

```bash
npx antigravity-awesome-skills
```

### Claude Code

```bash
npx antigravity-awesome-skills --claude
```

### 使用方式

```bash
>> /skill-name help me...
```

---

## 七、相关资源

- [Antigravity Awesome Skills](https://github.com/sickn33/antigravity-awesome-skills)
- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
- [cc_plugin 仓库](https://github.com/kongshan001/cc_plugin)

---

**文档更新时间**: 2026-03-04
**Claude Code 插件调研 - 第十二期**
