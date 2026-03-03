# Claude Code 游戏客户端自动化测试技能调研

## 📋 文档信息

- **调研日期**: 2026-03-03
- **分类**: 游戏测试 / 自动化测试 / Web 开发 / Playwright
- **状态**: ✅ 已调研

---

## 1. 浏览器自动化测试

### 1.1 Playwright Skill

| 项目 | 说明 |
|-----|------|
| **GitHub** | [lackeyjb/playwright-skill](https://github.com/lackeyjb/playwright-skill) |
| **Star** | ⭐ 1.8k |
| **功能** | Playwright 浏览器自动化 |
| **特点** | 模型调用的 Playwright 自动化 |

### 核心功能

- **Web 应用测试**: 自动化测试 Web 应用功能
- **UI 验证**: 验证前端功能和行为
- **截图捕获**: 自动截图记录测试状态
- **调试支持**: 辅助调试 UI 行为
- **Bot 检测绕过**: Patchright 支持反检测

### 技术架构

```
用户请求 → Claude Code → Playwright Skill → 浏览器自动化
                                        ↓
                              测试结果/截图 → 返回 Claude
```

### 适用场景

- Web 游戏测试
- H5 游戏测试
- 前端功能验证
- UI 自动化测试
- 回归测试

---

### 1.2 Playwright Undetected Skill

| 项目 | 说明 |
|-----|------|
| **GitHub** | [dalbit-mir/playwright-undetected-skill](https://github.com/dalbit-mir/playwright-undetected-skill) |
| **Star** | ⭐ 4 |
| **特点** | Bot 检测绕过 |

### 核心功能

- **本地主机测试**: Localhost 测试
- **截图捕获**: UI 交互截图
- **UI 交互**: 模拟真实用户操作
- **反检测**: Patchright 绕过检测

### 适用场景

- 需要绕过 bot 检测的测试
- 复杂 Web 应用测试
- 登录流程测试

---

### 1.3 Webapp Testing

| 项目 | 说明 |
|-----|------|
| **GitHub** | [ComposioHQ/awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills) |
| **功能** | 本地 Web 应用测试 |
| **依赖** | Playwright |
| **特点** | 端到端测试能力 |

### 核心功能

- **本地测试**: 测试本地运行的 Web 应用
- **功能验证**: 验证前端功能正常
- **UI 调试**: 调试 UI 行为问题
- **截图记录**: 捕获测试截图

### 使用示例

```bash
# 触发技能
"测试一下本地 Web 应用的用户登录功能"
```

Claude Code 会：
1. 启动 Playwright
2. 导航到目标页面
3. 执行测试操作
4. 验证结果
5. 报告测试状态

---

## 2. 软件工程测试技能

### 2.1 Claude Skills Marketplace

| 项目 | 说明 |
|-----|------|
| **GitHub** | [mhattingpete/claude-skills-marketplace](https://github.com/mhattingpete/claude-skills-marketplace) |
| **Star** | ⭐ 427 |
| **功能** | 软件工程工作流技能 |

### 核心功能

- **Git 自动化**: Git 操作自动化
- **测试技能**: 多种测试技能
- **代码审查**: 自动化代码审查

### 测试相关技能

| 技能名称 | 功能 |
|---------|------|
| **test-fixing** | 测试修复 |
| **test-writing** | 测试编写 |
| **test-running** | 测试运行 |
| **bug-finding** | Bug 查找 |

---

### 2.2 Fieldwork Skills

| 项目 | 说明 |
|-----|------|
| **GitHub** | [buildoak/fieldwork-skills](https://github.com/buildoak/fieldwork-skills) |
| **Star** | ⭐ 12 |
| **特点** | 生产级测试技能 |

### 核心功能

- **端到端测试**: 完整测试流程
- **Bug 修复**: 自动化 Bug 修复
- **质量保证**: 代码质量检查

---

## 3. Unity 测试技能

### 3.1 Unity Test Framework Skill

| 项目 | 说明 |
|-----|------|
| **来源** | cc-plugin-unity-gamedev |
| **功能** | Unity 单元测试 |

### 核心功能

- **EditMode 测试**: 编辑器模式测试
- **PlayMode 测试**: 运行时测试
- **异步测试**: 异步代码测试
- **Mocking**: 测试模拟

### 技术特点

```csharp
// EditMode 测试
[Test]
public void TestEditMode() { }

// PlayMode 测试
[UnityTest]
public IEnumerator TestPlayMode() { }

// 异步测试
[UnityTest]
public IEnumerator TestAsync() { }
```

---

## 4. 游戏客户端测试方案

### 现有技能对比

| 技能 | 适用场景 | 优点 | 局限 |
|-----|---------|------|------|
| **Playwright** | Web 游戏/H5 游戏 | 功能强大生态好 | 需 Web 环境 |
| **Webapp Testing** | Web 应用测试 | 集成度高 | 依赖 Playwright |
| **iOS Simulator** | iOS 游戏测试 | 原生集成 | 仅限 iOS |
| **Unity Test** | Unity 游戏测试 | 专业集成 | 需 Unity |

### 游戏测试扩展方案

针对游戏客户端测试，可以结合以下技能：

1. **截图对比**: 使用 Playwright 的截图功能
2. **UI 交互**: Playwright 模拟用户操作
3. **API 验证**: 结合 API 测试技能验证后端
4. **性能监控**: 配合性能分析技能

---

## 5. 自动化开发技能

### 5.1 Claude Auto Dev

| 项目 | 说明 |
|-----|------|
| **GitHub** | [djnsty23/claude-auto-dev](https://github.com/djnsty23/claude-auto-dev) |
| **Star** | ⭐ 2 |
| **特点** | 自主开发技能 |

### 核心功能

- **任务循环**: 自动化任务处理
- **测试自动化**: 自动化测试
- **部署自动化**: CI/CD 集成

---

### 5.2 My Claude Skills

| 项目 | 说明 |
|-----|------|
| **GitHub** | [brody-0125/my-claude-skills](https://github.com/brody-0125/my-claude-skills) |
| **Star** | ⭐ 2 |

### 核心功能

- **实现工作流**: 开发实现流程
- **测试自动化**: 测试相关技能
- **架构路由**: 架构决策辅助
- **数值验证**: 数值计算验证

---

## 6. 部署指南

### 安装 Playwright

```bash
# 安装 Playwright
npm install -g playwright
playwright install chromium

# 或使用 Python 版本
pip install playwright
playwright install
```

### 安装 Playwright Skill

```bash
# 克隆技能仓库
git clone https://github.com/lackeyjb/playwright-skill.git

# 复制到技能目录
cp -r playwright-skill ~/.claude/skills/
```

### 安装反检测版本

```bash
# 克隆反检测版本
git clone https://github.com/dalbit-mir/playwright-undetected-skill.git

# 安装 Patchright
npm install -g @anthropic-ai/patchright

# 复制技能
cp -r playwright-undetected-skill ~/.claude/skills/
```

### 配置测试环境

```javascript
// playwright.config.js
module.exports = {
  testDir: './tests',
  timeout: 30000,
  use: {
    baseURL: 'http://localhost:3000',
    screenshot: 'only-on-failure',
  },
};
```

---

## 7. 技能选择建议

### 按测试类型选择

| 测试类型 | 推荐技能 | 优先级 |
|---------|---------|-------|
| **Web/E2E 测试** | Playwright Skill | ⭐⭐⭐⭐⭐ |
| **反检测测试** | Playwright Undetected | ⭐⭐⭐⭐ |
| **游戏客户端** | Unity Test Framework | ⭐⭐⭐⭐ |
| **代码质量** | Claude Skills Marketplace | ⭐⭐⭐⭐ |
| **自动化开发** | Claude Auto Dev | ⭐⭐⭐ |

### 按游戏引擎选择

| 引擎 | 推荐测试方案 |
|-----|------------|
| **Web/H5 游戏** | Playwright + Webapp Testing |
| **Unity 游戏** | Unity Test Framework |
| **iOS 游戏** | iOS Simulator Skill |
| **Android 游戏** | Android Emulator + Playwright |

---

## 8. 优缺点分析

### ✅ 优点

| 优点 | 说明 |
|-----|------|
| **生态成熟** | Playwright 社区活跃 |
| **多浏览器** | 支持 Chromium/Firefox/WebKit |
| **跨平台** | Windows/Mac/Linux |
| **AI 集成** | Claude Code 原生集成 |
| **截图功能** | 便于问题追踪 |
| **反检测** | 可绕过 bot 检测 |

### ❌ 缺点

| 缺点 | 说明 |
|-----|------|
| **Web 限定** | 不适合原生游戏客户端 |
| **环境依赖** | 需安装浏览器驱动 |
| **学习曲线** | 需了解 Playwright API |
| **性能局限** | 不适合大型游戏测试 |
| **检测限制** | 反检测可能被识别 |

---

## 9. 游戏客户端测试扩展

### 原生游戏测试方案

对于非 Web 游戏客户端，可以考虑：

1. **截图识别**: 使用 OCR/图像识别进行验证
2. **API Mock**: 模拟游戏服务器响应
3. **内存检测**: 辅助调试内存问题
4. **日志分析**: 解析游戏日志

### 推荐技能组合

| 用途 | 技能组合 |
|-----|---------|
| **Web/H5 游戏** | Playwright + Webapp Testing |
| **API 测试** | API 集成技能 + 日志分析 |
| **性能测试** | 监控系统集成 |
| **截图比对** | 图像处理技能 |
| **Unity 游戏** | Unity Test Framework + Profiling |
| **iOS 游戏** | iOS Simulator Skill |

---

## 📎 相关资源

### 测试相关

- [Playwright Skill](https://github.com/lackeyjb/playwright-skill)
- [Playwright Undetected](https://github.com/dalbit-mir/playwright-undetected-skill)
- [Webapp Testing](https://github.com/ComposioHQ/awesome-claude-skills)
- [Claude Skills Marketplace](https://github.com/mhattingpete/claude-skills-marketplace)
- [test-driven-development](https://github.com/obra/superpowers)

### iOS/Unity 相关

- [iOS Simulator Skill](https://github.com/conorluddy/ios-simulator-skill)
- [Unity GameDev Skills](https://github.com/tjboudreaux/cc-plugin-unity-gamedev)

### 开发者工具

- [Claude Code Templates](https://github.com/davila7/claude-code-templates)
- [Fullstack Dev Skills](https://github.com/jeffallan/claude-skills)

---

*游戏客户端测试需要根据具体技术栈选择合适方案，Web 游戏可直接使用 Playwright 系列技能。*
