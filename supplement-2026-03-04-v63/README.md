# Claude Code 热门插件补充调研 (v63)

> 2026年3月 游戏/Python/测试/开发者工具热门插件完整调研 - 持续更新版

---

## 一、调研概述

### 1.1 本次调研重点

本次调研继续深入分析 Claude Code 热门插件，重点关注以下方向：
1. **游戏客户端开发** - Unity、Unreal、Godot、GameMaker 集成
2. **Python 开发** - FastAPI、Django、Pydantic AI、数据科学
3. **游戏客户端自动化测试** - Playwright、移动端测试、UI 自动化
4. **其他开发者工具** - GitHub 集成、云服务、开发者效率工具

### 1.2 数据来源

- awesome-claude-code (GitHub 8616+ 仓库索引)
- GitHub Topics: claude-skill, mcp-server, claude-code
- ClawHub 插件市场
- 官方 MCP 服务器

---

## 二、游戏客户端开发插件深度分析

### 2.1 Unity 开发技能矩阵

| 插件 | GitHub Stars | 技能数量 | 推荐指数 |
|-----|-------------|---------|----------|
| cc-plugin-unity-gamedev | ⭐ 活跃 | 21 技能 | ⭐⭐⭐⭐⭐ |
| OH-Unity-GameDev-Skills | ⭐ 6 | 5+ 技能 | ⭐⭐⭐⭐ |
| unity-ai-workflow | ⭐ 4 | 完整工作流 | ⭐⭐⭐⭐ |
| Claude-Code-Skills-For-Unity | 活跃 | 多种资产 | ⭐⭐⭐ |

#### cc-plugin-unity-gamedev 核心技能

| 类别 | 技能 | 功能 |
|-----|------|------|
| **资源管理** | Addressables | 异步资源加载/管理 |
| **数据序列化** | MemoryPack | 高效二进制序列化 |
| **配置管理** | ScriptableObjects | Unity 配置系统 |
| **性能分析** | Profiling | 性能优化工具 |
| **动画系统** | PrimeTween | 高性能动画库 |
| **AI 行为** | Behavior Designer | 行为树编辑器 |
| **技能系统** | GAS | Gameplay Ability System |
| **音频** | Wwise | 专业音频集成 |
| **相机** | Cinemachine | 虚拟相机系统 |
| **UI** | UGUI | Unity UI 开发 |
| **导航** | NavMesh | 寻路系统 |
| **DI** | VContainer | 依赖注入 |
| **异步** | UniTask | 异步编程 |

### 2.2 Godot 开发技能

| 插件 | GitHub Stars | 适用版本 |
|-----|-------------|----------|
| claude-resources (Godot) | ⭐ 3 | Godot 4.x |
| Godot GDScript MCP | ⭐ 45+ | Godot 3.x/4.x |

#### Godot 4.x 核心技能

- **GDScript 编程**: 与 Python 相似的脚本语言
- **节点系统**: 场景即节点树
- **信号系统**: 事件驱动编程
- **资源管理**: 动态加载和资源打包
- **Shader 开发**: 着色器编写
- **GDExtension**: C++ 扩展开发

### 2.3 Unreal Engine 开发

| 插件 | GitHub Stars | 特点 |
|-----|-------------|------|
| Unreal-MCP | ⭐ 150+ | 官方 MCP 服务器 |

#### Unreal-MCP 核心功能

- 蓝图自动化生成
- 材质和纹理处理
- 关卡设计辅助
- 性能分析集成
- C++ 代码生成

### 2.4 GameMaker Studio 开发

| 插件 | GitHub Stars | 语言 |
|-----|-------------|------|
| gamemaker-skills | ⭐ 2 | GML |

#### 核心功能

- 对象创建和管理
- GML 语法专家
- Shaders 着色器开发
- 网络功能多人游戏

### 2.5 游戏开发 MCP 服务器

```bash
# 安装游戏开发 MCP
npm install -g unreal-mcp-server
npm install -g godot-mcp-server

# 配置 Claude Desktop
# ~/.config/claude-desktop/mcp.json
{
  "mcpServers": {
    "unreal": {
      "command": "npx",
      "args": ["-y", "unreal-mcp-server"]
    }
  }
}
```

---

## 三、Python 开发插件深度分析

### 3.1 Web 框架 MCP 服务器

