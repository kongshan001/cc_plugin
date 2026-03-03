# Claude Code 插件补充调研 - 第三十二期

> 聚焦游戏客户端开发、Python开发、游戏客户端自动化测试、开发者工具

---

## 调研时间
2026-03-04

## 数据来源
- Antigravity Skills (900+ 技能)
- awesome-claude-code
- GitHub trending

---

## 一、游戏客户端开发技能

### 1.1 Unity 开发技能

| 技能 | ID | 描述 | 来源 |
|-----|-----|------|------|
| **unity-developer** | unity-developer | Build Unity games with optimized C# scripts, efficient rendering, and proper asset management. Masters Unity 6 LTS, URP/HDRP pipelines, and cross-platform deployment. | community |
| **unity-ecs-patterns** | unity-ecs-patterns | Unity DOTS/ECS开发模式 | community |

#### unity-developer 核心能力

```
### Core Unity Mastery
- Unity 6 LTS features and Long-Term Support benefits
- Unity Editor customization and productivity workflows
- Package Manager and custom package development
- Cross-platform build optimization and platform-specific configurations

### Modern Rendering Pipelines
- Universal Render Pipeline (URP) optimization and customization
- High Definition Render Pipeline (HDRP) for high-fidelity graphics
- Shader Graph visual shader creation and optimization
- Post-processing stack configuration and custom effects

### Performance & Architecture
- ECS (Entity Component System) and DOTS patterns
- Object pooling and memory management
- IL2CPP and scripting backend optimization
- GPU instancing and draw call optimization
```

### 1.2 Unreal Engine 开发技能

| 技能 | ID | 描述 | 来源 |
|-----|-----|------|------|
| **unreal-engine-cpp-pro** | unreal-engine-cpp-pro | Expert guide for Unreal Engine 5.x C++ development, covering UObject hygiene, performance patterns, and best practices. | self |

#### unreal-engine-cpp-pro 核心能力

```
### UE5 C++ 开发最佳实践
- UObject 清洁与内存管理
- 性能优化模式
- Slate UI 开发
- Actor 和 Component 系统
- 网络同步与 replication
- Gameplay Ability System (GAS)
```

### 1.3 Godot 开发技能

| 技能 | ID | 描述 | 来源 |
|-----|-----|------|------|
| **godot-gdscript-patterns** | godot-gdscript-patterns | Master Godot 4 GDScript patterns including signals, scenes, state machines, and optimization. | community |
| **godot-4-migration** | godot-4-migration | Godot 4 迁移指南 | community |

#### godot-gdscript-patterns 核心能力

```
### Godot 4.x GDScript 模式
- Signals 通信模式
- Scene 和 Node 架构
- State Machine 状态机
- 性能优化技巧
- 资源管理
- 4.x 新特性
```

### 1.4 通用游戏开发技能

| 技能 | ID | 描述 | 来源 |
|-----|-----|------|------|
| **game-development** | game-development | Game development orchestrator. Routes to platform-specific skills based on project needs. | community |
| **2d-games** | 2d-games | 2D game development principles. Sprites, tilemaps, physics, camera. | community |
| **3d-games** | 3d-games | 3D game development principles. Rendering, shaders, physics, cameras. | community |
| **web-games** | web-games | Web browser game development principles. Framework selection, WebGPU, optimization, PWA. | community |
| **mobile-games** | mobile-games | Mobile game development principles. Touch input, battery, performance, app stores. | community |
| **multiplayer** | multiplayer | 网络游戏开发 | community |
| **game-art** | game-art | 游戏美术工作流 | community |
| **game-audio** | game-audio | 游戏音频开发 | community |
| **game-design** | game-design | 游戏设计原理 | community |

#### 游戏技能覆盖范围

```
## 游戏开发技能矩阵
| 类型 | 技能 |
|------|------|
| 2D游戏 | 2d-games |
| 3D游戏 | 3d-games |
| Web游戏 | web-games |
| 移动游戏 | mobile-games |
| PC游戏 | pc-games |
| 网络游戏 | multiplayer |
| 游戏美术 | game-art |
| 游戏音频 | game-audio |
| 游戏设计 | game-design |
```

