# System Patterns

## 🏗️ Architecture

The system follows a **Modular Agentic Architecture**:

- **Agents (`.agent/agents/`)**: JSON/Markdown definitions of persona behaviors.
- **Skills (`.agent/skills/`)**: Folder-based capabilities. Each skill has `SKILL.md` (instructions) and optional `scripts/`.
- **Rules (`.agent/rules/`)**: Hierarchical rule sets (`GEMINI.md` is root).

## 📂 Directory Structure

```plaintext
.agent/
├── memory-bank/         # (NEW) Persistent context
├── agents/              # Persona definitions
├── skills/              # Capability modules
├── workflows/           # Routine procedures
├── rules/               # Governance (GEMINI.md)
└── scripts/             # Validation logic (checklist.py)
```

## 📝 Code Standards

- **Clean Code**: Concise, self-documenting, no over-engineering.
- **Testing**: Pyramid approach. Unit > Integration > E2E.
- **Safety**: 5-Phase Deployment. No secrets in code.

## 🧠 Memory Bank Protocol

- **Read-First**: Agents must read context before acting.
- **Update-Last**: Agents must update context after acting.
- **Git-Backed**: All context files are committed to the repo.