| 插件 | GitHub Stars | 评分 | 适用框架 |
|-----|-------------|------|----------|
| FastAPI MCP | ⭐ 120+ | 1.054-1.121 | FastAPI |
| Django MCP | 活跃 | - | Django |
| tadata/fastapi_mcp | 活跃 | - | FastAPI (认证) |

#### FastAPI MCP 核心功能

| 功能 | 说明 |
|------|------|
| 高性能 | 与 Node.js 和 Go 相当 |
| 自动文档 | Swagger UI/ReDoc |
| 类型安全 | Pydantic 集成 |
| 异步支持 | async/await |

#### 安装配置

```bash
pip install fastapi-mcp-server

# 配置
{
  "mcpServers": {
    "fastapi": {
      "command": "fastapi-mcp-server",
      "args": ["--port", "3000"]
    }
  }
}
```

### 3.2 Pydantic AI 技能

| 插件 | GitHub Stars | 特点 |
|-----|-------------|------|
| pydantic-ai-skills | ⭐ 136 | 类型安全 AI 开发 |

#### 核心功能

- 类型强制检查
- 渐进式提示披露
- 主流 LLM 集成
- 内置数据验证

### 3.3 数据库技能

| 插件 | 功能 | 安全性 |
|-----|------|-------|
| read-only-postgres | 只读查询 | ⭐⭐⭐⭐⭐ |
| postgres (完整版) | 全面数据库操作 | ⭐⭐⭐ |
| AWS RDS MCP | 云数据库 | ⭐⭐⭐⭐ |

#### read-only-postgres 安全特性

```sql
-- 支持的查询类型
SELECT * FROM users WHERE id = 1;
SHOW max_connections;
EXPLAIN ANALYZE SELECT * FROM orders;

-- 安全限制
- 仅 SELECT/SHOW/EXPLAIN/WITH
- 超时控制
- 行数限制
- 多连接支持
```

### 3.4 AWS 云服务集成

| 插件 | GitHub Stars | 支持服务 |
|-----|-------------|----------|
| aws-mcp-server | ⭐ 1350+ | 完整 AWS |

#### 支持的 AWS 服务

- **计算**: EC2, Lambda, ECS, EKS
- **存储**: S3, EBS, EFS
- **数据库**: RDS, DynamoDB, ElastiCache
- **网络**: VPC, CloudFront, Route53
- **安全**: IAM, Secrets Manager

### 3.5 Python 类型安全

| 技能 | 功能 |
|-----|------|
| mypy | 静态类型检查 |
| pyright | 快速类型检查 |
| pydantic | 运行时类型验证 |

### 3.6 语音转文字集成

| 插件 | 特点 |
|-----|------|
| stt-mcp-server-linux | 本地运行/Docker/隐私保护 |

---

## 四、游戏客户端自动化测试插件深度分析

### 4.1 Web/H5 游戏测试

| 插件 | GitHub Stars | 评分 | 用途 |
|-----|-------------|------|------|
| Playwright MCP | ⭐ 500+ | 3.581 | Web E2E 测试 |
| playwright-skill | ⭐ 1.8k | - | 模型驱动测试 |
| Playwright Undetected | 活跃 | - | 反检测测试 |

#### Playwright MCP 核心功能

- 浏览器自动化
- 跨浏览器测试 (Chromium/Firefox/WebKit)
- API 测试
- 移动端测试
- 截图和视频录制

#### 安装配置

```bash
# 安装
npm install -g @anthropic/playwright-mcp-server

# 配置
{
  "mcpServers": {
    "playwright": {
      "command": "npx",
      "args": ["-y", "@anthropic/playwright-mcp-server"]
    }
  }
}
```

### 4.2 Unity 测试框架

| 测试类型 | 工具 | 特点 |
|---------|------|------|
| EditMode | Unity Test Framework | 编辑器测试 |
| PlayMode | Unity PlayMode | 运行时测试 |
| 集成测试 | NUnit | 单元测试 |

#### Unity 测试示例

```csharp
// EditMode 测试
[Test]
public void TestEditMode() { 
    Assert.AreEqual(1 + 1, 2);
}

// PlayMode 测试
[UnityTest]
public IEnumerator TestPlayMode() {
    var go = new GameObject("Test");
    yield return null;
    Assert.IsNotNull(go);
}

// 异步测试
[UnityTest]
public IEnumerator TestAsync() {
    var task = LoadAssetAsync();
    yield return new WaitUntil(() => task.IsCompleted);
    Assert.IsTrue(task.IsCompleted);
}
```

