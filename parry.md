# Parry 提示注入扫描器

> Claude Code Hook 安全防护工具，多层检测提示注入攻击

## 1. 背景需求

Claude Code 处理外部输入时面临提示注入攻击风险，需要自动化安全检测。

## 2. 目标

提供多层安全防护：
- PreToolUse: 工具使用前检测
- PostToolUse: 工具输出后检测
- UserPromptSubmit: 提示提交前审计

## 3. 设计方案

```
┌─────────────────────────────────────────────────────────────┐
│                      Parry 安全层                            │
├─────────────────────────────────────────────────────────────┤
│  PreToolUse Hook (5层防护)                                   │
│  ┌─────────────────────────────────────────────────────┐   │
│  │ 1. Taint Enforcement                                │   │
│  │ 2. CLAUDE.md Scanning                               │   │
│  │ 3. Exfil Blocking                                   │   │
│  │ 4. Sensitive Path Blocking                         │   │
│  │ 5. Input Content Injection                         │   │
│  └─────────────────────────────────────────────────────┘   │
│                                                             │
│  ML 检测模式                                                │
│  ┌─────────────┬─────────────┬─────────────────────────┐   │
│  │ fast        │ DeBERTa v3  │ ~50-70ms                │   │
│  │ full        │ DeBERTa+    │ ~1.5s                   │   │
│  │             │ Llama Guard │                         │   │
│  └─────────────┴─────────────┴─────────────────────────┘   │
└─────────────────────────────────────────────────────────────┘
```

## 4. 本地部署

```bash
# 安装
cargo binstall parry-ai
# 或
cargo install --path crates/cli

# 配置 HuggingFace
export HF_TOKEN="hf_..."

# Claude Code Hook 配置 (~/.claude/settings.json)
{
  "hooks": {
    "PreToolUse": [{ "command": "parry hook", "timeout": 1000 }],
    "PostToolUse": [{ "command": "parry hook", "timeout": 5000 }],
    "UserPromptSubmit": [{ "command": "parry hook", "timeout": 2000 }]
  }
}
```

## 5. 效果展示

- 检测能力：60+ 敏感路径、40+ 外泄域名、40+ 凭证模式
- ML 模型：DeBERTa v3 + Llama Prompt Guard 2
- 缓存：~8ms 缓存命中

## 6. 优缺点

✅ 多层防护 ✅ ML 检测 ✅ 自动缓存  
⚠️ 需 HuggingFace 账户 ⚠️ 早期开发 ⚠️ macOS 测试为主

## 7. 平替

| 插件 | 特点 |
|------|------|
| Dippy | 命令级别过滤 |
| Snyk Agent Scan | 漏洞扫描 |

## 8. 落地过程

1. 创建 HuggingFace 账户
2. 接受模型许可证
3. 安装 parry
4. 配置 Hook
5. 测试检测效果
