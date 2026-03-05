# Git Context Controller Git 风格上下文管理

> 长期项目的上下文管理框架

## 1. 背景需求

长期项目需要跨会话的上下文管理能力。

## 2. 目标

提供 Git 风格的上下文版本控制。

## 3. 设计方案

- COMMIT - 保存上下文快照
- BRANCH - 分支管理
- MERGE - 合并上下文
- 长周期任务记忆

## 4. 本地部署

```bash
git clone https://github.com/faugustdev/git-context-controller ~/.claude/plugins/
```

## 5. 效果展示

- GitHub Stars：⭐ 新兴

## 6. 优缺点

✅ 上下文版本化 ✅ 灵活切换  
⚠️ 学习成本 ⚠️ 功能复杂

## 7. 平替

| 插件 | 特点 |
|------|------|
| claude-mem | 智能记忆 |
| project-memory | 项目状态 |

## 8. 落地过程

1. 安装技能
2. 初始化项目上下文
3. 使用 COMMIT/BRANCH 管理
