# Claude Code 插件调研 - 第四十六期

> 热门插件深度调研：游戏客户端开发、Python开发、自动化测试、开发者工具

## 调研时间
2026-03-04

## 数据来源
- awesome-claude-code (hesreallyhim/awesome-claude-code)
- Antigravity Awesome Skills (970+ Skills)
- ComposioHQ/awesome-claude-skills (100+ 技能)
- GitHub Topics: claude-code-skills
- cc_plugin 仓库历史调研文档

---

## 一、游戏客户端开发插件

### 1.1 游戏开发编排器 (官方推荐)

#### game-development ⭐⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **分类** | 游戏开发编排器 |
| **类型** | Orchestrator (路由技能) |
| **评价** | 官方推荐 ⭐⭐⭐⭐⭐ |

**核心能力:**

| 技能 | 用途 |
|------|------|
| `game-development/web-games` | Web 游戏 (HTML5, WebGL) |
| `game-development/mobile-games` | 移动游戏 (iOS, Android) |
| `game-development/pc-games` | PC 游戏 (Steam, Desktop) |
| `game-development/vr-ar` | VR/AR 游戏 |
| `game-development/2d-games` | 2D 游戏开发 |
| `game-development/3d-games` | 3D 游戏开发 |
| `game-development/multiplayer` | 多人游戏/网络 |
| `game-development/game-art` | 游戏美术/资产管线 |
| `game-development/game-audio` | 游戏音频/音效 |
| `game-development/game-design` | 游戏设计/GDD |

**游戏循环架构:**
```
INPUT  → 读取玩家输入
UPDATE → 处理游戏逻辑 (固定时间步长)
RENDER → 渲染帧 (插值)
```

**性能预算 (60 FPS = 16.67ms):**

| 系统 | 预算 |
|------|------|
| 输入处理 | 1ms |
| 物理引擎 | 3ms |
| AI 计算 | 2ms |
| 游戏逻辑 | 4ms |
| 渲染 | 5ms |
| 缓冲 | 1.67ms |

**安装:**
```bash
# 技能会自动根据项目需求路由到对应的子技能
# 在项目中使用
claude-code 将会自动识别游戏类型并路由到合适的技能
```

---

### 1.2 Unity 开发技能

#### unity-developer ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | Antigravity Awesome Skills |
| **技能数** | 21+ 专业 Unity 技能 |
| **评价** | ⭐⭐⭐⭐ 强烈推荐 |

**Unity 技能覆盖:**

| 类别 | 技能 |
|------|------|
| 开发框架 | Unity 基础、ECS 架构、MonoBehaviour 模式 |
| AI | 寻路、行为树、状态机 |
| 物理 | 刚体、碰撞、关节系统 |
| 渲染 | Shader Graph、URP、HDRP |
| 性能 | IL2CPP、DOTS、Jobs System |
| 测试 | Unity Test Framework、Play Mode |

**Unity ECS 模式:**
```
Entity          → 数据组件
Component       → 数据容器
System          → 逻辑处理
```

#### unity-ecs-patterns ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **分类** | Unity ECS 架构模式 |
| **评价** | ⭐⭐⭐⭐ 高性能游戏开发 |

**核心模式:**
- Data-Oriented Design
- Burst Compiler 优化
- Job System 并行
- Entity Command Buffer

---

### 1.3 Godot 开发技能

#### godot-4-migration ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **目标** | Godot 3.x → 4.x 迁移 |
| **评价** | ⭐⭐⭐⭐ 推荐 |

#### godot-gdscript-patterns ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | Antigravity Awesome Skills |
| **语言** | GDScript 4.x |
| **评价** | ⭐⭐⭐⭐ 强烈推荐 |

**GDScript 4.x 核心模式:**

| 模式 | 用途 |
|------|------|
| @export 变量 | 编辑器暴露 |
| @onready | 节点引用 |
| signal | 信号系统 |
| await | 异步处理 |
| class_name | 类型定义 |

---

### 1.4 Unreal Engine 开发

#### unreal-engine-cpp-pro ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **语言** | C++ / Blueprints |
| **评价** | ⭐⭐⭐⭐ 专业开发 |

**核心能力:**
- Actor/Component 架构
- UPROPERTY/UFUNCTION
- UObject 生命周期
- Blueprint 集成

---

### 1.5 Web 游戏开发

#### web-games ⭐⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **平台** | HTML5, WebGL, Canvas |
| **评价** | ⭐⭐⭐⭐⭐ 高度推荐 |

**技术栈:**

| 技术 | 用途 |
|------|------|
| Phaser.js | 2D 游戏框架 |
| Three.js | 3D/WebGL |
| Pixi.js | 2D 渲染 |
| Babylon.js | 3D 游戏引擎 |

