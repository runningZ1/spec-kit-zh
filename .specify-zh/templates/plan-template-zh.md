# 实施计划：[功能]

**分支**：`[###-feature-name]` | **日期**：[日期] | **规格**：[链接]
**输入**：来自 `/specs/[###-feature-name]/spec.md` 的功能规格

**注意**：此模板由 `/speckit.plan` 命令填写。有关执行工作流程，请参阅 `.specify/templates/commands/plan.md`。

## 摘要

[从功能规格中提取：主要需求 + 来自研究的技术方法]

## 技术上下文

<!--
  需要操作：用技术细节替换此部分的内容
  为项目。这里的结构以咨询身份呈现以指导
  迭代过程。
-->

**语言/版本**：[例如，Python 3.11、Swift 5.9、Rust 1.75 或需要澄清]  
**主要依赖**：[例如，FastAPI、UIKit、LLVM 或需要澄清]  
**存储**：[如果适用，例如，PostgreSQL、CoreData、文件或 N/A]  
**测试**：[例如，pytest、XCTest、cargo test 或需要澄清]  
**目标平台**：[例如，Linux 服务器、iOS 15+、WASM 或需要澄清]
**项目类型**：[单个/web/移动 - 确定源结构]  
**性能目标**：[特定于领域，例如，1000 req/s、10k lines/sec、60 fps 或需要澄清]  
**约束**：[特定于领域，例如，<200ms p95、<100MB 内存、离线功能或需要澄清]  
**规模/范围**：[特定于领域，例如，10k 用户、1M LOC、50 个屏幕或需要澄清]

## 章程检查

*关卡：必须在阶段 0 研究之前通过。阶段 1 设计后重新检查。*

[根据章程文件确定的关卡]

## 项目结构

### 文档（此功能）

```
specs/[###-feature]/
├── plan.md              # 此文件（/speckit.plan 命令输出）
├── research.md          # 阶段 0 输出（/speckit.plan 命令）
├── data-model.md        # 阶段 1 输出（/speckit.plan 命令）
├── quickstart.md        # 阶段 1 输出（/speckit.plan 命令）
├── contracts/           # 阶段 1 输出（/speckit.plan 命令）
└── tasks.md             # 阶段 2 输出（/speckit.tasks 命令 - 不是由 /speckit.plan 创建）
```

### 源代码（仓库根目录）
<!--
  需要操作：用具体的布局替换下面的占位符树
  为这个功能。删除未使用的选项并扩展所选结构
  实际路径（例如，apps/admin、packages/something）。交付的计划必须
  不包括选项标签。
-->

```
# [如果未使用则删除] 选项 1：单个项目（默认）
src/
├── models/
├── services/
├── cli/
└── lib/

tests/
├── contract/
├── integration/
└── unit/

# [如果未使用则删除] 选项 2：Web 应用程序（检测到"前端" + "后端"时）
backend/
├── src/
│   ├── models/
│   ├── services/
│   └── api/
└── tests/

frontend/
├── src/
│   ├── components/
│   ├── pages/
│   └── services/
└── tests/

# [如果未使用则删除] 选项 3：移动 + API（检测到"iOS/Android"时）
api/
└── [与上面的后端相同]

ios/ 或 android/
└── [平台特定结构：功能模块、UI 流程、平台测试]
```

**结构决策**：[记录所选结构并引用上面捕获的实际
目录]

## 复杂性跟踪

*仅在章程检查有必须证明的违规时填写*

| 违规 | 为什么需要 | 被拒绝的更简单替代方案，因为 |
|-----------|------------|-------------------------------------|
| [例如，第 4 个项目] | [当前需求] | [为什么 3 个项目不够] |
| [例如，仓库模式] | [特定问题] | [为什么直接数据库访问不够] |