---

## 二、Python 开发技能

### 2.1 核心 Python 技能

| 技能 | ID | 描述 | 来源 |
|-----|-----|------|------|
| **python-pro** | python-pro | Master Python 3.12+ with modern features, async programming, performance optimization, and production-ready practices. | community |
| **python-patterns** | python-patterns | Python 设计模式和最佳实践 | community |
| **python-development-python-scaffold** | python-development-python-scaffold | Python 项目脚手架 | community |
| **python-fastapi-development** | python-fastapi-development | FastAPI 开发最佳实践 | community |
| **python-packaging** | python-packaging | Python 包发布和管理 | community |
| **python-performance-optimization** | python-performance-optimization | Python 性能优化 | community |

#### python-pro 核心能力

```
### Modern Python Features (3.12+)
- Python 3.12+ 新特性
- 高级 async/await 模式
- Context managers
- Dataclasses, Pydantic models
- Pattern matching
- Type hints 和 Generics

### Modern Tooling
- uv - 2024最快Python包管理器
- ruff - 代码格式化和linting
- mypy/pyright - 类型检查
- pyproject.toml - 现代配置标准

### Performance
- asyncio, aiohttp, trio
- 内存优化
- 性能分析
```

### 2.2 Python 测试技能

| 技能 | ID | 描述 | 来源 |
|-----|-----|------|------|
| **python-testing-patterns** | python-testing-patterns | Comprehensive testing strategies with pytest, fixtures, mocking, and TDD. | community |
| **temporal-python-testing** | temporal-python-testing | Temporal 工作流测试 | community |
| **unit-testing-test-generate** | unit-testing-test-generate | 单元测试生成 | community |

### 2.3 Python 异步和数据处理

| 技能 | ID | 描述 | 来源 |
|-----|-----|------|------|
| **async-python-patterns** | async-python-patterns | Master Python asyncio, concurrent programming, and async/await patterns. | community |
| **backtesting-frameworks** | backtesting-frameworks | 金融回测框架 | community |
| **dbos-python** | dbos-python | DBOS Python 工作流 | community |

### 2.4 Python 云和 AI 集成

| 技能 | ID | 描述 | 来源 |
|-----|-----|------|------|
| **airflow-dag-patterns** | airflow-dag-patterns | Apache Airflow DAG 开发最佳实践 | community |
| **n8n-code-python** | n8n-code-python | n8n 工作流自动化 | community |
| **temporal-python-pro** | temporal-python-pro | Temporal 工作流开发 | community |

---

## 三、自动化测试技能

### 3.1 浏览器自动化测试

| 技能 | ID | 描述 | 来源 |
|-----|-----|------|------|
| **playwright-skill** | playwright-skill | Complete browser automation with Playwright. Auto-detects dev servers, writes clean test scripts. | community |
| **e2e-testing** | e2e-testing | End-to-end testing workflow with Playwright for browser automation, visual regression, cross-browser testing. | personal |
| **go-playwright** | go-playwright | Go 语言 Playwright 绑定 | community |
| **azure-microsoft-playwright-testing-ts** | azure-microsoft-playwright-testing-ts | Azure Playwright 测试服务 | community |

#### playwright-skill 核心能力

```
### Playwright 自动化测试
1. **自动检测开发服务器**
   - 自动检测 localhost 服务器
   - 多服务器时让用户选择
   
2. **测试脚本管理**
   - 写入 /tmp 目录，不污染项目
   - 支持截图、视觉回归测试
   
3. **浏览器配置**
   - 默认使用可见浏览器
   - 支持无头模式
   
4. **测试场景**
   - 页面测试
   - 表单填写
   - 响应式设计检查
   - UX 验证
   - 登录测试
```

### 3.2 通用测试技能