### 4.3 移动端游戏测试

| 平台 | 插件 | 特点 |
|-----|------|------|
| Android | android_ui_verification | ADB 自动化 |
| Android | ADB Skill | 设备控制/截图/日志 |
| iOS | ios-simulator-skill | ⭐ 557 模拟器集成 |

#### Android ADB 核心功能

- 设备校准
- UI 检查
- 交互命令
- 截图验证
- 日志分析

### 4.4 测试方案对比

| 测试类型 | 推荐方案 | 优点 | 局限 |
|---------|---------|------|------|
| Web/H5 游戏 | Playwright MCP | 功能强大 | 需 Web 环境 |
| Unity 单元测试 | Unity Test Framework | 专业集成 | 需 Unity |
| Unity 集成测试 | Unity PlayMode | 完整测试 | 性能较慢 |
| Android 游戏 | Android ADB | 设备控制 | 需 SDK |
| iOS 游戏 | iOS Simulator | 原生模拟器 | macOS only |
| UI 交互 | Playwright + 截图 | 直观 | 维护成本 |

---

## 五、其他开发者工具插件深度分析

### 5.1 版本控制与 Git

| 插件 | GitHub Stars | 功能 |
|-----|-------------|------|
| GitHub MCP Server | ⭐ 活跃 | 官方 GitHub 集成 |
| git-mcp-server | 官方 | Git 操作 |
| claude-tmux | 活跃 | tmux 会话管理 |

#### GitHub MCP 核心功能

- 仓库操作
- Issue 管理
- PR 创建和审查
- Actions 触发
- 代码搜索

### 5.2 代码文档服务

| 插件 | GitHub Stars | 支持框架 |
|-----|-------------|----------|
| Context7 MCP Server | ⭐ 活跃 | 50+ 框架 |

#### Context7 特点

- 实时更新的代码文档
- 无需 API Key
- 支持 50+ 主流框架
- 本地缓存

### 5.3 浏览器开发工具

| 插件 | GitHub Stars | 功能 |
|-----|-------------|------|
| Chrome DevTools MCP | ⭐ 活跃 | 浏览器自动化 |
| Chrome DevTools | 官方 | 开发者工具集成 |

### 5.4 开发者效率工具

#### Superpowers (⭐ 4.1k+)

| 功能 | 说明 |
|------|------|
| 规划 | 项目规划和任务分解 |
| 审查 | 代码审查和质量把关 |
| 测试 | 单元测试和集成测试 |
| 调试 | 问题定位和修复 |

#### AgentSys (⭐ 500+)

| 功能 | 说明 |
|------|------|
| 任务自动化 | 任务到生产工作流 |
| PR 管理 | 自动化 PR 处理 |
| 代码清理 | 自动代码优化 |
| 性能调查 | 性能问题诊断 |
| 漂移检测 | 配置漂移监控 |
| 多代理审查 | 团队代码审查 |

### 5.5 安全工具

| 插件 | 功能 | 评分 |
|-----|------|------|
| Parry | Prompt 注入扫描 | 安全防护 |
| Dippy | AST 命令批准 | 安全+效率 |
| Trail of Bits Skills | 安全审计 | ⭐ 专业级 |

#### Parry 核心功能

- 扫描工具输入/输出
- 检测注入攻击
- 敏感信息检测
- 数据泄露防护

#### Dippy 核心功能

- AST 命令解析
- 自动批准安全命令
- 危险操作提醒
- 支持 Claude Code/Gemini CLI/Cursor

### 5.6 Claude Scientific Skills

| 插件 | GitHub Stars | 适用人群 |
|-----|-------------|----------|
| claude-scientific-skills | 活跃 | 科研工作者 |

#### 核心功能

- 研究技能
- 科学分析
- 工程计算
- 数据分析
- 金融建模
- 学术写作

### 5.7 项目管理与工作流

| 插件 | GitHub Stars | 特点 |
|-----|-------------|------|
| Claude Code PM | 活跃 | 专业项目管理 |
| Claude CodePro | 活跃 | TDD 强制 |
| cc-devops-skills | 活跃 | IaC 代码生成 |

### 5.8 新兴热门插件 (2026年3月)

