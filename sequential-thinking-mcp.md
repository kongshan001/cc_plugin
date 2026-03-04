# Sequential Thinking MCP

> 动态反思性问题解决的思维序列

## 项目信息

- **官方维护**: Model Context Protocol
- **技能类别**: 开发者工具 / AI 思维增强
- **状态**: ✅ 官方参考实现

---

## 简介

Sequential Thinking MCP 服务器是 Model Context Protocol 官方参考实现，通过思维序列实现动态和反思性问题解决。

---

## 核心功能

| 功能 | 说明 |
|------|------|
| 思维序列 | 分步骤思考复杂问题 |
| 反思机制 | 动态调整解决思路 |
| 问题分解 | 将复杂问题拆解 |
| 方案评估 | 评估多个解决方案 |

---

## 技术原理

该服务器实现了一种让 AI 进行"思考"的技术：

1. **问题分解**: 将复杂问题分解为可管理的步骤
2. **迭代推理**: 逐步推理，每步都可回顾和修正
3. **方案对比**: 考虑多种可能的解决方案
4. **最终决策**: 基于推理给出最佳答案

---

## 应用场景

- **复杂问题解决**: 需要多步推理的技术问题
- **代码审查**: 系统性的代码分析
- **架构设计**: 分步骤的系统设计
- **调试排错**: 逻辑严密的调试过程

---

## 安装方式

```bash
# 官方参考实现，可从以下地址获取
# https://github.com/modelcontextprotocol/servers/tree/main/src/sequentialthinking
```

---

## 使用示例

```json
{
  "tool": "sequential_thinking",
  "input": {
    "problem": "设计一个高可用的微服务架构",
    "constraints": ["成本控制", "易于扩展", "容错机制"]
  }
}
```

---

## 相关链接

- [MCP 官方服务器仓库](https://github.com/modelcontextprotocol/servers)
- [Memory MCP](./memory-mcp-server.md)
