# Claude Code 自动化测试技能补充调研

## 📋 文档信息

- **调研日期**: 2026-03-03
- **分类**: 自动化测试 / 游戏客户端测试 / Web 测试 / CI/CD
- **状态**: ✅ 补充调研

---

## 1. 浏览器自动化测试

### 1.1 Playwright Skill (核心)

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

### 基本用法

```python
# 使用技能进行测试
"测试登录页面功能"
"验证用户下单流程"
"检查首页加载时间"
```

### 适用场景

- Web 游戏测试
- H5 游戏测试
- 前端功能验证
- UI 自动化测试
- 回归测试

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

### 1.3 Webapp Testing

| 项目 | 说明 |
|-----|------|
| **GitHub** | [ComposioHQ/awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills) |
| **功能** | 本地 Web 应用测试 |
| **依赖** | Playwright |
| **特点** | 端到端测试能力 |

---

## 2. 游戏客户端测试方案

### 2.1 Unity 测试

#### Unity Test Framework Skill

| 项目 | 说明 |
|-----|------|
| **来源** | cc-plugin-unity-gamedev |
| **功能** | Unity 单元测试 |

### 测试类型

| 类型 | 说明 | 适用场景 |
|-----|------|---------|
| **EditMode** | 编辑器环境测试 | 工具类、辅助功能 |
| **PlayMode** | 运行时测试 | 游戏逻辑、UI |
| **Performance** | 性能测试 | 性能优化 |

### 2.2 Web/H5 游戏测试

| 方案 | 工具 | 优点 |
|-----|------|------|
| **Playwright** | 浏览器自动化 | 功能全面、生态好 |
| **Puppeteer** | 浏览器自动化 | 轻量级 |
| **Selenium** | 浏览器自动化 | 多浏览器支持 |

### 2.3 原生游戏客户端测试

| 测试类型 | 方案 | 说明 |
|---------|------|------|
| **UI 测试** | 截图对比 + OCR | 视觉回归测试 |
| **API 测试** | Mock Server | 模拟后端响应 |
| **性能测试** | Unity Profiler | 性能分析 |
| **内存测试** | Memory Profiler | 内存泄漏检测 |

---

## 3. 测试开发技能 (TDD/BDD)

### 3.1 Test-Driven Development

| 命令 | 来源 | 功能 |
|-----|------|------|
| **/tdd** | zscott/pane | TDD 开发流程 |
| **/tdd-implement** | jerseycheese/Narraitor | TDD 实现 |
| **testing_plan_integration** | buster-so/buster | 测试计划集成 |

### TDD 流程

```
红色 (Red)     → 编写失败的测试
       ↓
绿色 (Green)   → 实现最小代码通过测试
       ↓
重构 (Refactor)→ 重构代码保持测试通过
```

### 3.2 测试编写技能

| 技能 | 功能 |
|-----|------|
| **test-fixing** | 测试修复 |
| **test-writing** | 测试编写 |
| **test-running** | 测试运行 |
| **bug-finding** | Bug 查找 |

### 3.3 测试修复工作流

```
发现问题 → 编写复现测试 → 修复代码 → 验证测试通过
```

---

## 4. 代码质量检查

### 4.1 /check 命令

| 项目 | 说明 |
|-----|------|
| **来源** | rygwdn/slack-tools |
| **功能** | 代码质量和安全检查 |

### 检查内容

- **静态分析**: 代码结构检查
- **安全扫描**: 漏洞扫描
- **代码风格**: 格式规范
- **详细报告**: 问题汇总

### 4.2 /clean 命令

| 项目 | 说明 |
|-----|------|
| **来源** | Graphlet-AI/eridu |
| **功能** | 代码格式化 |

### 自动修复

- **Black**: Python 格式化
- **isort**: import 整理
- **Flake8**: Lint 问题
- **Mypy**: 类型错误

### 4.3 /repro-issue 命令

| 项目 | 说明 |
|-----|------|
| **来源** | rzykov/metabase |
| **功能** | 可复现测试用例 |

### 用法

```bash
/repro-issue #123
```

自动创建：
- 复现步骤文档
- 最小化测试用例
- 失败测试代码

---

## 5. CI/CD 集成

### 5.1 /run-ci 命令

