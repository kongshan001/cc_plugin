# Claude Code 插件调研报告 - 补充调研第六期

> 持续跟踪 Claude Code 生态热门插件，聚焦游戏开发、Python 开发、自动化测试、开发者工具方向

---

## 📋 本期调研概要

| 维度 | 统计 |
|-----|------|
| **调研时间** | 2026-03-04 |
| **覆盖方向** | 游戏开发、Python开发、自动化测试、开发者工具 |
| **新增技能** | 30+ |
| **数据来源** | Antigravity Skills, awesome-claude-code, GitHub trending |

---

## 一、游戏客户端开发技能 (补充)

### 1.1 Antigravity Game Development 技能体系

Antigravity 提供完整的游戏开发技能体系，覆盖所有主流平台和维度：

| 技能ID | 名称 | 核心能力 |
|--------|------|----------|
| **game-development** | 游戏开发总览 | 路由到平台特定技能 |
| **2d-games** | 2D游戏开发 | Sprites, tilemaps, physics, camera |
| **3d-games** | 3D游戏开发 | Rendering, shaders, physics, cameras |
| **pc-games** | PC/主机游戏 | Engine selection, platform features |
| **mobile-games** | 移动游戏 | Touch input, battery, performance |
| **web-games** | 网页游戏 | WebGPU, PWA, optimization |
| **multiplayer** | 多人游戏 | Architecture, networking |
| **vr-ar** | VR/AR开发 | Comfort, interaction, performance |
| **game-art** | 游戏美术 | Visual style, asset pipeline |
| **game-audio** | 游戏音频 | Sound design, adaptive audio |
| **game-design** | 游戏设计 | GDD, balancing, psychology |

### 1.2 游戏开发核心原则

#### 游戏循环模式
```
INPUT  → 读取玩家输入
UPDATE → 处理游戏逻辑 (固定时间步长)
RENDER → 渲染帧 (插值)
```

#### 性能预算 (60 FPS = 16.67ms)
| 系统 | 预算 |
|------|------|
| 输入 | 1ms |
| 物理 | 3ms |
| AI | 2ms |
| 游戏逻辑 | 4ms |
| 渲染 | 5ms |
| 缓冲 | 1.67ms |

#### 设计模式选择矩阵
| 模式 | 使用场景 |
|------|----------|
| **状态机** | 3-5个离散状态 |
| **对象池** | 频繁生成/销毁对象 |
| **观察者** | 跨系统通信 |
| **ECS** | 大量相似实体 |
| **命令模式** | 撤销、回放、网络同步 |
| **行为树** | 复杂AI决策 |

### 1.3 Unity 帧同步游戏开发技能

针对 game-frame-sync 项目的推荐技能组合：

| 技能 | 用途 |
|------|------|
| **cc-plugin-unity-gamedev** | Unity C# 开发，21个专业技能 |
| **OH-Unity-GameDev-Skills** | Unity + DoTween + MediaPipe |
| **unity-ai-workflow** | Unity 6.2+ AI-first工作流 |
| **Claude-Code-Game-Studios** | 48代理全栈游戏开发 |

### 1.4 Web 游戏开发趋势

#### WebGPU 浏览器支持 (2025)
| 浏览器 | 支持版本 | 状态 |
|--------|----------|------|
| Chrome | v113+ | ✅ |
| Edge | v113+ | ✅ |
| Firefox | v131+ | ✅ |
| Safari | 18.0+ | ✅ |
| **全球支持率** | - | **~73%** |

#### Web 游戏框架选择
| 框架 | 特点 | 适用场景 |
|------|------|----------|
| Phaser 4 | 完整2D引擎 | 商业2D游戏 |
| PixiJS 8 | 高性能渲染 | 自定义渲染 |
| Babylon.js 7 | 完整3D引擎 | 3D游戏、XR |
| Three.js | 渲染为主 | 3D可视化 |

---

## 二、Python 开发技能 (补充)

### 2.1 Python Pro 技能 (Antigravity)

**Python-pro** 是 Antigravity 技能市场中最重要的 Python 开发技能：

| 特性 | 说明 |
|------|------|
| **版本** | Python 3.12+ |
| **包管理** | uv (2024最快) |
| **代码质量** | ruff (替代black/isort/flake8) |
| **类型检查** | mypy, pyright |
| **Web框架** | FastAPI, Django, Flask |

#### 核心能力

