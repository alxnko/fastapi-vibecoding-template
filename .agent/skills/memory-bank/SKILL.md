---
name: memory-bank
description: Mandatory protocol for maintaining project context in .agent/memory-bank/
---

# Memory Bank Protocol

> **CRITICAL**: This skill is **MANDATORY** for all complex tasks. You must read the memory bank at the start of a session and update it at the end.

## 🧠 What is the Memory Bank?

The Memory Bank is a set of living documentation files in `.agent/memory-bank/` that acts as the project's long-term and short-term memory. It ensures context is preserved across sessions and agents.

### The Files

1.  **`projectContext.md`** (stable):
    - **Purpose**: High-level context, tech stack, and overall goals.
    - **Update When**: Major architectural pivots, new tech stack choices.
2.  **`productContext.md`** (stable):
    - **Purpose**: Why we are building this, user problems, core workflows.
    - **Update When**: Product requirements change, new features defined.
3.  **`systemPatterns.md`** (evolving):
    - **Purpose**: Architecture, design patterns, code standards, directory structure.
    - **Update When**: You refactor code, add new patterns, or change structure.
4.  **`activeContext.md`** (volatile):
    - **Purpose**: "Where did we leave off?" - current session goal, active tasks, next steps.
    - **Update When**: **ALWAYS** at the end of a session or task.

## 📋 The Protocol

### Phase 1: Context Loading (Start of Task)

Before doing ANY work, you MUST read the active context and relevant files:

```markdown
1. Read `.agent/memory-bank/activeContext.md` -> Understand status.
2. Read `.agent/memory-bank/projectContext.md` -> Understand goals.
3. (Optional) Read `systemPatterns.md` -> If writing code.
```

### Phase 2: Execution & Maintenance (During Task)

1.  **Follow the Plan**: Execute the steps in `activeContext.md`.
2.  **Update patterns**: If you create a new abstraction or pattern, document it in `systemPatterns.md` immediately. Do not let knowledge exist only in code.

### Phase 3: Context Dumping (End of Task)

Before calling `notify_user` or finishing a task:

1.  **Update `activeContext.md`**:
    - Mark completed items.
    - Add new findings.
    - Clearly state **Next Steps** for the next session.
2.  **Update other files**: If you changed architecture or product scope, update the respective files.

## ⚠️ Critical Rules

1.  **Never delete the Memory Bank**: These files are the brain of the project.
2.  **Be concise**: Use bullet points and summaries. Do not dump raw logs.
3.  **Git Integration**: These files must be committed to git. They travel with the branch.
