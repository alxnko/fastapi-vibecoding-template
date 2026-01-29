# Product Context

## 🧩 Problem Statement

Generic AI coding assistants often "forget" project context between sessions, lack specialized domain knowledge (e.g., Security vs. UI Design), and struggle with maintaining architectural consistency over time.

## 💡 Solution: Antigravity Kit

A "Second Brain" for the coding agent. It injects specialized knowledge (Skills) and enforces strict behavioral rules (Agents) to transform a generic LLM into a team of expert engineers.

## 👥 User Experience

- **Intervention**: Users interact via Natural Language or Slash Commands (`/plan`, `/debug`).
- **Transparency**: The system communicates "Mode" changes (e.g., "Applying knowledge of @[agent]...").
- **Trust**: Verification scripts (`checklist.py`) run automatically to prove correctness.

## 🔄 Core Workflows

1.  **Complex Build**: User Request -> Socratic Gate -> Plan (Implementation Plan) -> Execute -> Verify.
2.  **Quick Fix**: User Request -> Auto-Route -> Code -> Test.
3.  **Discovery**: `/brainstorm` -> Explore options -> Architecture Decision.