| 插件 | GitHub Stars | 特点 |
|-----|-------------|------|
| ClaudeForge | 活跃 | CLAUDE.md 生成器 |
| skyll | 活跃 | 技能自主发现学习 |
| n8n-mcp | 活跃 | n8n 工作流构建 |
| serena | 活跃 | 语义检索编辑 |
| ruflo | 活跃 | 多代理编排平台 |

---

## 六、快速推荐

### 游戏客户端开发推荐

| 插件 | 推荐指数 | 适用场景 |
|------|----------|----------|
| cc-plugin-unity-gamedev | ⭐⭐⭐⭐⭐ | Unity 完整开发 |
| Unreal-MCP | ⭐⭐⭐⭐⭐ | Unreal AAA 开发 |
| Godot GDScript MCP | ⭐⭐⭐⭐ | Godot 轻量级开发 |
| gamemaker-skills | ⭐⭐⭐ | GameMaker 2D |

### Python 开发推荐

| 插件 | 推荐指数 | 适用场景 |
|------|----------|----------|
| FastAPI MCP | ⭐⭐⭐⭐⭐ | 现代 Web 开发 |
| Django MCP | ⭐⭐⭐⭐ | 企业 Web 开发 |
| pydantic-ai-skills | ⭐⭐⭐⭐⭐ | AI 应用开发 |
| aws-mcp-server | ⭐⭐⭐⭐⭐ | AWS 云服务 |
| read-only-postgres | ⭐⭐⭐⭐ | 安全数据库查询 |

### 自动化测试推荐

| 插件 | 推荐指数 | 适用场景 |
|------|----------|----------|
| Playwright MCP | ⭐⭐⭐⭐⭐ | Web E2E 测试 |
| Unity Test Framework | ⭐⭐⭐⭐ | Unity 单元测试 |
| Android ADB | ⭐⭐⭐⭐ | Android 测试 |
| iOS Simulator | ⭐⭐⭐⭐ | iOS 测试 |

### 开发者工具推荐

| 插件 | 推荐指数 | 适用场景 |
|------|----------|----------|
| GitHub MCP | ⭐⭐⭐⭐⭐ | GitHub 集成 |
| Context7 MCP | ⭐⭐⭐⭐⭐ | 文档服务 |
| Superpowers | ⭐⭐⭐⭐⭐ | 核心工程技能 |
| AgentSys | ⭐⭐⭐⭐⭐ | 工作流自动化 |
| Parry/Dippy | ⭐⭐⭐⭐ | 安全防护 |

---

## 七、安装指南

### MCP 服务器安装

```bash
# Python (pip)
pip install fastapi-mcp-server
pip install aws-mcp-server
pip install pytest-mcp-server

# Node.js (npm)
npm install -g @github/mcp-server
npm install -g @context7/mcp-server
npm install -g @anthropic/playwright-mcp-server

# Claude Desktop 配置
# ~/.config/claude-desktop/mcp.json
{
  "mcpServers": {
    "github": {
      "command": "npx",
      "args": ["-y", "@github/mcp-server"]
    },
    "playwright": {
      "command": "npx", 
      "args": ["-y", "@anthropic/playwright-mcp-server"]
    }
  }
}
```

### 技能安装

```bash
# 克隆技能仓库
git clone https://github.com/tjboudreaux/cc-plugin-unity-gamedev ~/.claude/plugins/
git clone https://github.com/obra/superpowers ~/.claude/plugins/
git clone https://github.com/avifenesh/agentsys ~/.claude/plugins/
```

---

## 八、总结

### 关键发现

1. **游戏开发**: Unity 技能最成熟 (21 技能)，Unreal-MCP 是 AAA 开发首选
2. **Python 开发**: FastAPI MCP 和 Pydantic AI Skills 最受欢迎
3. **测试自动化**: Playwright MCP 是 Web 测试标准方案
4. **开发者工具**: Superpowers (4.1k+ stars) 提供最完整工程实践
5. **安全工具**: Parry 和 Dippy 提供双重安全防护

### 生态趋势

- MCP 服务器数量快速增长 (8566+ 仓库)
- 技能专业化程度提高
- 跨平台支持增强
- 安全性越来越受重视

---

> 调研时间：2026年3月4日
> 数据来源：awesome-claude-code、GitHub Topics、ClawHub