**现代Python特性:**
- Python 3.12+ 特性 (改进的错误信息、性能优化)
- 高级 async/await 模式 (asyncio, aiohttp, trio)
- Pydantic 模型和数据验证
- 模式匹配 (match语句)
- 类型提示和 Protocol 类型

**现代工具链:**
```bash
# uv - 最快的Python包管理器
uv init my-project
uv venv
uv pip install -r requirements.txt

# ruff - 代码格式化和linting
ruff check .
ruff format .
```

**测试与质量保证:**
- pytest 及插件
- Hypothesis 属性测试
- pytest-cov 覆盖率分析
- pytest-benchmark 性能测试

### 2.2 Python 开发技能汇总

| 技能ID | 核心能力 | 适用场景 |
|--------|----------|----------|
| **python-pro** | Python 3.12+ 全栈 | 通用开发 |
| **python-patterns** | 开发原则和决策 | 架构设计 |
| **python-fastapi-development** | FastAPI 后端开发 | API 服务 |
| **python-testing-patterns** | pytest/测试策略 | 质量保证 |
| **async-python-patterns** | asyncio 异步编程 | 高并发 |
| **python-performance-optimization** | 性能优化 | 性能关键 |
| **temporal-python-pro** | Temporal 工作流 | 分布式事务 |

### 2.3 数据库集成

| 技能 | 功能 | 安全性 |
|------|------|--------|
| **read-only-postgres** | PostgreSQL只读查询 | ⭐⭐⭐⭐⭐ |
| **postgres** | PostgreSQL完整集成 | ⭐⭐⭐ |

#### read-only-postgres 安全特性
- 只读查询 (SELECT/SHOW/EXPLAIN/WITH)
- 超时控制
- 行数限制
- 多连接支持

---

## 三、自动化测试技能 (补充)

### 3.1 Playwright 浏览器自动化

**playwright-skill** 是 Claude Code 最热门的浏览器自动化技能：

| 项目 | 说明 |
|------|------|
| **GitHub** | lackeyjb/playwright-skill |
| **Star** | ⭐ 1.8k+ |
| **功能** | 完整浏览器自动化 |

#### 核心工作流

1. **自动检测开发服务器**
2. **编写脚本到 /tmp** (不污染项目)
3. **使用可见浏览器** (默认 headless: false)
4. **参数化 URL** (可通过环境变量配置)

#### 典型用途
- Web 应用功能测试
- UI 验证
- 截图捕获
- 响应式
- 登录设计检查流程测试
- 表单自动化

### 3.2 游戏客户端自动化测试方案

| 测试类型 | 方案 | 适用场景 |
|---------|------|---------|
| **Web/H5游戏** | Playwright | 功能测试、回归测试 |
| **Unity游戏** | Unity Test Framework | 单元测试、集成测试 |
| **性能测试** | Unity Profiler | 帧率、内存测试 |
| **Android游戏** | ADB + uiautomator | UI自动化 |
| **iOS游戏** | ios-simulator-skill | 模拟器测试 |

### 3.3 移动端游戏测试

#### Android UI 测试
```bash
# 设备校准 - 获取屏幕分辨率
adb shell wm size

# UI 检查 - 获取元素信息
adb shell uiautomator dump /sdcard/view.xml
```

### 3.4 TDD 开发流程

```
红色 (Red)     → 编写失败的测试
       ↓
绿色 (Green)   → 实现最小代码通过测试
       ↓
重构 (Refactor)→ 重构代码保持测试通过
```

#### 相关 Slash Commands
| 命令 | 功能 |
|------|------|
| `/tdd` | TDD 开发流程指导 |
| `/tdd-implement` | 实现 TDD 流程 |
| `/testing_plan_integration` | 测试计划集成 |

---

## 四、开发者工具技能 (补充)

### 4.1 开发者工具包

| 技能 | GitHub | Star | 功能 |
|------|--------|------|------|
| **developer-kit** | giuseppe-trisciuoglio/developer-kit | ⭐128 | 模块化插件系统 |
| **claude-code-tools** | pchalasani/claude-code-tools | - | 会话连续性工具 |
| **claudekit** | carlrannaberg/claudekit | - | CLI工具包，20+子代理 |

#### Claudekit 子代理
| 代理 | 功能 |
|------|------|
| **oracle** | GPT-5 集成 |
| **code-reviewer** | 6方面深度分析 |
| **typescript-expert** | TypeScript 专家 |
| **ai-sdk-expert** | Vercel AI SDK |

