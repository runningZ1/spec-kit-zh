---
description: 使用计划模板执行实施规划工作流程以生成设计文件。
---

## 用户输入

```text
$ARGUMENTS
```

在继续之前，你**必须**考虑用户输入（如果非空）。

## 概述

1. **设置**：从仓库根目录运行 `.specify/scripts/powershell/setup-plan.ps1 -Json` 并解析 JSON 获取 FEATURE_SPEC、IMPL_PLAN、SPECS_DIR、BRANCH。

2. **加载上下文**：读取 FEATURE_SPEC 和 `.specify/memory/constitution.md`。加载 IMPL_PLAN 模板（已复制）。

3. **执行计划工作流程**：按照 IMPL_PLAN 模板中的结构：
   - 填写技术上下文（将未知标记为"需要澄清"）
   - 从章程填写章程检查部分
   - 评估关卡（如果违规未经证明则错误）
   - 阶段 0：生成 research.md（解决所有需要澄清的问题）
   - 阶段 1：生成 data-model.md、contracts/、quickstart.md
   - 阶段 1：通过运行代理脚本更新代理上下文
   - 设计后重新评估章程检查

4. **停止并报告**：命令在阶段 2 规划后结束。报告分支、IMPL_PLAN 路径和生成的文件。

## 阶段

### 阶段 0：大纲和研究

1. **从上面的技术上下文中提取未知**：
   - 对于每个需要澄清 → 研究任务
   - 对于每个依赖 → 最佳实践任务
   - 对于每个集成 → 模式任务

2. **生成和派遣研究代理**：
   ```
   对于技术上下文中的每个未知：
     任务："研究{功能上下文}的{未知}"
   对于每个技术选择：
     任务："查找{领域}中{技术}的最佳实践"
   ```

3. **在 `research.md` 中合并发现**使用格式：
   - 决策：[选择了什么]
   - 理由：[为什么选择]
   - 考虑的替代方案：[评估了什么]

**输出**：research.md，所有需要澄清的问题已解决

### 阶段 1：设计和合约

**先决条件：** `research.md` 完成

1. **从功能规格中提取实体** → `data-model.md`：
   - 实体名称、字段、关系
   - 来自需求的验证规则
   - 如果适用的状态转换

2. **从功能需求生成 API 合约**：
   - 对于每个用户操作 → 端点
   - 使用标准 REST/GraphQL 模式
   - 输出 OpenAPI/GraphQL 架构到 `/contracts/`

3. **代理上下文更新**：
   - 运行 `.specify/scripts/powershell/update-agent-context.ps1 -AgentType claude`
   - 这些脚本检测正在使用哪个 AI 代理
   - 更新适当的特定于代理的上下文文件
   - 仅从当前计划添加新技术
   - 保留标记之间的手动添加

**输出**：data-model.md、/contracts/*、quickstart.md、特定于代理的文件

## 关键规则

- 使用绝对路径
- 关卡失败或未解决的澄清错误

