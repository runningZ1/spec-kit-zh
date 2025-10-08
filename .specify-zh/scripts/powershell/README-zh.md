# PowerShell 脚本 - 中文版

本目录包含规格驱动开发工作流程的 PowerShell 脚本的中文翻译版本。

## 文件说明

- **check-prerequisites-zh.ps1** - 综合先决条件检查脚本（中文注释）
- **common-zh.ps1** - 通用 PowerShell 函数（中文注释）
- **create-new-feature-zh.ps1** - 创建新功能脚本（中文注释）
- **setup-plan-zh.ps1** - 设置实施计划脚本（中文注释）
- **update-agent-context-zh.ps1** - 更新代理上下文脚本（中文注释）

## 使用说明

这些脚本与原始英文版本功能完全相同，只是注释和文档字符串被翻译成了中文。

**注意**：这些脚本保留了原始的函数名、变量名和参数名（英文），以保持与原始工作流程的兼容性。只有注释和文档被翻译。

## 使用示例

```powershell
# 检查任务先决条件
.\check-prerequisites-zh.ps1 -Json

# 创建新功能
.\create-new-feature-zh.ps1 -Json "用户登录功能"

# 设置实施计划
.\setup-plan-zh.ps1 -Json

# 更新代理上下文
.\update-agent-context-zh.ps1 -AgentType claude
```

## 原始脚本

原始英文版本的脚本位于 `.specify/scripts/powershell/` 目录。

