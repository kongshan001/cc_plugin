# Claude Code PR Review Toolkit

> 官方 PR 审查工具包，6 个专业审查代理

## 1. 背景需求

代码审查是保证代码质量的关键环节，但人工审查耗时且容易遗漏。 Claude Code 官方推出了 PR Review Toolkit，通过多个专业代理实现自动化、全面的代码审查。

## 2. 目标

提供 6 个专业审查代理，覆盖代码注释、测试覆盖、错误处理、类型设计、综合审查和代码简化等维度。

## 3. 设计方案

### 核心架构

```
PR Review Toolkit
├── comment-analyzer       # 代码注释分析
├── pr-test-analyzer      # 测试覆盖分析
├── silent-failure-hunter # 错误处理检查
├── type-design-analyzer  # 类型设计分析
├── code-reviewer         # 综合代码审查
└── code-simplifier       # 代码简化优化
```

### 审查维度

| 代理 | 评分方式 | 关注点 |
|------|---------|--------|
| comment-analyzer | 高置信度 | 注释准确性、文档完整性、技术债务 |
| pr-test-analyzer | 1-10 分 | 行为覆盖、关键缺口、边缘 case |
| silent-failure-hunter | 严重性级别 | 静默失败、错误处理、异常日志 |
| type-design-analyzer | 4维度x1-10 | 封装性、不变性、可用性、执行力 |
| code-reviewer | 0-100 分 | CLAUDE.md 合规、风格违规、bug |
| code-simplifier | 复杂度评估 | 可读性、不必要复杂性、一致性 |

## 4. 本地部署

### 安装方式

```bash
# 方式一：使用 /plugin 命令
/plugin
# 搜索 "pr-review-toolkit"
# 安装

# 方式二：手动配置
# 在 .claude/settings.json 中添加
{
  "plugins": ["pr-review-toolkit"]
}
```

### 使用示例

```bash
# 触发测试分析
"Can you check if the tests cover all edge cases?"

# 触发错误处理检查
"Review the error handling in the API client"

# 触发代码审查
"Review my recent changes"

# 触发多个代理并行审查
"I'm ready to create this PR. Please:
1. Review test coverage
2. Check for silent failures
3. Verify code comments are accurate
4. Review any new types
5. General code review"
```

## 5. 效果展示

### 审查流程

```
用户请求 → 自动触发相关代理 → 并行/顺序分析 → 结构化输出
```

### 输出示例

```
## PR Test Analyzer - 测试覆盖分析

**评分**: 8/10 (良好)

### 发现的问题

1. **关键缺口** - `src/api/user.ts:45`
   - 未测试用户注销场景
   - 建议添加: logout() 方法的测试

2. **边缘 case** - `src/utils/validation.ts:23`
   - 缺少空字符串边界测试

### 建议

- 添加负面测试用例
- 覆盖异常数据场景
```

## 6. 优缺点分析

### 优点

✅ **专业分工**: 6 个代理各司其职
✅ **置信度评分**: 量化问题严重程度
✅ **自动触发**: 根据上下文智能选择代理
✅ **官方支持**: 由 Anthropic 维护
✅ **可扩展**: 可自定义代理

### 缺点

⚠️ 需要明确触发条件
⚠️ 复杂问题仍需人工判断
⚠️ 部分代理需要具体文件上下文

## 7. 平替对比

| 工具 | 特点 | 适用场景 |
|------|------|---------|
| PR Review Toolkit | 6 专业代理 | Claude Code 用户 |
| Code Review Plugin | 5 并行代理 | 快速 PR 审查 |
| Superpowers | 综合技能 | 全面质量保证 |
| AgentSys | 工作流自动化 | CI/CD 集成 |

## 8. 落地过程

### 集成工作流

1. **开发阶段**
   - 编写代码 → code-reviewer 自检
   - 添加测试 → pr-test-analyzer 验证
   
2. **提交前**
   - 错误处理 → silent-failure-hunter 检查
   - 代码注释 → comment-analyzer 审核
   
3. **PR 前**
   - 全面审查 → 触发所有相关代理
   - 代码优化 → code-simplifier 改进
   
4. **审查后**
   - 修复问题 → 重新触发验证

### 最佳实践

- 明确指定审查范围（文件、行号）
- 按优先级处理问题（先修复严重问题）
- 迭代审查（修复后重新运行）
- 结合 Superpowers 使用

---

*文档版本: 1.0*
*更新时间: 2026-03-05*
