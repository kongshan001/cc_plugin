# unibrowse 高级浏览器自动化插件

> Claude Code 高级浏览器自动化 | QA 测试

## 1. 背景需求

游戏客户端的 Web 组件、官网、后台管理系统等需要进行全面的浏览器自动化测试，包括 Web 爬取、表单填写、电商流程、QA 测试等场景。

## 2. 目标

提供高级浏览器自动化能力，通过专业子代理和宏命令简化复杂的浏览器测试任务。

## 3. 设计方案

**核心架构**
- 5 个专业子代理
- 57+ 宏命令
- 智能任务委托
- 浏览器操作库

**功能模块**
- Web 爬取代理
- 表单自动化代理
- 电商自动化代理
- QA 测试代理
- 智能委托系统

## 4. 本地部署

```bash
# 克隆仓库
git clone https://github.com/sackio/unibrowse.git
cd unibrowse

# 安装依赖
npm install

# 配置 Claude Code skills 目录
cp -r unibrowse ~/.claude/skills/
```

## 5. 效果展示

- **GitHub Stars**: ⭐ 4
- **功能**: 5 子代理 + 57 宏
- **场景**: 爬取/表单/电商/QA

## 6. 优缺点

| 优点 | 缺点 |
|------|------|
| 多专业子代理 | Stars 较低 |
| 57+ 宏命令 | 文档待完善 |
| 智能委托 | |
| 场景覆盖广 | |

## 7. 平替插件

| 插件 | 特点 |
|------|------|
| playwright-skill | 1,863 Stars 主流选择 |
| claude-code-playwright-mcp-test | YAML 配置框架 |

## 8. 落地过程

1. 克隆仓库并安装依赖
2. 复制到 Claude Code skills 目录
3. 调用子代理执行任务
4. 使用宏命令简化操作
