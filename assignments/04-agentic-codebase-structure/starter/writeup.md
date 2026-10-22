# Week 4 Assignment Writeup: Agentic Codebase Structure & Workflow

## Overview
This writeup reflects on transforming a FastAPI and SQLite link shortener into an agent-native repository, establishing comprehensive agent guidance, scoping test instructions, creating a reusable Gemini CLI skill, and implementing the Custom Alias feature.

## Reflection & Detailed Answers

### 1. Purpose and Value of Repository Guidance (`AGENTS.md`)
Repository guidance serves as the foundational operational contract for coding agents. By keeping `AGENTS.md` concise (under 60 lines), we provided essential clarity regarding the application's FastAPI and SQLite architecture, key files (`main.py`, `test_main.py`), setup and execution commands (`pip install -r requirements.txt`, `pytest`), product boundaries, and the core Understand → Test → Implement → Verify workflow. This concise structure prevents coding agents from wandering into architectural drift or making incorrect assumptions.

### 2. Scoped Testing Instructions for Root-Level Tests
Because existing tests reside in the project root (`test_main.py`) rather than a dedicated `tests/` subdirectory, path-scoped subfolder rules do not automatically apply. We solved this by documenting a reliable loading strategy in `GEMINI.md` that directs agents to explicitly reference testing standards when working on `test_main.py`, avoiding inaccurate claims about automatic discovery.

### 3. Reusable Gemini CLI Skill (`implement-feature`)
The `.gemini/skills/implement-feature/SKILL.md` skill establishes a repeatable, high-integrity workflow across seven sequential steps: (1) reading task and repository guidance, (2) inspecting related code and tests, (3) stating expected behavior and affected files, (4) adding a failing behavioral test, (5) implementing the smallest necessary change, (6) running `pytest`, and (7) summarizing changes and remaining risks. This enforces test-driven development and rigorous validation.

### 4. Discovery Mechanisms in Gemini CLI
Gemini CLI discovers project context through convention-based entry points. The root `GEMINI.md` file acts as the primary pointer directing agents to `AGENTS.md`, while custom skills are automatically detected and loaded from the `.gemini/skills/` directory structure.

### 5. The PLAN → IMPLEMENT → REVIEW Lifecycle
Adhering to the Research → Strategy/Plan → Execution → Validation → Review lifecycle ensured seamless execution without side effects or regressions. During planning, the agent mapped out database conflict handling and Pydantic validation requirements. During review, all changes and test outputs were rigorously audited.

### 6. Custom Alias Feature Implementation & Learnings
For Task 1 (Custom Alias), the agent updated the `ShortenRequest` Pydantic model and `POST /shorten` endpoint in `main.py` to accept an optional `alias`. It added success and conflict test cases (`test_custom_alias_success`, `test_custom_alias_conflict`) in `test_main.py`. Running `pytest` successfully produced **5 passed, 1 warning**, confirming robust behavioral correctness. The final review outcome was **ACCEPT**. Overall, this assignment demonstrated how agent-ready structures and structured skills enable reliable, autonomous software engineering.
