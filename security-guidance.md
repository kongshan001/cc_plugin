# Claude Code Security Guidance Plugin

> 官方安全提醒钩子，监控 9 种安全模式

## 1. 背景需求

在代码开发过程中，安全漏洞容易被忽视。Claude Code 官方提供 Security Guidance 插件，在编辑文件时主动提醒潜在的安全问题。

## 2. 目标

通过 PreToolUse 钩子监控 9 种常见安全模式，在问题出现前及时提醒开发者。

## 3. 设计方案

### 监控的安全模式

| 模式 | 风险类型 | 示例 |
|------|---------|------|
| Command Injection | 命令注入 | `os.system(user_input)` |
| XSS Attack | 跨站脚本 | `innerHTML = user_data` |
| Eval Usage | eval 执行 | `eval(code_string)` |
| Dangerous HTML | 危险 HTML | 直接插入未转义 HTML |
| Pickle Deserialization | pickle 反序列化 | `pickle.loads(data)` |
| SQL Injection | SQL 注入 | 字符串拼接 SQL |
| Path Traversal | 路径遍历 | 未验证的文件路径 |
| Hardcoded Secrets | 硬编码密钥 | API keys in code |
| Insecure Random | 不安全随机 | `random.random()` for security |

### 架构

```
PreToolUse Hook
    ↓
安全模式检测 (正则 + AST)
    ↓
风险评估
    ↓
警告信息 + 修复建议
```

## 4. 本地部署

### 状态

**内置插件，无需安装**

Security Guidance 是 Claude Code 内置插件，默认启用。

### 配置

```json
// .claude/settings.json
{
  "hooks": {
    "PreToolUse": ["security-guidance"]
  }
}
```

## 5. 效果展示

### 警告示例

```
⚠️ Security Warning: Command Injection Risk

**位置**: src/utils.sh:42
**问题**: 使用 os.system() 执行用户输入
**风险**: 攻击者可通过输入注入恶意命令

**建议**:
- 使用 subprocess.run() 替代
- 验证并清理用户输入
- 避免 shell=True 参数

**操作**:
- [y] 继续执行
- [n] 取消
- [e] 编辑命令
```

## 6. 优缺点分析

### 优点

✅ **主动防御**: 在执行前发现问题
✅ **全面覆盖**: 9 种常见安全模式
✅ **官方维护**: 由 Anthropic 提供
✅ **零配置**: 开箱即用
✅ **修复建议**: 提供具体改进方案

### 缺点

⚠️ 无法覆盖所有安全场景
⚠️ 误报可能影响开发效率
⚠️ 复杂逻辑需要人工判断

## 7. 平替对比

| 插件 | 特点 | 适用场景 |
|------|------|---------|
| Security Guidance | 9 种安全模式 | 日常开发 |
| Trail of Bits | CodeQL + Semgrep | 深度安全审计 |
| Parry | 提示注入扫描 | 输入安全 |
| TDD Guard | TDD 原则守护 | 开发流程 |

## 8. 落地过程

### 使用建议

1. **认真对待警告**: 安全问题不容忽视
2. **理解风险**: 仔细阅读风险说明
3. **采用建议**: 优先使用推荐方案
4. **持续关注**: 保持安全意识

### 配合使用

- **PR Review Toolkit**: 提交前全面审查
- **代码格式化**: 保持代码规范
- **类型检查**: 静态分析辅助

---

*文档版本: 1.0*
*更新时间: 2026-03-05*