| 技能 | ID | 描述 | 来源 |
|-----|-----|------|------|
| **test-automator** | test-automator | AI-powered test automation with modern frameworks, self-healing tests. | community |
| **test-driven-development** | test-driven-development | TDD 开发流程 | community |
| **testing-qa** | testing-qa | Comprehensive testing and QA workflow covering unit, integration, E2E testing. | personal |
| **testing-patterns** | testing-patterns | 测试模式和最佳实践 | community |
| **test-fixing** | test-fixing | 测试修复指南 | community |
| **javascript-testing-patterns** | javascript-testing-patterns | JavaScript 测试模式 | community |
| **e2e-testing-patterns** | e2e-testing-patterns | E2E 测试模式 | community |

#### test-automator 核心能力

```
### AI 驱动测试自动化
- 现代测试框架集成
- 自愈合测试 (Self-healing tests)
- 可扩展测试策略
- 高级 CI/CD 集成

### 测试类型
- 单元测试
- 集成测试
- E2E 测试
- 视觉回归测试
- 性能测试
```

### 3.3 移动端测试

| 技能 | ID | 描述 | 来源 |
|-----|-----|------|------|
| **android_ui_verification** | android_ui_verification | Automated end-to-end UI testing on Android Emulator using ADB. | community |
| **webapp-testing** | webapp-testing | Web 应用测试 | community |

---

## 四、开发者工具技能

### 4.1 API 和服务测试

| 技能 | ID | 描述 | 来源 |
|-----|-----|------|------|
| **api-security-testing** | api-security-testing | API 安全测试工作流 | community |
| **api-testing-observability-api-mock** | api-testing-observability-api-mock | API Mock 和可观测性 | community |
| **api-fuzzing-bug-bounty** | api-fuzzing-bug-bounty | API fuzzing 测试 | community |

### 4.2 自动化工作流

| 技能 | ID | 描述 | 来源 |
|-----|-----|------|------|
| **automation-workflow** | workflow-automation | 工作流自动化 | community |
| **cicd-automation-workflow-automate** | cicd-automation-workflow-automate | CI/CD 自动化 | community |
| **browser-automation** | browser-automation | 浏览器自动化 | community |

### 4.3 云平台集成

| 技能 | ID | 描述 | 来源 |
|-----|-----|------|------|
| **aws-skills** | aws-skills | AWS 开发与云架构 | community |
| **cloud-devops** | cloud-devops | 云端 DevOps | community |
| **appdeploy** | appdeploy | Web 应用部署 | community |

### 4.4 开发工具

| 技能 | ID | 描述 | 来源 |
|-----|-----|------|------|
| **chrome-extension-developer** | chrome-extension-developer | Chrome 扩展开发 | community |
| **apify-actor-development** | apify-actor-development | Apify Actor 开发 | community |
| **azure-functions** | azure-functions | Azure Functions 开发 | community |

---

## 五、技能使用建议

### 5.1 游戏开发推荐技能栈

```
## Unity 开发
→ unity-developer + unity-ecs-patterns

## Unreal Engine 开发
→ unreal-engine-cpp-pro

## Godot 开发
→ godot-gdscript-patterns + godot-4-migration

## 通用游戏开发
→ game-development (orchestrator) → 2d-games/3d-games/web-games/mobile-games
```

### 5.2 Python 开发推荐技能栈

```
## 现代 Python 开发
→ python-pro + python-patterns

## Web/API 开发
→ python-fastapi-development

## 测试
→ python-testing-patterns + test-driven-development

## 异步编程
→ async-python-patterns
```

### 5.3 测试推荐技能栈

```
## 浏览器自动化
→ playwright-skill + e2e-testing

## 综合测试
→ test-automator + testing-qa

## TDD
→ test-driven-development + python-testing-patterns
```

---

## 六、总结

本补充调研收集了 Antigravity Skills 生态中与以下方向相关的技能：

| 方向 | 技能数量 | 代表技能 |
|------|---------|---------|
| 游戏客户端开发 | 15+ | unity-developer, unreal-engine-cpp-pro, godot-gdscript-patterns |
| Python 开发 | 12+ | python-pro, python-testing-patterns, async-python-patterns |
| 自动化测试 | 15+ | playwright-skill, test-automator, e2e-testing |
| 开发者工具 | 20+ | api-security-testing, aws-skills, appdeploy |

**数据来源**: Antigravity Skills (900+ 技能索引)