| 项目 | 说明 |
|-----|------|
| **来源** | hackdays-io/toban-contribution-viewer |
| **功能** | CI 兼容检查 |

### 工作流

```
激活虚拟环境 → 运行检查脚本 → 迭代修复错误 → 验证全部通过
```

### 5.2 自动化部署测试

```yaml
# GitHub Actions 示例
name: Test Suite
on: [push, pull_request]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Run tests
        run: |
          pip install -r requirements.txt
          pytest tests/
```

---

## 6. E2E 测试框架

### 6.1 Claude Skills Marketplace

| 项目 | 说明 |
|-----|------|
| **GitHub** | [mhattingpete/claude-skills-marketplace](https://github.com/mhattingpete/claude-skills-marketplace) |
| **Star** | ⭐ 427 |
| **功能** | 软件工程工作流技能 |

### 测试技能

| 技能名称 | 功能 |
|---------|------|
| **test-fixing** | 测试修复 |
| **test-writing** | 测试编写 |
| **test-running** | 测试运行 |
| **bug-finding** | Bug 查找 |
| **code-review** | 代码审查 |

### 6.2 Fieldwork Skills

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

## 7. 游戏客户端测试扩展

### 7.1 测试策略

#### 单元测试
```csharp
// Unity 单元测试
[Test]
public void TestPlayerHealth() {
    var player = new Player();
    Assert.AreEqual(100, player.Health);
    
    player.TakeDamage(30);
    Assert.AreEqual(70, player.Health);
}
```

#### 集成测试
```csharp
// Unity 集成测试
[UnityTest]
public IEnumerator TestPlayerMovement() {
    var player = new GameObject("Player");
    var movement = player.AddComponent<PlayerMovement>();
    
    movement.Move(Vector2.right);
    yield return new WaitForSeconds(0.1f);
    
    Assert.IsTrue(player.transform.position.x > 0);
}
```

### 7.2 视觉回归测试

```python
# Playwright 截图对比
from playwright.sync_api import sync_playwright

def test_visual_regression(page):
    page.goto("http://localhost:3000")
    page.screenshot(path="baseline.png")
    
    # 比较截图
    assert compare_images("screenshot.png", "baseline.png")
```

### 7.3 API Mock 测试

```python
# 使用 Playwright Mock
async def test_with_mock_api(page):
    await page.route("**/api/user", lambda route: route.fulfill(
        json={"id": 1, "name": "Test User"}
    ))
    
    page.goto("/profile")
    await page.wait_for_selector(".user-name")
    assert await page.text_content(".user-name") == "Test User"
```

---

## 8. 移动端游戏测试

### 8.1 Android UI 自动化测试

#### android_ui_verification

| 项目 | 说明 |
|-----|------|
| **GitHub** | Antigravity Skills |
| **功能** | Android 模拟器 UI 测试 |
| **工具** | ADB (Android Debug Bridge) |
| **特点** | 端到端 UI 验证 |

#### 核心功能

- **设备校准**: 自动获取屏幕分辨率
- **UI 检查**: uiautomator dump 获取元素位置
- **交互命令**: tap、swipe、text input、key events
- **验证报告**: 截图验证、日志分析

#### 工作流程

```bash
# 1. 设备校准 - 获取屏幕分辨率
adb shell wm size

# 2. UI 检查 - 获取元素信息
adb shell uiautomator dump /sdcard/view.xml
adb pull /sdcard/view.xml ./artifacts/view.xml

# 3. 交互操作
adb shell input tap <x> <y>
adb shell input swipe <x1> <y1> <x2> <y2> <duration_ms>
adb shell input text "Hello"

# 4. 截图验证
adb shell screencap -p /sdcard/screen.png
adb pull /sdcard/screen.png ./artifacts/test_result.png
```

#### 适用场景

- Android 游戏 UI 测试
- React Native 应用测试
- 移动端游戏自动化测试
- 布局问题调试

### 8.2 iOS 模拟器测试

#### ios-simulator-skill

| 项目 | 说明 |
|-----|------|
| **GitHub** | [conorluddy/ios-simulator-skill](https://github.com/conorluddy/ios-simulator-skill) |
| **Star** | ⭐ 557 |
| **功能** | iOS 模拟器集成 |
| **平台** | macOS |

#### 核心功能

- **模拟器控制**: 启动/停止模拟器
- **应用安装**: 安装 iOS 应用
- **UI 交互**: 自动化 UI 测试
- **截图捕获**: 状态记录

### 8.3 移动端游戏测试方案对比

| 平台 | 推荐工具 | 适用场景 |
|-----|---------|---------|
| **Android** | android_ui_verification + ADB | Android 游戏测试 |
| **iOS** | ios-simulator-skill | iOS 游戏测试 |
| **跨平台** | Appium | Unity/Cocos 游戏 |
| **WebView** | Playwright | 混合应用测试 |

---

## 9. 部署指南

### 8.1 安装 Playwright

```bash
# 安装 Playwright
npm install -g playwright
playwright install chromium

# 或使用 Python 版本
pip install playwright
playwright install
```

### 8.2 安装 Playwright Skill

```bash
# 克隆技能仓库
git clone https://github.com/lackeyjb/playwright-skill.git

# 复制到技能目录
cp -r playwright-skill ~/.claude/skills/
```

### 8.3 安装反检测版本

```bash
# 克隆反检测版本
git clone https://github.com/dalbit-mir/playwright-undetected-skill.git

# 安装 Patchright
npm install -g @anthropic-ai/patchright

# 复制技能
cp -r playwright-undetected-skill ~/.claude/skills/
```

### 8.4 配置测试环境

```javascript
// playwright.config.js
module.exports = {
  testDir: './tests',
  timeout: 30000,
  use: {
    baseURL: 'http://localhost:3000',
    screenshot: 'only-on-failure',
    video: 'on-first-retry',
  },
};
```

---

## 9. 技能选择建议

### 9.1 按测试类型选择

| 测试类型 | 推荐技能 | 优先级 |
|---------|---------|-------|
| **Web/E2E 测试** | Playwright Skill | ⭐⭐⭐⭐⭐ |
| **反检测测试** | Playwright Undetected | ⭐⭐⭐⭐ |
| **游戏客户端** | Unity Test Framework | ⭐⭐⭐⭐ |
| **Android UI 测试** | android_ui_verification | ⭐⭐⭐⭐ |
| **iOS 测试** | ios-simulator-skill | ⭐⭐⭐⭐ |
| **代码质量** | Claude Skills Marketplace | ⭐⭐⭐⭐ |
| **TDD 开发** | /tdd, /tdd-implement | ⭐⭐⭐⭐ |
| **Bug 复现** | /repro-issue | ⭐⭐⭐ |

### 9.2 按游戏引擎/平台选择

| 引擎/平台 | 推荐测试方案 |
|---------|------------|
| **Web/H5 游戏** | Playwright + Webapp Testing |
| **Unity 游戏** | Unity Test Framework |
| **iOS 游戏** | iOS Simulator Skill |
| **Android 游戏** | android_ui_verification + ADB |
| **跨平台移动游戏** | Appium |
| **原生游戏客户端** | Unity Profiler + 截图对比 |

---

## 10. 优缺点分析

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

## 11. 测试最佳实践

### 11.1 测试金字塔

```
        /\
       /  \      E2E 测试 (少量)
      /----\    
     /      \   集成测试 (中量)
    /--------\  
   /          \ 单元测试 (大量)
  --------------
```

### 11.2 命名规范

```
test_<模块>_<行为>.py
test_player_take_damage.py
test_user_login_success.py
```

### 11.3 测试数据

- 使用工厂模式创建测试数据
- 每个测试独立数据
- 清理测试副作用

---

## 📎 相关资源

### 测试相关

- [Playwright Skill](https://github.com/lackeyjb/playwright-skill)
- [Playwright Undetected](https://github.com/dalbit-mir/playwright-undetected-skill)
- [Webapp Testing](https://github.com/ComposioHQ/awesome-claude-skills)
- [Claude Skills Marketplace](https://github.com/mhattingpete/claude-skills-marketplace)
- [test-driven-development](https://github.com/obra/superpowers)

### 游戏测试

- [Unity Test Framework](https://docs.unity3d.com/Manual/testing.html)
- [Playwright 文档](https://playwright.dev/)
- [Unity Profiler](https://docs.unity3d.com/Manual/Profiler.html)

---

*游戏客户端测试需要根据具体技术栈选择合适方案，Web 游戏可直接使用 Playwright 系列技能。*
