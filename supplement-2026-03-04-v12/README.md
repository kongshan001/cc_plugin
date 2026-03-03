# Claude Code 插件调研报告 - 补充调研第十四期

> 持续跟踪 Claude Code 生态热门插件，聚焦游戏开发、Python 开发、自动化测试、开发者工具方向

---

## 📋 本期调研概要

| 维度 | 统计 |
|-----|------|
| **调研时间** | 2026-03-04 |
| **覆盖方向** | 游戏开发、Python开发、自动化测试、开发者工具 |
| **新增技能** | 30+ |
| **数据来源** | awesome-claude-code, GitHub trending |

---

## 一、最新热门插件 (2026年3月)

### 1.1 Claude Scientific Skills ⭐ NEW

| 项目 | 说明 |
|-----|------|
| **GitHub** | [K-Dense-AI/claude-scientific-skills](https://github.com/K-Dense-AI/claude-scientific-skills) |
| **Star** | ⭐ 大量 |
| **特点** | 科学研究、工程、分析、金融和写作的即用型代理技能 |

#### 核心能力

```python
# 科学研究技能示例
from claude_scientific import ResearchAgent, AnalysisTool

# 1. 文献综述
researcher = ResearchAgent()
paper_summary = await researcher.summarize_literature(
    query="machine learning game AI",
    max_papers=50
)

# 2. 数据分析
analysis = AnalysisTool()
results = analysis.execute(
    data="experiment_results.csv",
    method="statistical_test",
    confidence=0.95
)

# 3. 数学建模
model = MathematicalModel()
solution = model.solve(
    equations=["f(x) = x^2 + 2x + 1"],
    domain="real"
)
```

### 1.2 Parry - 提示注入扫描器

| 项目 | 说明 |
|-----|------|
| **GitHub** | [vaporif/parry](https://github.com/vaporif/parry) |
| **特点** | Claude Code Hooks 的提示注入扫描器 |

#### 核心功能

```typescript
// Hook 配置示例
{
  "hooks": {
    "Notify": [
      {
        "matcher": ".*",
        "hooks": ["parry-scan"]
      }
    ]
  }
}

// Parry 扫描类型
- 提示注入攻击
- 敏感信息泄露
- 数据外泄尝试
- 恶意命令注入
```

### 1.3 Dippy - 智能安全批准

| 项目 | 说明 |
|-----|------|
| **GitHub** | [ldayton/Dippy](https://github.com/ldayton/Dippy) |
| **特点** | AST 自动批准安全命令，提示危险操作 |
| **支持** | Claude Code, Gemini CLI, Cursor |

#### 工作原理

```python
# 安全命令自动批准
# ls, cat, git status ✓
# rm -rf / ✗ (需要确认)

# AST 解析示例
class CommandAnalyzer:
    def analyze(self, cmd: str) -> CommandSafety:
        tree = self.parse(cmd)
        
        # 检查危险操作
        if self.is_destructive(tree):
            return CommandSafety.PROMPT
        if self.is_safe(tree):
            return CommandSafety.APPROVE
        return CommandSafety.UNKNOWN
```

### 1.4 Sudocode - 轻量级编排工具

| 项目 |说明 |
|-----|------|
| **GitHub** | [sudocode-ai/sudocode](https://github.com/sudocode-ai/sudocode) |
| **特点** | 轻量级 agent 编排工具，集成各种规范框架 |

#### 特性

```yaml
# sudocode 配置
orchestrator:
  name: "Game Development"
  agents:
    - role: "game-designer"
      prompt: "设计游戏玩法和机制"
    - role: "backend-dev"
      prompt: "开发游戏后端服务"
    - role: "qa-engineer"
      prompt: "编写测试用例"

  workflow:
    - designer → backend-dev
    - backend-dev → qa-engineer
    - qa-engineer → designer (反馈循环)
```

### 1.5 Claude-tmux - 会话管理

| 项目 | 说明 |
|-----|------|
| **GitHub** | [nielsgroen/claude-tmux](https://github.com/nielsgroen/claude-tmux) |
| **特点** | 在 tmux 中管理 Claude Code |

#### 功能

- tmux 弹出窗口显示所有 Claude Code 实例
- 快速切换
- 状态监控
- 会话生命周期管理
- git worktree 支持
- PR 支持

### 1.6 Claude-esp - 隐藏输出流式传输

| 项目 | 说明 |
|-----|------|
| **GitHub** | [phiat/claude-esp](https://github.com/phiat/claude-esp) |
| **特点** | Go 编写的 TUI，将 Claude Code 隐藏输出流式传输到独立终端 |

---

## 二、游戏客户端开发技能 (更新)

### 2.1 Claude Code Game Studios

| 项目 | 说明 |
|-----|------|
| **GitHub** | [Donchitos/Claude-Code-Game-Studios](https://github.com/Donchitos/Claude-Code-Game-Studios) |
| **Star** | ⭐ 26 |
| **特点** | 48个AI代理 + 36个工作流技能 + 完整协调系统 |

#### 支持引擎

- Unity
- Unreal Engine
- Godot
- WebGL

### 2.2 Unity 开发技能汇总

| 技能 | Star | 特点 |
|-----|------|------|
| cc-plugin-unity-gamedev | ⭐1 | 21个专业技能 |
| OH-Unity-GameDev-Skills | ⭐6 | Unity基础+DoTween+MediaPipe |
| unity-ai-workflow | ⭐4 | Unity 6.2+ AI-first工作流 |
| Claude-Code-Game-Studios | ⭐26 | 全栈覆盖 |

### 2.3 Web/H5 游戏开发

#### 引擎选择

| 引擎 | 适用场景 | WebGPU 支持 |
|------|----------|-------------|
| Phaser 4 | 2D 完整引擎 | ✅ |
| PixiJS 8 | 2D 原始渲染 | ✅ |
| Babylon.js 7 | 3D + 物理 + XR | ✅ |
| Three.js | 3D 渲染 | ✅ |

---

## 三、Python 开发技能 (更新)

### 3.1 Pydantic AI Skills

| 项目 | 说明 |
|-----|------|
| **GitHub** | [DougTrajano/pydantic-ai-skills](https://github.com/DougTrajano/pydantic-ai-skills) |
| **Star** | ⭐ 136 |

#### 核心能力

- 类型安全：Pydantic 模型强制类型检查
- 渐进式提示：按需披露信息
- AI 集成：与主流 LLM 无缝集成
- 验证系统：内置强大的数据验证

### 3.2 uv - Python 包管理器

| 项目 | 说明 |
|-----|------|
| **GitHub** | [astral-sh/uv](https://github.com/astral-sh/uv) |
| **特点** | 10-100x faster than pip |

```bash
# 安装
curl -LsSf https://astral.sh/uv/install.sh | sh

# 项目初始化
uv init my-project
uv venv
uv pip install -r requirements.txt
```

### 3.3 PostgreSQL 只读查询

| 技能 | 功能 | 安全性 |
|-----|------|--------|
| read-only-postgres | PostgreSQL 只读查询 | ⭐⭐⭐⭐⭐ |
| postgres | PostgreSQL 完整集成 | ⭐⭐⭐ |

---

## 四、自动化测试技能 (更新)

### 4.1 Playwright 技能

| 技能 | GitHub | Star | 功能 |
|-----|--------|------|------|
| playwright-skill | lackeyjb/playwright-skill | ⭐1.8k | Playwright 浏览器自动化 |
| playwright-undetected-skill | dalbit-mir/playwright-undetected-skill | ⭐4 | Bot 检测绕过 |

### 4.2 游戏客户端测试方案

| 测试类型 | 方案 | 适用场景 |
|---------|------|---------|
| Web/H5游戏 | Playwright | 功能测试、回归测试 |
| Unity游戏 | Unity Test Framework | 单元测试、集成测试 |
| 性能测试 | Unity Profiler | 帧率、内存测试 |
| Android游戏 | ADB + uiautomator | UI自动化 |
| iOS游戏 | ios-simulator-skill | 模拟器测试 |

---

## 五、开发者工具 (更新)

### 5.1 安全审计工具

| 技能 | GitHub | 特点 |
|-----|--------|------|
| trailofbits-skills | trailofbits/skills | CodeQL/Semgrep 集成 |
| parry | vaporif/parry | 提示注入扫描器 |
| Dippy | ldayton/Dippy | AST 自动批准安全命令 |

### 5.2 DevOps 工具

| 技能 | GitHub | 特点 |
|-----|--------|------|
| cc-devops-skills | akin-ozer/cc-devops-skills | IaC 代码生成 |
| ContextKit | FlineDev/ContextKit | 4 阶段规划方法论 |

### 5.3 Hooks 生态系统

| 技能 | GitHub | 语言 |
|-----|--------|------|
| claude-hooks | johnlindquist/claude-hooks | TypeScript |
| cchooks | GowayLee/cchooks | Python |
| claude-code-hooks-sdk | beyondcode/claude-hooks-sdk | PHP |

---

## 六、技能组合推荐

### 6.1 游戏后端开发

```
推荐: /python-pro + /python-fastapi-development
     /async-python-patterns + /temporal-python-pro
     /aws-serverless + /aws-cost-optimizer
```

### 6.2 游戏客户端开发

```
推荐: /unity-developer + /unity-ecs-patterns (性能)
     /godot-gdscript-patterns + /godot-4-migration
     /unreal-engine-cpp-pro + /game-development
```

### 6.3 自动化测试

```
推荐: /e2e-testing + /e2e-testing-patterns
     /browser-automation + /api-security-testing
     /python-testing-patterns
```

### 6.4 安全开发

```
推荐: /parry + /Dippy
     /trailofbits-skills
     /api-security-testing
```

---

## 📚 参考资源

- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)
- [awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills)
- [Claude Code 官方文档](https://docs.anthropic.com/en/docs/claude-code/overview)

---

*文档更新: 2026-03-04*