**Web 游戏优化:**
- 对象池化
- 批量渲染
- 纹理图集
- 懒加载资源

---

### 1.6 移动游戏开发

#### mobile-games ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **平台** | iOS, Android |
| **框架** | React Native, Flutter, Unity |
| **评价** | ⭐⭐⭐⭐ 推荐 |

**移动端特性:**
- 触控输入处理
- 设备适配
- 手势识别
- 性能优化

---

### 1.7 多人游戏/网络

#### multiplayer ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **协议** | TCP, UDP, WebSocket |
| **架构** | 客户端-服务器, P2P |
| **评价** | ⭐⭐⭐⭐ 专业网络 |

**网络同步方案:**

| 方案 | 延迟容忍 | 带宽需求 |
|------|----------|----------|
| 帧同步 | < 100ms | 低 |
| 状态同步 | < 200ms | 中 |
| 预测插值 | < 300ms | 可变 |

---

## 二、Python 开发插件

### 2.1 异步编程

#### async-python-patterns ⭐⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **分类** | Python 异步编程 |
| **评价** | ⭐⭐⭐⭐⭐ 强烈推荐 |

**核心模式:**

| 模式 | 用途 |
|------|------|
| async/await | 异步语法 |
| asyncio | 事件循环 |
| aiohttp | 异步 HTTP |
| aiomysql | 异步数据库 |
| asyncio.gather | 并发任务 |
| asyncio.create_task | 任务调度 |

**高性能异步应用:**
```python
async def fetch_data(urls):
    async with aiohttp.ClientSession() as session:
        tasks = [session.get(url) for url in urls]
        return await asyncio.gather(*tasks)
```

---

### 2.2 FastAPI 开发

#### fastapi ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **评分** | 1.121 |
| **分类** | 高性能 Web 框架 |
| **评价** | ⭐⭐⭐⭐ 推荐 |

**FastAPI 核心特性:**

| 特性 | 描述 |
|------|------|
| Pydantic 验证 | 自动数据验证 |
| 类型提示 | 完整类型支持 |
| 依赖注入 | 优雅的依赖管理 |
| 自动文档 | OpenAPI/Swagger |
| 异步支持 | 原生 async/await |

**安装:**
```bash
pip install fastapi uvicorn
```

---

### 2.3 Python 测试技能

#### bats-testing-patterns ⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **分类** | Shell 脚本测试 |
| **评价** | ⭐⭐⭐ 基础技能 |

#### test-runner ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **评分** | 1.189 |
| **分类** | 测试运行器 |
| **评价** | ⭐⭐⭐⭐ 推荐 |

#### test-master ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **评分** | 1.158 |
| **分类** | 测试管理 |
| **评价** | ⭐⭐⭐⭐ 推荐 |

---

### 2.4 Python 数据库技能

#### read-only-postgres ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **安全** | 只读操作 ✅ |
| **评价** | ⭐⭐⭐⭐ 安全查询 |

**高级功能:**
- 多连接支持
- 深度防御安全机制
- 查询超时保护
- 行数限制
- EXPLAIN 分析

---

### 2.5 Python 现代化工具链

#### modern-python (Trail of Bits) ⭐⭐⭐⭐

| 工具 | 用途 | 速度 |
|------|------|------|
| **uv** | 包管理器 (Rust) | 比 pip 快 10-100x |
| **ruff** | 代码检查 | 比 flake8 快 10-100x |
| **ty** | 类型检查 | 比 mypy 快 |
| **pytest** | 测试 | 标准 |
| **coverage** | 覆盖率 | 标准 |

**安装:**
```bash
# uv (极速包管理)
curl -LsSf https://astral.sh/uv/install.sh | sh

# ruff (极速检查)
pip install ruff

# ty (极速类型检查)
pip install ty

# 使用示例
uv pip install -r requirements.txt
ruff check .
ty check .
pytest --cov=.
```

---

## 三、自动化测试插件

### 3.1 浏览器自动化

#### playwright ⭐⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **评分** | 3.538 |
| **GitHub Stars** | ⭐ 1.8k+ |
| **评价** | ⭐⭐⭐⭐⭐ TOP 技能 |

**核心功能:**

| 功能 | 描述 |
|------|------|
| 浏览器控制 | Chromium, Firefox, WebKit |
| 元素定位 | CSS, XPath, 文本 |
| 断言库 | 内置 expect |
| 截图/录屏 | 可视化调试 |
| 并行执行 | 多浏览器测试 |

