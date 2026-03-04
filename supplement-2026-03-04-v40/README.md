# Claude Code 插件调研 - 第四十期

> 聚焦：游戏客户端开发、Python开发、游戏客户端自动化测试、开发者工具

## 调研时间
2026-03-04

## 数据来源
- awesome-claude-code (hesreallyhim/awesome-claude-code)
- GitHub Topics: claude-code-skills
- VoltAgent/awesome-agent-skills (500+ 官方技能)
- 各技术栈官方技能库

---

## 一、游戏客户端开发技能

### 1.1 Claude Code Game Studios ⭐⭐⭐⭐⭐

| 项目 | 说明 |
|-----|------|
| **GitHub** | [Donchitos/Claude-Code-Game-Studios](https://github.com/Donchitos/Claude-Code-Game-Studios) |
| **Star** | ⭐ 26-30 |
| **更新** | 活跃 (3天内) |
| **License** | MIT |

#### 核心能力

- **48个专业AI代理**: 覆盖游戏开发全流程（设计、编程、测试、部署）
- **36个工作流技能**: 完整游戏开发管线
- **工作室协调系统**: 模拟真实游戏工作室工作流
- **多引擎支持**: Unity, Unreal, Godot, WebGL, Custom Engines

#### 技能分类

| 分类 | 数量 | 示例 |
|-----|------|------|
| 游戏设计 | 8 | 关卡设计、叙事设计、系统设计 |
| 编程开发 | 12 | 核心机制、网络同步、UI系统 |
| 美术/音频 | 6 | 材质、着色器、音频集成 |
| 测试/QA | 8 | 单元测试、集成测试、性能测试 |
| 运维/部署 | 6 | CI/CD、版本管理、热更新 |

#### 适用场景

- ✅ 大型游戏项目开发
- ✅ 游戏工作室工作流自动化
- ✅ 跨团队协作开发
- ✅ 全栈游戏开发
- ❌ 小型项目（过度设计）

#### 本地部署

```bash
git clone https://github.com/Donchitos/Claude-Code-Game-Studios.git ~/.claude/plugins/game-studios
```

---

### 1.2 Unity 开发技能集

#### cc-plugin-unity-gamedev

| 项目 | 说明 |
|-----|------|
| **GitHub** | [tjboudreaux/cc-plugin-unity-gamedev](https://github.com/tjboudreaux/cc-plugin-unity-gamedev) |
| **Star** | ⭐ 1 |
| **技能数** | 21个专业技能 |

**技能分类:**

| 分类 | 技能 |
|-----|------|
| **工具类(8)** | Addressables, MemoryPack, ScriptableObjects, Profiling, IL2CPP, Burst Compiler, Entities, URP |
| **动画/物理(5)** | Animation, Physics, NavMesh, Object Pooling, State Machine |
| **AI/行为(2)** | Behavior Designer, GAS (Gameplay Ability System) |
| **音视频(2)** | Wwise音频, Cinemachine相机 |
| **UI(2)** | UGUI, Mobile Optimization |
| **测试(1)** | Unity Test Framework |
| **DI/异步(1)** | VContainer, UniTask |

#### OH-Unity-GameDev-Skills

| 项目 | 说明 |
|-----|------|
| **GitHub** | [OstrichHermit/OH-Unity-GameDev-Skills](https://github.com/OstrichHermit/OH-Unity-GameDev-Skills) |
| **Star** | ⭐ 6 |

**特点:**
- Unity基础开发技能
- DoTween动画系统
- MediaPipe机器学习集成
- 适合初学者入门

#### unity-ai-workflow

| 项目 | 说明 |
|-----|------|
| **GitHub** | [David-GD13/unity-ai-workflow](https://github.com/David-GD13/unity-ai-workflow) |
| **Star** | ⭐ 4 |
| **要求** | Unity 6.2+ |

**特点:**
- AI-first开发工作流
- 现代化Unity开发实践
- 适合Unity 6新项目

---

### 1.3 Unreal Engine 技能

#### unreal-claude-skills

| 项目 | 说明 |
|-----|------|
| **GitHub** | [search: unreal claude code skills](https://github.com/topics/unreal-engine) |
| **Star** | 较少 |

**现状:**
- Unreal Engine 相关 Claude Code 技能相对较少
- 社区仍在发展中
- 推荐使用官方文档 + CLAUDE.md 配合

---

### 1.4 Godot 技能

#### godot-claude-integration

| 项目 | 说明 |
|-----|------|
| **GitHub** | [HenreK/GDScript-Code-Agent](https://github.com/HenreK/GDScript-Code-Agent) |
| **Star** | ⭐ 15+ |

**特点:**
- GDScript 代码生成
- Godot 4.x 最佳实践
- 节点和场景结构指导

---

## 二、Python 开发技能

### 2.1 Python MCP Server (官方)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [modelcontextprotocol/python-mcp-server](https://github.com/modelcontextprotocol/python-mcp-server) |
| **Star** | ⭐ 2000+ |
| **官方** | ✅ Anthropic |

#### 核心功能

- **Python执行**: 安全运行Python代码
- **包管理**: pip, uv, poetry 集成
- **虚拟环境**: venv, conda 支持
- **类型检查**: mypy 集成
- **代码格式化**: black, ruff 集成

#### 安装

```bash
pip install mcp-server-python
# 或
uvx mcp-server-python
```

#### 配置 (claude_desktop_config.json)

```json
{
  "mcpServers": {
    "python": {
      "command": "uvx",
      "args": ["mcp-server-python"]
    }
  }
}
```

---

### 2.2 Python 开发最佳实践

#### aws-mcp-server (含Python开发指南)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [alexei-led/aws-mcp-server](https://github.com/alexei-led/aws-mcp-server) |
| **Star** | ⭐ 1350+ |
| **CLAUDE.md** | ✅ 包含详细Python开发规范 |

**Python开发规范亮点:**

```python
# 1. 环境设置
- 多种Python环境选项
- 虚拟环境管理
- 依赖版本锁定

# 2. 代码风格
- PEP 8 严格遵循
- 类型注解要求
- 文档字符串规范

# 3. 错误处理
- 自定义异常类
- 上下文管理器使用
- 日志记录最佳实践

# 4. 安全考虑
- 密钥管理
- 输入验证
- SQL注入防护
```

---

### 2.3 Python 测试技能

#### /tdd Slash Command

| 项目 | 说明 |
|-----|------|
| **来源** | zscott/pane |
| **功能** | 测试驱动开发引导 |

**TDD流程:**

1. **Red** - 编写失败的测试
2. **Green** - 编写最小化代码使测试通过
3. **Refactor** - 重构代码

#### /tdd-implement Slash Command

| 项目 | 说明 |
|-----|------|
| **来源** | jerseycheese/Narraitor |
| **功能** | 完整TDD实现流程 |

**特点:**
- 需求分析
- 测试优先
- 增量实现
- 持续重构

---

### 2.4 Python 项目推荐

#### EDSL (Expected Parrot)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [expectedparrot/edsl](https://github.com/expectedparrot/edsl) |
| **Star** | 活跃 |
| **特点** | 严格代码规范 |

**Python开发规范:**
- Black 格式化
- mypy 类型检查
- pytest 测试要求
- comprehensive testing guidelines

#### SPy (Python解释器)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [spylang/spy](https://github.com/spylang/spy) |
| **Star** | 活跃 |
| **特点** | 严格的测试要求 |

---

## 三、游戏客户端自动化测试

### 3.1 Playwright MCP (Web/游戏Web版)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [Playwright/mcp-playwright](https://github.com/Playwright/mcp-playwright) |
| **Star** | ⭐ 3000+ |
| **官方** | ✅ Microsoft |

#### 核心功能

- **浏览器自动化**: 完整浏览器控制
- **UI测试**: Web应用端到端测试
- **截图/录制**: 视觉回归测试基础
- **移动端模拟**: 响应式游戏测试

#### 适用场景

- ✅ WebGL游戏测试
- ✅ HTML5游戏测试
- ✅ 游戏官网测试
- ✅ 游戏内嵌Web视图测试

#### 安装配置

```bash
npm install -g @playwright/mcp-server
# 或
npx @playwright/mcp-server
```

---

### 3.2 游戏自动化测试框架

#### 游戏测试 MCP 技能

| 技能 | 用途 |
|-----|------|
| **UI自动化** | 游戏界面交互测试 |
| **API测试** | 游戏后端接口验证 |
| **性能测试** | 帧率、内存、CPU监控 |
| **网络测试** | 延迟、丢包模拟 |
| **回归测试** | 版本对比测试 |

#### 游戏特定测试挑战

| 挑战 | 解决方案 |
|-----|----------|
| **图形渲染** | 截图对比 + 视觉回归 |
| **音频** | 音频指纹对比 |
| **多人同步** | 帧同步/状态同步测试 |
| **随机性** | 种子复现测试 |
| **性能** | 持续性能监控 |

---

### 3.3 测试最佳实践

#### AgentSys 工作流自动化

| 项目 | 说明 |
|-----|------|
| **GitHub** | [avifenesh/agentsys](https://github.com/avifenesh/agentsys) |
| **Star** | ⭐ 活跃 |
| **测试相关** | ✅ 代码清理、性能调查、漂移检测 |

**测试自动化能力:**

- 自动化测试生成
- 性能调查分析
- 代码漂移检测
- 多代理代码审查
- PR管理集成

#### TDD Guard Hook

| 项目 | 说明 |
|-----|------|
| **GitHub** | [nizos/tdd-guard](https://github.com/nizos/tdd-guard) |
| **功能** | 强制TDD原则的Hook |

**功能:**
- 实时监控文件操作
- 阻止违反TDD原则的更改
- 测试先行 enforcement

---

## 四、开发者工具技能

### 4.1 Superpowers (核心工程技能集)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [obra/superpowers](https://github.com/obra/superpowers) |
| **Star** | ⭐ 4100+ |
| **维护** | 活跃 |

#### 核心技能覆盖

| 领域 | 技能 |
|-----|------|
| **规划** | 需求分析、任务分解 |
| **审查** | 代码审查、最佳实践 |
| **测试** | 单元测试、集成测试 |
| **调试** | 问题定位、日志分析 |
| **部署** | CI/CD、发布流程 |

#### 特点

- ✅ 广泛的SDLC覆盖
- ✅ 代码质量优先
- ✅ 最佳实践整合
- ✅ 适配性强
- ⚠️ 学习曲线较陡

---

### 4.2 Claude Code Tools (会话工具)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [pchalasani/claude-code-tools](https://github.com/pchalasani/claude-code-tools) |
| **Star** | ⭐ 活跃 |

#### 核心功能

1. **会话连续性**: 避免上下文压缩
2. **跨代理切换**: Claude Code ↔ Codex CLI
3. **全文搜索**: Rust/Tantivy 快速搜索
4. **Tmux集成**: 终端会话管理
5. **安全Hook**: 危险命令拦截

#### 安装

```bash
# 方式1: 直接克隆
git clone https://github.com/pchalasani/claude-code-tools.git ~/.claude/plugins/cc-tools

# 方式2: npm
npm install -g claude-code-tools
```

---

### 4.3 AgentSys (工作流自动化)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [avifenesh/agentsys](https://github.com/avifenesh/agentsys) |
| **Star** | ⭐ 活跃 (v5.3.7) |
| **代码量** | 数千行 + 数千测试 |

#### 核心能力

| 功能 | 说明 |
|-----|------|
| **任务自动化** | 任务到生产工作流 |
| **PR管理** | 自动化Pull Request流程 |
| **代码清理** | 自动化代码规范 |
| **性能调查** | 性能问题定位 |
| **漂移检测** | 配置漂移监控 |
| **多代理审查** | 并行代码审查 |

#### 架构特点

- **确定性检测**: Regex + AST
- **LLM判断**: 智能推理
- **生产验证**: 多生产系统使用

---

### 4.4 Claude Code Settings (开发环境)

| 项目 | 说明 |
|-----|------|
| **GitHub** | [fcakyon/claude-codex-settings](https://github.com/fcakyon/claude-codex-settings) |
| **Star** | ⭐ 活跃 |
| **版本** | v2.1.0 |

#### 支持平台

| 平台 | 集成 |
|-----|------|
| **云服务** | GitHub, Azure, MongoDB |
| **AI服务** | Tavily, OpenAI |
| **测试** | Playwright |
| **部署** | 主流CI/CD |

---

### 4.5 Trail of Bits 安全技能

| 项目 | 说明 |
|-----|------|
| **GitHub** | [trailofbits/skills](https://github.com/trailofbits/skills) |
| **Star** | ⭐ 专业级 |
| **数量** | 12+ 安全技能 |

#### 安全技能分类

| 技能 | 功能 |
|-----|------|
| **CodeQL** | 静态分析 |
| **Semgrep** | 代码模式匹配 |
| **变体分析** | 跨代码库漏洞查找 |
| **修复验证** | 漏洞修复确认 |
| **差异审查** | 代码变更安全审查 |

#### 适用场景

- ✅ 安全审计
- ✅ 漏洞检测
- ✅ 代码加固
- ✅ 合规检查

---

## 五、MCP 服务器生态

### 5.1 热门MCP服务器

| 服务器 | GitHub Star | 用途 |
|--------|-------------|------|
| **playwright-mcp** | ⭐ 3000+ | 浏览器自动化 |
| **aws-mcp-server** | ⭐ 1350+ | AWS云服务 |
| **python-mcp-server** | ⭐ 2000+ | Python执行 |
| **filesystem-mcp** | ⭐ 1000+ | 文件系统访问 |

### 5.2 MCP服务器安装

```bash
# 使用 npx
npx -y <mcp-server-name>

# 使用 uvx
uvx mcp-server-<name>

# 使用 npm
npm install -g @<org>/mcp-server-<name>
```

---

## 六、总结与建议

### 6.1 技能推荐矩阵

| 方向 | 推荐技能 | 优先级 |
|------|----------|--------|
| **游戏开发** | Claude Code Game Studios | ⭐⭐⭐⭐⭐ |
| **Unity开发** | cc-plugin-unity-gamedev | ⭐⭐⭐⭐ |
| **Python开发** | python-mcp-server | ⭐⭐⭐⭐⭐ |
| **游戏测试** | playwright-mcp | ⭐⭐⭐⭐ |
| **工程实践** | Superpowers | ⭐⭐⭐⭐⭐ |
| **安全审计** | Trail of Bits | ⭐⭐⭐⭐ |

### 6.2 学习路径建议

```
新手入门:
├── 1. 安装 python-mcp-server
├── 2. 学习 Superpowers 基础技能
└── 3. 配置 claude-code-tools

进阶技能:
├── 1. 游戏开发 → Claude Code Game Studios
├── 2. Unity开发 → cc-plugin-unity-gamedev  
├── 3. 测试开发 → TDD Guard + Playwright
└── 4. 安全审计 → Trail of Bits

专家级:
├── 1. AgentSys 工作流自动化
├── 2. 多代理协作
└── 3. 自定义技能开发
```

### 6.3 注意事项

1. **安全审查**: 安装第三方技能前检查代码
2. **版本兼容**: 确认与当前Claude Code版本兼容
3. **社区活跃度**: 优先选择活跃维护的项目
4. **文档质量**: 选择有良好文档的技能

---

## 参考链接

- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
- [VoltAgent/awesome-agent-skills](https://github.com/VoltAgent/awesome-agent-skills)
- [GitHub: claude-code-skills](https://github.com/topics/claude-code-skills)
- [Claude Code 官方文档](https://docs.anthropic.com/en/docs/claude-code)
