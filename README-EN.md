# Spec-Driven Development Workflow - English Version

This repository contains the Simplified Chinese translation version of the Spec-Driven Development workflow.

## 📁 Directory Structure

```
.
├── .claude/
│   ├── commands/           # Original English command files
│   └── commands-zh/        # Chinese translated command files ✨
│
├── .specify/
│   ├── memory/             # Original English memory files
│   ├── templates/          # Original English template files
│   └── scripts/            # Original English scripts
│
└── .specify-zh/            # Chinese translation version ✨
    ├── memory/             # Chinese memory files
    ├── templates/          # Chinese template files
    └── scripts/            # Chinese scripts (with comments)
```

## 📝 Translated Files

### Command Files (`.claude/commands-zh/`)

All command files have been translated into Chinese:

- ✅ `speckit.analyze-zh.md` - Analyze command
- ✅ `speckit.checklist-zh.md` - Checklist command
- ✅ `speckit.clarify-zh.md` - Clarify command
- ✅ `speckit.constitution-zh.md` - Constitution command
- ✅ `speckit.implement-zh.md` - Implement command
- ✅ `speckit.plan-zh.md` - Plan command
- ✅ `speckit.specify-zh.md` - Specify command
- ✅ `speckit.tasks-zh.md` - Tasks command

### Template Files (`.specify-zh/templates/`)

All template files have been translated into Chinese:

- ✅ `agent-file-template-zh.md` - Agent file template
- ✅ `checklist-template-zh.md` - Checklist template
- ✅ `plan-template-zh.md` - Plan template
- ✅ `spec-template-zh.md` - Specification template
- ✅ `tasks-template-zh.md` - Tasks template

### Memory Files (`.specify-zh/memory/`)

- ✅ `constitution-zh.md` - Constitution template

### Script Files (`.specify-zh/scripts/powershell/`)

- ✅ `check-prerequisites-zh.ps1` - Prerequisite check script (Chinese comments)
- ℹ️ For detailed Chinese translations of other scripts, refer to the README in the PowerShell directory.

## 🚀 Usage

### Using Chinese Commands

The Chinese version command files are located in the `.claude/commands-zh/` directory. You can:

1. **Method 1**: Directly refer to the Chinese documentation to understand how the commands work
2. **Method 2**: Modify your AI assistant configuration to use the Chinese version of the commands

### Using Chinese Templates

Chinese template files are located in the `.specify-zh/templates/` directory. When using:

```bash
# Copy Chinese template to your feature directory
cp .specify-zh/templates/spec-template-zh.md specs/001-my-feature/spec.md
```

### Using Chinese Scripts

PowerShell scripts maintain the same functionality, but comments have been translated into Chinese:

```powershell
# Use the Chinese commented version of the script
.\.specify-zh\scripts\powershell\check-prerequisites-zh.ps1 -Json
```

## 📖 Workflow Overview

The Spec-Driven Development workflow includes the following main steps:

1. **Specify** - Define functional requirements
2. **Clarify** - Clarify ambiguous requirements
3. **Plan** - Create technical implementation plan
4. **Tasks** - Generate detailed task lists
5. **Checklist** - Create quality checklists
6. **Analyze** - Analyze consistency and quality
7. **Implement** - Execute implementation plan

For detailed workflow explanations, refer to the individual command files.

## 🎯 Core Concepts

### Specification-Driven Development

- **Specification First**: Clearly define requirements before coding
- **User Story Prioritization**: Organize features by priority (P1, P2, P3)
- **Independently Testable**: Each user story can be implemented and tested independently
- **Incremental Delivery**: Supports MVP priority and incremental delivery strategies

### Checklists as Unit Tests

Checklists are not for testing implementation, but for testing **requirement quality**:

- ✅ Correct: "Has accessibility requirement been defined for all interactive elements?"
- ❌ Wrong: "Verify if button click works normally"

### Constitution-Driven

The project constitution defines non-negotiable principles and constraints. All specifications, plans, and tasks must comply with the constitution.

## 🔧 Configuration

### Claude AI Configuration

If you use Claude AI, you can configure it to use Chinese commands in `.claude/config`:

```yaml
commands:
  - path: .claude/commands-zh/
```

### Cursor AI Configuration

If you use Cursor, you can add Chinese rule references in `.cursor/rules/`.

## 📚 Documentation Resources

- Original English documentation: `.claude/commands/` and `.specify/`
- Chinese translation documentation: `.claude/commands-zh/` and `.specify-zh/`
- PowerShell script instructions: `.specify-zh/scripts/powershell/README-zh.md`

## 🤝 Contributing

If you find translation errors or have improvement suggestions, welcome to submit Issues or Pull Requests.

## 📄 License

This translation follows the original project's license agreement.

---

**Note**: This translation version is functionally identical to the original English version, only differing in language. All command names, parameter names, and file structures remain the same as the original to ensure compatibility.