**游戏测试应用:**
```python
# 游戏 UI 测试
from playwright.sync_api import sync_playwright

def test_game_ui():
    with sync_playwright() as p:
        browser = p.chromium.launch()
        page = browser.new_page()
        page.goto("game://localhost")
        # 测试游戏界面
        assert page.locator("#score").text_content() == "0"
        browser.close()
```

#### playwright-mcp ⭐⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **评分** | 3.581 |
| **分类** | MCP 服务器 |
| **评价** | ⭐⭐⭐⭐⭐ TOP 2 |

**MCP 集成:**
- 模型驱动自动化
- 自然语言控制
- 会话管理

---

### 3.2 移动端测试

#### android-adb ⭐⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **评分** | 1.220 |
| **分类** | 移动端测试 TOP 1 |
| **评价** | ⭐⭐⭐⭐⭐ 强烈推荐 |

**游戏测试功能:**

| 功能 | 描述 |
|------|------|
| UI 层级检查 | UI Automator |
| 触控模拟 | adb input tap |
| 性能监控 | FPS, 内存, CPU |
| 日志分析 | logcat |
| 截图/录屏 | 游戏表现记录 |

**使用示例:**
```bash
# 安装技能
git clone https://github.com/conorluddy/android-adb ~/.claude/skills/

# 游戏测试命令
adb shell input tap 500 500  # 点击屏幕
adb shell screenrecord /sdcard/game.mp4  # 录屏
adb shell dumpsys gfxinfo com.game.app  # 帧率分析
```

---

### 3.3 API 测试

#### api-security-testing ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **分类** | API 安全测试 |
| **评价** | ⭐⭐⭐⭐ 推荐 |

**测试覆盖:**

| 类别 | 测试项 |
|------|--------|
| 认证 | OAuth, JWT, API Key |
| 授权 | IDOR, 权限提升 |
| 输入验证 | SQL 注入, XSS |
| 速率限制 | DoS 防护 |

#### api-testing-observability-api-mock ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **分类** | API Mock 服务 |
| **评价** | ⭐⭐⭐⭐ 开发支持 |

---

### 3.4 E2E 测试

#### browser-automation ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **评分** | 3.772 |
| **分类** | 浏览器自动化 |
| **评价** | ⭐⭐⭐⭐⭐ TOP 工具 |

**游戏客户端自动化:**
- 登录流程自动化
- 剧情/任务测试
- 支付流程验证
- 性能基准测试

---

## 四、开发者工具插件

### 4.1 版本控制

#### git-essentials ⭐⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **评分** | 1.298 |
| **分类** | 版本控制 TOP 1 |
| **评价** | ⭐⭐⭐⭐⭐ 强烈推荐 |

**核心功能:**

| 功能 | 描述 |
|------|------|
| 分支管理 | Git Flow, GitHub Flow |
| 提交规范 | Conventional Commits |
| 冲突解决 | 智能合并 |
| 历史管理 | rebase, cherry-pick |

---

### 4.2 容器化

#### docker-essentials ⭐⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **评分** | 3.694 |
| **分类** | DevOps TOP 1 |
| **评价** | ⭐⭐⭐⭐⭐ 强烈推荐 |

**核心功能:**

| 功能 | 描述 |
|------|------|
| 镜像构建 | Dockerfile 优化 |
| 多阶段构建 | 减小镜像体积 |
| 网络配置 | 容器网络 |
| 数据卷 | 持久化存储 |

**Dockerfile 优化:**
```dockerfile
# 多阶段构建示例
FROM node:18-alpine AS builder
WORKDIR /app
COPY package*.json ./
RUN npm ci --only=production

FROM node:18-alpine
WORKDIR /app
COPY --from=builder /app/node_modules ./node_modules
COPY . .
CMD ["node", "server.js"]
```

#### docker ⭐⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **评分** | 3.577 |
| **评价** | ⭐⭐⭐⭐⭐ 完整功能 |

---

### 4.3 CI/CD

#### automation-workflows ⭐⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **评分** | 3.699 |
| **分类** | 工作流自动化 |
| **评价** | ⭐⭐⭐⭐⭐ TOP 工具 |

**支持平台:**
- GitHub Actions
- GitLab CI
- Jenkins
- CircleCI

---

### 4.4 GitHub 自动化

#### github ⭐⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **评分** | 3.790 |
| **分类** | GitHub 自动化 TOP 1 |
| **评价** | ⭐⭐⭐⭐⭐ 强烈推荐 |

**功能:**

| 功能 | 描述 |
|------|------|
| PR 管理 | 创建、审查、合并 |
| Issue 处理 | 自动标签、分配 |
| Release | 版本发布 |
| 安全扫描 | 漏洞检测 |

---

### 4.5 代码质量