### 4.2 Claude Code Settings

| 项目 | 说明 |
|------|------|
| **GitHub** | fcakyon/claude-codex-settings |
| **Star** | ⭐ 250+ |
| **覆盖** | 核心开发者活动 |

#### 支持平台
- GitHub
- Azure
- MongoDB
- Tavily
- Playwright

### 4.3 AWS 集成

| 技能 | GitHub | 功能 |
|------|--------|------|
| **aws-mcp-server** | alexei-led/aws-mcp-server | AWS CLI 集成 |

**支持服务:**
- 计算: EC2, Lambda, ECS, EKS
- 存储: S3, EBS, EFS
- 数据库: RDS, DynamoDB, ElastiCache
- 网络: VPC, CloudFront, Route53

### 4.4 编排工具 (Orchestrators)

| 工具 | 说明 | 特点 |
|------|------|------|
| **Claude Squad** | 多代理并行工作 | 终端应用 |
| **Claude Swarm** | 代理群组 | 分布式 |
| **Claude Code Flow** | 递归代理循环 | 代码优先 |
| **Auto-Claude** | 自主多代理 | Kanban UI |
| **TSK** | Docker沙箱 | 隔离执行 |

### 4.5 Superpowers 技能包

| 项目 | 说明 |
|------|------|
| **GitHub** | obra/superpowers |
| **Star** | ⭐ 500+ |
| **特点** | 核心工程能力，覆盖SDLC |

#### 覆盖范围
- 规划 (Planning)
- 审查 (Reviewing)
- 测试 (Testing)
- 调试 (Debugging)
- 完整软件生命周期

---

## 五、技能索引

### 5.1 按方向分类

#### 游戏开发
| 技能 | 来源 | 优先级 |
|------|------|--------|
| game-development | Antigravity | ⭐⭐⭐⭐⭐ |
| cc-plugin-unity-gamedev | GitHub | ⭐⭐⭐⭐ |
| Claude-Code-Game-Studios | GitHub | ⭐⭐⭐⭐ |
| unity-ai-workflow | GitHub | ⭐⭐⭐ |

#### Python 开发
| 技能 | 来源 | 优先级 |
|------|------|--------|
| python-pro | Antigravity | ⭐⭐⭐⭐⭐ |
| python-fastapi-development | Antigravity | ⭐⭐⭐⭐ |
| python-testing-patterns | Antigravity | ⭐⭐⭐⭐ |
| read-only-postgres | GitHub | ⭐⭐⭐⭐ |

#### 自动化测试
| 技能 | 来源 | 优先级 |
|------|------|--------|
| playwright-skill | Antigravity | ⭐⭐⭐⭐⭐ |
| browser-automation | Antigravity | ⭐⭐⭐⭐ |
| Superpowers | GitHub | ⭐⭐⭐⭐ |

#### 开发者工具
| 技能 | 来源 | 优先级 |
|------|------|--------|
| claude-code-tools | GitHub | ⭐⭐⭐⭐⭐ |
| claudekit | GitHub | ⭐⭐⭐⭐ |
| aws-mcp-server | GitHub | ⭐⭐⭐⭐ |
| developer-kit | GitHub | ⭐⭐⭐ |

---

## 六、推荐技能组合

### 6.1 帧同步游戏开发 (game-frame-sync)

```
python-pro (后端)
  ↓
cc-plugin-unity-gamedev (Unity客户端)
  ↓
playwright-skill (Web界面测试)
  ↓
Superpowers (代码质量)
```

### 6.2 Python Web 全栈

```
python-pro (核心开发)
  ↓
python-fastapi-development (API)
  ↓
python-testing-patterns (测试)
  ↓
read-only-postgres (数据)
```

### 6.3 游戏自动化测试

```
playwright-skill (Web测试)
  ↓
browser-automation (浏览器)
  ↓
Superpowers (质量保证)
```

---

## 📚 参考资源

- [awesome-claude-code](https://github.com/Burtella/awesome-claude-code)
- [Antigravity Skills](https://github.com/purpleclay/antigravity-awesome-skills)
- [Claude Code 官方文档](https://docs.anthropic.com/en/docs/claude-code/overview)

---

*文档更新: 2026-03-04*
*下次更新: 2026-03-11*
