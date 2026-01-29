# Project Context

## 📋 Overview

**Antigravity Kit** is a comprehensive, modular toolkit designed to expand the capabilities of AI agents. It provides a structured environment with specialized agents, domain-specific skills, and automated workflows to handle complex coding tasks autonomously.

## 🥅 High-Level Goals

1.  **Modularity**: Decouple agent capability from the core model using "Skills".
2.  **Reliability**: Enforce strict protocols (Rules > Plans > Verification) to ensure high-quality output.
3.  **Autonomy**: Enable agents to perform end-to-end tasks (planning to deployment) with minimal user hand-holding.

## 🛠️ Technology Stack

- **Core**: Python
- **Framework**: FastAPI (implied by template structure)
- **AI System**: Gemini (Agentic Mode)
- **Architecture**: Role-based (Agents + Skills + Workflows)

## 📂 Core Components

- **Agents**: 20 specialized personas (e.g., `backend-specialist`, `security-auditor`).
- **Skills**: 36 knowledge modules (e.g., `api-patterns`, `clean-code`).
- **Workflows**: 11 slash commands for common procedures.
- **Memory Bank**: (`.agent/memory-bank/`) Distributed context storage.
