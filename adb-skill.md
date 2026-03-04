# ADB 设备操作技能

> Android 设备自动化操作技能

## 项目信息

- **GitHub Stars**: 0 (新增)
- **技能类别**: 自动化测试 / 移动端
- **状态**: ✅ 已调研
- **应用场景**: 游戏客户端测试

---

## 简介

ADB (Android Debug Bridge) 设备操作技能为 Claude Code 提供 Android 设备自动化能力，特别适用于游戏客户端测试场景。

---

## 核心功能

| 功能 | 说明 |
|------|------|
| 构建安装 | APK 构建和安装 |
| UI 操作 | 点击、滑动、缩放 |
| 截图 | 屏幕截图 |
| 日志 | Logcat 日志查看 |
| 视觉验证 | 通过 ADB 进行 UI 验证 |

---

## 游戏客户端测试应用

该技能特别适用于以下游戏测试场景：

- **功能测试**: 自动测试游戏核心功能
- **UI 测试**: 验证游戏界面交互
- **回归测试**: 自动化冒烟测试
- **性能测试**: 配合性能监控工具

---

## 安装方式

```bash
# 技能名称: adb-skill
# 源码: https://github.com/pengdev/claude-adb-skill
```

---

## 常用命令

```bash
# 安装 APK
adb install game.apk

# 截图
adb shell screencap -p /sdcard/screen.png
adb pull /sdcard/screen.png

# 点击坐标
adb shell input tap x y

# 滑动操作
adb shell input swipe x1 y1 x2 y2 duration

# 查看日志
adb logcat -d
```

---

## 相关技能

| 技能 | 用途 |
|------|------|
| playwright-mcp | Web/浏览器自动化测试 |
| android-reverse-engineering | Android 逆向工程 |
| claude-android-skill | Android 现代应用开发 |

---

## 相关链接

- [ADB 官方文档](https://developer.android.com/studio/command-line/adb)
- [游戏客户端测试技能](./game-client-testing.md)
