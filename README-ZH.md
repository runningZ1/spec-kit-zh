# Spec-Driven Development 工作流程 - 中文版

本仓库包含 Spec-Driven Development（规格驱动开发）工作流程的中文简体翻译版本。

## 📁 目录结构

```
.
├── .claude/
│   ├── commands/           # 原始英文命令文件
│   └── commands-zh/        # 中文翻译命令文件 ✨
│
├── .specify/
│   ├── memory/             # 原始英文记忆文件
│   ├── templates/          # 原始英文模板文件
│   └── scripts/            # 原始英文脚本
│
└── .specify-zh/            # 中文翻译版本 ✨
    ├── memory/             # 中文记忆文件
    ├── templates/          # 中文模板文件
    └── scripts/            # 中文脚本（带注释）
```

## 📝 已翻译文件

### 命令文件（`.claude/commands-zh/`）

所有命令文件都已翻译成中文：

- ✅ `speckit.analyze-zh.md` - 分析命令
- ✅ `speckit.checklist-zh.md` - 检查清单命令
- ✅ `speckit.clarify-zh.md` - 澄清命令
- ✅ `speckit.constitution-zh.md` - 章程命令
- ✅ `speckit.implement-zh.md` - 实施命令
- ✅ `speckit.plan-zh.md` - 计划命令
- ✅ `speckit.specify-zh.md` - 规格命令
- ✅ `speckit.tasks-zh.md` - 任务命令

### 模板文件（`.specify-zh/templates/`）

所有模板文件都已翻译成中文：

- ✅ `agent-file-template-zh.md` - 代理文件模板
- ✅ `checklist-template-zh.md` - 检查清单模板
- ✅ `plan-template-zh.md` - 计划模板
- ✅ `spec-template-zh.md` - 规格模板
- ✅ `tasks-template-zh.md` - 任务模板

### 记忆文件（`.specify-zh/memory/`）

- ✅ `constitution-zh.md` - 章程模板

### 脚本文件（`.specify-zh/scripts/powershell/`）

- ✅ `check-prerequisites-zh.ps1` - 先决条件检查脚本（中文注释）
- ℹ️ 其他脚本的详细中文翻译请参考 PowerShell 目录中的 README

## 🚀 使用方法

### 使用中文命令

中文版本的命令文件位于 `.claude/commands-zh/` 目录。你可以：

1. **方法 1**：直接参考中文文档来理解命令的工作原理
2. **方法 2**：修改你的 AI 助手配置以使用中文版本的命令

### 使用中文模板

中文模板文件位于 `.specify-zh/templates/` 目录。使用时：

```bash
# 复制中文模板到你的功能目录
cp .specify-zh/templates/spec-template-zh.md specs/001-my-feature/spec.md
```

### 使用中文脚本

PowerShell 脚本保持了相同的功能，只是注释被翻译成中文：

```powershell
# 使用中文注释版本的脚本
.\.specify-zh\scripts\powershell\check-prerequisites-zh.ps1 -Json
```

## 📖 工作流程概述

Spec-Driven Development 工作流程包含以下主要步骤：

1. **Specify（规格）** - 定义功能需求
2. **Clarify（澄清）** - 澄清模糊的需求
3. **Plan（计划）** - 创建技术实施计划
4. **Tasks（任务）** - 生成详细的任务列表
5. **Checklist（检查清单）** - 创建质量检查清单
6. **Analyze（分析）** - 分析一致性和质量
7. **Implement（实施）** - 执行实施计划

详细的工作流程说明请参考各个命令文件。

## 🎯 核心概念

### 规格驱动开发

- **以规格为先**：在编码之前明确定义需求
- **用户故事优先级**：按优先级组织功能（P1、P2、P3）
- **独立可测试**：每个用户故事都可以独立实施和测试
- **增量交付**：支持 MVP 优先和增量交付策略

### 检查清单即单元测试

检查清单不是用于测试实施，而是用于测试**需求的质量**：

- ✅ 正确："是否为所有交互元素定义了可访问性需求？"
- ❌ 错误："验证按钮点击是否正常工作"

### 章程驱动

项目章程定义了不可协商的原则和约束，所有规格、计划和任务都必须符合章程。

## 🔧 配置

### Claude AI 配置

如果你使用 Claude AI，可以在 `.claude/config` 中配置使用中文命令：

```yaml
commands:
  - path: .claude/commands-zh/
```

### Cursor AI 配置

如果你使用 Cursor，可以在 `.cursor/rules/` 中添加中文规则引用。

## 📚 文档资源

- 原始英文文档：`.claude/commands/` 和 `.specify/`
- 中文翻译文档：`.claude/commands-zh/` 和 `.specify-zh/`
- PowerShell 脚本说明：`.specify-zh/scripts/powershell/README-zh.md`

## 🤝 贡献

如果你发现翻译错误或有改进建议，欢迎提交 Issue 或 Pull Request。

## 📄 许可

本翻译遵循原项目的许可协议。

---

**注意**：本翻译版本与原始英文版本在功能上完全一致，只是语言不同。所有的命令名称、参数名称和文件结构都保持与原版相同，以确保兼容性。