#### code-analysis ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **分类** | 代码分析 |
| **评价** | ⭐⭐⭐⭐ 推荐 |

**分析维度:**
- 代码复杂度
- 重复代码检测
- 技术债务
- 安全性分析

---

### 4.6 API 客户端

#### rest-client ⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **分类** | REST API 客户端 |
| **评价** | ⭐⭐⭐⭐ 开发支持 |

**功能:**
- HTTP 请求构建
- 响应验证
- 环境变量
- 集合管理

---

## 五、本期推荐技能组合

### 5.1 游戏客户端开发推荐

```
🎮 游戏客户端开发完整技能栈:

游戏引擎:
├── game-development (编排器 ⭐⭐⭐⭐⭐)
├── unity-developer (21+ 技能)
├── godot-gdscript-patterns
└── unreal-engine-cpp-pro

Web 游戏:
├── web-games (HTML5/WebGL)
├── Three.js
└── Phaser.js

移动游戏:
├── mobile-games
├── android-adb (测试)
└── iOS Simulator 集成

多人游戏:
├── multiplayer (网络同步)
└── WebSocket/UDP
```

### 5.2 Python 开发推荐

```
🐍 Python 开发完整技能栈:

异步编程:
├── async-python-patterns (⭐⭐⭐⭐⭐)
├── aiohttp
└── asyncio

Web 框架:
├── fastapi (⭐⭐⭐⭐)
└── uvicorn

测试:
├── test-runner (1.189)
├── test-master (1.158)
└── pytest

数据库:
├── read-only-postgres (安全)
└── asyncpg

工具链:
├── uv (极速包管理)
├── ruff (极速检查)
└── ty (极速类型)
```

### 5.3 自动化测试推荐

```
🧪 自动化测试完整技能栈:

浏览器自动化:
├── playwright (3.538 ⭐⭐⭐⭐⭐)
├── playwright-mcp (3.581)
└── browser-automation (3.772)

移动端测试:
├── android-adb (1.220 TOP 1)
└── iOS Simulator

API 测试:
├── api-security-testing
└── api-testing-observability-api-mock

E2E 测试:
├── test-master (1.158)
└── test-runner (1.189)
```

### 5.4 开发者工具推荐

```
🔧 开发者工具完整技能栈:

版本控制:
├── git-essentials (1.298 TOP 1)
└── github (3.790 TOP 1)

容器化:
├── docker-essentials (3.694 TOP 1)
└── docker (3.577)

CI/CD:
├── automation-workflows (3.699)
└── GitHub Actions

代码质量:
├── code-analysis
└── linting tools
```

---

## 六、总结

### 6.1 本期亮点

| 类别 | 推荐插件 | 评分 |
|------|----------|------|
| **游戏开发** | game-development | ⭐⭐⭐⭐⭐ 编排器 |
| **Unity** | unity-developer | ⭐⭐⭐⭐ 21+ 技能 |
| **Python 异步** | async-python-patterns | ⭐⭐⭐⭐⭐ |
| **Playwright** | playwright | ⭐⭐⭐⭐⭐ 3.538 |
| **Docker** | docker-essentials | ⭐⭐⭐⭐⭐ 3.694 |
| **GitHub** | github | ⭐⭐⭐⭐⭐ 3.790 |

### 6.2 快速入门

```bash
# 1. 游戏开发技能
git clone https://github.com/antigravity-awesome-skills/skills/game-development ~/.claude/skills/game-development

# 2. Unity 开发
git clone https://github.com/antigravity-awesome-skills/skills/unity-developer ~/.claude/skills/unity-developer

# 3. Python 异步编程
git clone https://github.com/antigravity-awesome-skills/skills/async-python-patterns ~/.claude/skills/async-python-patterns

# 4. Playwright 测试
git clone https://github.com/antigravity-awesome-skills/skills/playwright ~/.claude/skills/playwright

# 5. Docker 工具
git clone https://github.com/antigravity-awesome-skills/skills/docker-essentials ~/.claude/skills/docker-essentials
```

### 6.3 下一步行动

1. **游戏开发**: 使用 game-development 编排器，根据项目类型自动路由
2. **Python 开发**: 采用异步编程模式提升性能
3. **自动化测试**: 集成 Playwright 进行 E2E 测试
4. **开发者工具**: 使用 Docker 和 GitHub 技能提升开发效率

---

## 📚 参考资源

- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
- [Antigravity Awesome Skills](https://github.com/antigravity-awesome-skills)
- [awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills)
- [anthropics/skills](https://github.com/anthropics/skills)
- [trailofbits/skills](https://github.com/trailofbits/skills)
- [cc_plugin 仓库](https://github.com/kongshan001/cc_plugin)
